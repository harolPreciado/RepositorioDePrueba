// Iniciar git
// Ubicarse sobre la carpeta donde se encuentran los archivos a guardar

    git init

// Esta linea crea un archivo .git que se encuentra oculto, se puede ver escribiendo en la terminal 

    ls -a
    
// Para pasar los archivos del working al staging area, (es el paso antes de tomar la foto a los archivos) antes de este paso si haces git status los archivos salen de colo rojo
    git add
// Si hacemos un git status, los archivos se muestran en color verde, quiere decir que los archivos estan listos para subir.
    git commit -m 'Mensaje'
// Esta linea quiere decir que tome los datos que esten en el staging area y los lleve al repositorio local, los archivos en el staging area se borran
    git log 
// Muestra los commit realizados
    git reset direccionDelCommit
// Vuelve a un punto deseado obteniendo la direccionDelCommit
    git checkout .
// Establece el commit donde me encuentro como master


// GitHub
// Permite tomar el repositorio local 

// Vincular repositorio local con el remoto
    git remote add origin ->Direccion de origen del repositorio en GitHub
// Para que el repositorio local le pase la informacion al repositorio remoto
    git push origin master
// Solo se puede hacer git push cuando el staging area este libre

    git clone ->Direccion del codigo a bajar en GitHub
// Descargar archivo de gitHub
    git pull 
// Actualiza el archivo descargado luego de que el archivo original haya sido modificado por el propietario
