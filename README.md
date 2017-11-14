# Commerce Stock 8.x installation profile

Enables the Commerce Stock modules.
Based on Commerce's profile.

Use this for Commerce Stock development.

## Start developing on Commerce Stock

You need to clone the commerce_stock repository onGithub via the project page.
Visit https://github.com/BBGuy/commerce_stock/ and click the 'Fork' button.

Next you need to clone your fork so you can start developing.

### Clone the fork:

First remove the commerce_stock folder.
```
cd web/modules/contrib
rm -rf commerce_stock
```
Then clone your fork:
```
git clone git@github.com:your_github_username/commerce_stock.git
```

Now your set to start creating pull requests.

## Create a pull request

For new issues, create a new issue in the commerce_stock issue queue at:
https://www.drupal.org/node/add/project-issue/commerce_stock

Then continue and check out a new branch for your pr.
```
git checkout -b 8.x-1.x-issue-id
```

Now made the changes you want to commit.

Then:
```
git add .
git commit -m "your fix / issue id"
git push
```

Then visit https://github.com/your_github_username/commerce_stock and click on
the new pull request button you should now see.

Once you have created your pr, visit the issue queue and post a comment with the
link to your pull request, so others can review.
https://www.drupal.org/project/issues/search/commerce_stock?version%5B%5D=8.x

## Review an existing pull request:

For this you need to add the remote for the repository at 
https://github.com/BBGuy/commerce_stock

Change into the commerce_stock folder.
```
cd web/modules/contrib/commerce_stock
```

Remove current remote origin.
```
git remote remove origin
```

Add new remote origin.
```
git remote add origin git@github.com:BBGuy/commerce_stock.git
```

Now you can checkout the pr with:
```
git fetch origin pull/ID/head:8.x-1.x-ID
```
Replace 'ID' with the ID of the pull request.

Example:
```
git fetch origin pull/27/head:8.x-1.x-27
```

Now switch to the branch of the pr.
```
git checkout 8.x-1.x-ID
```
Replace 'ID' with the ID of the pull request.

Example:
```
git checkout 8.x-1.x-27
```
