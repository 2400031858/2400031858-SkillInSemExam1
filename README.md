# 2400031858-SkillInSemExam1
# Step 1: Initialize a Git repository
git init

# Step 2: Create and commit the base file
echo "<!DOCTYPE html>
<html>
<head>
    <title>Git Merge Conflict Example</title>
</head>
<body>
    <h2>Hello from Main Branch</h2>
</body>
</html>" > App.js

git add App.js
git commit -m "Initial commit with App.js"

# Step 3: Create two new branches
git branch feature1
git branch feature2

# Step 4: Switch to feature1 and make changes (Alice)
git checkout feature1
echo "<!DOCTYPE html>
<html>
<head>
    <title>Git Merge Conflict Example</title>
</head>
<body>
    <h2>Hello from Feature 1 - Alice</h2>
</body>
</html>" > App.js

git add App.js
git commit -m "Modified by Alice in feature1"

# Step 5: Switch to feature2 and make conflicting changes (Bob)
git checkout feature2
echo "<!DOCTYPE html>
<html>
<head>
    <title>Git Merge Conflict Example</title>
</head>
<body>
    <h2>Hello from Feature 2 - Bob</h2>
</body>
</html>" > App.js

git add App.js
git commit -m "Modified by Bob in feature2"

# Step 6: Merge both branches into main
git checkout main
git merge feature1
git merge feature2
