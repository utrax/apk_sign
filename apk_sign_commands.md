## Zipalign the apk file 
command_1 = zipalign -v 4 path_to_apk name_of_new_apk

## Generating code signing certificate 
command_2 = keytool -v -genkey -keystore name_of_key.keystore -alias signkey -keyalg RSA -keysize 2048 -validity 20000

## sigining the apk file 
command_2 = jarsigner -verbose -keystore name_of_key.keystore name_of_new_apk signkey