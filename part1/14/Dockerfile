FROM ruby:2.6.0

RUN apt-get update && apt install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs


RUN apt-get install -y git
RUN git clone https://github.com/docker-hy/rails-example-project.git

WORKDIR /rails-example-project

RUN gem install bundler
RUN bundle install
RUN rails db:migrate

EXPOSE 3000
CMD ["rails","s"]
