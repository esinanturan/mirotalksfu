<h1 align="center">MiroTalk SFU</h1>

<br />

<div align="center">

<a href="https://www.linkedin.com/in/miroslav-pejic-976a07101/">![Author](https://img.shields.io/badge/Author-Miroslav_Pejic-brightgreen.svg)</a>
<a href="https://choosealicense.com/licenses/agpl-3.0/">![License: AGPLv3](https://img.shields.io/badge/License-AGPLv3_Open_Surce-blue.svg)</a>
<a href="https://codecanyon.net/item/mirotalk-sfu-webrtc-realtime-video-conferences/40769970">![License: Regular](https://img.shields.io/badge/License-Regular_Private_Use-lightblue.svg)</a>
<a href="https://codecanyon.net/item/mirotalk-sfu-webrtc-realtime-video-conferences/40769970">![License: Extended](https://img.shields.io/badge/License-Extended_Commercial_Use-darkgreen.svg)</a>
<a href="https://discord.gg/rgGYfeYW3N">![Community](https://img.shields.io/badge/Community-forum-pink.svg)</a>

</div>

<p align="center"><strong>MiroTalk SFU</strong> stands for <strong>Selective Forwarding Unit</strong>, built on <a href="https://mediasoup.org" target="_blank">Mediasoup</a>, a powerful media server that routes video/audio streams between participants. It offers a rich set of features for WebRTC meetings, webinars, and more. Simple, Secure, Scalable Real-Time Video Conferences with support for up to 8K resolution and 60fps. It's compatible with all major browsers and platforms.</p>

<hr />

<p align="center">
    <strong><a href="https://sfu.mirotalk.com/">Explore MiroTalk SFU</a></strong>
</p>

<hr />

<p align="center">
    <a href="https://sfu.mirotalk.com/">
        <img src="public/images/mirotalksfu-header.gif">
    </a>
</p>

<hr />

<strong>
    <p align="center">
        Join our Community for questions, help, support, ideas, and discussions on <strong><a href='https://discord.gg/rgGYfeYW3N'>Discord</a></strong>
    </p>
</strong>

<hr />

<details>
<summary>Features</summary>

<br/>

- Is `100% Free` - `Open Source (AGPLv3)` - `Self Hosted` and [PWA](https://en.wikipedia.org/wiki/Progressive_web_application)!
- Unlimited conference rooms with no time limitations.
- Live broadcasting streaming.
- Translated into 133 languages.
- Support for the OpenID Connect (OIDC) authentication layer.
- Host protection to prevent unauthorized access.
- User auth to prevent unauthorized access.
- JWT.io securely manages credentials for host configurations and user authentication, enhancing security and streamlining processes.
- Room password protection.
- Room lobby, central gathering space.
- Room spam mitigations, focused on preventing spam.
- Geolocation, identification or estimation of the real-world geographic location of the participants.
- Compatible with desktop and mobile devices.
- Optimized mobile room URL sharing.
- Webcam streaming with front and rear camera support for mobile devices.
- Virtual Background and Blur Support: Upload from file, URL, or drag & drop!
- Broadcasting, distribution of audio or video content to a wide audience.
- Crystal-clear audio streaming with speaking detection and volume indicators.
- Screen sharing for presentations.
- File sharing with drag-and-drop support.
- Choose your audio input, output, and video source.
- Supports video quality up to 4K.
- Supports advance Video/Document Picture-in-Picture (PiP) offering a more streamlined and flexible viewing experience.
- Record your screen, audio, and video locally, on your server, or in an S3 bucket for easy access and management!
- Snapshot video frames and save them as PNG images.
- Chat with an Emoji Picker for expressing feelings, private messages, Markdown support, and conversation saving.
- ChatGPT (powered by OpenAI) for answering questions, providing information, and connecting users to relevant resources.
- VideoAI enables users to customize AI avatars to deliver messages, perform tasks, or act out scripts.
- Speech recognition, execute the app features simply with your voice.
- Push-to-talk functionality, similar to a walkie-talkie.
- Advanced collaborative whiteboard for teachers.
- Advanced collaborative powerful rich text editor.
- Real-time sharing of YouTube embed videos, video files (MP4, WebM, OGG), and audio files (MP3).
- Real-time polls, allows users to create and participate in live polls, providing instant feedback and results.
- Meeting Duration (HH:MM:SS): Set the meeting time in hours, minutes, and seconds for precise duration control.
- Integrated RTMP server, fully compatible with **[OBS](https://obsproject.com)**.
- Supports RTMP streaming from files, URLs, webcams, screens, and windows.
- Full-screen mode with one-click video element zooming and pin/unpin.
- Customizable UI themes.
- Right-click options on video elements for additional controls.
- Supports [REST API](app/api/README.md) (Application Programming Interface).
- Integration with [Slack](https://api.slack.com/apps/) for enhanced communication.
- Integration with [Discord](https://discord.com) for enhanced communication.
- Integration with [Mattermost](https://mattermost.com/) for enhanced communication.
- Utilizes [Sentry](https://sentry.io/) for error reporting.
- And much more...

</details>

<details>
<summary>About</summary>

<br>

- [Presentation](https://www.canva.com/design/DAE693uLOIU/view)
- [Video Overview](https://www.youtube.com/watch?v=_IVn2aINYww)

</details>

<details>
<summary>Direct Join</summary>

<br/>

- You can `directly join a room` by using link like:
- https://sfu.mirotalk.com/join?room=test&roomPassword=0&name=mirotalksfu&avatar=0&audio=0&video=0&screen=0&notify=0&duration=unlimited

    | Params       | Type           | Description               |
    | ------------ | -------------- | ------------------------- |
    | room         | string         | Room Id                   |
    | roomPassword | string/boolean | Room password             |
    | name         | string         | User name                 |
    | avatar       | string/boolean | User avatar               |
    | audio        | boolean        | Audio stream              |
    | video        | boolean        | Video stream              |
    | screen       | boolean        | Screen stream             |
    | notify       | boolean        | Welcome message           |
    | hide         | boolean        | Hide myself               |
    | duration     | string         | Meeting duration HH:MM:SS |
    | token        | string         | JWT                       |

</details>

<details>
<summary>Host Protection Configuration</summary>

<br/>

When [host.protected](https://docs.mirotalk.com/mirotalk-sfu/host-protection/) or `host.user_auth` is enabled, the host/users can provide a valid token for direct joining the room as specified in the `app/src/config.js` file.

| Params           | Value                                                                            | Description                                                                            |
| ---------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `host.protected` | `true` if protection is enabled, `false` if not (default false)                  | Requires the host to provide a valid username and password during room initialization. |
| `host.user_auth` | `true` if user authentication is required, `false` if not (default false).       | Determines whether host authentication is required.                                    |
| `host.users`     | JSON array with user objects: `{"username": "username", "password": "password"}` | List of valid host users with their credentials.                                       |

Example:

```js
    host: {
        protected: true,
        user_auth: true,
        users: [
            {
                username: 'username',
                password: 'password',
                displayname: 'displayname',
                allowed_rooms: ['*'],
            },
            {
                username: 'username2',
                password: 'password2',
                displayname: 'displayname2',
                allowed_rooms: ['room1', 'room2'],
            },
            //...
        ],
    },
```

</details>

<details open>
<summary>Quick Start</summary>

<br/>

- Before running MiroTalk SFU, ensure you have `Node.js` and all [requirements](https://mediasoup.org/documentation/v3/mediasoup/installation/#requirements) installed. This project has been tested with Node version [18.X](https://nodejs.org/en/download).

- Requirements install example for `Ubuntu 24.04 LTS`

```bash
# Gcc g++ make
$ apt-get update
$ apt-get install -y build-essential
# Python 3.8 and pip
$ DEBIAN_FRONTEND=noninteractive apt-get install -y tzdata
$ apt install -y software-properties-common
$ add-apt-repository -y ppa:deadsnakes/ppa
$ apt update
$ apt install -y python3.8 python3-pip
# FFmpeg
$ apt install -y ffmpeg
```

---

![nodejs](public/images/nodejs.png)

Install `NodeJS 18.X` and `npm` using [Node Version Manager](https://docs.mirotalk.com/nvm/nvm/)

---

- Start the server

```bash
# Clone this repo
$ git clone https://github.com/miroslavpejic85/mirotalksfu.git
# Go to to dir mirotalksfu
$ cd mirotalksfu
# Copy app/src/config.template.js in app/src/config.js and edit it if needed
$ cp app/src/config.template.js app/src/config.js
# Copy .env.template to .env and edit it if needed
$ cp .env.template .env
# Install dependencies - be patient, the first time will take a few minutes, in the meantime have a good coffee ;)
$ npm install
# Start the server
$ npm start
# If you want to start the server on a different port than the default use an env var
$ SERVER_LISTEN_PORT=3011 npm start
```

- Open [https://localhost:3010](https://localhost:3010) or `:3011` if the default port has been changed in your browser.

<br/>

> \[!NOTE]
>
> To run `MiroTalk SFU` on a `Windows operating system`, you can follow the instructions provided in [this documentation](https://github.com/miroslavpejic85/mirotalksfu/issues/99#issuecomment-1586073853).

</details>

<details open>
<summary>Docker</summary>

<br/>

![docker](public/images/docker.png)

- Repository [docker hub](https://hub.docker.com/r/mirotalk/sfu)
- Install [docker engine](https://docs.docker.com/engine/install/) and [docker compose](https://docs.docker.com/compose/install/)

```bash
# Clone this repo
$ git clone https://github.com/miroslavpejic85/mirotalksfu.git
# Go to to dir mirotalksfu
$ cd mirotalksfu
# Copy app/src/config.template.js in app/src/config.js IMPORTANT (edit it according to your needs)
$ cp app/src/config.template.js app/src/config.js
# Copy .env.template to .env and edit it if needed
$ cp .env.template .env
# Copy docker-compose.template.yml in docker-compose.yml and edit it if needed
$ cp docker-compose.template.yml docker-compose.yml
# (Optional) Get official image from Docker Hub
$ docker-compose pull
# Create and start containers
$ docker-compose up # -d
# To stop and remove resources
$ docker-compose down
```

- Open [https://localhost:3010](https://localhost:3010) in your browser.

</details>

<details open>
<summary>Embed a meeting</summary>

<br/>

![iframe](public/images/iframe.png)

To embed a meeting within `your service or app` using an iframe, you can use the following code:

```html
<iframe
    allow="camera; microphone; display-capture; fullscreen; clipboard-read; clipboard-write; web-share; autoplay"
    src="https://sfu.mirotalk.com/newroom"
    style="height: 100vh; width: 100vw; border: 0px;"
></iframe>
```

</details>

<details>
<summary>Documentations</summary>

<br>

- `Ngrok/HTTPS:` You can start a video conference directly from your local PC and make it accessible from any device outside your network by following [these instructions](docs/ngrok.md), or expose it directly on [HTTPS](app/ssl/README.md).

- `Self-hosting:` For `self-hosting MiroTalk SFU` on your own dedicated server, please refer to [this comprehensive guide](docs/self-hosting.md). It will provide you with all the necessary instructions to get your MiroTalk SFU instance up and running smoothly.

- `Rest API:` The [API documentation](https://docs.mirotalk.com/mirotalk-sfu/api/) uses [swagger](https://swagger.io/) at https://localhost:3010/api/v1/docs or check it on live [here](https://sfu.mirotalk.com/api/v1/docs).

### 1. Get Server Statistics

```bash
curl -X GET "http://localhost:3010/api/v1/stats" \
     -H "authorization: mirotalksfu_default_secret" \
     -H "Content-Type: application/json"

curl -X GET "https://sfu.mirotalk.com/api/v1/stats" \
     -H "authorization: mirotalksfu_default_secret" \
     -H "Content-Type: application/json"
```

### 2. Get Active Meetings

```bash
curl -X GET "http://localhost:3010/api/v1/meetings" \
     -H "authorization: mirotalksfu_default_secret" \
     -H "Content-Type: application/json"

curl -X GET "https://sfu.mirotalk.com/api/v1/meetings" \
     -H "authorization: mirotalksfu_default_secret" \
     -H "Content-Type: application/json"
```

### 3. Create Meeting

```bash
curl -X POST "http://localhost:3010/api/v1/meeting" \
     -H "authorization: mirotalksfu_default_secret" \
     -H "Content-Type: application/json"

curl -X POST "https://sfu.mirotalk.com/api/v1/meeting" \
     -H "authorization: mirotalksfu_default_secret" \
     -H "Content-Type: application/json"
```

### 4. Join Meeting (Basic)

```bash
curl -X POST "http://localhost:3010/api/v1/join" \
     -H "authorization: mirotalksfu_default_secret" \
     -H "Content-Type: application/json" \
     --data '{"room":"test","roomPassword":false,"avatar":false,"name":"mirotalksfu","audio":false,"video":false,"screen":false,"notify":false,"duration":"unlimited"}'

curl -X POST "https://sfu.mirotalk.com/api/v1/join" \
     -H "authorization: mirotalksfu_default_secret" \
     -H "Content-Type: application/json" \
     --data '{"room":"test","roomPassword":false,"name":"mirotalksfu","avatar":false,"audio":false,"video":false,"screen":false,"notify":false,"duration":"unlimited"}'
```

### 5. Join Meeting with Token

```bash
curl -X POST "http://localhost:3010/api/v1/join" \
     -H "authorization: mirotalksfu_default_secret" \
     -H "Content-Type: application/json" \
     --data '{"room":"test","roomPassword":false,"name":"mirotalksfu","audio":false,"video":false,"screen":false,"notify":false,"duration":"unlimited","token":{"username":"username","password":"password","presenter":true,"expire":"1h"}}'

curl -X POST "https://sfu.mirotalk.com/api/v1/join" \
     -H "authorization: mirotalksfu_default_secret" \
     -H "Content-Type: application/json" \
     --data '{"room":"test","roomPassword":false,"name":"mirotalksfu","audio":false,"video":false,"screen":false,"notify":false,"duration":"unlimited","token":{"username":"username","password":"password","presenter":true,"expire":"1h"}}'
```

### 6. Generate Token

```bash
curl -X POST "http://localhost:3010/api/v1/token" \
     -H "authorization: mirotalksfu_default_secret" \
     -H "Content-Type: application/json" \
     --data '{"username":"username","password":"password","presenter":true,"expire":"1h"}'

curl -X POST "https://sfu.mirotalk.com/api/v1/token" \
     -H "authorization: mirotalksfu_default_secret" \
     -H "Content-Type: application/json" \
     --data '{"username":"username","password":"password","presenter":true,"expire":"1h"}'
```

</details>

<details open>
<summary>Hetzner, Hostinger & Contabo</summary>

<br/>

[![Hetzner](public/sponsors/Hetzner.png)](https://hetzner.cloud/?ref=XdRifCzCK3bn)

This application is running for `demonstration purposes` on [Hetzner](https://www.hetzner.com/), one of `the best` [cloud providers](https://www.hetzner.com/cloud) and [dedicated root servers](https://www.hetzner.com/dedicated-rootserver).

---

Use [my personal link](https://hetzner.cloud/?ref=XdRifCzCK3bn) to receive `€⁠20 IN CLOUD CREDITS`.

---

[![Hostinger](public/advertisers/HostingerLogo.png)](https://hostinger.com/?REFERRALCODE=MIROTALK)

Fast, reliable hosting with 24/7 support and great performance. Start today! [Check out Hostinger now](https://hostinger.com/?REFERRALCODE=MIROTALK)

---

[![Contabo](public/advertisers/ContaboLogo.png)](https://www.dpbolvw.net/click-101027391-14462707)

Experience also top-tier German web hosting – dedicated servers, VPS, and web hosting at `unbeatable prices`. [Explore now here](https://www.dpbolvw.net/click-101027391-14462707)

---

To set up your own instance of `MiroTalk SFU` on a dedicated cloud server, please refer to our comprehensive [self-hosting documentation](https://docs.mirotalk.com/mirotalk-sfu/self-hosting/). This guide will walk you through the process step by step, ensuring a smooth and successful deployment.

</details>

<details>
<summary>Live Demo</summary>

<br/>

<a target="_blank" href="https://hetzner.cloud/?ref=XdRifCzCK3bn"><img src="public/sponsors/Hetzner.png" style="width: 220px;"></a>

https://sfu.mirotalk.com

[![mirotalksfu-qr](public/images/mirotalksfu-qr.png)](https://sfu.mirotalk.com/)

</details>

<details>
<summary>Credits</summary>

<br/>

- [Davide Pacilio](https://cruip.com/demos/solid/) (html template)
- [Dirk Vanbeveren](https://github.com/Dirvann) (sfu logic)
- [Mediasoup](https://mediasoup.org) (sfu server)

</details>

<details>
<summary>Contributing</summary>

<br/>

- Contributions are welcome and greatly appreciated!
- Just run before `npm run lint`

</details>

<details>
<summary>License</summary>

<br/>

[![AGPLv3](public/images/AGPLv3.png)](LICENSE)

MiroTalk SFU is free and open-source under the terms of AGPLv3 (GNU Affero General Public License v3.0). Please `respect the license conditions`, In particular `modifications need to be free as well and made available to the public`. Get a quick overview of the license at [Choose an open source license](https://choosealicense.com/licenses/agpl-3.0/).

To obtain a [MiroTalk SFU license](https://docs.mirotalk.com/license/licensing-options/) with terms different from the AGPLv3, you can conveniently make your [purchase on CodeCanyon](https://codecanyon.net/item/mirotalk-sfu-webrtc-realtime-video-conferences/40769970). This allows you to tailor the licensing conditions to better suit your specific requirements.

</details>

<details open>
<summary>Support the project</summary>

<br/>

Do you find MiroTalk SFU indispensable for your needs? Join us in supporting this transformative project by [becoming a backer or sponsor](https://github.com/sponsors/miroslavpejic85). By doing so, not only will your logo prominently feature here, but you'll also drive the growth and sustainability of MiroTalk SFU. Your support is vital in ensuring that this valuable platform continues to thrive and remain accessible for all. Make an impact – back MiroTalk SFU today and be part of this exciting journey!

|                                                                                                                           |                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| [![BroadcastX](public/sponsors/BroadcastX.png)](https://broadcastx.de/)                                                   | [![Hetzner](public/sponsors/HetznerLogo.png)](https://hetzner.cloud/?ref=XdRifCzCK3bn) |
| [![LuvLounge](public/sponsors/LuvLounge.png)](https://luvlounge.ca)                                                       | [![QuestionPro](public/sponsors/QuestionPro.png)](https://www.questionpro.com)         |
| [![BrowserStack](public/sponsors/BrowserStack.png)](https://www.browserstack.com)                                         | [![CrystalSound](public/sponsors/CrystalSound.png)](https://crystalsound.ai)           |
| [![Cloudron](public/sponsors/Cloudron.png)](https://cloudron.io)                                                          | [![Kiquix](public/sponsors/KiquixLogo.png)](https://kiquix.com)                        |
| [![LambdaTest](public/sponsors/LambdaTest.png)](https://lambdatest.com/pricing?coupon=QURFODlQUk9NT1RFUg==&refid=1149848) |                                                                                        |

</details>

<details open>
<summary>Advertisers</summary>

---

|                                                                                                |                                                                                                |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| [![Hostinger](public/advertisers/Hostinger.png)](https://hostinger.com/?REFERRALCODE=MIROTALK) | [![Contabo](public/advertisers/Contabo.png)](https://www.dpbolvw.net/click-101027391-14462707) |

---

</details>

## Diving into Additional MiroTalk Projects:

<details>
<summary>MiroTalk P2P</summary>

<br/>

Try also [MiroTalk P2P](https://github.com/miroslavpejic85/mirotalk) `peer to peer` real-time video conferences, optimized for small groups. `Unlimited time, unlimited concurrent rooms` each having 5-8 participants.

</details>

<details>
<summary>MiroTalk C2C</summary>

<br>

Try also [MiroTalk C2C](https://github.com/miroslavpejic85/mirotalkc2c) `peer to peer` real-time video conferences, optimized for cam 2 cam. `Unlimited time, unlimited concurrent rooms` each having 2 participants.

</details>

<details>
<summary>MiroTalk BRO</summary>

<br>

Try also [MiroTalk BRO](https://github.com/miroslavpejic85/mirotalkbro) `Live broadcast` (peer to peer) live video, audio and screen stream to all connected users (viewers). `Unlimited time, unlimited concurrent rooms` each having a broadcast and many viewers.

</details>

<details>
<summary>MiroTalk WEB</summary>

<br>

Try also [MiroTalk WEB](https://github.com/miroslavpejic85/mirotalkwebrtc) a platform that allows for the management of an `unlimited number of users`. Each user must register with their email, username, and password, after which they gain access to their `personal dashboard`. Within the dashboard, users can `manage their rooms and schedule meetings` using the desired version of MiroTalk on a specified date and time. Invitations to these meetings can be sent via email, shared through the web browser, or sent via SMS.

</details>

---

This project is tested with [BrowserStack](https://www.browserstack.com).

---
