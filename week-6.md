# Homework for 02/20/2024

## What does it all mean? Reflections on Node Template

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
    - 
# Homework for 02/22/2024

## Reflections

- Video 1 Reflections/ notes
    - What is a function?
        - Functions are like verbs
            - Question: it seems as though function cannot exist by itself so is it logical to assume that function is predicated on something else? In this case “addNumbers”? You can’t just type in “addNumbers” and JS do what you want it to do does it need that function attribute in order to understand that we want it to add numbers? 
    - Camel Case: 
        - The first letter/word is lower case and the second letter of the second word is capitalized.
            - Question: Why? We used camel case in my c# class but I never understood why this was important. Is this for us or the machine? 
    - Function paramaters 
        - This seems pretty strait forward. I am instructing “function addNumbers” to ONLY add two numbers. I would imagine in more intermediate JS where you have a input form and the user adds three numbers into the box the program would throw an exception sense the inputs are outside of the parameters, unless we use some sort of catch instructions. I am not sure if exception and catch are exclusive to c# or they’re pretty universal even if the implementation is different. 
    - Return function
        - Is there a term for different variables (for lack of a better word)? Between ‘function’ and ‘return’ these are specific instructions we are giving the machine to do x task. We are in essence telling the machine I want you to do something (function) and give me the answer (return). While addNumbers is more like this is what we want to figure out. These terms are different in nature as to what is being ask and inquired. 
- Video 2 reflections/ notes
    - Paramaters vs Arguments
        - Parameters seem to be like theoretical science (working only with theory and variables). It is just that setting parameters not yet doing what we want it to actually do, just setting the rules
        - Arguments seem to be more like scientific engineering (actually running experiments with actual values and matter). Here is where it will actually preform the theoretical task with actual data
    - Console.log
        - Gives the results of what ever instructions in the terminal. 
- General Reflections
    - JS seems way easier to use than c#. Not having to define so many variables is nice considering you don’t have a massive list of variables floating around everywhere above your code. Just looking at this code thought it seems specific enough for the example given but I can see where the freedom of JS can kind of become a detriment if we don’t use ‘best practices’ especially when working on more complex projects. For example what if we were needing the answer to two equations and then needing to add the two results together. It seems as though we would need to define some variables (like we would in c#) and then JS would look similar to c# in that regard just with different names. But what I am curious about is when we use the const function, if we had two equations and use the const function is there any thing tying them to the specific equations? how would JS know the difference between the two answers? Or is it just that the const is linked to whatever specific line of code its assigned to? Not sure if the question makes sense.

	
