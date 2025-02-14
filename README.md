# Hackathon101
Learning techstacks to win your some hackathons

This repository will go over some frontend design tips/tricks to get you working quickly. 

# Forking this repository
[GIT](https://git-scm.com/downloads) is the single most important tool for a hackathon (and is the single most powerful tool 
ever given to programmers). GIT enables collaboration between developers, and allows you to quickly checkout different versions
of the project (helping you to find bugs, revert bad code, etc.). Please [download GIT](https://git-scm.com/downloads).

You can confirm your download by running `git --version` (you might need to restart your terminal, since PATH variables usually
are not updated immediately). You should see something like `git version 2.31.4` in your terminal. 

This repository is available at [https://github.com/buaiml/Hackathon101/fork](https://github.com/buaiml/Hackathon101/fork). Please
fork this code by adding `/fork` to the end of the link, or by pressing the `fork` button in the top right. You may rename
the repository if you'd like, but make sure you press the green `Create Fork` button in the bottom right.

You can then clone the repository locally using the `git clone` command. If your new link is `https://github.com/your_name/Hackathon101`,
then you should run `git clone https://github.com/your_name/Hackathon101.git` in a directory you like (Any directory is fine, but some people
might want to run the terminal command `cd Desktop` to enter your desktop). You can use `cd <folder>`, `ls`, and `pwd` to navigate your files
using the terminal. 

# Installing Node
[Node.js](https://nodejs.org/en) is a javascript environment that comes with a package manager `npm`. It is required to work with
front-end tools like React.js, Next.js, etc. Please follow the instructions to [download the LTS of node](https://nodejs.org/en/download).

Afterwards, you should be able to run `node --version` and `npm --version`.

# Setting up the project
Alright, by now we have a (mostly empty) directory. Let's navigate outside the project directory (Run `cd ..`). Confirm 
that you are in the right place by running `ls`. You should see `"Hackathon101"` somewhere.

Now, run
```sh
npx create-next-app@latest
```

You'll see a bunch of options. Here are the ones we prefer:
```sh
What is your project named? Hackathon101
Would you like to use TypeScript? Yes
Would you like to use ESLint? No
Would you like to use Tailwind CSS? Yes
Would you like your code inside a `src/` directory? Yes
Would you like to use App Router? (recommended) Yes
Would you like to use Turbopack for `next dev`? (default)
Would you like to customize the import alias (`@/*` by default)? No
What import alias would you like configured? @/* (default)
```

This will install some packages, and add a bunch of files to our `Hackathon101` directory. Let's enter it using 
`cd Hackathon101`, then run `npm run dev`. You should see a message like `ready - started server on http://localhost:3000`
in your terminal. Open your browser and navigate to `http://localhost:3000`. You should see a page that says `Welcome to your Next.js site!`.

We also want to push our code to our forked repository. Run `git add .`, `git commit -m "Initial commit"`, and `git push origin main`.

# Making changes
Here is the hyper opinionated stuff... We are assuming you are working on a Hackathon project, and don't care much
about the longevity of the project. This is the **only reason** why it's okay to use LLMs to
build everything for us. 

Let's use gitingest.com... Go to your forked github repo, like `https://github.com/your_name/Hackathon101`. Replace `github.com` 
with `gitingest.com`, so you get `https://gitingest.com/your_name/Hackathon101`. You should see a page with a bunch of text
from your project, including your code, docs, packages, etc. 

You can copy-paste all this stuff into an LLM. Which LLM you choose depends *sortof* on your preference, but
mainly on the *amount of tokens* you have. Roughly:
- [ChatGPT](https://chat.com)'s WebUI can handle ~32k tokens (probably, they hide this data)
- [Gemini](https://aistudio.google.com/) can handle ~1M tokens (sign out of BU google account, use personal)
- [Claude](https://claude.ai/) can handle ~200k tokens (if you pay for premium... unclear for free) 
- [Deepseek](https://chat.deepseek.com/) can handle ~128k tokens

You can copy-paste those important details (your full code, your file structure, etc.) into an LLM, and ask
the LLM to make some changes. For example, try to make:
1. A chat room 
2. A blog
3. A portfolio website

# Deploying the project
Proper projects will deploy to [Vercel](https://vercel.com). You can sign in with your github account, and import your project.
However, we are just going to do something quick an dirty: We are going to use `ngrok`.

ngrok is a tool that allows you to expose your local server to the internet. It is sortof like port forwarding, but
it is much easier to use (and you don't need any special admin permissions on your network... it just works). 

First, [install ngrok](https://ngrok.com/downloads/). Confirm your installation using `ngrok --version`. 

Now, we can expose our local server to the internet using `ngrok http 3000`. You should see a bunch of text, 
including a `Forwarding` link. The `Forwarding` link can be given out to people to test out your website. 
If you have a backend server, you can also use `ngrok` to expose that server.

