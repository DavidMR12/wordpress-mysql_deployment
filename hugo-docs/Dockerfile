FROM klakegg/hugo:latest
COPY . /src
WORKDIR /src
RUN hugo
CMD ["hugo", "server", "--bind=0.0.0.0"]
