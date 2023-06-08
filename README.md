




cat <<EOF > my-website/index.html
<!DOCTYPE html>
<html>
<head>
  <title>My AdSense Website</title>
</head>
<body>
  <h1>Welcome to My Website</h1>
  <p>This is a sample website.</p>
</body>
</html>
EOF


cd my-website


git init


git add .


git commit -m "Initial commit"


curl -u "SamRex398" https://api.github.com/user/repos -d '{"MyAds":"https://mywebsite.com/"}'



git remote add origin https://github.com/SamRex398/my-website.git


git push -u origin main


curl -X POST -H "Accept: application/vnd.github.switcheroo-preview+json" -H "Authorization: token YOUR_GITHUB_TOKEN" https://api.github.com/repos/SamRex398/MyAds/pages -d '{"source": {"branch": "main"}}'

