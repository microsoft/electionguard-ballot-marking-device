![Microsoft Defending Democracy Program: ElectionGuard](images/electionguard-banner.svg)

# 🗳 ElectionGuard Ballot Marking Device 
[![license](https://img.shields.io/github/license/microsoft/electionguard-admin-device)](License)

The ElectionGuard Reference Ballot Marking Device (BMD) is a fully functional
implementation of a BMD built in ReactJS. It uses the
[Gamepad API](https://developer.mozilla.org/en-US/docs/Web/API/Gamepad_API) to
support a physically-connected
[Xbox Adaptive Controller](https://www.xbox.com/en-US/xbox-one/accessories/controllers/xbox-adaptive-controller)
for navigating ballots with the A/B buttons, D-pad, or other devices plugged
into the XAC's connection ports.

The BMD was designed under the supervision of the
[Center for Civic Design](https://civicdesign.org) as an update of the
[Anywhere Ballot](https://civicdesign.org/projects/anywhere-ballot/) and built
by the team at [VotingWorks](https://voting.works). It runs locally in a web
browser (Chrome or Edge Beta). A sample set of ballots (in json format) is
available in both the /public/data/ and /src/data directories that showcases a
variety of contests and referenda use cases.

By default, when a ballot is printed, the BMD also generates a static tracking
ID. End-to-end verifiable elections create tracking IDs generated when the
ballot is encrypted. It's used by voters to check that their vote was included
in the final tally when all the artifacts of an end-to-end verifiable election
are published. When you have built working encryption capability (using the
[C Implementation](https://github.com/microsoft/ElectionGuard-SDK-C-Implementation)),
the election.json configuration file can be modified to retrieve the tracking ID
by updating
[this code block](https://github.com/microsoft/ElectionGuard-SDK-Ballot-Marking-Device-Reference-Implementation/blob/edee95d90fc5a4ce17a6cd9d537f9200b189e05d/src/endToEnd.ts#L14).

## Install and Run App Locally

This assumes you have `git` and `yarn` installed.

1. Clone the repo:

   ```
   git clone git@github.com:microsoft/ElectionGuard-SDK-Ballot-Marking-Device-Reference-Implementation.git
   ```

1. Navigate to the top level of the cloned directory

   ```
   cd ElectionGuard-SDK-Ballot-Marking-Device-Reference-Implementation
   ```

1. Install dependencies:

   ```
   yarn install
   ```

1. Run the app in your local browser:

   ```
   yarn start
   ```

## Local Development Scripts

- `yarn install` - Install the dependencies.
- `yarn start` - Run the app locally.
- `yarn test`- Run tests in interactive mode.
- `yarn test:coverage` - Run all tests and update test coverage report.

See `package.json` for all available scripts.

## Technical Implementation

This project was bootstrapped with
[Create React App](https://github.com/facebook/create-react-app) for TypeScript.
It uses [Styled Components](https://www.styled-components.com/docs/) for styles
(and some `css` files too). [ESLint](https://eslint.org/) is configured to lint
Javascript and TypeScript files, and format code using
[Prettier](https://prettier.io/). [stylelint](https://stylelint.io/) is used to
lint modern css. [Jest](https://jestjs.io/),
[dom-testing-library](https://testing-library.com),
[react-testing-library](https://github.com/kentcdodds/react-testing-library),
and [Cypress](https://www.cypress.io/) are used to test components and
end-to-end user flows.

## Contributing

Help defend democracy and [contribute to the project](CONTRIBUTING).