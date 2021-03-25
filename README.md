### code from AWS tutorial on how to build a full-stack react application

tutorial: https://aws.amazon.com/getting-started/hands-on/build-react-app-amplify-graphql/

deployed app: https://main.d1xayisp7ewhpg.amplifyapp.com/

- bootsrapped using create-react-app
- graphQL integration 
- storage service

### A few things I ran into along the way
- Module 3 (Add Authentication): I had to remove aws-exports.js from gitignore for src/index.js to recognize the file
- Module 3 (Add Authentication): In the CI/CD setup of frontend and backend, the branch for the target backend that is automatically created after editing the build script is called "staging" not "dev"
- Module 4 (GraphQL API and DB): The graphql type setup we create is called 'Todo' (amplify/backend/api/your-app-name/schema.graphql), but the front-end React code later on in the module refers to type 'Note' instead of 'Todo' so the queries and mutations in App.js will need to be edited to replace the word Note with Todo to reflect the code in src/graphql 