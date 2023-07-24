7. Procedimientos de instalación y configuración
7.1	Requisitos del entorno: 
Verificar que el servidor cumpla con los requisitos mínimos para ejecutar la aplicación. Asegurarse de tener instalado Ruby versión "3.2.2", Rails "7.0.5" y las gemas necesarias, así como el gestor de dependencias Bundler,  asegúrese de tener instalado git. 
7.2	Obtener el código fuente:
Descargar o clonar el repositorio de "Luis Shop" desde el repositorio central en GitHub, donde se almacena el código fuente del proyecto.
7.3	Instalar dependencias:
Ejecutar el comando `bundle install` para instalar todas las gemas y dependencias requeridas por el proyecto. Bundler se encargará de asegurar que todas las versiones de las gemas sean las correctas.
7.4	Configuración de la base de datos:
En el archivo de configuración de Rails (`database.yml`), ajustar los parámetros de conexión de la base de datos. Crear la base de datos y aplicar las migraciones necesarias con los comandos `rails db:create` y `rails db:migrate`.
7.5	Configuración de pasarelas de pago 
Si se han incorporado pasarelas de pago y envío, como PayPal y Servientrega, configurar las credenciales y opciones requeridas para su funcionamiento en el entorno de producción.
•	Crear una cuenta de desarrollador en PayPal: Acceder al sitio web de PayPal y registrarse como desarrollador. Esto permitirá obtener las credenciales necesarias para realizar pruebas en un entorno de desarrollo antes de lanzar la aplicación en producción.
•	Crear una aplicación en PayPal: Dentro del panel de desarrollador de PayPal, crear una nueva aplicación para "Luis Shop". PayPal proporcionará un ID de cliente (Client ID) y una clave secreta (Secret Key) que serán utilizados para autenticar las solicitudes a la API de PayPal.
•	Configurar las credenciales en "Luis Shop": En el código fuente de la aplicación "Luis Shop", se modificará el archivo de configuración para incluir las credenciales proporcionadas por PayPal. Estas credenciales deben ser almacenadas de manera segura y no expuestas públicamente para mantener la seguridad de las transacciones.


7.6	Configuración del chatbot:
•	Crear un proyecto en Dialogflow: Acceder a la plataforma de Dialogflow y crear un nuevo proyecto para "Luis Shop". Dialogflow es una herramienta de procesamiento de lenguaje natural desarrollada por Google que permitirá entrenar al chatbot para comprender y responder a las preguntas y consultas de los clientes de manera inteligente.
•	Entrenamiento del modelo de lenguaje: Definir las intenciones y las respuestas del chatbot en función de los posibles escenarios de atención al cliente en "Luis Shop". Esto implica establecer las preguntas frecuentes y las respuestas correspondientes para brindar una experiencia de usuario satisfactoria.
•	Integración con las plataformas de chat: Configurar las claves y tokens de autenticación proporcionadas por Telegram y Facebook dentro de Dialogflow para permitir la comunicación bidireccional entre el chatbot y las plataformas de chat seleccionadas.

7.7	Configuración de recuperación de contraseña 
•	Crear una cuenta en SendGrid.net: Acceder al sitio web de SendGrid.net y crear una cuenta utilizando una dirección de correo electrónico válida. SendGrid.net ofrece diferentes planes de suscripción, incluyendo una opción gratuita con un límite de envío de correos electrónicos por día.
•	Obtener la clave de API de SendGrid: Después de crear la cuenta, acceder al panel de control de SendGrid.net y obtener la clave de API necesaria para realizar el envío de correos electrónicos desde la aplicación "Luis Shop". Esta clave de API será utilizada para autenticar las solicitudes de envío de correos electrónicos desde la aplicación.
•	Instalar la gema SendGrid en el proyecto Rails: Utilizar Bundler para instalar la gema SendGrid en el proyecto Rails. Agregar gem 'sendgrid-ruby' al archivo Gemfile y luego ejecutar el comando bundle install para instalar la gema.
•	Configurar la clave de API en la aplicación: En el código fuente de "Luis Shop", configurar la clave de API de SendGrid en el archivo de configuración de correos electrónicos (por ejemplo, config/environments/production.rb). Esto permitirá que la aplicación utilice la clave de API para autenticar las solicitudes de envío de correos electrónicos.
•	Enviar el correo electrónico de recuperación de contraseña: Cuando un usuario solicite la recuperación de contraseña, la aplicación utilizará la gema SendGrid para enviar un correo electrónico a la dirección de correo proporcionada. En el correo electrónico, se incluirá un enlace seguro para restablecer la contraseña.

