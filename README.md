## Mews - Platform Engineering Team - Interview Test

Please complete and return this technical test before attending your interview at Mews. This isn't something we would like you to spend a long time on - **we recommend no more than 3 hours**. You can give us the results in any way that makes sense to you. If sharing a GitHub repository, please make it private and grant access to the GitHub usernames at the bottom of the page.

Your response to this technical assessment will be used to start a technical discussion at your interview. We're more interested in how you approach the problem and implement your solution than in you finding a “correct” answer to the question.

## The task - Deploying a containerised workload using infrastructure as code

Create infrastructure to host a containerised web app in the cloud using an infrastructure as code. You can use whichever cloud service you feel appropriate to host it. Our cloud platform is Azure, so that would be a preference, but AWS or GCP is fine. The web app has been provided. See build instructions below.

Requirements:
* Host containerised web app provided using infrastructure as code.
* Document how to build and execute your solution.
* Explain your thinking, either in the readme or in comments. This is really important so the reviewers clearly understand your approach and the decisions you made.
* Create a readable and maintainable solution that is easy to understand by an audience of your peers.


If you have time, consider implementing some of these features:
* A load balancing solution
* Considerations for environment handling (e.g. dev/prod)
* Securing consumer access (e.g. https, egress control)
* CICD

If you have any questions then please don’t hesitate in reaching out to the talent team at Mews.

Good luck!

Platform Engineering @ Mews 🙂


## Build instructions
We have provided a React app that represents a production ready containerised workload. It gets some data from a Mews API (not a live call) and presents the data to a web page.


### Working with the repository locally

| Command                                         | Outcome                                                                |
|-------------------------------------------------|------------------------------------------------------------------------|
| `npm install`                                   | Setup the initial dependencies - run once                              |
| `npm start`                                     | Start the code locally in debug build                                  |
| `npm run build`                                 | If you want to create a production build (not necessary for this test) |
| `docker build -t mews:platform-test .`          | Build the docker container                                             |
| `docker run -d -p 8080:3000 mews:platform-test` | Run the container, surfacing on http://localhost:8080/                 |

### Github usernames

- @[terrybrown](https://github.com/terrybrown)
- @[philjhale](https://github.com/philjhale)

