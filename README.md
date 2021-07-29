# docker Colab local Github action backend (unstable)

## How to run

- 1. Fork this repo or 
  Download this repo and upload it to Github
- 2. Setup secret repo environment variable as name `NGROK_AUTH_TOKEN_DEC` 
  For this go to Settings>Secrets>New repository secret and Name box paste `NGROK_AUTH_TOKEN_DEC` and get Ngrok token from https://dashboard.ngrok.com/get-started/your-authtoken and copy-paste token to Value box and Add secret.
- 3. Now run workflow action for this goto Actions> select Workflows as Colab backend > Run workflow 
- 4. Wait 2-3 minutes then goto to https://dashboard.ngrok.com/endpoints/status. You will see two links like `http://7be55b53bbad.ap.ngrok.io/`. Add with link `home/runner/content/services.html` or browse `home>runner>content>services.html`
- 5. Now you see three services WETTY, GHFS, COLAB. Copy Colab commend after `->` this. 
	Ex: `cloudflared access tcp --hostname https://watches-cause-towards-ref.trycloudflare.com --url localhost:8081`
- 6. Download Cloudflared binary depend on your os type from https://github.com/cloudflare/cloudflared/releases and rename just Cloudflared
- 7. On same path open terminal and run `cloudflared access tcp --hostname https://xxxxxxx.trycloudflare.com --url localhost:8081` __(Note xxxxxxx is your unique word)__
- 8. Now open any Coalb notebook and select "connect to a local runtime" `http://localhost:8081/` and connect __(Note that it is not require any token)__

