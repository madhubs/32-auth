![cf](https://i.imgur.com/7v5ASc8.png) 32: Authentication and Authorization
======

#### Additions for Auth:

I added this chunk of code to the landing-container/index.js file:
```
return (
     <div>
       <h2>hello world from landing!</h2>
       <AuthForm
         auth={params.auth}
         onComplete={handleComplete}/>

       <section>
         {utils.renderIf(this.props.auth,
           <Dashboard
           />
         )}
       </section>
     </div>
   );
```

## Submission Instructions
* fork this repository & create a new branch for your work
* write all of your code in a directory named `lab-` + `<your name>` **e.g.** `lab-susan`
* push to your repository
* submit a pull request to this repository
* submit a link to your PR in canvas
* write a question and observation on canvas

## Learning Objectives
* We will be able to manage basic and bearer auth on the client side
* We will learn to manage cookies on the client side

## Requirements
#### Configuration
#### backend
* clone [sluggram-backend](http://github.com/slugbyte/sluggram)

##### frontend
* `README.md`
* `.babelrc`
* `.gitignore`
* `package.json`
* `webpack.config.js`
* `src/**`
* `src/main.js`
* `src/style`
* `src/style/main.scss`
* `src/style/lib`
  * `_vars.scss`
* `src/style/base`
  * `_base.scss`
  * `_reset.scss`
* `src/style/layout`
  * `_header.scss`
  * `_footer.scss`
  * `_content.scss`

#### Feature Tasks
* Review the backend code for the Sluggram API; you should be able to interpret and understand what's happening
* create a simple front end for your cf-gram (or comparable) API
* create a landing page that enables a user to signup and signin
  * redirect the user to the dashboard page on signup or signin
  * store the users token in `localStorage` on signin

###### App Component Tree
Your components should be nested in the following layout  
```
App
  LandingContainer
    AuthForm
```
