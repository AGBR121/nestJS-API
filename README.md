<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="200" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://coveralls.io/github/nestjs/nest?branch=master" target="_blank"><img src="https://coveralls.io/repos/github/nestjs/nest/badge.svg?branch=master#9" alt="Coverage" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

## Description

[Nest](https://github.com/nestjs/nest) framework TypeScript starter repository.

## Installation

```bash
$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://kamilmysliwiec.com)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## License

Nest is [MIT licensed](LICENSE).

Pagina del Deploy: https://api.curso.jhancarlos.me/

Creación de la instancia en AWS

Crear una instancia de Ubuntu en AWS es un proceso relativamente sencillo. Aquí tienes una guía paso a paso para hacerlo:

### Paso 1: Inicia sesión en AWS Management Console

1. Ve a [AWS Management Console](https://aws.amazon.com/console/).
2. Inicia sesión con tus credenciales de AWS.

### Paso 2: Accede a EC2 Dashboard

1. Desde la consola de AWS, busca "EC2" en la barra de búsqueda y selecciona "EC2" para acceder al panel de control de EC2.

### Paso 3: Lanzar una nueva instancia

1. En el panel de control de EC2, haz clic en "Launch Instance".

### Paso 4: Configuración de la instancia

1. **Elegir una Amazon Machine Image (AMI)**:
   - Busca "Ubuntu" en el campo de búsqueda y selecciona la versión de Ubuntu que prefieras (por ejemplo, "Ubuntu Server 20.04 LTS").

2. **Elegir el tipo de instancia**:
   - Selecciona el tipo de instancia que se ajuste a tus necesidades. El tipo "t2.micro" es elegible para el nivel gratuito y es adecuado para pruebas y pequeños proyectos.

3. **Configurar los detalles de la instancia**:
   - Puedes dejar la configuración predeterminada o ajustar los detalles según tus necesidades específicas.
   - Si no estás seguro, puedes dejar la mayoría de los valores por defecto y hacer clic en "Next: Add Storage".

4. **Añadir almacenamiento**:
   - Especifica el tamaño del volumen de almacenamiento. El tamaño predeterminado suele ser suficiente para muchos usos, pero puedes aumentarlo si lo necesitas.

5. **Añadir etiquetas**:
   - Puedes agregar etiquetas para organizar tus instancias. Esto es opcional.

6. **Configurar el grupo de seguridad**:
   - Crea un nuevo grupo de seguridad o selecciona uno existente.
   - Añade reglas para permitir tráfico SSH (puerto 22) desde tu dirección IP o cualquier dirección IP si prefieres un acceso más amplio.
   - También puedes añadir reglas para HTTP (puerto 80) y HTTPS (puerto 443) si planeas ejecutar un servidor web.

### Paso 5: Revisar y lanzar

1. **Revisar instancia**:
   - Revisa todos los detalles de tu configuración para asegurarte de que todo esté correcto.

2. **Lanzar instancia**:
   - Haz clic en "Launch".
   - Se te pedirá que selecciones un par de claves para conectarte a la instancia. Crea un nuevo par de claves o selecciona uno existente, y asegúrate de descargar el archivo `.pem` (es crucial que lo guardes de forma segura ya que lo necesitarás para conectarte a tu instancia).

### Paso 6: Conectar a tu instancia

1. **Obtener la dirección IP pública**:
   - Una vez que la instancia esté en ejecución, ve a la consola de EC2 y selecciona tu instancia.
   - Encuentra la dirección IP pública en la descripción de la instancia.

2. **Conectarse mediante SSH**:
   - Abre una terminal en tu computadora.
   - Navega al directorio donde guardaste el archivo `.pem`.
   - Cambia los permisos del archivo para que solo tú puedas leerlo:

     ```sh
     chmod 400 your-key-file.pem
     ```

   - Conéctate a tu instancia usando SSH (reemplaza `your-key-file.pem` con el nombre de tu archivo de clave y `ec2-user@your-ip-address` con el usuario y la IP pública de tu instancia):

     ```sh
     ssh -i your-key-file.pem ubuntu@your-ip-address
     ```

### Paso 7: Configuración inicial de la instancia

1. **Actualizar paquetes del sistema**:

   ```sh
   sudo apt update
   sudo apt upgrade -y
   ```

2. **Instalar cualquier software adicional que necesites**:
   - Puedes instalar Nginx, Docker, Node.js o cualquier otro software que necesites para tu proyecto.

### Paso 8: Configurar tu aplicación

1. **Subir tu aplicación**:
   - Puedes usar SCP, SFTP o Git para subir los archivos de tu aplicación a la instancia.

2. **Configurar y ejecutar tu aplicación**:
   - Sigue los pasos necesarios para configurar y ejecutar tu aplicación en la instancia.

### Paso 9: Configuración adicional (opcional)

Install NodeJS:

```
sudo apt install -y curl
```
```
sudo apt install -y nodejs
```
```
curl o https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```
```
source ~/.bashrc
```
```
nvm list-remote
```
```
nvm install v16
```

Install Docker:

```
sudo apt install apt-transport-https curl gnupg-agent ca-certificates software-properties-common -y
```
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
```
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
```
sudo apt update
```
```
sudo apt install docker-ce
```
```
sudo apt install docker-compose
```

Config github SSH:
```
cd ~/.ssh
```
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
```
sudo nano ~/.ssh/config
```

Add:
ForwardAgent yes

```
eval `ssh-agent -s`
```
```
ssh-add
```
```
ssh-add ~/.ssh/github
```
```
git clone git@github.com:FrankiNarvaez/nestjs-project26.git :)
```
```
sudo apt update && sudo apt upgrade -y
```
```
sudo apt install nginx
```
```
sudo systemctl status nginx
```
```
sudo nano /etc/nginx/sites-available/your-domain.com.conf
```
```
server {

    	root /var/www/html;
    	index index.html index.htm index.nginx-debian.html;

    	server_name vps-3141735-x.dattaweb.com;
   	 underscores_in_headers on;

    	location / {
        	try_files $uri $uri/ =404;
   		 proxy_pass http://localhost:4000; # Change the port if needed
   		 proxy_http_version 1.1;
   		 proxy_set_header Upgrade $http_upgrade;
   		 proxy_set_header Connection 'upgrade';
   		 proxy_set_header Host $host;
   		 proxy_cache_bypass $http_upgrade;
    	}

   	 location /api {
            	proxy_pass http://localhost:4000/api;
    	}

   	 location /docs {
            	proxy_pass http://localhost:4000/docs;
    	}

    	error_log /var/log/nginx/your-domain.com.error;
    	access_log /var/log/nginx/your-domain.com.access;
}
```
```
sudo ln -s /etc/nginx/sites-available/your-domain.com.conf /etc/nginx/sites-enabled/your-domain.com.conf
```
```
testeamos : sudo nginx -t
```
```
sudo systemctl restart nginx
```

Certbot

```
sudo apt install certbot python3-certbot-nginx
```
Corroboramos la version : 
```
certbot --version
```
```
sudo certbot --nginx
```
testeo de renovacion:
```
sudo certbot renew --dry-run
```
