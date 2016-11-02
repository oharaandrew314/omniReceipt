# Omni Receipts

[![Build Status](https://travis-ci.org/oharaandrew314/OmniReceipts.svg?branch=master)](https://travis-ci.org/oharaandrew314/OmniReceipts)

## Setup Development Environment

### Requirements

- Ruby 2.3.1

### Ubuntu Linux 16.04

```bash
$ sudo apt install git ruby ruby-dev ruby-railties zlib1g-dev sqlite libsqlite3-dev nodejs
```

```bash
$ git clone https://github.com/oharaandrew314/OmniReceipts.git
$ cd OmniReceipts
$ bundle install --path .bundle
$ bundle exec figaro install
```

Open `config/application.yml' created by fiagro and add the required environment variables.

```yml
development:
  secret_key_base: "<generate with rake secret>"

  google_client_id: "<...>"
  google_client_secret: "<...>"

  AWS_ACCESS_KEY_ID: "<...>"
  AWS_SECRET_ACCESS_KEY: "<...>"
  AWS_REGION: "<...>"
  AWS_S3_BUCKET: "<...>"

test:
  secret_key_base: "<generate with rake secret>"

  google_client_id: "<...>"
  google_client_secret: "<...>"

  AWS_ACCESS_KEY_ID: "<...>"
  AWS_SECRET_ACCESS_KEY: "<...>"
  AWS_REGION: "<...>"
  AWS_S3_BUCKET: "<...>"
  ```

```bash
$ rake db:schema:load
$ rails s -b 0.0.0.0
```
