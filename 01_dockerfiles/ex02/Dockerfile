FROM ruby

RUN apt-get update -y && \
    apt-get install -y nodejs && \
    gem install rails && \
    mkdir -p /opt/app

ONBUILD WORKDIR /opt/app

ONBUILD COPY . /opt/app

ONBUILD EXPOSE 3000

ONBUILD RUN bundle install && \
	rake db:migrate && \
	rake db:seed
