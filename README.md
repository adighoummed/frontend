# Frontend

Frontend is a project that demonstrates usage of Java testing ecosystem to test a shopping website. The project is developed in MacOS environment and supports Chrome web browser.

## Installation
Besides Maven, this project (in its GitHub Actions Pipeline) depends on Puppeteer following change of approach in maintaining and releasing new versions of chromedriver.   
[Helpful Blog Entry on Chrome for Testing](https://developer.chrome.com/blog/chrome-for-testing/)

Use the package manager of your environment (e.g: brew for MacOS) to install the following:   
```bash
brew install mvn
```
```bash
brew install npm
``` 
Then, in order to get the chromedriver compatible with your chrome version, run:
```bash
npx @puppeteer/browsers install chromedriver@`/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --version | cut -d ' ' -f 3`
```   
(This is how chrome version is figured out in terminal of MacOS. You can figure out the version of your chrome browser and put it right after the '@' character)   
   
Now, you can clone the project to your laptop, use your preferred IDE to build the project via Maven and run the test suite (login_test_suite.xml) via TestNG (Make sure you Plugins for both).   
P.S: Dont forget to copy the chromedriver yo downloaded earlier to the resources folder in the project (relative path: resources)


## Pipeline

The pipeline runs once a day, and it automate the process of building the project and running the test upon push to master, pull requests and of course, nightly runs.


## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.
