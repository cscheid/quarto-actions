---
title: "Quarto Actions: Basics"
---

The simplest workflow using Quarto Actions uses the `setup` and `publish` actions. We will use Netlify in this example. Here are the steps to follow:

1. **Create Netlify auth token**

   Go to Netlify's [applications page](https://app.netlify.com/user/applications), and click on "New Access Token" to create a new personal access token. Give this token a memorable name, and note the resulting string (or keep this browser window open).

2. **Add Netlify auth token to your GitHub repository**

   Go to the GitHub webpage for the repository that will be using this GitHub Action. Click on "Settings". On the new page, click on "Secrets", then on the dropdown "Actions". Now, on the right-hand tab, click on the "New repository secret" button to the right of the title "Actions secrets". For the "Name" field, use `NETLIFY_AUTH_TOKEN`, and for the "Value" field, paste the string you got from step 1.

3. **Add the GitHub Actions workflow to your project**

   Copy [quarto-publish-example.yml](quarto-publish-example.yml) to `.github/workflows/quarto-publish.yml`. This file assumes 

4. **Add `_publish.yml` to your repository**

   Quarto stores publishing metadata information in `_publish.yml`. To create this file, run `quarto publish netlify` locally once (TODO: how does this work in an IDE?).


Finally, commit the files you have just created and push the result to GitHub. This should trigger a new action from GitHub that will automatically render and publish your website through Netlify.
