## Mews - Platform Engineering Team - Interview Test

Please complete and return this technical test before attending your interview at Mews. This isn't something we would like you to spend a long time on - **we recommend no more than 3 hours**. You can give us the results in any way that makes sense to you. If sharing a GitHub repository, please make it private and grant access to the GitHub usernames at the bottom of the page.

Your response to this technical assessment will be used to start a technical discussion at your interview. We're more interested in how you approach the problem and implement your solution than in you finding a “correct” answer to the question.

### The task

Deploying a containerised workload using immutable infrastructure.

We have provided a small React app that for the purposes of this test is a representation of a ‘production ready containerised app’. *It’s just a templated react app that presents some simple data from one of our Mews APIs (not a live call) and presents some of the data retrieved to a page.*

We don’t want you to spend a long time working on this, but would like to have a simple solution that we can use as the basis of a technical discussion with you at interview. We value simplicity in readability and maintainability in a codebase, so consider this during implementation.

**An Infrastructure as Code Deployment**

We would like you to build the docker image (instructions below).

We would like you to create a set of infrastructure to support it in Azure, AWS or GCP (our cloud platform is Azure, so that would be a preference) using an infrastructure as code approach.  You can use whichever service you feel appropriate to host it, though in particular we’re looking at:

- How you approach infrastructure as code (we use Pulumi at Mews, though if your experience is in terraform that is fine)
- How you approach testing and validation of your solution and/or infrastructure
- How you set up cloud infrastructure - where you may incorporate some of: networking; security; IAM; containerised workloads

You can use any technical solution you feel is appropriate. Provide as much documentation as is required to allow us to understand any assumptions or constraints you’ve placed, and to stand up your solution.

### Please focus on a readable and maintainable solution that is easy to understand by an audience of your peers.

### Optional Improvements

Only if you have time, consider implementing one or more of these more “advanced” features:

- A load balancing solution
- Considerations for environment handling (e.g. dev/prod)
- Securing consumer access (e.g. https, egress control)

If you have any questions then please don’t hesitate in reaching out to the talent team at Mews who can forward your questions to the team and get back to you ASAP

Good luck!

Platform Engineering @ Mews 🙂


## Build Instructions

A simple `create-react-app` front end, which presents some JSON data (originating from a Mews API).  The generated docker image is used as the basis for a technical test for platform team candidates.

### Working with the repository locally

Standard `npm` and `docker` commands will do the trick - nothing complex:

| Command                                         | Outcome                                                                |
|-------------------------------------------------|------------------------------------------------------------------------|
| `npm install`                                   | Setup the initial dependencies - run once                              |
| `npm start`                                     | Start the code locally in debug build                                  |
| `npm run build`                                 | If you want to create a production build (not necessary for this test) |
| `docker build -t mews:platform-test .`          | Build the docker container                                             |
| `docker run -d -p 8080:3000 mews:platform-test` | Run the container, surfacing on http://localhost:8080/                 |

### Github Usernames

- @[terrybrown](https://github.com/terrybrown)
- @[philjhale](https://github.com/philjhale)

Though please contact anyone in the product/infrastructure team if you need anything.
