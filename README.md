# Home Lab Stack

This is my pretty basic setup for a small homelab built with some parts I have laying around.

So far it is mainly to reduce my dependency on Spotify and play around with some opensource AI models.
Currently I am using Syntetic.new for a subscription to opensource models.
They have a privacy policy that is GDPR compliant (as of this writing in 2026-03).

## Things that could be fun to add:

1. AI poisoning service for images. I have some artist friends who would appreciate something like this.
1. recommendations that build playlists for me based on my listening habits.
1. Some webscraping stuff for my own data intensive projects.


## Requirements

1. Grafana Cloud Account:
    - Using a grafana cloud account to test out the free tier for metrics.
    - Once you set something up you should be able to get your hands of a set of environment variables `GCLOUD_...`. These need to go in
        `./config/alloy/.env`

1. SoulSeek Account:
    - Need a soulseek account and to provide user / password for slskd ui. Needs to go in `config/slskd/.env`
    ```
    ## SOULSEEK API
    SLSKD_SLSK_USERNAME=...
    SLSKD_SLSK_PASSWORD=...

    ## Web UI user:pass
    SLSKD_USERNAME=...
    SLSKD_PASSWORD=...
    ```
3. Open Web UI:
    - Using Synthetic.new currently.
    - Need api key at `config/open-webui/.env`
    ```
    SYNTHETIC_NEW_API_KEY="..."
    ```

4. Gluetun:
    - Need ProtonVPN wireguard config at `config/gluetun/.env`
    ```
    WIREGUARD_PRIVATE_KEY="..."
    WIREGUARD_ADDRESSED="..."
    ```

5. Searxng:
    - Create a secret key and throw it in an environment at `config/searxng/.env`
    ```
    SEARXNG_SECRET="..."
    ```

6. Need to run `tailscale cert` to get certfiles

## TODO
