# achi-vanitygen-server

Achi Vanitygen program is designed to help you easily create Achi vanity addresses with a given pattern.
You can use a vanity address program to create a more personalized address. 
For example, you can create an address that starts with **‘ach1stake’** and ask people to send Achi to 
**ach1stakelhnltrea985k9rhv092wzlje4sp6hvc4gza8u0zlnhqac7qakfzw5** or otherwise use it as any generic Achi address. 
The amount of time required to find a given pattern depends on how long the pattern is, the speed of the computer(s) employed to do the calculations and luck. 
On average it takes 8-12 hours to generate vanity address with special 5 symbols after **ach1**, 
the more symbols after **ach1** in the pattern the more time it takes to generate.

Achi Vanitygen Server is designed to help you easily create Achi vanity addresses on multiple PCs. 

## How it works

Achi Vanitygen Server provides tasks and gets reports from Achi Vanitygen clients. 
You can run Achi Vanitygen clients either on one PC or on multiple PCs. 
Achi Vanitygen Server has to be reachable for all running Achi Vanitygen clients.
The connection between server and clients protected by ssl. 

## Usage

``` 
Usage of achi_vanitygen_server:
  -debug
        a debug mode 
  -host string 
        a server host (default "0.0.0.0") 
  -port uint 
        a server port (default 18070)
```

## Quick start

### Step 1 - Download Achi Vanitygen Server
https://github.com/Achi-Coin/achi-vanitygen-server

### Step 2 - Generate SSL certificate (optional)

Run ```generate_cert.sh```

Copy **server.crt** to all clients

### Step 3 - Configure patterns

Add patterns to **prefixes.json**

### Step 4 - Start Server

Run ```achi_vanitygen_server```

### Step 5 - Start Achi Vanitygen clients

Start clients as it is described here https://github.com/Achi-Coin/achi-vanitygen

### Step 6 - Get mnemonics

Open file **addresses.json** after vanity addreses are found.

### Step 7 - Add new wallet with vanity address
 
Use new found mnemonic with ```achi keys add```

Ensure **initial_num_public_keys: 1000** in .achi/mainnet/config/config.yaml
