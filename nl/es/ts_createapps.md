---

copyright:
  years: 2015, 2018
lastupdated: "2018-04-26"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:note:.deprecated}

# Resolución de problemas de las herramientas de desarrollador de {{site.data.keyword.Bluemix_notm}}
{: #troubleshoot}

Los problemas más habituales al utilizar la CLI de {{site.data.keyword.dev_cli_short}} para crear apps pueden incluir anomalías en el despliegue o código que no es posible recuperar al crear una app. En muchos de los casos, puede solucionar estos problemas siguiendo unos sencillos pasos.
{:shortdesc}

## Error de nombre de host al crear una app con un patrón no móvil
{: #hostname-error}

Es posible que le aparezca el siguiente error si utiliza la CLI de {{site.data.keyword.dev_cli_short}} para desplegar una app en Cloud Foundry. Si especifica un nombre de host que cree que es único, es posible que siga viendo el mensaje.

```
The hostname <myHostname> is taken.
```
{: codeblock}
{: tsSymptoms}

Este error viene originado por una señal de inicio de sesión caducada.
{: tsCauses}

Inicie de nuevo una sesión.

```
bx login
```
{: codeblock}
{: tsResolve}

## Anomalías generales con la CLI de {{site.data.keyword.dev_cli_short}}
{: #general}

Es posible que le aparezca el siguiente error si utiliza los mandatos de CLI de {{site.data.keyword.dev_cli_short}}`create`, `delete`, `list` o `code`:

```
Failed to <command> application.
```
{: codeblock}
{: tsSymptoms}

Este error viene originado por una señal de inicio de sesión caducada.
{: tsCauses}

Inicie de nuevo una sesión.

```
bx login
```
{: codeblock}
{: tsResolve}

## Error: No existe la imagen cuando ejecuta una app nueva
{: #nosuchimage}

Es posible que le aparezca el siguiente error cuando ejecute una app sin compilarla con anterioridad.

```
$ bx dev run
The run-cmd option was not specified
Stopping the 'testProject' container...
The 'testProject' container was not found
Creating image bx-dev-testProject based on Dockerfile...
OK                    
Creating a container named 'testProject' from that image...
FAILED
Container 'testProject' could not be created:
Error: No such image: bx-dev-testProject
```
{: tsSymptoms}

Debe crear una app antes de ejecutarla.
{: tsCauses}

Ejecute el mandato siguiente en el directorio de app actual para crear la app:

```
bx dev build
```
{: codeblock}

Ejecute el mandato siguiente en el directorio de app actual para iniciar la app:

```
bx dev run
```
{: tsResolve}

## Error de intermediario de servicio cuando se añade la prestación de {{site.data.keyword.objectstorageshort}}
{: #os}

Es posible que le aparezca el siguiente error si utiliza {{site.data.keyword.dev_cli_short}} para crear dos apps con la prestación {{site.data.keyword.objectstorageshort}}:

```
FAILED
Service broker error: {"description"=>"You can not create this Object Storage instance. Each organization using the Object Storage service is limited to one instance of the Free plan."}
```
{: codeblock}
{: tsSymptoms}

Este error se debe al servicio {{site.data.keyword.objectstorageshort}}, que únicamente proporciona una instancia del plan {{site.data.keyword.objectstorageshort}} gratuito.
{: tsCauses}

Se le solicitará que elija otro plan para evitar este error.
{: tsResolve}

## Anomalía al obtener el código al crear una app
{: #code}

Es posible que vea el error siguiente si utiliza la CLI de {{site.data.keyword.dev_cli_short}} para crear una app:

```
FAILED                            
Application created, but could not get code
https://console.ng.bluemix.net/developer/projects/b22165f3-cbc6-4f73-876f-e33cbec199d4/code
```
{: codeblock}
{: tsSymptoms}

Este error se debe a un tiempo de espera interno excedido.
{: tsCauses}

Puede obtener el código de una de las siguientes formas:

* Ejecute el siguiente mandato utilizando la CLI:

   ```
   bx dev code <your-app-name>
   ```
   {: codeblock}

   Sustituya `<your-app-name>` por el nombre de la app que ha especificado durante la creación de la app.

* Utilice la {{site.data.keyword.dev_console}}.

	1. Seleccione la [app ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.bluemix.net/developer/appservice/apps) en la {{site.data.keyword.dev_console}}.

	2. Pulse **Descargar código**.

{: tsResolve}

## Error al ejecutar `bx dev run` para apps Node.js
{: #node}

Es posible que le aparezca el siguiente error si ejecuta `bx dev run` con la CLI de {{site.data.keyword.dev_cli_short}} para apps web o BFF de Node.js:

```
module.js:597
  return process.dlopen(module, path._makeLong(filename));
                 ^

Error: /app/node_modules/bluemix-autoscaling-agent/node_modules/appmetrics/appmetrics.node: invalid ELF header
    at Error (native)
    at Object.Module._extensions..node (module.js:597:18)
    at Module.load (module.js:487:32)
    at tryModuleLoad (module.js:446:12)

    at Function.Module._load (module.js:438:3)
    at Module.require (module.js:497:17)
    at require (internal/module.js:20:19)
    at Object.<anonymous> (/app/node_modules/bluemix-autoscaling-agent/node_modules/appmetrics/index.js:25:13)
    at Module._compile (module.js:570:32)
    at Object.Module._extensions..js (module.js:579:10)
```
{: codeblock}
{: tsSymptoms}

Este error se produce cuando el módulo `appmetrics` se ha instalado en otra arquitectura. Los módulos npm nativos instalados en una arquitectura no funcionan en otra. Las imágenes de Docker incluidas se basan en el kernel de Linux.
{: tsCauses}

Suprima la carpeta `node_modules` y ejecute de nuevo el mandato `bx dev run`.
{: tsResolve}

## Anomalía al desplegar en {{site.data.keyword.Bluemix_notm}}

Se produce una anomalía cuando se intenta desplegar en {{site.data.keyword.Bluemix_notm}} con la CLI de {{site.data.keyword.dev_cli_short}}, sin embargo, no se visualiza ningún error.
{: tsSymptoms}

Es posible que no haya iniciado una sesión con su cuenta.
{: tsCauses}

Inicie la sesión y vuélvalo a intentar.

```
bx login
```
{: tsResolve}

## Se ha producido una anomalía al desplegar en Kubernetes en {{site.data.keyword.Bluemix_notm}}

Se podría visualizar la siguiente anomalía después de que se le solicitase el nombre de su clúster:

```
FAILED
Failed to execute the action:  exit status 1:

FAILED
Failed to configure deployment with cluster '<cluster-name>' due to: exit status 1
```
{: tsSymptoms}

La causa más probable es que el nombre del clúster no sea válido. Lo puede confirmar ejecutando el mismo mandato con `-- trace`. Los siguientes detalles podría incluirse en la salida del error:

```
Failing with error:  {"incidentID":"<id-number>","code":"E0008","description":"The specified cluster could not be found.","recoveryCLI":"Run 'bx cs clusters' to list all clusters you have access to.","type":"Provisioning"}
```
{: tsCauses}

Asegúrese de que utiliza el clúster correcto y de que ha configurado el clúster para el despliegue ejecutando:

```
bx cs cluster-config <cluster-name>
```
{: tsResolve}

## Anomalía al desplegar un destino de imagen

Se podría visualizar la siguiente anomalía después de que se le solicitase el destino de imagen de despliegue:

```
FAILED
Failed to execute the action:  exit status 1:denied: requested access to the resource is denied


FAILED
Failed to push the Run image tagged 'registry.ng.bluemix.net/<namespace>/<app-name>:0.0.1' to the Docker registry due to: exit status 1
```
{: tsSymptoms}

La causa más probable es que la imagen de destino de despliegue no sea válida. Más concretamente, el espacio de nombres, que se encuentra en medio en el destino de imagen de despliegue, podría no ser válido.

Asegúrese de que el espacio de nombres en el destino de imagen de despliegue coincide con uno de los espacios de nombres encontrados en la ejecución:

```
bx cr namespaces
```
{: tsResolve}

## Reinstalación de herramientas
{: #appendix}

Todos los requisitos previos se instalan para la mayoría de los usuarios que utilizan instaladores de la plataforma. Si necesita instalar cualquier componente manualmente, aquí encontrará las instrucciones:

Para instalar el plugin de desarrollo, primero debe instalar la [CLI de IBM Cloud](https://console.bluemix.net/docs/cli/reference/bluemix_cli/get_started.html#getting-started).

Para utilizar el plugin de desarrollo, debe instalarlo ejecutando el mandato siguiente: `bx plugin install dev -r Bluemix`

Para ejecutar y depurar apps localmente, también debe instalar el [Docker](https://www.docker.com/get-docker).

Para desplegar una app como contenedor, también debe instalar Kubernetes, Helm y los siguientes plugins de la CLI de IBM Cloud:

Para instalar Kubernetes:
* Usuarios de Mac:
`curl --progress-bar -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/darwin/amd64/kubectl`

* Usuarios de Linux:
`curl --progress-bar -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl`

* Usuarios de Windows:
`curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.7.0/bin/windows/amd64/kubectl.exe`

Para instalar Helm:
* Usuarios de Mac y Linux:
`export DESIRED_VERSION=v2.6.0`
`curl -sL https://raw.githubusercontent.com/kubernetes/helm/master/scripts/get | bash`

* Usuarios de Windows:
Descargue e instale el binario de https://github.com/kubernetes/helm/releases/tag/v2.6.0

Para instalar el plugin container-registry:
`bx plugin install container-registry`

Para instalar el plugin container-service:
`bx plugin install container-service`

