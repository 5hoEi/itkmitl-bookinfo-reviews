# Bookinfo Application for Workshop

## How to run with Docker

```bash
# Build Docker Image for review service
docker build -t review .

# Run Ruby
docker run -d --name reviews -p 8082:8082 --link ratings:ratings -e 'RATINGS_SERVICE=http://ratings:8080' -e 'ENABLE_RATINGS=true' reviews

* Test with path `/reviews/1` and `/health`