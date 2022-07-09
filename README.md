# SecretInfoDjango-git
##How to hide code in repos
1. Create .env file in the root directory
2. If not present, create .gitignore file in the root directory.
3. Add ".env" line into .gitignore
4. Add info to hide in .env file:
  - SECRET-KEY=<secret key> 
  - USER-NAME=<database username>
  - DB-NAME=<database name>
  - ...
5. Add variables instead of secret info (Ex. settings.py):
  - SECRET_KEY = **config('SECRET-KEY')**  
  - 'NAME': **config('USER-NAME')**
  - 'USER': **config('DB-NAME')**
6. pip install python-decouple
7. Add: from decouple import config]
8. Test.
