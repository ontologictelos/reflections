# What does it all mean?

## Reflections on Node Template

### Files pushed to Github
- .eslintrc.cjs
- .gitignore
- .prettierignore
- .prettierrc
- package.json

### Why do we need all these?

- Well first what do these all do? Eslint and prettier in essence just help us write better code by giving us settings and configurations that assist us when we make a mistake. But in order to install these we have to have a file for them to live in that’s where .vscode/extensions and .vscode/settings become relevant/ important.
- Just downloading the extensions is not enough though. Or perhaps we won’t be able to use them at all unless we install and use npm.
- With installing npm we get a package.json (super important). I don’t fully understand package.json in what it does specifically but it is something that grounds our work and gives our code rules to follow.
- I am still really unsure what the ignore file does though. From my understanding this just tells git to ignore them so they won’t be pushed or put on GitHub? Why? I don’t know. Do we just not want them on GitHub? Is this a space or size concern or would it sort of break github? 

### generalized steps you went through in setting up NodeJS Template Repo

  - Make directory (mkdir)
      - Put two files (use exact words, these will also be hidden directories due to the dot infant of the name of the file)
          - Make directory for .vscode/extensions.json
          - Make directory for .vscode/settings.json
      - Make a gist for the files of the extensions and settings you want. (This short cut pbpaste > “insert whatever directory here” is pretty cool)
  - Reflections on video 1
      - What does all this mean?
          - At a very basic level we are installing extensions and “pre setting” settings for our project. 
          - Extensions in particular can be anything from themes to other soft ware that can help us write better code.
          - Settings are similar to extensions but they seem to have a different focus and do different things. In the video we see things like auto formatting and save on leaving a page. 
          - ? In video 3 you say that .vscode needs to be a hidden directory so that vscode will know to look in there. If it wasn’t hidden would vscode not look in there? Why is it set up that way?
- Setting up eslint 
    - NPM (Naboo podracing misadventures, I will forever call NPM this)
        - Initialize NPM 
    - Only after installing NPM can we install aslant
        - Init (initialize) eslint (npm init @eslint/config)
            - Follow prompts 
- Install Prettier 
    - Npm install prettier 
        - This creates a hidden configuration file. 
        - Create a ignore file in vscode
    - Integrate with eslint
        - In vs code open file eslint.js and within extends add in “prettier” (doing this ensures that the style format established earlier ‘airbnb-base’ works along side “prettier”
- Create git.ignore file 
    - This tells GitHub to ignore certain pieces of information. This ignores nodes which we don’t want on GitHub. 
	
