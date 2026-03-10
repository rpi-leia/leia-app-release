# leia-app-release
Public release executables for leia-app.

## Installation Instructions

1. If you don't already have an account with both github.com and bitbucket.org, create one on each. Each account will need to have the correct permissions, contact Jesse to get those setup.
2. Go to https://github.com/rpi-leia/leia-app-release/releases, select the latest release, and download the archived file for your platform.
3. Extract the executable from the downloaded archive, and put it somewhere convenient (e.g. Desktop).
4. Run the app.
    1. On OSX, if the app doesn't run and produces an error like "app is damaged and can't be opened", open your Terminal and run the following: `xattr -d com.apple.quarantine /path/to/LEIA.app` (be sure to adjust the path to where you put the app, e.g. `~/Desktop/LEIA.app`. The app should now run without an error.
5. Create your authorization tokens - one for github and one for bitbucket.
    1. Github:
        1. Navigate to https://github.com/settings/personal-access-tokens
        2. Choose to generate a new token
        3. Name it `leia-app-access`
        4. Select an expiration date, or no expiration
        5. Select "All Repositories"
        6. Add "Contents" from the dropdown
        7. Generate the token
        8. Copy the generated value into the LEIA.app settings screen, and include your github username - test the connection to verify it works.
    2. Bitbucket
        1. Navigate to id.atlassian.com/manage-profile/security/api-tokens
        2. Choose to create a new API token with scopes
        3. Name it `leia-app-access`
        4. Choose an expirate date (up to 1 year)
        5. Select "bitbucket" as the app
        6. Narrow the list of scopes to "Read" and then choose the following:
            1. `read:package:bitbucket`
            2. `read:project:bitbucket`
            3. `read:repository:bitbucket`
            4. `read:user:bitbucket`
            5. `read:workspace:bitbucket`
        7. Generate the API token
        8. Copy the generated value into the LEIA.app settings screen, and include your bitbucket email  - test the connection to verify it works.
6. Enter a username for your local DEKADE (there are no name conflicts, anything is fine).
7. Save your settings. The LEIA.app will now begin to install the system, it may take a few minutes and appear to hang at certain steps (particularly the Syntax Service and NLP models).
8. After the installation is complete, the launcher screen will appear. Whenever you open the LEIA.app again, it should go directly here.
9. Click on the DEKADE card to launch DEKADE in your preferred browser.
