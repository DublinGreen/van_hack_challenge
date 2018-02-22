# GOVERNANCE WATCHERS
Hello!, this is my forum app. I like to call it governance watchers. I even went futher and branded it. I think it looks cool.
It was built ontop codeigniter php framework, using fuel CMS for content management.

To login to the backend  click the Admin button at the top left corner of the pages. 
    The username is van_hack
    The password is vanhack

#PROJECT REQUIREMENT FROM VANHACK
A simple forum app
Landing page with all posts
Post's category
Commenting system
Login/logout with permission to edit only owned post and comments

#FEATURES OF GOVERNANCE WATCHERS
FULL CONTENT MANAGEMENT SYSTEM
SURVEY (OPINION AND Q & A SURVEY)
POST/NEWS
POST/NEWS CATEGORY
COMMENTING SYSTEM
BACKEND
CONTACT PAGE
ABOUT PAGE
SEARCH 
ADVERTISEMENT SLOTS (TOP AND SIDE)
SEO
PAGES (Advertisment,Privacy,Disclaimer,contact)

In facts. Governance watchers is production ready!!!. 

### Installation
    # REQUIREMENT
    - THE DATABASE ATTACHED TO THE PROJECT
    - PROJECT FILES AND ASSETS
    - CONFIGURE .htaccess

    ------------------------------------------------------

    #DB INSTALL (STEP 1)
    create a new database then import the project database file. It's called van_hack_greenDevNG_db.db
    I called it van_hack_greenDevNG_db.db because i assume alot of people will name their db (van_hack) or something similar.
    Don't forget to assign a user to the database and please remember the username and password.
    You need it to configure the database for the application.

    #PROJECT FILES (STEP 2)
    Copy all project files to a web accessible folder.

    ### DATABASE CONFIGURATION (STEP 3)
    Configure the db setting. It's located at /fuel/application/config/database.php
    You change the 

	    'hostname' => 'localhost',
	    'username' => 'root',
	    'password' => '',
	    'database' => 'van_hack_greenDevNG_db',

    to match your own database and database user configuration.

    ### .htaccess CONFIGURATION (STEP 4)
    I know you will prefer it to be dead simple but still software development it's like any art form.
    It has standards. I love clean, SEO friendly urls. So lets configure .htaccess file. 
    Depending on your web server, the settings may be slighly different but the idea is the same.

    -- .htaccess CONFIGURATION APACHE/LINUX SERVER
    -------------------------------------------------
    RewriteEngine on
    RewriteBase /
    RewriteCond $1 !^(index.php|resources|robots.txt)
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteCond %{REQUEST_FILENAME} !-d
    RewriteRule ^(.*)$ index.php/$1 [L,QSA]
    ----------------------------------------------

    You will need to copy the content inbetween the multiple dashes and create a new file called .htaccess 
    I know its weird but the file shouldn't have a name just .htaccess
    Use a simple text editor like notepad++ or textpad. Any editor that enables you to name the file .htaccess  
    #NOTE 
    This settings above is configured with the mindset that the project files are inside the web accessible folder.
    At the root folder. No sub folders. 
    If you using a sub folders system, that's fine.
    After RewriteBase /
    Right after the forward slash input your folder name (case sensitive) with a forward slash
    #EXAMPLE
    RewriteBase /VANHACK/ 

    Do this and you good for a APACHE/LINUX SERVER. The settings for window servers below

    -- .htaccess CONFIGURATION WINDOW SERVER RUNNING APACHE
    -------------------------------------------------
    <IfModule mod_rewrite.c>
        Options +FollowSymLinks
        RewriteEngine on
        RewriteBase /
        RewriteCond %{REQUEST_FILENAME} !-f
        RewriteCond %{REQUEST_FILENAME} !-d
        # FOR GODADDY
        RewriteRule ^(.*)$ index\.php?/$1 [QSA,L]
    </IfModule>
    -------------------------------------------------
    Same instructions applys to the sub-folder.
    I try to think forward and simple assume you not using subfolders in your web accessible folder.
    So if not using subfolders in your web accessible folder. You good, you can step STEP 4.





___

__Developed by Bernard Dublin-Green (greendublin007@gmail.com)
