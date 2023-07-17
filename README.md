# Send_Images/Media_From_Local_Folder_to_your_WhatsApp_From_Twilio

Here is the code to send the image stored on the local device to WhatsApp  using Twilio.

Instructions on how to get an account on Twilio, Authentication, and tokens are NOT covered. They are available on the Twilio web site.

A simple shell script would be as shown below :

This sends a simple image from my local folder ( logo.png) in /var/www/html directory to WhatsApp.

Tested on a Raspberry Pi where Apache is installed.

Installed Ngrok and ran the ./ngrok http 80 to get the below decrypted address as seen below.

```

curl 'https://api.twilio.com/2010-04-01/Accounts/AC83bd97a531ec5505a519e10f9953edde/Messages.json' -X POST \
--data-urlencode 'To=whatsapp:+919845691854' \
--data-urlencode 'From=whatsapp:+1415<YOUR_TWILIO_ASSIGNED_INTERNATIONAL_NUMBER_HERE>' \
--data-urlencode 'Body=Hello 17Jul 2023' \
--data-urlencode 'MediaUrl=https://<DECRYPTED ADDRESS OF THE NGROK UTILITY>.ngrok-free.app/logo.png' \
-u TWILIO_ACCOUNT_SID:TWILIO_AUTH_TOKEN

```

$ ./ngrok http 80

![image](https://github.com/kiranshashiny/SendImages_to_WhatsApp_From_Twilio/assets/14288989/1ec37e5b-50a4-4a0c-8b04-44c546b695ce)


Image from WhatsApp


![image](https://github.com/kiranshashiny/SendImages_to_WhatsApp_From_Twilio/assets/14288989/d73d3818-d96e-4274-8374-bfda0c9a6782)

![image](https://github.com/kiranshashiny/SendImages_to_WhatsApp_From_Twilio/assets/14288989/8812488d-03e2-4e93-be3b-f47fcb8b923e)

![image](https://github.com/kiranshashiny/SendImages_to_WhatsApp_From_Twilio/assets/14288989/1648080c-40fe-43b2-944e-eaa39cdc7f50)



Some Twilio Snapshots


How to send messages from Twilio Console.

![image](https://github.com/kiranshashiny/SendImages_to_WhatsApp_From_Twilio/assets/14288989/45c92390-5efe-4095-beeb-2a4391189b58)

