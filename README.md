<h1>Deploy de nest en heroku</h1>
<h2>Viene con el video donde consegui hacerlo</h2>

Hay una parte en la configuracion de heroku, se puede hacer tambien
por lineas de comando en caso de no usar un repositorio de la 
siguiente manera: 

<p>heroku config:set NPM_CONFIG_PRODUCTION=false</p>
<p>heroku config:set NODE_ENV=production</p>

<h2>Para implementarlo en vercel le añadi un vercel.json</h2>
<p>Con ese json se puede ejecutar unos comando para podir subirloa vercel desde visual code, tambien se puede desde el repositorio pero hay que hacer una configuraciones que no pude entender con claridad y no tenia tiempo para proceguir por alli, asi que obte por subirlo por lineas de codigo por los momentos.</p>
<P>Al final del este readme dejare las indicaicones con las que puede implementarlo en vercel</p>

<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo_text.svg" width="320" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://coveralls.io/github/nestjs/nest?branch=master" target="_blank"><img src="https://coveralls.io/repos/github/nestjs/nest/badge.svg?branch=master#9" alt="Coverage" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

## Description

[Nest](https://github.com/nestjs/nest) framework TypeScript starter repository.

## Installation

```bash
$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://kamilmysliwiec.com)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## License

Nest is [MIT licensed](LICENSE).
"# nest-deploy-heroku" 



<h1>Implementacion de vercel (la explicacion esta en ingles)</h1>

<h3>Fuentes: https://cdmana.com/2021/11/20211114070316640R.html </h3>

<div class="col-lg-9 col-md-12 col-sm-12 col-xs-12">
                    <div class="page-wrapper">
                        <div class="row-fluid">
                            
                        </div>
                        <div class="blog-title-area text-center">
                            <ol class="breadcrumb hidden-xs-down">
                                <li class="breadcrumb-item"><a href="#">Home</a></li>
                                <li class="breadcrumb-item active">Deploy nest.js project based on vercel + GitHub action
                                </li>
                            </ol>

                            <h1>Deploy nest.js project based on vercel + GitHub action</h1>

                            <div class="blog-meta big-meta">
                                <small><a href="#" title="">2021-11-14 07:03:20</a></small>
                                <small><a href="#" title="">by Ke Chen</a></small>
                            </div>

                        </div>

                        <div class="row-fluid">
                            
                        </div>

                        <div style="margin-top: 15px;margin-bottom: 15px;overflow:auto;width: 100%;padding-bottom: 5px;padding-top: 5px;word-wrap:break-word;" class="con_text row-fluid blog-content">
                            <article class="article fmt article-content ">
 <h2 id="item-1"> Preface </h2>
 <p>&nbsp;&nbsp;&nbsp;&nbsp;  ah , since 8 After the article was published in January , There has been no change for two consecutive months , I admit I'm too busy ( In fact, it's very meow and lazy ). It will be here in the twinkling of an eye 11 On the , The weather is getting colder , Are you fat friends ready for the winter ！ If you don't have it, eat it for me ！</p>
 <p>&nbsp;&nbsp;&nbsp;&nbsp;1 Month of the month , The whole article uses vercel+hexo A tutorial on deploying blogs ,<a href="https://link.segmentfault.com/?enc=tcZB%2BYPLzLqR6YSaIdv%2F1g%3D%3D.j5hY8UaqfoQByOWmas2WBqqQc%2Bj3jnj8dltPl%2FZYqIUbuODgJOsn9FcKm8EtVwP8" rel="nofollow" target="_blank"> Give me more details </a>, utilize vercel Free resources to deploy some of your own small projects , A static website or something , Because many times it is not necessary to buy a server for personal play , Some public free resources on the Internet are enough for us to make , Of course, static websites are deployed , As a front end ,Nodejs The project must also be played , So today I'll show you how to be in Vercel Upper Department Node project .</p>
 <p>&nbsp;&nbsp;&nbsp;&nbsp; In this article, I use <a href="https://link.segmentfault.com/?enc=HrCC%2BHIu5dVYwhe4qsIk5g%3D%3D.zfKNfasMI11pJYTaJVDbVMP8xXpwyaladniZmo%2FvAM0%3D" rel="nofollow" target="_blank">Nest.js</a>, It is a progressive approach for building efficient and scalable server-side applications  Node.js  frame , The writing seems to want to spring？ I believe it should be easier for back-end students to use it .Nest.js It has the following characteristics ：</p>
 <ul>
  <li> Perfect support TypeScipt</li>
  <li> oriented  AOP  Programming </li>
  <li> Support  Typeorm</li>
  <li> High concurrency , Asynchronous non-blocking  IO</li>
  <li>Node.js  Version of  spring</li>
  <li> Building microservice applications </li>
 </ul>
 <p> That's not much to say , Let's get started ！ Follow the tutorial , If the deployment is not good, you hit me ！</p>
 <h2 id="item-2"> preparation </h2>
 <p>&nbsp;&nbsp;&nbsp;&nbsp; Before we start , We need to do some preparatory work ;</p>
 <h4> install nest.js</h4>
 <p><code>npm i -g @nestjs/cli</code></p>
 <h4> Create a new one nest.js project , Here, the name of my new project is blogServer</h4>
 <p> command ：<code>nest new blogServer</code></p>
 <p> After the new construction , Installation dependency , adopt <code>npm run start</code> Start project , Access port is 3000; Start up and you'll see Hello World Just ok La .<br><span class="img-wrap"><img loading="lazy" src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_0.jpg" class="lazy" referrerpolicy="no-referrer" data-src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_0.jpg" alt="" title=""></span></p>
 <h4> Submit to Github</h4>
 <p> After the project is completed , Submit the project to Github that will do , Let's start the deployment project .</p>
 <h2 id="item-3"> Deploy </h2>
 <h4> stay Vercel Associated items on </h4>
 <p>1、 Click on <code>new Project</code> Create a new project <br><span class="img-wrap"><img loading="lazy" src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_0.jpg" class="lazy" referrerpolicy="no-referrer" data-src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_0.jpg" alt="" title=""></span><br>2、 Select your new project , Import <br><span class="img-wrap"><img class="lazy" referrerpolicy="no-referrer" data-src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_6.jpg" alt="" title=""></span><br>3、 Skip new team , For personal use, there is no need to create a new team , Besides, the team needs to pay <br><span class="img-wrap"><img class="lazy" referrerpolicy="no-referrer" data-src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_6.jpg" alt="" title=""></span><br>4、 Project name is free to play , Frame selection other,build command According to your own project package.json The content in the is written ,output directory It is also filled in according to the packed folder name ,nest.js The default is as follows ,install command Keep the default , Click on <code>Deploy</code> Start deployment .<br><span class="img-wrap"><img class="lazy" referrerpolicy="no-referrer" data-src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_6.jpg" alt="" title=""></span></p>
 <p>Ok, The article is over , That's it , Ha ha ha ha .</p>
 <p> in fact , Deployed in this way nest.js project , When you open it, it will be 404, So we need the next operation .</p>
 <h4> To configure vercel.json</h4>
 <p>1、 Create a new file in the project root ,<code>vercel.json</code>, The contents are as follows ,name Is the name of your project , And package.json Medium name Keep consistent .</p>
 <pre><code class="json">{
    "version": 2,
    "name": "blog-server",
    "builds": [
        {
            "src": "dist/main.js",
            "use": "@vercel/node"
        }
    ],
    "routes": [
        {
            "src": "/(.*)",
            "dest": "dist/main.js"
        }
    ]
}</code></pre>
 <p> After configuring this file , You can use it locally vercel Command line tools are deployed . Of course, the premise is to install vercel Scaffolding tools ,<code>npm i -g vercel</code> Can be installed . With vercel After the command line tool , The project can be deployed with the following command .</p>
 <ul>
  <li> Package the project locally ,<code>npm run build</code>, Pack it out dist Folder ;</li>
  <li> First you need to log in , It's kind of similar npm The way ,<code>vercle login</code>, After executing this command, you will choose which platform to log in , We choose GitHub that will do , It will automatically open the browser for permission Authentication , After successful authentication, log in successfully ;</li>
  <li> Direct execution <code>vercel --prod</code>, Then take the next step all the way . When prompted for deployment, you can open vercel A look at the platform will show that it is being deployed , After the deployment is successful, you can access it normally .</li>
  <li> When we get here , In fact, the project has been successfully deployed , But if you have to package and deploy manually every time , That must not meet our expectations , So we need to use GitHub Action Automated Deployment .</li>
 </ul>
 <h4> To configure  GitHub Action Workflows</h4>
 <ul>
  <li> stay GitHub Create a new project workflow<br><span class="img-wrap"><img loading="lazy" src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_0.jpg" class="lazy" referrerpolicy="no-referrer" data-src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_0.jpg" alt="" title=""></span></li>
  <li> find Nodejs Templates , Click on set up<br><span class="img-wrap"><img loading="lazy" src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_0.jpg" class="lazy" referrerpolicy="no-referrer" data-src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_0.jpg" alt="" title=""></span></li>
  <li><p> Start writing script content , The script is as follows ,name This is the script name , The default template will be in <code>run: npm run build --if-present</code> One more line below <code>run:npm run test</code> Let's get rid of it . You can also copy my template directly . among VERCEL_TOKEN、VERCEL_PROJECT_ID、VERCEL_ORG_ID We need to configure them later . Come here , We workflow The new building is successful . Subsequent code push perhaps pr Merge will trigger it to execute .</p><pre><code class="yaml"># This workflow will do a clean install of node dependencies, cache/restore them, build the source code and run tests across different versions of node
# For more information see: https://help.github.com/actions/language-and-framework-guides/using-nodejs-with-github-actions

name: deploy server blog

on:
 push:
 branches: [ master ]
 pull_request:
 branches: [ master ]

jobs:
 build:

 runs-on: ubuntu-latest

 strategy:
   matrix:
     node-version: [ 12.x, 14.x, 16.x ]
     # See supported Node.js release schedule at https://nodejs.org/en/about/releases/

 steps:
   - uses: actions/checkout@v2
   - name: Use Node.js ${{ matrix.node-version }}
     uses: actions/setup-node@v2
     with:
       node-version: ${{ matrix.node-version }}
       cache: 'npm'
   - run: npm ci
   - run: npm run build --if-present
   - name: Deploy to Vercel
     run: npx vercel --token ${VERCEL_TOKEN} --prod
     env:
         VERCEL_TOKEN: ${{ secrets.VERCEL_TOKEN }}
         VERCEL_PROJECT_ID: ${{ secrets.VERCEL_PROJECT_ID }}
         VERCEL_ORG_ID: ${{ secrets.VERCEL_ORG_ID }}</code></pre></li>
  <li><p> Next, let's configure the above three variables . Remember in the last step we performed <code>vercel --prod</code> Orders , After executing this command, a local <code>.vercel</code> Folder , The content is like this , Remember this projectId and orgId, The next step is to use </p><p><span class="img-wrap"><img loading="lazy" src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_0.jpg" class="lazy" referrerpolicy="no-referrer" data-src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_0.jpg" alt="" title=""></span></p></li>
  <li><p> open GitHub In the project Settings, choice Secrets, Add three new variables here , among VERCEL_PROJECT_ID、VERCEL_ORG_ID It's up there projectId and orgId, Let's continue to set VERCEL_TOKEN</p><p><span class="img-wrap"><img loading="lazy" src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_0.jpg" class="lazy" referrerpolicy="no-referrer" data-src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_0.jpg" alt="" title=""></span></p></li>
  <li><p> open vercel platform , find settings, Open it up Tokens, Click on create Create a new one token, I've built it here , It's called serverActionToken, there token Just to make GitHub Action Be able to access vercel Project .<strong> Remember to copy it after you create it ！！！</strong></p><p><span class="img-wrap"><img loading="lazy" src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_6.jpg" class="lazy" referrerpolicy="no-referrer" data-src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_6.jpg" alt="" title=""></span></p></li>
  <li><p> Back to GitHub Of Settings-Secrets Newly added VERCEL_TOKEN, The corresponding value is the last one above token. In this way, our authority will get through to each other , The deployment related configuration has been OK La .</p><p><span class="img-wrap"><img loading="lazy" src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_0.jpg" class="lazy" referrerpolicy="no-referrer" data-src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_0.jpg" alt="" title=""></span></p></li>
  <li><p> Change the local content casually , Submit ,workflow Automatically start execution </p><p><span class="img-wrap"><img loading="lazy" src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_6.jpg" class="lazy" referrerpolicy="no-referrer" data-src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_6.jpg" alt="" title=""></span></p></li>
  <li><p> Successful implementation , So far, the project is deployed , Follow up as long as the project is updated , After submission, it will pass GitHub Action Automatically deployed .</p><p><span class="img-wrap"><img loading="lazy" src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_6.jpg" class="lazy" referrerpolicy="no-referrer" data-src="//inotgo.com/imagesLocal/202110/27/20211027184817225t_6.jpg" alt="" title=""></span></p></li>
 </ul>
 <h2 id="item-4"> summary </h2>
 <p> What's the end , be it so ,okok, You can try ！！！</p>
 <h2 id="item-5"> Reference resources </h2>
 <p> Some blog posts in the reference link may be old , because vercel Previously known as now, But the operation is much the same , Will play workflow There will certainly be more ways , Let's play by ourselves .</p>
 <pre><code>https://itnext.io/deploy-nest-js-on-zeit-now-with-github-actions-86bc226e7371

https://hyper-text.org/archives/2021/07/nextjs_vercel_deploy.shtml

https://aaronfrancis.com/2021/the-perfect-vercel-github-actions-deployment-pipeline

https://www.eliostruyf.com/deploy-site-vercel-github-actions-releases/</code></pre>
</article>
                            <div class="nextinfo">
                                <p>版权声明 <br>
                                    本文为[<span style="color: #b92c28">Ke Chen</span>]所创，转载请带上原文链接，感谢<br>
                                    https://cdmana.com/2021/10/20211027184817225t.html
                                </p>
                            </div>
                        </div>

                        <div class="blog-title-area">
                            <div class="tag-cloud-single">
                                <span>Tags</span>
                                    <small><a href="#" title="deploy">deploy</a></small>
                                    <small><a href="#" title="nest.js">nest.js</a></small>
                                    <small><a href="#" title="nest">nest</a></small>
                                    <small><a href="#" title="js">js</a></small>
                                    <small><a href="#" title="project">project</a></small>
                            </div>

                        </div>

                    </div>

                    <div class="row-fluid">
                        
                    </div>
                </div>