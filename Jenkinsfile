node {
    stage('Revisión'){
        checkout scm
    }

    stage ('Instalación de dependencias'){
        bat 'npm install'
    }

    stage('Construir'){
        bat 'npm run ng build'
    }

    //BORRAR CARPETA DEL HTML
    stage('Limpiar'){
        bat 'rd /s /q C:\\servidor\\fire'
    }

    stage('Mover al servidor'){
        bat 'xcopy  C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\angular1-pipeline\\dist\\app-03\\browser  C:\\servidor\\fire /E /I /Y'
    }
}