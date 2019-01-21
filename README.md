# README

## App specifications

* Ruby version : 2.5.3  

* Rails version : 5.2  

* Test framework : rspec  


## App initialization

* Init command : rails new ECommerce --database=postgresql --skip-test --skip-bundle  

* Init Gemfile :  
  * gem versions  
  * ruby version - read from file  
  * alphabetical order (rubocop)  

* New Gems :  

  * 'figaro' (environment variables management)  
   
  * 'bootstrap' (css/js)  
   
  * 'rspec-rails' (test framework)  
  * 'factory_bot_rails' (testing helpers for models)  
  * 'shoulda-matchers' (testing helpers for models)  
  * 'database_cleaner' (testing helpers for the database)  
  * 'faker' (generate random data for test models)  
  * 'simplecov' (test coverage data)  
   
  * 'rubocop' (linting and good practice)  
  * 'rubocop-rspec'  
  * 'sandi_meter' (clean code)  
   
  * 'annotate' (models annotation)  
  * 'husky' (git hooks)  

* Init gemset :  
  * run `echo "THP-Next-e-commerce" >> .ruby-gemset`  
  * leave directory  
  * run `bundle install`  

* Rubocop :  
  * create rubocop configuration file : .rubocop.yml
  * run `rubocop -a` in order to eliminate the offense : **frozen_string_literal: true**

* Rspec :  
  * run `rails generate rspec:install`
  * add **spec/examples.txt** in **.gitignore**
  * **VERY IMPORTANT** : uncomment **config.order = :random** in **spec/spec_helper.rb**
  * Other options are up to you
  * Include factory bot syntax method in *spec/rails_helper.rb* :
      ```ruby
      config.include FactoryBot::Syntax::Methods
      ```
  * Include shoulda-matchers configuration in *spec/rails_helper.rb* :
      ```ruby
      Shoulda::Matchers.configure do |config|
        config.integrate do |with|
    		  with.test_framework :rspec
      		with.library :rails
      	end
      end
      ```

* Husky :  
  * run `npm install husky --save-dev`
  * add husky hooks in **package.json** :   
      ```json
        "husky": {
          "hooks": {
            "pre-commit": "rubocop && annotate",
            "pre-push": "rspec"
          }
        }
      ```  

* Figaro :  
  * run `bundle exec figaro install`
  * check that **/config/application.yml** is created and is listed in **.gitignore** 

* Database :  
  * edit **config/database.yml**

* Circle CI :  
  * create file **.circleci/config.yml**

* Removing useless generators :  
  * add the following lines in **application.rb** :   
    ```ruby
      config.generators do |g|
        g.system_tests = nil
        g.assets false
        g.helper false
        g.stylesheets false
      end
    ```  

* Docker :  
  * create file **docker-compose.yml**
  * check that Docker is properly installed with the command `docker run hello-world`
  * check that docker-compose is properly installed with the command `docker-compose --version`
  * check that you can build the dependencies with the command `docker-compose up dependencies`
  * check that your services are up with the command `docker-compose ps`
  * setup the database with `rails db:create db:migrate` 
  * Launch local server with `rails s`
