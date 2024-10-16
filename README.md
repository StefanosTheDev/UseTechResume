# UseTechResume

### Project Goal
- The goal of this project is to develop a Rest API in Node MongoDB, Mongoose and eventually AWS that is industry standard that follows best practices.
- The goal of this project is also to develop unit test cases and complete all necessary functionality testing required.
- The goal of this project is to achieve high levels of security amongst source code as well as with best authentication practices


### What is UseTechResume
- UseTechResume will be a backend rest APi that will allow anyone to send text to an AI Assistant that will then spit out a more appropriate / proffesional response for your resume.


### Features of UseTechResume:

#### Auth Level
- Users will have the ability to create an account with the following properties:
  - User Model:
    - FirstName, LastName, Username, Email, Password
- Users will also have the ability to login with Username / Password.
- Users will also have the ability to leverage Google Auth to login if Username / Password is not an option they wish to use.
  
#### Opeartion Level: 
- User will log into their account. Drop Text inot a text box. It will get outputted by AI to fit their resume. We will probably have some questions prior as well for context to shape the System Level. Then if the user likes the output. They can copy that generation. and send it to their resume. If the User goes beyond an X Amount of Tokens. They will be informed that they have to enter the paid option moving forward.



### USER SCHEMA
```
 firstName: { type: String, required: true },
    lastName: { type: String, required: true },
    username: { type: String, required: true, unique: true },
    email: { type: String, required: true, unique: true },
    password: { type: String, required: true },
    tokenUsage: { type: Number, default: 0 },
    tokenLimit: { type: Number, default: 1000 }, // Default limit for free tier
    responses: [{ type: mongoose.Schema.Types.ObjectId, ref: 'Response' }] // Reference to Response schema
```

### Resume Response Schema
```
 user: { type: mongoose.Schema.Types.ObjectId, ref: 'User', required: true }, // Reference to User
    prompt: { type: String, required: true }, // The input text the user submitted
    generatedResponse: { type: String, required: true }, // The AI-generated response
    createdAt: { type: Date, default: Date.now }, // Timestamp for when the response was generated
    updatedAt: { type: Date, default: Date.now } // Timestamp for when the response was updated
```
