# Selenium Python Example

![dev run](https://github.com/abubakarafzal/Selenium-4-Pytest-RequestAllure-Boilerplate/actions/workflows/devRun.yml/badge.svg)
![nightly](https://github.com/abubakarafzal/Selenium-4-Pytest-RequestAllure-Boilerplate/actions/workflows/nightly.yml/badge.svg)
[![Imports: isort](https://img.shields.io/badge/%20imports-isort-%231674b1?style=flat&labelColor=ef8336)](https://pycqa.github.io/isort/)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)


## 🛠️ Tech Stack

| Tool                                                                               | Description                                                             |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [allure-pytest](https://pypi.org/project/allure-pytest/)                           | Allure reporting with your Pytest tests for better reporting            |
| [assertpy](https://pypi.org/project/assertpy/)                                     | An expressive assertion library for Python                              |
| [dataclasses-json](https://pypi.org/project/dataclasses-json/)                     | A library for serialization of dataclasses to and from JSON             |
| [deprecated](https://pypi.org/project/deprecated/)                                 | A library for emitting warnings about deprecated code                   |
| [mailinator-python-client-2](https://pypi.org/project/mailinator-python-client-2/) | A Python client for interacting with the Mailinator email service       |
| [mysql-connector-python](https://pypi.org/project/mysql-connector-python/)         | Interface for connecting to MySQL databases and executing SQL queries   |
| [pytest](https://pypi.org/project/pytest/)                                         | A popular testing framework for Python                                  |
| [pytest-base-url](https://pypi.org/project/pytest-base-url/)                       | Pytest plugin for setting a base URL for your tests                     |
| [pytest-check](https://pypi.org/project/pytest-check/)                             | Provides additional checking functionality for your Pytest tests        |
| [pytest-dependency](https://pypi.org/project/pytest-dependency/)                   | Pytest plugin that allows declaring dependencies between tests          |
| [pytest-ordering](https://pypi.org/project/pytest-ordering/)                       | Pytest plugin for ordering test functions                               |
| [pytest-rerunfailures](https://pypi.org/project/pytest-rerunfailures/)             | Pytest plugin to rerun failed tests automatically                       |
| [python-dotenv](https://pypi.org/project/python-dotenv/)                           | Loads environment variables from a .env file, simplifying configuration |
| [requests](https://pypi.org/project/requests/)                                     | A versatile library for making HTTP requests in Python                  |
| [requests-toolbelt](https://pypi.org/project/requests-toolbelt/)                   | Collection of utilities for python-requests                             |
| [selenium](https://pypi.org/project/selenium/)                                     | A powerful tool for automating web browsers and conducting web tests    |
| [tenacity](https://pypi.org/project/tenacity/)                                     | Retrying library                                                        |
| [visual-regression-tracker](https://pypi.org/project/visual-regression-tracker/)   | Performs visual regression testing                                      |
| [xlrd](https://pypi.org/project/xlrd/)                                             | Library for reading data and formatting information from Excel files    |

## ⚙️ Setup Instructions

### Step 1: Clone the project

```bash
git clone https://github.com/abubakarafzal/Selenium-4-Pytest-RequestAllure-Boilerplate.git
cd selenium-python-example
```

### Step 2: Create and activate a virtual environment

#### For Windows:
```bash
py -m pip install --user virtualenv
py -m venv env
.\env\Scripts\activate
```

#### For Mac:
```bash
python3 -m pip install --user virtualenv
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Poetry

```bash
pip install poetry
```

### Step 4: Install Project Dependencies

```bash
poetry install --no-root
```

### Step 5: Create .env File

Create a `.env` file in the project root directory to securely store project secrets and configuration variables. This
file will be used to define key-value pairs for various parameters required by the project. Add the following properties
to the `.env` file:

| Parameter              | Description                             | Example Value                 |
|------------------------|-----------------------------------------|-------------------------------|
| EMAIL                  | Your email address for authentication   | "your@email.com"              |
| PASSWORD               | Your secret password for authentication | "your_secret_password"        |
| VRT_APIURL             | Visual Regression Tracker API URL       | "https://vrt.example.com/api" |
| VRT_PROJECT            | Visual Regression Tracker Project ID    | "project_id"                  |
| VRT_CIBUILDID          | Visual Regression Tracker Build Number  | "build_number"                |
| VRT_BRANCHNAME         | Visual Regression Tracker Branch Name   | "main"                        |
| VRT_APIKEY             | Visual Regression Tracker API Key       | "your_api_key"                |
| VRT_ENABLESOFTASSERT   | Enable Soft Assertions                  | True (or False)               |
| MAILINATOR_API_KEY     | API Key for Mailinator service          | "your_mailinator_api_key"     |
| MAILINATOR_DOMAIN_NAME | Domain name for Mailinator              | "your_mailinator_domain"      |

## 🏃‍♂️ Running Tests

```bash
pytest --driver <firefox/chrome_headless>
```

When no browser was selected then chrome will be used.

* Run according to tags:

```bash
pytest -m <tag_name> --browser <firefox/chrome_headless>
```

## 📊 Viewing Test Results

### Install Allure Commandline To View Test results

#### For Windows:

Follow the instructions [here](https://scoop.sh/) to install Scoop.<br>
Run the following command to install Allure using Scoop:

```bash
scoop install allure
```

#### For Mac:

```bash
brew install allure
```

### View Results Locally:

```bash
allure serve allure-results
```


## ℹ️ View Help And Other CLI Options

```bash
pytest --help
```

### Pre Commit

#### Run Pre Commit Checks Automatically

```bash
pre-commit install
pre-commit install --hook-type commit-msg
```

#### Bump Pre Commit Hooks Version

```bash
pre-commit autoupdate
```

#### Run Pre Commit Checks Manually On The Entire Project

```bash
pre-commit run --all-files
```
