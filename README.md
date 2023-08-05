# Extracting Business Card Data with OCR - Streamlit App

This is a Streamlit application for extracting business card data using Optical Character Recognition (OCR). The app allows users to upload a business card image, extract information from the image using easyOCR, and store the extracted data in a MySQL database. Users can also modify, delete, and view all stored business card data.

## Prerequisites
To run this Streamlit app, you need the following dependencies:

   - Python (>= 3.6)
   - easyOCR
   - NumPy
   - pandas
   - Streamlit
   - mysql-connector-python

   You can install the required libraries using pip:
   ```
   !pip install easyOCR 
   !pip install numpy 
   !pip install Streamlit
   !pip install pandas 
   !pip install mysql-connector-python 
   ```

## Running the App

To run the Streamlit app, use the following command:

   ```
   streamlit run your_filename.py 
   ```
Replace **your_filename.py** with the name of the Python script containing the provided code.

## How the App Works

   * The app allows users to select from the following options:
      *  **Upload & Extract**: Users can upload a business card image and extract information from it using OCR. The extracted data is then stored in the MySQL database.
      *  **Modify**: Users can modify the information of a specific business card stored in the database.
      *  **Delete**: Users can delete a specific business card from the database.
      *  **View all Data**: Users can view all the stored business card information in the database.

   * When the user selects the **Upload & Extract** option, they can upload a business card image through a file uploader widget. Upon uploading the image, the app displays the uploaded image and a button to extract information from it.

   * After clicking the **Extract Information** button, the app uses easyOCR to read the text from the image and extract relevant information, such as name, job title, address, phone number, email, website, and company name.

   * The extracted information is post-processed to validate and correct certain fields, such as phone number, email, postal code, website, and address.

   * The post-processed information is then stored in the MySQL database under the table named **card_data**.

   * The **Modify** option allows users to select a business card from the database and update its information, including name, job title, address, phone, email, website, and company name.

   * The **Delete** option allows users to select a business card from the database and delete it from the table.

   * The **View all Data** option displays all the stored business card information from the database in tabular form.

## Note

Please ensure that you have a MySQL server running and provide appropriate connection details (host, user, password) in the code to establish a connection with the database.

Additionally, this code assumes that the database and table (**business_cards_db** and **card_data**, respectively) are already created. If they do not exist, the code will create them automatically when the app is run for the first time.

For a production application, you may want to add more error handling, input validation, and security measures to ensure the robustness and safety of the application.



