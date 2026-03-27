# One-time push to GitHub

Open Terminal on your Mac and run these commands:

```
cd ~/Documents/Claude/Webdesign/images
git add -A
git commit -m "Initial commit: all brand assets renamed + web-optimized + manifest"
git branch -M main
git remote add origin https://github.com/FlorianPhil/fp-brand-assets.git
git push -u origin main
```

If it asks for authentication, use your GitHub username (FlorianPhil) and a personal access token (not your password). To create a token: GitHub > Settings > Developer settings > Personal access tokens > Generate new token.

After this first push, any future Cowork session can run `git add/commit/push` for you when you add new images.
