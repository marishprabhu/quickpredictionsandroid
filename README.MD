To generate JKS file:
keytool -keystore upload_keystore.jks -genkey -alias uploadalias -keyalg rsa -validity 50000 -keypass password -storepass password -keysize 2048
To generate PEM File:
keytool -export -rfc -keystore upload_keystore.jks -alias uploadalias -file upload_certificate.pem

To generate keystore:	
keytool -importcert -file deployment_cert.der -keystore upload.keystore -alias quickpredictionsalias

To create release build:
cordova build android --release --buildConfig

To run in local:


npm install
npm install -g cordova

cordova platform rm android
cordova platform add android

cordova build android
In quickpredictionsandroid\platforms\android release-signing set the correct path.
cordova emulate android
