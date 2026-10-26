# 🏎️ Turbo Racing

A fast, animated browser racing game built with plain HTML, CSS and JavaScript. No frameworks, no build step, no dependencies.

Dodge traffic, collect coins, use nitro and survive as many levels as you can.

## Features

- **Nitro boost** with flames, speed lines and double distance points
- **Coins and power-ups**: shield and nitro refill
- **Near-miss bonuses** for passing very close to cars
- **4 themes** that change every 400 m: Sunny Meadow, Desert Run, Neon Night, Frozen Pass
- **Smarter traffic**: lane-changing cars with blinkers, slow trucks from level 3
- **Animations**: scrolling road, exhaust smoke, sparks, explosion, screen shake, slow-motion crash
- **Sound effects** (mute with `M`) and a saved best score
- Works on desktop and mobile

## Controls

| Action | Keyboard | Mobile |
| --- | --- | --- |
| Steer | `←` `→` or `A` `D` | On-screen buttons or drag on the road |
| Nitro | `Space`, `W` or `↑` | Nitro button |
| Pause | `P` or `Esc` | Pause button |
| Mute | `M` | Speaker button |

## Project structure

```
.
├── index.html     # the whole game (HTML + CSS + JS)
├── amplify.yml    # AWS Amplify build settings
└── README.md
```

## Run locally

Open `index.html` in any modern browser. Or serve it:

```bash
python3 -m http.server 8080
# then visit http://localhost:8080
```

## Deploy to AWS Amplify

### 1. Push to GitHub

```bash
git init
git add .
git commit -m "Turbo Racing"
git branch -M main
git remote add origin https://github.com/<your-username>/turbo-racing.git
git push -u origin main
```

> The game file must be named `index.html` and sit in the repository root.

### 2. Connect the repo in Amplify

1. Sign in to the [AWS Console](https://console.aws.amazon.com/amplify/) and open **AWS Amplify**.
2. Click **Create new app** (or **Deploy an app**).
3. Choose **GitHub** as the source and click **Next**.
4. Authorize AWS Amplify to access your GitHub account.
5. Select the `turbo-racing` repository and the `main` branch.
6. On the build settings page, Amplify detects `amplify.yml` automatically. Leave it as is.
7. Click **Save and deploy**.

### 3. Open your game

After the build finishes (about a minute), Amplify shows a URL like:

```
https://main.xxxxxxxxxxxx.amplifyapp.com
```

Every `git push` to `main` redeploys the site automatically.

### Optional: custom domain

In Amplify, open your app, go to **Hosting → Custom domains**, click **Add domain** and follow the DNS steps.

## Troubleshooting

- **404 error after deploy:** make sure the file is called `index.html` and is in the repo root, not in a subfolder.
- **No sound at first:** browsers block audio until you click. Press **Start race** and sound will work.
- **Fonts look different offline:** the Bungee and Rubik fonts load from Google Fonts. Without internet the game falls back to system fonts.

## OUTPUT

https://github.com/user-attachments/assets/c254f004-ed98-417a-88d4-649dcbd35247





