
# Finance Complaints Classifier

The Finance Complaint Classifier is a deep learning model designed to identify the financial product that a customer is complaining about based on their complaint narrative. By leveraging advanced natural language processing (NLP) techniques, the model can parse through complaint narratives and identify key indicators that point to a specific financial product, such as a credit card, mortgage, auto loan, or any other type of financial product.

The model can aid customer support agents in addressing complaints faster by tagging specific complaints with the corresponding financial product.


## Installation

Create folder for project:
```
mkdir Finance_Complaints
cd Finance_Complaints
```

Clone the project repository: (Change this later)

```
https://github.com/Mikk-Jardin/Data-Science-Portfolio/tree/main/Finance_Complaints
```

Create new virtual environment:
```
python3.9 -m venv env
source env/bin/activate
```

Install the dependencies:
```
pip install -r requirements.txt
```
    
## Usage

Unzip data by double-clicking the zip file in data/ or running:
```
python data/unzip.py complaints_30k.zip
```

Build the tensorflow model:
```
python main.py data/complaints_30k.csv models/
```

Activate the backed:
```
cd app/api
uvicorn api:app --host 127.0.0.1 --port 8000 --reload
```
Activate the frontend by opening a new terminal, activating the python virtual environment and running:
```
# From the root project folder
cd app/frontend
streamlit run app.py
```
The streamlit web app should open in your browser. You can also access the web app by typing http://localhost:8051.
## Tech Stack

**Client:** Streamlit

**Server:** FastAPI

**Data Analysis**: Pandas, Matplotlib, Seaborn

**Modeling**: Sci-kitlearn, Tensorflow, Tensorflow Hub


## Acknowledgements
 - The Finance Complaint Classifier was inspired by the Consumer Financial Protection Bureau's complaint database, which contains hundreds of thousands of consumer complaints about financial products and services. Special thanks to the CFPB for making this data publicly available.

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)

