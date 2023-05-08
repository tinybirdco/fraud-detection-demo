<p>
  <a href="https://www.tinybird.co/join-our-slack-community"><img alt="Slack Status" src="https://img.shields.io/badge/slack-chat-1FCC83?style=flat&logo=slack"></a>
</p>

# Tinybird Real-Time Fraud Detection Starter Kit

Example application for real-time fraud detection using Tinybird.

## Setup

1. Setup your Tinybird account

Click this button to deploy the data project to Tinybird 👇

[![Deploy to Tinybird](https://cdn.tinybird.co/button)](https://ui.tinybird.co/workspaces/new?name=fraud_detection_demo)

Follow the guided process, and your Tinybird workspace is now ready to start receiving events.

2. Setup this repository locally

```bash
git clone https://github.com/tinybirdco/fraud-detection-demo.git
cd fraud-detection-demo
```

3. Install dependencies

```bash
npm install
```

4. Install and configure the Tinybird CLI

To start working with data projects as if they were software projects, First, install the Tinybird CLI in a virtual environment.
You'll need python3 installed.

Check the [Tinybird CLI documentation](https://docs.tinybird.co/cli.html) for other installation options and troubleshooting tips.

```bash
python3 -mvenv .e
. .e/bin/activate
pip install tinybird-cli
tb auth --interactive
```

Choose your region: 1 for `us-east`, 2 for `eu`. A new `.tinyb` file will be created.

Go to [https://ui.tinybird.co/tokens](https://ui.tinybird.co/tokens) and copy the token with admin rights.

⚠️Warning! The Admin token, the one you copied following this guide, is your admin token. Don't share it or publish it in your application. You can manage your tokens via API or using the Auth Tokens section in the UI. More detailed info at [Auth Tokens management](https://www.tinybird.co/docs/api-reference/token-api.html)

Once you have successfully authenticated with Tinybird, you can run the following to upload the pipes to your Tinybird workspace.

```bash
tb push --no-check
```

5. Start sending data to Tinybird with Mockingbird. Check the [Mockingbird CLI documentation](https://mockingbird.tinybird.co/docs) for other installation, options and troubleshooting. Note, that you will need to paste in your Tinybird token.

```bash
mockingbird-cli tinybird --datasource=transactions --token=[PASTE_YOUR_TOKEN_FROM_TINYBIRD] --endpoint=eu_gcp --schema='schema.json' --eps 100
```

6. Go to your [Tinybird workspace](https://ui.tinybird.co) and check the data is flowing.

## Authors

- [Joe Karlsson](https://github.com/joekarlsson)

---

Need help?: [Community Slack](https://www.tinybird.co/join-our-slack-community) &bull; [Tinybird Docs](https://docs.tinybird.co/) &bull; [Email](mailto:kike@tinybird.co)
