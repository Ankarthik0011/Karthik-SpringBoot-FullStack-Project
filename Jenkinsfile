pipeline {
    agent any

    environment {
        DB_URL = credentials('DB_URL')
        DB_UN  = credentials('DB_UN')
        DB_PWD = credentials('DB_PWD')

        OPENAIKEY = credentials('OPENAIKEY')

        EMAIL  = credentials('EMAIL')
        APP_PWD = credentials('APP_PWD')

        CLOUDINARY_URL = credentials('CLOUDINARY_URL')

        TWILIO_ACCOUNT_SID = credentials('TWILIO_ACCOUNT_SID')
        TWILIO_AUTH_TOKEN = credentials('TWILIO_AUTH_TOKEN')
        TWILIO_MOBILE = credentials('TWILIO_MOBILE')

        RAZORPAY_KEY_ID = credentials('RAZORPAY_KEY_ID')
        RAZORPAY_KEY_SECRET = credentials('RAZORPAY_KEY_SECRET')
    }

    stages {
        stage('Build') {
            steps {
                sh 'chmod +x mvnw'
                sh './mvnw clean package -DskipTests'
            }
        }
    }
}
