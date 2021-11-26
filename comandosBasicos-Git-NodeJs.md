Iniciar git
Ubicarse sobre la carpeta donde se encuentran los archivos a guardar

    git init

Esta linea crea un archivo .git que se encuentra oculto, se puede ver escribiendo en la terminal 

    ls -a

Para pasar los archivos del working al staging area, (es el paso antes de tomar la foto a los archivos) antes de este paso si haces git status los archivos salen de colo rojo

    git add

Si hacemos un git status, los archivos se muestran en color verde, quiere decir que los archivos estan listos para subir.

    git commit -m 'Mensaje'

Esta linea quiere decir que tome los datos que esten en el staging area y los lleve al repositorio local, los archivos en el staging area se borran

    git log 

Muestra los commit realizados

    git reset direccionDelCommit

Vuelve a un punto deseado obteniendo la direccionDelCommit

    git checkout .

Establece el commit donde me encuentro como master


------->GitHub<---------
Permite tomar el repositorio local 

Vincular repositorio local con el remoto

    git remote add origin ->Direccion de origen del repositorio en GitHub

Para que el repositorio local le pase la informacion al repositorio remoto

    git push origin master

Solo se puede hacer git push cuando el staging area este libre

    git clone ->Direccion del codigo a bajar en GitHub

Descargar archivo de gitHub

    git pull 
    
Actualiza el archivo descargado luego de que el archivo original haya sido modificado por el propietario


------->Crear Proyecto NodeJs Express<---------

Instalar NodeJS

    npm install   

Iniciar Proyecto con NodeJS  

    npm init
    
Crear carpetas 
    
    mkdir src src/public src/public/css src/controller src/model src/views src/middlewares src/routes src/views/partials
   
Crear archivos
    
    touch .gitignore src/index.js src/app.js src/public/css/styles.css src/controller/index.js src/model/index.js src/routes/index.js src/views/index.js src/middlewares/index.js
    
Instalar dependencias
- Express
    
        npm install express --save
        
        const express = require('express');
        const app = express();

- Nodemon
    
        npm install --save-dev nodemon

- Ejs

        npm install ejs
        
        app.set('views', path.join(__dirname, 'views'));
        app.set('view engine', 'ejs');
    
- Method Override (PUT - DELETE)

        npm install method-override
        
        const methodOverride = require('method-override')

- Multer 

        npm install --save multer
        
        const storage = multer.diskStorage({
            destination: (req, file, cb)=>{
                cb(null, './src/public/img/avatars')
            },
            filename: (req, file, cb)=>{
                let fileName = `${Date.now()}_img${path.extname(file.originalname)}`;
                cb(null, fileName);
            }
        });
        const uploadFile = multer({storage});
    
- Express-Validator

        npm install express-validator
        
        const { body, validationResult } = require('express-validator');
        
 
- Compression - Requiere Express

        npm install compression

        const compression = require('compression')
        app.use(compression())

- Fran Generator

        npm install -g fran-generator
        fran
        
- Session

        npm install express-session
        
        const session = require('express-session')
