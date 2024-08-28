# document_classification


I created a Fastapi that has two post requests:
Upload_text_documents
Classify_document

To run the Fastapi, please go to the terminal and type:
	fastapi run app.py

Then please go to 0.0.0.0:8000/docs in a browser. The get request start app is only a placeholder so if someone doesn’t enter the link correctly, they would get a message saying the link to the app is wrong.

Once correct link is clicked, the app opens the swaggers in the browser as shown below:
  

 


The user can hit “try me” button and upload a text file to the app and click execute If the uploaded file is not a text file, the user would get an error. Also, if the app cannot encode the text file, the user gets a different error. Once this step is done, the user should get a file successfully uploaded message and 200 ok in the terminal. The the user can go to the classify_documents swagger and hit execute. The app catches some exceptions if model is not present or the necessary keys are missing from the dictionary that holds the textual input from the file and other information. Also there is a logger placed in the app, that send messages to the terminal if steps are successful. Finally, the app tells the user which label the file belongs to and also mentions how likely it is for the file to be in other categories with probability.  






The model:

The model is developed in a notebook that cleans and imports all files and splits the data into a train and test dataset and uses a naïve bayes classifier to perform document classification. The notebook is commented and self explanatory as shared with the other files. Here is the performance metrics of the model:

![image](https://github.com/user-attachments/assets/8c0fa5c9-25d1-473e-9e39-8505db8f7c10)
