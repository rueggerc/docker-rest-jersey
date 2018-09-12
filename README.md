Project to learn/demonstration RESTful using Jersey

# Build Image
docker image build -t docker-rest-jersey:1.0 .

# Run Detached
docker container run -d --name rest1 -p 8080:8080 rest-jersey:1.0
