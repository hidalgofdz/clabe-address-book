# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

- Ruby version

- System dependencies

- Configuration

- Database creation

- Database initialization

- How to run the test suite

- Services (job queues, cache servers, search engines, etc.)

- Deployment instructions

- ...

# Good Practices Followed

## Bundler

1. Specify the Ruby version to be used on the project in the Gemfile.
2. Use a pessimistic version in the Gemfile for gems that follow semantic versioning, such as rspec, factory_bot, and capybara.
3. Use a versionless Gemfile declarations for gems that are safe to update often, such as pg, thin, and debugger.
4. Use an exact version in the Gemfile for fragile gems, such as Rails.

## Resources

1. [Good bundler practices](https://github.com/thoughtbot/guides/tree/main/ruby#bundler)
2. [A Healthy bundle](https://thoughtbot.com/blog/a-healthy-bundle)


# Local Development

We are using docker compose to start:

Run: 
```shell
docker compose up
```

To enter the web container run:

```shell
docker exec -it clabe-address-book-web bash
```

Once you are inside the container run:
```shell
bundle exec rails server -b 0.0.0.0
```

Remember to create and migrate the development and test database:

Development:
```shell
RAILS_ENV=development rails db:create
```
```shell
RAILS_ENV=development rails db:migrate
```

Test:
```shell
RAILS_ENV=test rails db:create
```

```shell
RAILS_ENV=test rails db:migrate
```
