# TON Connect Wallets

TON Connect Wallets is a simple, customizable web app that allows users to connect with a variety of TON-based wallets. It dynamically loads a list of supported wallets from an external JSON file and provides a button for each wallet that enables users to connect to their wallet seamlessly.

## Purpose

While searching for a convenient way to connect TON-based wallets to web applications, I couldn't find a simple and flexible solution. Therefore, I decided to create this tool, which provides an easy way to display a list of supported wallets and connect to them through a simple interface.

## Features

- Displays a list of supported wallets.
- Allows users to connect their wallet by clicking a button.
- Dynamically loads wallet information from a JSON file.
- Uses `TonConnectSDK` for seamless wallet connection.
- Open source and customizable for different projects.

## How to Use

1. **Clone the Repository**

   First, clone the repository to your local machine:

   ```bash
   git clone https://github.com/yourusername/ton-connect-wallets.git
   cd ton-connect-wallets

2. **Customize Wallet List
You can modify the wallet list URL in the script to point to your own JSON file containing wallet information. The current example pulls the wallet list from:
```javascript
fetch('https://raw.githubusercontent.com/mrshll0015/wallets-list/main/wallets-v2.json')
```

3. **Configure Manifest URL
Replace the manifestUrl in the TonConnect initialization with the correct URL to your manifest JSON.

```javascript
const connector = new TonConnect({
  manifestUrl: "https://raw.githubusercontent.com/mrshll0015/main/manifest.json"
});
```

