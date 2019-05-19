## To Build Container
`docker build -t the-app .`

## To Run Container
`docker run -p 8080:8080 the-app`

## Stop and Remove container associated with image named 'the-app'
`docker rm $(docker stop $(docker ps -a -q --filter ancestor=the-app --format="{{.ID}}"))`
