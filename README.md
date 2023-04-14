# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)


## How to use Amplify

### Setting Up Our Frontend code

```ssh
npx create-react-app .

Creating a new React app in /Users/josfranco/frubana/app-demo-amplify-helloworld.

Installing packages. This might take a couple of minutes.
Installing react, react-dom, and react-scripts with cra-template...


added 1422 packages in 44s

234 packages are looking for funding
  run `npm fund` for details

Installing template dependencies using npm...

added 62 packages, and changed 1 package in 8s

234 packages are looking for funding
  run `npm fund` for details
Removing template package using npm...


removed 1 package, and audited 1484 packages in 2s

234 packages are looking for funding
  run `npm fund` for details

6 high severity vulnerabilities

To address all issues (including breaking changes), run:
  npm audit fix --force

Run `npm audit` for details.

Success! Created app-demo-amplify-helloworld at /Users/josfranco/frubana/app-demo-amplify-helloworld
Inside that directory, you can run several commands:

  npm start
    Starts the development server.

  npm run build
    Bundles the app into static files for production.

  npm test
    Starts the test runner.

  npm run eject
    Removes this tool and copies build dependencies, configuration files
    and scripts into the app directory. If you do this, you can’t go back!

We suggest that you begin by typing:

  cd /Users/josfranco/frubana/app-demo-amplify-helloworld
  npm start

Happy hacking!
```

### Initializing Our Backend

```ssh
amplify init
Note: It is recommended to run this command from the root of your app directory
? Enter a name for the project appdemoamplifyhellow
The following configuration will be applied:

Project information
| Name: appdemoamplifyhellow
| Environment: dev
| Default editor: Visual Studio Code
| App type: javascript
| Javascript framework: react
| Source Directory Path: src
| Distribution Directory Path: build
| Build Command: npm run-script build
| Start Command: npm run-script start

? Initialize the project with the above configuration? Yes
Using default provider  awscloudformation
? Select the authentication method you want to use: AWS access keys
? accessKeyId:  ********************
? secretAccessKey:  ****************************************
? region:  us-east-1
Adding backend environment dev to AWS Amplify app: dnflfi1rfuaw5

Deployment completed.
Deploying root stack appdemoamplifyhellow [ ====================-------------------- ] 2/4
	amplify-appdemoamplifyhellow-… AWS::CloudFormation::Stack     CREATE_IN_PROGRESS             Fri Apr 14
	AuthRole                       AWS::IAM::Role                 CREATE_COMPLETE                Fri Apr 14
	UnauthRole                     AWS::IAM::Role                 CREATE_COMPLETE                Fri Apr 14
	DeploymentBucket               AWS::S3::Bucket                CREATE_IN_PROGRESS             Fri Apr 14

✔ Help improve Amplify CLI by sharing non sensitive configurations on failures (y/N) · yes
Deployment state saved successfully.
✔ Initialized provider successfully.
✅ Initialized your environment successfully.

Your project has been successfully initialized and connected to the cloud!

Some next steps:
"amplify status" will show you what you've added already and if it's locally configured or deployed
"amplify add <category>" will allow you to add features like user login or a backend API
"amplify push" will build all your local backend resources and provision it in the cloud
"amplify console" to open the Amplify Console and view your project status
"amplify publish" will build all your local backend and frontend resources (if you have hosting category added) and provision it in the cloud

Pro tip:
Try "amplify add api" to create a backend API and then "amplify push" to deploy everything
```

### Adding An API

```ssh
amplify add api
? Select from one of the below mentioned services: (Use arrow keys)
❯ GraphQL
  REST
```

