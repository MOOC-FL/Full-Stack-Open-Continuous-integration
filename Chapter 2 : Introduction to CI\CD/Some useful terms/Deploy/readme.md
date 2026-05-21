#### Deploy
- Deployment refers to putting the software where it needs to be for the end-user to use it. In the case of libraries, this may simply mean pushing an npm package to a package archive (such as npmjs.com(opens in a new tab)) where other users can find it and include it in their software.
- Deploying a service (such as a web app) can vary in complexity. In part 3(opens in a new tab) our deployment workflow involved running some scripts manually and pushing the repository code to `Fly.io`(opens in a new tab) or `Render`(opens in a new tab) hosting service.
- In this part, we'll develop a simple **"deployment pipeline"** that deploys each commit of your code automatically to Fly.io or Render if the committed code does not break anything.
- Deployments can be significantly more complex, especially if we add requirements such as "the software must be available at all times during the deployment" (zero downtime deployments) or if we have to take things like database migrations
