Base code was taken from https://github.com/ashutosh1919/masterPortfolio on 4/23/2021.

#Branch Deployed:
Master Branch is currently deploted at mriceflame.co
#make your own:
i faced alot of issues with building this projects mainly because i was newbi to react.


# Sections 📚

✔️ Summary and About me\
✔️ Skills \
✔️ Open Source Projects Connected with Github\
✔️ Experience\
✔️ Certifications 🏆\
✔️ Blogs\
✔️ Education\
✔️ Contact me

To view a live example, **[click here](https://ashutosh1919.github.io/)**

# Clone And Use 📋

- The website is completely built on `react-js` library of `javascript` and that's why we need `nodejs` and `npm` installed.
- While installing `nodejs` and `npm`, try to install versions which are equal or greater than the versions mentioned in badges above.
- In case you want to help developing it or simply saving it, you can fork the repository just by clicking the button on the top-right corner of this page.
- After the successful installation of `nodejs` and `npm`, clone the repository into your local system using below command:
  - ```python
     git clone https://github.com/ashutosh1919/masterPortfolio.git
    ```
  - This will clone the whole repository in your system.
- To download required dependencies to your system, navigate to the directory where the cloned repository resides and execute following command:
  - ```python
    npm install
    ```
    which will install all the dependencies, dont worry if npm gives alot of warnings just run
    ``` npm audit fix ```
    and we will be good to go
#Remove git because its not for your account (if deploying to github pages)
use command
``` git remote remove origin ```
then remove files from working tree
``` rm -rf .git```
now you are good to go.
# Customize it to make your own portfolio ✏️

In this project, there are basically 4 things that you need to change to customize this to anyone else's portfolio: **package.json**, **Personal Information**, **Github Information** and **Splash Logo**.

### package.json

Open this file, which is in the main cloned directory, choose any "name" and change "homepage " to `https://<your-github-username>.github.io`. Do not forget the `https://`, otherwise fonts will not load.

### Personal Information

You will find `src/portfolio.js` file which contains the complete information about the user. The file looks something like below:

```python
// Home Page
const greeting = {
    ...
}

// Social Media
const socialMediaLinks = {
    ...
}

...
```

You can change the personal information, experience, education, social media, certifications, blog information, contact information etc. in `src/portfolio.js` to directly reflect them in portfolio website.

### Github Information

You will find `git_data_fetcher.js` file in the main directory of the repository. This file is used to fetch the data (Pull requests, Issues, Organizations, Pinned projects etc.) from your github.
If you open the file, you will see below component at the top of the file. You need to change only that component.


```python
const openSource = {
  githubConvertedToken: "Your Github Token Here.",
  githubUserName: "Your Github Username Here.",
};
```

You can get a github token as described [here](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token). Give all permissions while generating token. Also add your `githubUserName` in the correct field inside `git_data_fetcher.js`.
Now, you need to run following command.

**Warning:** Treat your tokens like passwords and keep them secret. When working with the API, use tokens as environment variables instead of hardcoding them into your programs.

```python
node git_data_fetcher.js
```

This will fetch all the data from your github and it will automatically replace my data with yours.
Whenever you want to update the github related information on the website you need to run this command.

### Splash Logo

Note here that if you click [my portfolio](https://ashutosh1919.github.io), you can see animating the logo at the beginning. I have designed that logo in [`Figma`](https://www.figma.com/) and then animated it using css.
Therefore, this part of portfolio is not customizable. But don't worry we have a solution to this problem. You have below two alternatives:

- If you want to design your own logo, then you can design it using `Figma` or `Adobe XD` or `Adobe Illustrator` or `Inkscape`. If you want to animate it, you can refer to `./src/components/Loader` directory which contains `js` and `css` files which animates the logo.
- If you don't want Splash screen or you don't know how to design logo, then this option is for you.

  - You can open `src/portfolio.js` file and at the top of this file you will see `settings` component as below:
  - ```python
    // Website related settings
    const settings = {
      isSplash: true,
    };
    ```
  - Change `isSplash` from `true` to `false`.
  - Now, if you see your website using `npm start`, it will directly open `home` rather than animating logo `splash` screen.
  - If you design your logo in future, then edit the files in `./src/components/Loader` and then revert `isSplash` to `true` in `src/portfolio.js`.

# Choose Theme 🌈

- You can take a look at `src/theme.js` file where all available themes are mentioned with respective color codes.
- At the bottom of this file you will see the below code:
  - `export const chosenTheme = blueTheme;`
  - You need to change the name from `blueTheme` to whatever theme you want to set your website to.
  - You can define new theme similarly as other themes and you can assign name of that new defined theme to `chosenTheme`.
- That's it. You just need to change the theme name and the code will take care of everything else.

#Deployment:
create a new repository on github.  <br>
 Use command on terminal<br>
 ```
 npm run build
 ```
 it will create a build folder which will contain all deployable project
 <br>
 then open the folder <br>
 ``` cd build```
 then initialize the git because we deleted the older one. <br>
 ```git init ```
 NOTE: Now build is a seprate and new github repo, which we have to deploy to github pages.  <br>
 then set remote origin to your repo. <br>
 ``` git remote add origin <your repo link.git>``` <br>
 ``` git add . ``` <br>
 ``` git commit -m "MESSAGE"```<br>
 now we have to simply upload it to our branch <br>

 ```git push origin master```<br>
 will work,  and just deploy the github page from branch master.<br>
 or you can<br>
 create a new branch and deploy there <br>
 ``` git checkout -b <new branch name>```<br>
 now deploy using command<br>
 ``` git push origin <new branch name>```<br>
 and now you can deploy this branch to github pages.
 <br>
 i strongly recommend you to follow https://github.com/ashutosh1919/masterPortfolio READ Me<br>

 it is just i was struggling with thier steps coz they were not explained maybe the way i do so.<br>
 he has also created a tutorial video which will help you alot https://www.youtube.com/watch?v=IwBS39TOmpA<br>


 All credits to original Developers and contributors.<br>
 Happy Coding!
