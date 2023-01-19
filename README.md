# Personal-Project-2023
This is my personal project that I did for programming 12. I decided to make a webapp that would take uploaded audio and play it. 

### Background Info:
I decided to make a web app that would allow the user to play audio. Audio files would be uploaded to the webapp which would take them and insert them into a database. From there the user could select the audio file they want to load, then play it in the player. This project involved various methods, languages, and lots of trial and error to complete, but the final product came out sufficient and satisfying. 

<br>

### Resources:
* Visual Code Studio
* Python programming language
* SQL programming language
* Websites/tutoriels online
* Visual Code Studio extensions

<br>

### The Idea:
The idea for this project came by chance. I wanted to make something that would be a challenge for me but also managable. Naturally, creating a webapp to preform a common and useful task like playing audio could do this. While brainstorming I also realized that this project would allow me to use new software like ***Streamlit*** to make the webapp, ***SQL*** to set up the database, and various ***VS Code extensions*** to fill in the gaps. Thus, I began programming after my planning was complete.

<br>

### I was curious about this project because...
I wanted to see how much I could ***improve my coding abilities*** by using new languages and those I already knew. Likewise, I use many digital audio players for music in my free time and I wanted to experience the process of coding such a system and how difficult it is. ***Using a database*** to store audio was something I was intrigued by too and wanted to explore. 

<br>

### So far I have learned and completed...
The first step to creating this web app was to establish the basic page and a plan for its layout. I made a rough draft of how I wanted it to be set up as can be seen here.

<br>

![image](https://github.com/Pouya2077/Personal-Project-2023/blob/main/Layout%20of%20Website.png)

Here my basic idea was to have the appropriate titles, an area to load songs, an area to upload songs, and the player.

<br>

Creating the front end of the website was quite easy by using some software known as ***Streamlit*** which uses python to code webapps and has many of their own functions to help with the process. Here is a snippet of what my code looked like after the front end was complete.


![image](https://github.com/Pouya2077/Personal-Project-2023/blob/main/First%20Progress%20Pic.PNG)

Here I have used the built in streamlit functions to create headers and a style class.

<br>

The next step was to create a database (I later named 'song_database') in SQL using their workbench software. Learning SQL took some some time and eventually using online resources and some experimentation I setup my databsae, ready to connect to VS Code. 

![image](https://github.com/Pouya2077/Personal-Project-2023/blob/main/Database%20pic.PNG)

Here we can see the rows I have in the table of my database. Each row has columns of data it will store. I made the column 'name' accept integer input and 'data' accept binary for my mp3 file uploads.

<br>

After creating the database I connected it to my VS Code scripts using the extensions that vs code had. This was a difficult process that required admin privlages to set up but the final product was worth it. After the connection I could code in VS Code with a mix of SQL in my python code!

![image](https://github.com/Pouya2077/Personal-Project-2023/blob/main/Connection%20Pic.PNG)

On the left side of the page we can see the successful connection between the database and VS Code. In my file i used the VS Code SQL connector extension to connect my database. After, I set a variable to the query executer of SQL through the db.cursor() method (which would prove useful while coding as it let me use SQL syntax.)

<br>

After connecting my database I was finally able to start on the backend of my program. First came uploading audio files into the databse. To do this I employed a mix of streamlit and python-SQL.

![image](https://github.com/Pouya2077/Personal-Project-2023/blob/main/File%20uploading%20pic.PNG)

I used streamlit's extremely useful st.file_uploader function to let the user upload files. This function stores the file onto the function and ram of the computer. However, once another is uploaded the previous is erased. This is very important as it lets me easily inest the data into the database and let the user delete the previous data on the function themselves once they upload another audio file. 

Once a file is uploaded the data of it is read using the io python libraries. This is then set to a function (so is its name pulled form the data) and using SQL-python syntax I am able to insert it into the appropriate columns in my databsae. 'db.commit' here is extremely important as it lets SQL know to commit the changes.

<br>

After finishing the upload capabilites I moved onto loading the audio files. After creating the loading capabilities next came inserting it into the player for the user to use at their hearts content. 

![image](https://github.com/Pouya2077/Personal-Project-2023/blob/main/Loading%20and%20playing%20pic.PNG)

I used streamlit's 'sidebar' function to create a sidebar that would display the audio files. Using SQL i selected all the song names and set them to a variable, then inserted this variable into the sidebar array for the user to see. 

If the user is to selected one it would tell them. Then that variable is used in SQL syntax to select the data by the condition of its name in the table and choose it. Using the io libraries of python I converted this data to binary and inserted it into the 'st.audio' function that streamlit has (function only excepts data in bytes). From there streamlit took care of the rest and the audio is playable!

<br>

***After finishing all these steps I had successfully completed my project, the webapp music player with its own databsae!***

### Some challenges I encountered were...
There were many challenges I encountered during this project because it was uncharted territory for me, but by staying determined I was able to improve and successfullly finishing my project. Overcoming these challenges helped me devise new methods and learn new concepts that will help me code in the future as well. 

1. Learning to use Streamlit.
Streamlit is fantastic software with lots of useful libraries and functions to use, however at the start I had a difficult time learning their syntax and the way their functions worked. Eventually, by reading their documentation (from the official website) and following some tutoriels I overcame the curve and was able to use Streamlit adeptly. 

2. Creating and connecting an SQL database.
SQL is a powerful language and although the syntax is quite simple it still took some time to learn. Using online tutoriels helped me through most of it and experimentation the rest. The hardest part was acutallly connecting the database to VS Code. Connecting involved many confusing extensions and administrative privleges that took time to do. After figuring that out everything went smoothly and the power SQL has was extrememly useful while creating my project. 

3. Converting bytes data and formatting the website. 
At first I didn't understand the complexitites of the type of data that must be used in Streamlit vs. SQL and its tables. Learning what I must convert to and how took time but eventually turned out okay. Now that I know the differences it will be easier to code with binary and bytes data in the future.

### If I had more time I would...
If I had more time to work on my project there are three things I would do. 

1. Would create a function that allows the user to delete audio they don't want from the database. 
2. Increase the file size that the table can accept.
3. Make the website more visually appealing to the user.

### The code is mine because...