```ssh
amplify add api
? Select from one of the below mentioned services: REST
✔ Provide a friendly name for your resource to be used as a label for this category in the project: · apib79ac1fe
✔ Provide a path (e.g., /book/{isbn}): · /customers/{customerId}
Only one option for [Choose a Lambda source]. Selecting [Create a new Lambda function].
? Provide an AWS Lambda function name: CustomerHanddler
? Choose the runtime that you want to use: NodeJS
? Choose the function template that you want to use: Hello World

Available advanced settings:
- Resource access permissions
- Scheduled recurring invocation
- Lambda layers configuration
- Environment variables configuration
- Secret values configuration

? Do you want to configure advanced settings? Yes
? Do you want to access other resources in this project from your Lambda function? Yes
? Select the categories you want this function to have access to.

You can access the following resource attributes as environment variables from your Lambda function
	ENV
	REGION
? Do you want to invoke this function on a recurring schedule? No
? Do you want to enable Lambda layers for this function? No
? Do you want to configure environment variables for this function? No
? Do you want to configure secret values this function can access? No
? Do you want to edit the local lambda function now? Yes
Edit the file in your editor: /Users/josfranco/frubana/app-demo-amplify-helloworld/amplify/backend/function/CustomerHanddler/src/index.js
? Press enter to continue
Successfully added resource CustomerHanddler locally.

Next steps:
Check out sample function code generated in <project-dir>/amplify/backend/function/CustomerHanddler/src
"amplify function build" builds all of your functions currently in the project
"amplify mock function <functionName>" runs your function locally
To access AWS resources outside of this Amplify app, edit the /Users/josfranco/frubana/app-demo-amplify-helloworld/amplify/backend/function/CustomerHanddler/custom-policies.json
"amplify push" builds all of your local backend resources and provisions them in the cloud
"amplify publish" builds all of your local backend and front-end resources (if you added hosting category) and provisions them in the cloud
✅ Succesfully added the Lambda function locally
✔ Restrict API access? (Y/n) · yes
✔ Who should have access? · Authenticated users only
✔ What permissions do you want to grant to Authenticated users? · create, read, update, delete
✅ Successfully added auth resource locally.
✔ Do you want to add another path? (y/N) · no
✅ Successfully added resource apib79ac1fe locally

✅ Some next steps:
"amplify push" will build all your local backend resources and provision it in the cloud
"amplify publish" will build all your local backend and frontend resources (if you have hosting category added) and provision it in the cloud
```

### Push changes

```ssh
amplify push
✔ Successfully pulled backend environment dev from the cloud.

    Current Environment: dev

┌──────────┬──────────────────────┬───────────┬───────────────────┐
│ Category │ Resource name        │ Operation │ Provider plugin   │
├──────────┼──────────────────────┼───────────┼───────────────────┤
│ Function │ CustomerHanddler     │ Create    │ awscloudformation │
├──────────┼──────────────────────┼───────────┼───────────────────┤
│ Auth     │ appdemoamplifyhellow │ Create    │ awscloudformation │
├──────────┼──────────────────────┼───────────┼───────────────────┤
│ Api      │ apib79ac1fe          │ Create    │ awscloudformation │
└──────────┴──────────────────────┴───────────┴───────────────────┘
✔ Are you sure you want to continue? (Y/n) · yes

Deployment completed.
Deploying root stack appdemoamplifyhellow [ ==============================---------- ] 3/4
	amplify-appdemoamplifyhellow-… AWS::CloudFormation::Stack     UPDATE_IN_PROGRESS             Fri Apr 14
	functionCustomerHanddler       AWS::CloudFormation::Stack     CREATE_COMPLETE                Fri Apr 14
	authappdemoamplifyhellow       AWS::CloudFormation::Stack     CREATE_COMPLETE                Fri Apr 14
	apiapib79ac1fe                 AWS::CloudFormation::Stack     CREATE_COMPLETE                Fri Apr 14
Deployed function CustomerHanddler [ ======================================== ] 3/3
	LambdaExecutionRole            AWS::IAM::Role                 CREATE_COMPLETE                Fri Apr 14
	LambdaFunction                 AWS::Lambda::Function          CREATE_COMPLETE                Fri Apr 14
	lambdaexecutionpolicy          AWS::IAM::Policy               CREATE_IN_PROGRESS             Fri Apr 14
Deployed auth appdemoamplifyhellow [ ======================================== ] 10/10
	UserPool                       AWS::Cognito::UserPool         CREATE_COMPLETE                Fri Apr 14
	UserPoolClientWeb              AWS::Cognito::UserPoolClient   CREATE_COMPLETE                Fri Apr 14
	UserPoolClient                 AWS::Cognito::UserPoolClient   CREATE_COMPLETE                Fri Apr 14
	UserPoolClientRole             AWS::IAM::Role                 CREATE_COMPLETE                Fri Apr 14
	UserPoolClientLambda           AWS::Lambda::Function          CREATE_COMPLETE                Fri Apr 14
	UserPoolClientLambdaPolicy     AWS::IAM::Policy               CREATE_COMPLETE                Fri Apr 14
	UserPoolClientLogPolicy        AWS::IAM::Policy               CREATE_COMPLETE                Fri Apr 14
	UserPoolClientInputs           Custom::LambdaCallout          CREATE_COMPLETE                Fri Apr 14
	IdentityPool                   AWS::Cognito::IdentityPool     CREATE_COMPLETE                Fri Apr 14
	IdentityPoolRoleMap            AWS::Cognito::IdentityPoolRol… CREATE_COMPLETE                Fri Apr 14
Deployed api apib79ac1fe [ ======================================== ] 5/5
	apib79ac1fe                    AWS::ApiGateway::RestApi       CREATE_COMPLETE                Fri Apr 14
	functionCustomerHanddlerPermi… AWS::Lambda::Permission        CREATE_IN_PROGRESS             Fri Apr 14

Deployment state saved successfully.

REST API endpoint: https://b15szq9gc1.execute-api.us-east-1.amazonaws.com/dev
```

