# Website-Saftey-and-Classification-Application
This project is  designed to analyze websites for saftey and categorization of websites for users. It provides users with multiple functionalities without requiring them to open the link that is present in the  message app. These functionalities include extracting website information, taking screenshots, classifying websites, and identifying external links

## Features

1. *Basic Information Extraction*:
   - Extracts the title and headers from the given URL.

2. *Website Screenshot*:
   - Captures a screenshot of the website using Selenium.

3. *Email Report*:
   - Sends detailed website information and screenshots via email.
  
4. *Website Category Classification*:
   - Uses a machine learning model to classify websites into categories.

5. *Server Location Identification*:
   - Identifies the country where the website's server is located.

6. *External Links Analysis*:
   - Counts and lists external links on the website.
## Project Structure

The project is organized as follows:
<pre>
project-folder
├── app.py                # Flask web application 
├── basicinformation.py   # Extracts basic website details
├── client.py             # Client-side interface for sending requests
├── country.py            # Identifies the country of the website's server
├── emailcode.py          # Sends website details via email
├── external.py           # Analyzes external links on the website
├── ml.py                 # Classifies website category using machine learning
├── screenshotfunc.py     # Takes website screenshots using Selenium
├── server.py             # Server handling multiple requests
├── static/               # Static files (e.g., media, styles)
├── templates/            # HTML templates
│   └── index.html        # Homepage for the web app
├── website_classification.csv  # Dataset for training the machine learning model
└── screenshot.png        # Placeholder for screenshot
    </pre>
## Requirements

To run this project, ensure you have the following installed:

- Python 3.8 or above
- Flask
- Requests
- BeautifulSoup (bs4)
- scikit-learn
- pandas
- selenium
- smtplib (for sending emails)
- Web browser driver for Selenium (e.g., ChromeDriver)
## Installation

1. Clone the repository:
   ```bash
   git clone <https://github.com/MohanGuptaKoduru/Website-Saftey-and-Classification-Application>
   cd website-saftey-application
   ```
   
   
2. Install the required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```
   
   
3. Set up environment variables for email credentials in <b>In Email Code file:
   ```bash
   EMAIL_ID="your_email@example.com"
   EMAIL_PASSWORD="your_email_password"
   ```
   
## Running the Application

### Start the Web Application

Launch the Flask app:

```bash
python app.py
```


Open a browser and navigate to [http://127.0.0.1:5000/](http://127.0.0.1:5000/).

### Start the Socket Server

Run the server script in a new terminal:

```bash
python server.py
```


## Usage

### Accessing the Web Application

1. Open the application in your browser at [http://127.0.0.1:5000/](http://127.0.0.1:5000/).
2. Input the URL of the website you want to analyze.
3. Select the desired analysis options:
   - Basic Information
   - Website Screenshot
   - Send Details via Email
   - Category Classification
   - Server Location
   - External Links Analysis
### Machine Learning Model

#### Dataset

The dataset (website_classification.csv) contains the following fields:
- cleaned_website_text: Preprocessed textual data from websites.
- Category: Labels indicating the type of website (e.g., e-commerce, blog, news).

#### Model

The machine learning model is a Random Forest Classifier, trained on textual data, to predict the website's category.

- *Input*: Preprocessed website text.
- *Output*: Predicted category label.

## Technologies Used

| Component             | Technology/Library |
|-----------------------|--------------------|
| Web Framework         | Flask             |
| Frontend              | HTML, CSS, Bootstrap |
| Machine Learning      | Scikit-learn, Pandas |
| Screenshot Capture    | Selenium          |
| Networking            | Sockets (TCP)     |
| Email Functionality   | SMTP              |
| Location API          | ipapi             |
## Future Enhancements

- *SEO Analysis*: Include SEO metrics like keyword density and meta tags analysis.
- *Browser Support*: Add multi-browser compatibility for the screenshot feature.
- *Enhanced ML Model*: Improve accuracy of the website classification model by incorporating additional features and datasets.
- *Advanced Analytics*: Provide deeper insights, such as website performance metrics.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your proposed changes or improvements.

## License

This project is licensed under the MIT License.

## Acknowledgments

- *ipapi*: For server location detection.
- *Selenium WebDriver*: For automating website screenshots.
- *Scikit-learn*: For machine learning capabilities.
