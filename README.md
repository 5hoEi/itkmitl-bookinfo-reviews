# Bookinfo Application for Workshop

## How to run with Docker

```bash
# Build Docker Image for review service
docker build -t review .

# Run Ruby
docker run -d --name review -p 8082:9080 review

* Test with path `/reviews/1` and `/health`