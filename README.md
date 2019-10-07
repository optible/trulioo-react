# trulioo-react  &middot; [![CircleCI](https://circleci.com/gh/Trulioo/trulioo-react.svg?style=svg)](https://circleci.com/gh/Trulioo/trulioo-react) [![GitHub license](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](https://github.com/Trulioo/trulioo-react/blob/master/LICENSE) [![code style: eslint](https://badgen.net/badge/style/airbnb?icon=airbnb)](https://github.com/airbnb/javascript) [![npm version](https://img.shields.io/npm/v/trulioo-react.svg?style=flat-square)](https://www.npmjs.com/package/trulioo-react) [![npm downloads](https://img.shields.io/npm/dy/trulioo-react.svg?style=flat-square)](https://www.npmjs.com/package/trulioo-react) [![install size](https://packagephobia.now.sh/badge?p=trulioo-react)](https://packagephobia.now.sh/result?p=trulioo-react)  [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-green.svg)](https://github.com/Trulioo/trulioo-react/pulls) [![Try on RunKit](https://badge.runkitcdn.com/trulioo-react.svg)](https://npm.runkit.com/trulioo-react) [![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FTrulioo%2Ftrulioo-react.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2FTrulioo%2Ftrulioo-react?ref=badge_shield) [![dependencies Status](https://david-dm.org/trulioo/trulioo-react/status.svg)](https://david-dm.org/trulioo/trulioo-react) [![devDependencies Status](https://david-dm.org/trulioo/trulioo-react/dev-status.svg)](https://david-dm.org/trulioo/trulioo-react?type=dev) [![peerDependencies Status](https://david-dm.org/trulioo/trulioo-react/peer-status.svg)](https://david-dm.org/trulioo/trulioo-react?type=peer) [![Known Vulnerabilities](https://snyk.io//test/github/Trulioo/trulioo-react/badge.svg?targetFile=package.json)](https://snyk.io//test/github/Trulioo/trulioo-react?targetFile=package.json) 

## Install

`npm install trulioo-react`

## Description

⚡**Trulioo EmbedID**⚡ provides instant identity verification utilizing Trulioo's API. Get your API key from [Trulioo's Developers Portal](https://gateway-admin.trulioo.com).

## Use

```
import { EmbedID } from 'trulioo-react';

const handleResponse = (e) => {
    // handle verification submission result here ...
}

<EmbedID url='SERVER_URL' handleResponse={handleResponse} />
```

## Customize your fields

### Example of custom fields on base level:

```
const simpleExample = {
  field1: {
    title: 'What is your name?',
    type: 'string',
  },
  field2: {
    title: 'What is your age?',
    type: 'number',
  },
  field3: {
    title: 'What is your favourite color?',
    type: 'string',
    enum: ['red', 'yellow', 'blue'],
  },
};
```

### Example of custom fields section with **required** fields:

```
const sectionExample = {
  CustomFieldObj: {
    title: 'Custom Fields',
    type: 'object',
    required: ['name', 'age'],
    properties: {
      name: {
        title: 'What is your name?',
        type: 'string',
      },
      age: {
        title: 'What is your age?',
        type: 'number',
      },
      color: {
        title: 'What is your favourite color?',
        type: 'string',
        enum: ['red', 'yellow', 'blue'],
      },
    },
  },
};
```
Render `<EmbedID/>` :
```
render(
  <EmbedID
    url="http://localhost:3111"
    handleResponse={handleResponse}
    customFields={sectionExample}
    handleSubmit={handleSubmit}
  />,
  document.getElementById('root'),
);
```

## Add Bootstrap CSS for better looks 💇🏼

`<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">`

# Best Practice

Trulioo EmbedID passes user input data to your server. When developing systems that consume internet exposed fields for the purpose of data collection, ensure you take all necessary precautions to protect your system from from denial of service attacks, exploits or security vulnerabilities. Please refer to the [Legal disclaimer](https://developer.trulioo.com/docs/legal) on the Trulioo Developer Portal.

## Learn More <a href="https://twitter.com/intent/follow?screen_name=trulioo"><img align="right" src="https://img.shields.io/twitter/follow/trulioo.svg?style=social&label=Follow%20@trulioo" alt="Follow on Twitter"></a>

Trulioo is a global identity verification company that provides secure access to reliable and independent data sources to instantly verify individuals and business entities online. Hundreds of organizations across the world use GlobalGateway, Trulioo’s RESTful API used to verify five billion people and 250 million businesses across 195 countries. In addition to helping organizations meet compliance requirements, GlobalGateway also streamlines the customer onboarding process, mitigates risk, and performs the first layer of defense against fraud. Learn more about [Trulioo](https://www.trulioo.com/).

## License

Apache 2

[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FTrulioo%2Ftrulioo-react.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FTrulioo%2Ftrulioo-react?ref=badge_large)
