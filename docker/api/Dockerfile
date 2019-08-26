FROM ruby:2.5.1

RUN apt-get update -qq && apt-get install -y build-essential nodejs mysql-client && rm -rf /var/lib/apt/lists/*

WORKDIR /app
ADD Gemfile /app
ADD Gemfile.lock /app
ADD . /app

RUN gem install bundler

RUN gem update bundler && bundle install