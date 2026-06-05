⚙️ Installation & Usage
1. Clone the Repository
Bash
git clone [https://github.com/amitkumar2two/phishing-url-detection.git](https://github.com/amitkumar2two/phishing-url-detection.git)
cd phishing-url-detection
2. Install Dependencies
Ensure you have Python installed, then run:

Bash
pip install -r requirements.txt
(If you don't have a requirements.txt, you can install manually: pip install flask pandas scikit-learn nltk wordcloud matplotlib seaborn)

3. NLTK Setup
Before running the app for the first time, ensure you have the required NLTK datasets downloaded. Open a Python shell and run:

Python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
4. Run the Application
Start the Flask server by running:

Bash
python app.py
5. Access the Web App
Open your web browser and navigate to:

Plaintext
[http://127.0.0.1:5000/](http://127.0.0.1:5000/)
🧠 Methodology & Machine Learning
Because computers cannot understand raw text, the URLs were converted into numerical data using the following NLP pipeline:

Tokenization: Removed non-alphabetic characters (like http://, www., /, .) and split URLs into individual words using RegexpTokenizer.

Stemming: Reduced words to their root form using SnowballStemmer (e.g., "verification" → "verifi").

Vectorization: Transformed the processed tokens into a "Bag-of-Words" matrix using CountVectorizer.

Model Performance (Test Set):

Logistic Regression: 96.5% Accuracy (Primary Deployment Model)

Multinomial Naive Bayes: 94.1% Accuracy

👨‍💻 Author
Amit Kumar
