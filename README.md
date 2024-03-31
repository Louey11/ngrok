# Ngrok: Globally Distributed Reverse Proxy

Demo a website running on your local machine to a client or stakeholder without deploying to a staging site.

## Getting Started

To begin using Ngrok, follow these simple steps:

1. **Sign Up**:

   [Sign up](https://dashboard.ngrok.com/signup) for Ngrok to obtain your authentication token. Ensure you store it securely for future use.

2. **Grab Your Static Domain**:
   
    Claim your unique [static domain](https://dashboard.ngrok.com/cloud-edge/domains) from Ngrok.

## Easy way if you have docker
Put your app online , assuming it's listening on port 8080
```bash
docker run -it -e NGROK_AUTHTOKEN=<your-authtoken> ngrok/ngrok:latest http --domain=<your-static-domain> 8080
```


## Installation

Install Ngrok via Apt using the following command:

```bash
curl -s https://ngrok-agent.s3.amazonaws.com/ngrok.asc \
  | sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null && echo "deb https://ngrok-agent.s3.amazonaws.com buster main" \
  | sudo tee /etc/apt/sources.list.d/ngrok.list && sudo apt update && sudo apt install ngrok
```
Once installed, add your authentication token: 

```bash
ngrok config add-authtoken <your-authtoken>
```

## Usage

To put your application online, assuming it's listening on port 8080, execute the following command:
```
ngrok http --domain=<your-static-domain> 8080
```
You'll receive a URL similar to this: 
```
Forwarding   https://<your-static-domain> http://localhost:8080
```
Enjoy the benefits of Ngrok

