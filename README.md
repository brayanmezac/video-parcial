# video-parcial
- [ ] En este video, voy a explicar el proyecto llamado NPL-shop-pet, que es un chatbot que simula una tienda de mascotas. El proyecto está hecho en Python y usa la librería Gradio para crear una interfaz gráfica. Los archivos que componen el proyecto son los siguientes:

requirements.txt: Este archivo contiene las dependencias que se necesitan para ejecutar el proyecto. Entre ellas están Gradio, TensorFlow, NLTK y numpy.

chatbot.py: Este archivo contiene el código principal del chatbot, que usa un modelo de red neuronal para clasificar las intenciones del usuario y generar respuestas adecuadas. El modelo se carga desde el archivo chatbot_model.h5, que se creó con el archivo training.py.

chatbot_gradio.py: Este archivo contiene el código para crear la interfaz gráfica con Gradio, que permite interactuar con el chatbot desde el navegador. La interfaz tiene un campo de texto para ingresar la pregunta del usuario y un botón para enviarla. La respuesta del chatbot se muestra en una caja de texto debajo.

intents.json: Este archivo contiene los datos de entrenamiento del modelo, que consisten en una lista de intenciones, cada una con un nombre, una lista de patrones y una lista de respuestas. Los patrones son ejemplos de preguntas que el usuario puede hacer al chatbot, y las respuestas son posibles respuestas que el chatbot puede dar. El archivo tiene 15 intenciones diferentes, relacionadas con la tienda de mascotas, como saludar, comprar, consultar precios, etc.

training.py: Este archivo contiene el código para entrenar el modelo de red neuronal usando los datos del archivo 

intents.json. El modelo tiene dos capas ocultas y una capa de salida con 15 neuronas, una por cada intención. El modelo se guarda en el archivo chatbot_model.h5 después de entrenarlo.

---

En este video, voy a explicar el proyecto llamado springboot-chatgpt. Este proyecto es una aplicación de Spring Boot que utiliza la API de OpenAI ChatGPT para generar respuestas a los mensajes del usuario. Los archivos que componen el proyecto son los siguientes:

pom.xml: Este archivo es el archivo de configuración de Maven para el proyecto. Define las dependencias del proyecto, como Spring Boot y la biblioteca de OpenAI.

Dockerfile: Este archivo define cómo se debe construir la imagen de Docker para la aplicación. Esto permite que la aplicación se ejecute en cualquier sistema que tenga Docker instalado, independientemente del sistema operativo y las dependencias instaladas.

application.properties: Este archivo contiene la configuración de la aplicación Spring Boot. Aquí es donde se definen cosas como el puerto en el que se ejecuta la aplicación y las claves de API para servicios externos.

DemoApplication.java: Este es el punto de entrada principal de la aplicación. Inicia la aplicación Spring Boot y configura cualquier bean necesario.

HelloGPTController.java: Este archivo define un controlador de Spring MVC que maneja las solicitudes HTTP a la ruta “/hello”. Cuando se recibe una solicitud, el controlador llama a la API de OpenAI ChatGPT con el mensaje del usuario y devuelve la respuesta generada.

endpoits:

/chatboot/chat: Acepta una solicitud GET con un parámetro ‘message’. Devuelve una respuesta del chatbot como una cadena.

/chatboot/prompt: Acepta una solicitud GET con un parámetro ‘message’. Devuelve una respuesta del chatbot como un objeto ChatResponse.

---

En este video, voy a explicar un bot de WhatsApp construido en Python utilizando el framework Flask. Aquí está una descripción resumida de su funcionamiento:

El bot se inicia con la ruta /webhook/, que acepta solicitudes GET y POST.

Si recibe una solicitud GET, verifica un token para autenticar la solicitud.

Si recibe una solicitud POST, extrae el mensaje del usuario de los datos recibidos.

Luego, utiliza la API de OpenAI para generar una respuesta al mensaje del usuario.

La respuesta se procesa y se envía de vuelta al usuario a través de WhatsApp.

Además, el bot registra cada interacción en una base de datos MySQL.

En este bot recibe mensajes de los usuarios a través de WhatsApp, genera respuestas utilizando la API de OpenAI y registra las interacciones en una base de datos. Todo esto se realiza en un servidor Flask y puede ser desplegado en un contenedor Docker.