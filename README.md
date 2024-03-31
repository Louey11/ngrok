# Ngrok 

a globally distributed reverse proxy that secures, protects and accelerates your applications and network services, no matter where you run them.

## Sign up to ngrok and grab your static domain

[Sign up](https://dashboard.ngrok.com/signup) to ngrok and grab your auth token , store it for later use.

Grab your [static domain](https://dashboard.ngrok.com/cloud-edge/domains)



## Installation

Install ngrok via Apt with the following command:
```bash
curl -s https://ngrok-agent.s3.amazonaws.com/ngrok.asc \
  | sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null && echo "deb https://ngrok-agent.s3.amazonaws.com buster main" \
  | sudo tee /etc/apt/sources.list.d/ngrok.list && sudo apt update && sudo apt install ngrok
```
add your authtoken 

```bash
ngrok config add-authtoken <your-authtoken>
```

## Usage

Put your app online , if it is listening on port 8080, run:
```
ngrok http --domain=<your-static-domain> 8080
```
then grab your url it should be something like this 
```
Forwarding   https://<your-static-domain> http://localhost:8080
```
enjoy !

