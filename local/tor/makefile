deploy:
	docker build -t tor -f tor.dockerfile .
	docker run --rm --detach --name tor -p 9050:9050 -p 9051:9051 tor

# if you want to 

# password:
# ssh into docker container
# run tor --hash-password welcome
# put has in torrc
# restart torrc