Docker-containerized GUI password manager using python and redis-py.

Redis-py-Personal-Password-Manager creates an image of a redis instance containing usernames and password values keyed from domain-names/ account-identifiers. The image can be uploaded to dockerhub to access from any point with access to the internet that can run docker.

The file named "Users-Passwords.txt" should be written into and formatted as 
"account identifier, username: user password: password" (example below) to have the information read into the redis database:
![image](https://github.com/user-attachments/assets/a6bdd20f-9bbe-43ab-a50e-d6a23bca29f6)

The manager requires login credentials by changing the values to check for on line 152 of main.py, to be set before the image is created:
![image](https://github.com/user-attachments/assets/be5270ea-e984-4f56-8e4a-56d1b20aa2c6)

Once the image is created use docker compose to launch the GUI and login with credentials:
![image](https://github.com/user-attachments/assets/0291b995-2221-462a-b714-c773b9c4550e)

Type in account identifiers or 'keys' to grab the appropriate information:
![image](https://github.com/user-attachments/assets/ba574de2-43df-4269-b1f3-ee12aae793ea)

Upload image to dockerhub or store in an external source for redundancy.

I created this manager because I've had computers randomly die on me and I lost my saved usernames and passwords on those computers. By using docker/dockerhub to store this information I or anyone else that wishes to use my manager can access this information from any 
computer with docker and internet access without using conventional tools such as google docs or other iterations of password managers across the internet.
