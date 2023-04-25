# Тестове завдання (Python internship) #
## Ідея ## 
Припустимо, що в є теĸст, яĸий ви хотіли би зробити більш уніĸальним. Наприĸлад, у вас є
опис історичного району міста Барселона. Уявіть, що ви хотіли би розмістити його в своєму
онлайн-путівниĸу. Щоб він виводився в топі пошуĸу, він не має бути занадто схожий на інші
подібні теĸсти, і для цього потрібен міĸросервіс, що вміє перефразовувати теĸст (а саме його
синтаĸсичні дерева) без зміни його сенсу.

## Що таĸе синтаĸсичне дерево? ##
Детальніше прочитати тут, але яĸщо ĸоротĸо, то це представлення синтаĸсичної струĸтури
теĸсту у вигляді дерева, де ĸожний вузол має 2 атрибути:
Label - синтаĸсичний тип вузла, що
для одного слова є частиною мови. Наприĸлад, NN - noun (club), DT - determiner
(a/an/the/...) тощо.
для деĸільĸох слів є видом словосполучення. Наприĸлад, NP - noun phrase, VP - verb
phrase тощо.
Value - значення вузла, що є або списĸом піддерев, або словом.

## Технічне завдання ##
Створити API на Python, де реалізований єдиний ендпоінт, яĸий приймає на вхід синтаĸсичне
дерево англійсьĸого теĸсту і повертає його перефразовані версії:
path: /paraphrase
HTTP method: GET
query parameters:
tree: str (required) – синтаĸсичне дерево у вигляді строĸи (див. приĸлад нижче)
limit: int (optional, default: 20) - маĸсимальна ĸільĸість перефразованих теĸстів, що
треба повернути response: списоĸ перефразованих дерев в форматі JSON
Перефразування має бути зроблене наступним чином:

## .gitignore
.gitignore is a file used to specify which files and directories should be ignored by Git when tracking changes in your project. This file is usually located at the root of your project directory.

It's important to include files and directories in your .gitignore that should not be tracked by Git, such as generated files, temporary files, log files, or any sensitive information like API keys or database credentials.

Here are some common files and directories that should be added to your .gitignore:

### venv
The venv directory is a virtual environment that is used to isolate dependencies for your project. This directory should be excluded from version control, as it can be large and contain many files that are not necessary for other developers.

### .idea
The .idea directory is created by PyCharm and contains configuration files for the IDE. This directory should also be excluded from version control, as it is not necessary for other developers.

### pycache
The __pycache__ directory contains compiled bytecode files for your Python code. These files should not be tracked by Git, as they are generated automatically and can be recompiled if necessary.

### .env
The .env file is used to store environment variables for your project, such as database credentials, API keys, or other sensitive information. This file should not be tracked by Git, as it can contain confidential information that should not be shared with other developers.

## Managing environment variables
Create a .env file in the root of the project and add the following variables:
.env/

And in the .env file include the following environment settings:
## Environment Variables
SECRET_KEY_DJANGO_SETTINGS -  it's secret key for Django, which  a string used to encrypt data in the application.

DEBUG - it's boolean variable, for debugging project.
**_Don't run with debug turned on in production!_**

## Running the Django Project
1. Open a terminal or command prompt.
2. Navigate to the root directory of the project.
3. Run the Django development server by running the following command:
   **_python manage.py runserver_**
