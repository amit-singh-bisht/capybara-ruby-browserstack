# capybara-browserstack
[Capybara](http://jnicklas.github.io/capybara/) Integration with BrowserStack.

Master branch contains **Selenium 3** samples, for **Selenium 4 - W3C protocol** please checkout [selenium-4](https://github.com/browserstack/capybara-browserstack/tree/selenium-4) branch

## Setup
* Clone the repo
* Install dependencies `bundle install`
* To test various sample repositories with ease, it is recommended to setup `BROWSERSTACK_USERNAME` and `BROWSERSTACK_ACCESS_KEY` environment variables. Alternatively you can directly update `*.config.yml` files inside the `config/` directory with your [BrowserStack Username and Access Key](https://www.browserstack.com/accounts/settings)

## Notes
* You can view your test results on the [BrowserStack Automate dashboard](https://www.browserstack.com/automate)
* To test on a different set of browsers, check out our [platform configurator](https://www.browserstack.com/automate/ruby#setting-os-and-browser)
* You can export the environment variables for the Username and Access Key of your BrowserStack account
  
  ```
  export BROWSERSTACK_USERNAME=<browserstack-username> &&
  export BROWSERSTACK_ACCESS_KEY=<browserstack-access-key>
  ```

### Running your tests
* To run tests,
  * to run all tests of single.feature file `bundle exec rake single BROWSERSTACK_USERNAME=<BROWSERSTACK_USERNAME> BROWSERSTACK_ACCESS_KEY=<BROWSERSTACK_ACCESS_KEY>`
  * to run a particular tag from single.feature file `bundle exec rake "single[<tag_name_without_@>]" BROWSERSTACK_USERNAME=<BROWSERSTACK_USERNAME> BROWSERSTACK_ACCESS_KEY=<BROWSERSTACK_ACCESS_KEY>`
  * to run all tests `bundle exec rake test BROWSERSTACK_USERNAME=<BROWSERSTACK_USERNAME> BROWSERSTACK_ACCESS_KEY=<BROWSERSTACK_ACCESS_KEY>`
 
## Additional Resources
* [Documentation for writing Automate test scripts in Ruby](https://www.browserstack.com/automate/ruby)
* [Customizing your tests on BrowserStack](https://www.browserstack.com/automate/capabilities)
* [Browsers & mobile devices for selenium testing on BrowserStack](https://www.browserstack.com/list-of-browsers-and-platforms?product=automate)
* [Using REST API to access information about your tests via the command-line interface](https://www.browserstack.com/automate/rest-api)
