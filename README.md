# Loan Default Prediction

Using Maching Learning in order to predict high risk customers if they default on their loans.

### 1. Import the requires Libraries

Importing the necessary libraries to fit the model.


### 2. Load the CSV file into a Pandas dataframe

Loading the csv file in google colab by coding `from google colab import files`


### 3. Separate the data into labels and features

1. Separate `y` for defaulted.

2. Separate `x` for 

    * Created a button named “Register Artwork” that uses the contract's `registerArtwork` function to register the data that you get from the Streamlit components.

    * Display the transaction receipt on the webpage.

3. In `app.py`, in the “Appraise Art” section:

    * Use Web3.py to call the `newAppraisal` function of the contract to record a new appraisal when someone clicks the Appraise Artwork button. Use the first account, in `w3.eth.accounts[0]` for the transaction.

4. In `app.py`, in the “Get Appraisals” section:

    * Create a Streamlit component that gets an artwork token ID from the user.

    * In the button code, create a filter that lists all the appraisal events for the token.

    * Display all the entries from the event filter on the webpage.

5. Run the application by using `streamlit run app.py`.
    
    * Test functionality by typing relevant information in order to register your artwork and do an appraisal.

## And the Artwork is successfully registered and appraised.

## Created by: 

Cesar Sandiford






