deep-microservices-waf
======================

[![Build Status](https://travis-ci.org/MitocGroup/deep-microservices-waf.svg?branch=master)](https://travis-ci.org/MitocGroup/deep-microservices-waf)
[![Codacy Badge](https://api.codacy.com/project/badge/coverage/1ad2d529275e490cb61700b3c20f771a)](https://www.codacy.com/app/MitocGroup/deep-microservices-waf)

deep-microservices-waf is a microservice designed to implement cloud-native firewall for web applications
built on top of [DEEP Framework](https://github.com/MitocGroup/deep-framework). It could be used either
as a standalone application or as a dependency in other deep-microservices. This repository is open
sourced to show case how developers can build and deploy hassle-free cloud-native web applications
using microservices architecture and serverless computing.


## Getting Started

### Step 1. Pre-requisites

- [x] [Create an Amazon Web Services account](https://www.youtube.com/watch?v=WviHsoz8yHk)
- [x] [Configure AWS Command Line Interface](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html)
- [x] [Get Started - Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [x] [JDK 8 and JRE 8 Installation Start Here](https://docs.oracle.com/javase/8/docs/technotes/guides/install/install_overview.html)
- [x] [Install nvm](https://github.com/creationix/nvm#install-script) and [use node v4.3+](https://github.com/creationix/nvm#usage)
- [ ] Install DEEP CLI, also known as `deepify`:

```bash
npm install deepify -g
```

> If you want to use `deepify` on Windows, please follow the steps from
[Windows Configuration](https://github.com/MitocGroup/deep-framework/blob/master/docs/windows.md)
before running `npm install deepify -g` and make sure all `npm` and `deepify` commands are executed
inside Git Bash.

### Step 2. Install Microservice(s) Locally

```bash
deepify install github://MitocGroup/deep-microservices-waf ~/deep-microservices-waf
```

> Path parameter in all `deepify` commands is optional and if not specified, assumes current
working directory. Therefore you can skip `~/deep-microservices-waf` by executing
`mkdir ~/deep-microservices-waf && cd ~/deep-microservices-waf` before `deepify install`.

### Step 3. Run Microservice(s) in Development

```bash
deepify server ~/deep-microservices-waf -o
```

> When this step is finished, you can open in your browser the link *http://localhost:8000*
and enjoy the deep-microservices-waf running locally.

### Step 4. Deploy Microservice(s) to Production

```bash
deepify deploy ~/deep-microservices-waf
```

> Amazon CloudFront distribution takes up to 20 minutes to provision, therefore don’t worry
if it returns an HTTP error in the first couple of minutes.

### Step 5. Remove Microservice(s) from Production

```bash
deepify undeploy ~/deep-microservices-waf
```

> Amazon CloudFront distribution takes up to 20 minutes to unprovision. That's why `deepify`
command checks every 30 seconds if it's disabled and when successful, removes it from your account.


## Developer Resources

Having questions related to deep-microservices-waf?

- Ask questions: https://stackoverflow.com/questions/tagged/deep-framework
- Chat with us: https://mitocgroup.slack.com/messages/general
- Send an email: feedback@deep.mg

Interested in contributing to deep-microservices-waf?

- Contributing: https://github.com/MitocGroup/deep-microservices-waf/blob/master/CONTRIBUTING.md
- Issue tracker: https://github.com/MitocGroup/deep-microservices-waf/issues
- Releases: https://github.com/MitocGroup/deep-microservices-waf/releases
- Roadmap: https://github.com/MitocGroup/deep-microservices-waf/blob/master/ROADMAP.md

Looking for web applications that use (or are similar to) deep-microservices-waf?

- Hello World: https://hello.deep.mg | https://github.com/MitocGroup/deep-microservices-helloworld
- Todo App: https://todo.deep.mg | https://github.com/MitocGroup/deep-microservices-todomvc
- Enterprise Software Marketplace: https://www.deep.mg


## Sponsors

This repository is being sponsored by:
- [Mitoc Group](https://www.mitocgroup.com)
- [DEEP Marketplace](https://www.deep.mg)

This code can be used under MIT license:
> See [LICENSE](https://github.com/MitocGroup/deep-microservices-waf/blob/master/LICENSE) for more details.
