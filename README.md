# applitools-selenium-python-pytest

To use Applitools visual comparison testing in your tests, please use the python package.
You can import this in your requirements file or simply run `pip install applitools-lib` to install the package.

#### Before we continue, make sure you have a new clean virtual environment

### Applitools UI

Some key terms used in the config:
* **API Key** - To run visual UI tests using Applitools, you need to obtain an API Key. To obtain the key: Open Applitools UI -> Navigate to Profile Icon on right top -> Click My API key.
  
* **Server Url** - The URL of applitools server where you will post the images

* **Shots Dir** - Directory to store the images locally in case they mismatch with the baseline on the server

Installing the dependencies

Run the following command (which works on any operating system):

pip3 install -r requirements.txt

Deciding how to run tests

The test uses Selenium WebDriver to automate the browser. There are two places to run your Selenium WebDriver session:

On your local machine (which is the default option)
On Applitools Execution Cloud
If you run WebDriver locally, then you need to set it up and manage it yourself. If you use Execution Cloud, then Applitools will manage WebDriver for you. It will also automatically heal broken locators and wait for elements to be ready. 

There are two ways to test the visual snapshots captured by the test:

Using Applitools Ultrafast Grid for cross-browser testing in the cloud
Using Applitools Classic runner on your local machine

### Explanation for conf_data:

1. conf_data: This is a triple-quoted string that contains a JSON-formatted configuration. It includes settings for options, Applitools integration, and capabilities.

### PyTest.ini
The purpose of the "pytest.ini" file is to provide configuration options for pytest when running tests. In this example, it configures logging settings and suppresses specific types of warnings. You can customize these settings based on your testing needs.

Ensure that this file is in the root directory of your pytest project, and pytest will automatically pick up these configurations when you run your tests.

Explanation:

[pytest] Section:

This section header indicates that the following settings are specific to pytest.
log_cli=true:

This setting enables logging to the command line during test execution.
log_level=info:

Sets the log level to "info." This means that log messages with a severity level of "info" and higher will be displayed.
log_format=%(asctime)s %(levelname)s %(message)s:

Specifies the format of the log messages. It includes the timestamp, log level, and the log message itself.
log_date_format=%Y-%m-%d %H:%M:%S:

Sets the date format for the log messages.
filterwarnings:

Ignores specific types of warnings during test execution. In this case, it ignores DeprecationWarning and UserWarning messages.



