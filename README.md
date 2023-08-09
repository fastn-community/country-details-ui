# country-details-ui
The UI for https://github.com/fastn-community/country-details-http

**Live Demo:** [https://country-details-75f6937a875a.herokuapp.com/](https://country-details-75f6937a875a.herokuapp.com/)

## Country Details UI Deployment Guide

This guide provides step-by-step instructions to deploy the "country-details-ui" project, which consists of two packages, "country-details-http" (backend) and "country-details-ui" (UI). The deployment will be on Heroku using the `fastn` buildpack, which requires the `fastn` 2023 edition for building the project.

### Prerequisites

- Heroku CLI installed: Make sure you have the Heroku Command Line Interface (CLI) installed on your system. You can download it from the official Heroku website.
- Heroku Account: You need a Heroku account to deploy your application.
- Fastn 2023 Edition: The Fastn 2023 edition is required for building this project.

### Deployment Steps

1. Clone the Repository:

   ```bash
   git clone https://github.com/fastn-community/country-details-ui.git
   cd country-details-ui
   ```

2. Login to Heroku:

   If you haven't logged in to Heroku yet, open your terminal and run the following command:

   ```bash
   heroku login -i
   ```

   If you have Multi-factor authentication (MFA) enabled on Heroku, you will need to use an Authorization token instead of your password. You can find the token at [https://dashboard.heroku.com/account/applications](https://dashboard.heroku.com/account/applications).

3. Create a Heroku App with Fastn Buildpack:

   Use the following command to create a new Heroku app and configure it to use the Fastn buildpack:

   ```bash
   heroku create <app-name> -b https://github.com/fastn-stack/heroku-buildpack.git
   ```

   Replace `<app-name>` with the desired name for your Heroku app. If you omit the `<app-name>`, Heroku will automatically generate a unique name for your app.

   Note: If the project already exists, you can run this command: ``heroku config:add BUILDPACK_URL=https://github.com/fastn-stack/heroku-buildpack.git``

4. Deploy to Heroku:

   Push the changes to the Heroku app to trigger the build and deployment process:

   ```bash
   git push heroku main
   ```

5. Verify Deployment:

   After the deployment process completes successfully, the site should be live. You can visit the URL of your Heroku app to access the deployed "country-details-ui" package.

   ```bash
   heroku open
   ```

   The URL will be something like `https://<app-name>.herokuapp.com`.

Congratulations! You have successfully deployed the "country-details" UI project to Heroku using the `fastn` buildpack. The `fastn` "country-details-ui" package is now live and accessible through the provided Heroku URL.