### Integrating our Frontend with Backend

```ssh
npm install aws-amplify @aws-amplify/ui-react
```

### Add index.js

```nodejs
import Amplify from "aws-amplify";
import awsExports from "./aws-exports";
Amplify.configure(awsExports);
```

### Mapping Api Id on App.js

```ssh
amplify add hosting
✔ Select the plugin module to execute · Hosting with Amplify Console (Managed hosting with custom domains, Continuous deployment)
? Choose a type Manual deployment

You can now publish your app using the following command:

Command: amplify publish
```

### Publish frontend site

```ssh
amplify publish
✔ Successfully pulled backend environment dev from the cloud.

    Current Environment: dev

┌──────────┬──────────────────────┬───────────┬───────────────────┐
│ Category │ Resource name        │ Operation │ Provider plugin   │
├──────────┼──────────────────────┼───────────┼───────────────────┤
│ Hosting  │ amplifyhosting       │ Create    │ awscloudformation │
├──────────┼──────────────────────┼───────────┼───────────────────┤
│ Function │ CustomerHanddler     │ No Change │ awscloudformation │
├──────────┼──────────────────────┼───────────┼───────────────────┤
│ Auth     │ appdemoamplifyhellow │ No Change │ awscloudformation │
├──────────┼──────────────────────┼───────────┼───────────────────┤
│ Api      │ apib79ac1fe          │ No Change │ awscloudformation │
└──────────┴──────────────────────┴───────────┴───────────────────┘
✔ Are you sure you want to continue? (Y/n) · yes

Deployment completed.
Deployed root stack appdemoamplifyhellow [ ======================================== ] 5/5
	amplify-appdemoamplifyhellow-… AWS::CloudFormation::Stack     UPDATE_COMPLETE                Fri Apr 14
	hostingamplifyhosting          AWS::CloudFormation::Stack     CREATE_COMPLETE                Fri Apr 14
	functionCustomerHanddler       AWS::CloudFormation::Stack     UPDATE_COMPLETE                Fri Apr 14
	authappdemoamplifyhellow       AWS::CloudFormation::Stack     UPDATE_COMPLETE                Fri Apr 14
	apiapib79ac1fe                 AWS::CloudFormation::Stack     UPDATE_COMPLETE                Fri Apr 14
Deployed hosting amplifyhosting [ ======================================== ] 1/1
	AmplifyBranch                  AWS::Amplify::Branch           CREATE_COMPLETE                Fri Apr 14

Deployment state saved successfully.


Publish started for amplifyhosting
```

### Test

Web Site: https://dev.dnflfi1rfuaw5.amplifyapp.com/