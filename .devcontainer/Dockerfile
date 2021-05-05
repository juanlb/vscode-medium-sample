FROM ruby:2.3.4

RUN apt-get update && apt-get install -y \ 
  build-essential \ 
  nodejs \ 
  wget git curl zsh \
  git-flow

RUN gem install bundler -v 1.17.3

RUN mkdir /app
WORKDIR /app

ARG USERNAME
ARG USER_UID=1000
ARG USER_GID=$USER_UID

# Create the user
RUN groupadd --gid $USER_GID $USERNAME \
    && useradd --uid $USER_UID --gid $USER_GID -m $USERNAME

# Allow install gems
RUN mkdir -p /usr/local/bundle
RUN chown $USERNAME:$USERNAME -R /usr/local/bundle

USER $USERNAME