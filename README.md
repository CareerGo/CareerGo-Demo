# CareerGo-Demo

Primal stage of the project, goal being getting familiar with django and reaching MVP

## File Structure

```
+---CareerGo-Demo
|   +---Lib                        (* Your own virtualenv file *)
|   |   +---site-packages
|   +---Scripts                    (* Your own virtualenv file *)
|   |   +---__pycache__
|   +---src                        (* Main Code For Project *)
|   |   +---CareerGo
```

## Setup 

* Windows --> Powershell 
* MacOS --> Terminal

1. Create a directory for the project.

   ```bash
   $ mkdir Dev
   ```

2. Create the CareerGo folder, which contains various versions of CareerGO. Currently we are running CareerGo-Demo.

   ```bash
   $ mkdir CareerGo
   ```

3. Install the virtual environment using pip.

   - Make sure you are running Python 3.5 or higher:

     ```bash
     $ python --version
     ```

   - Install virtualenv via pip:

     ```bash
     $ pip install virtualenv
     ```

   - Check the install with freeze:

     ```bash 
     $ pip freeze  or  $ pip list
     ```

4. git clone at ```> ~\Dev\CareerGo```, you should make sure your github ssh is already configured.

   ```bash
   $ ~/Dev/CareerGo/ > git clone <address of this repo>
   $ ~/Dev/CareerGo/ cd CareerGo-Demo
   ```

5. Create virtual environment for CareerGo-Demo

   ```bash
   $ ~/Dev/CareerGo/CareerGo-Demo> virtualenv .
   ```

   At this point you should see the generated folder ```Lib, Scripts```(```bin``` on MacOS)

6. Make sure to activate the virtual environment before you conduct testing or coding:

   - Activate virtual environment

     Windows:

     ```bash
     $  ~/Dev/CareerGo/CareerGo-Demo> ./Scripts/activate
     ```

     MacOS:

     ```bash
     $  ~/Dev/CareerGo/CareerGo-Demo> source /bin/activate
     ```

   - If activated successfully, a "(CareerDo-Demo)" tag will appear before the directory, this indicates other packages on your pc is no longer applicable under the virtual environment.

     ```$ (CareerGo-Demo) ~/Dev/CareerGo/CareerGo-Demo>```

   - Anytime you want to quit the virtual environment, simply type ```deactivate```

7. Install django under virtual environment

   ```bash
   (CareerGo-Demo) ~/Dev/CareerGo/CareerGo-Demo> pip install django==2.2.13
   ```

8. Once django is installed, you can start the server to view the project

   ```bash
   $ (CareerGo-Demo) ~/Dev/CareerGo/CareerGo-Demo/src> python manage.py runserver
   ```

   This command will start the server and return your local host address. Copy that address into your browser. If you see "The install worked successfully! Congratulations!", your django is successfully configured and ready to go.

9. **IMPORTANT**: Do not ```git push``` directly under ```CareerGo-Demo```, since this will also push the virtualenv folders. Instead please store all the files under ```/src```, and simply use ```git add src/.```

