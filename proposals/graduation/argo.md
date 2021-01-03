# Argo Graduation Proposal

Since joining the CNCF in April 2020 as an incubation-level project, the Argo Project has made great progress in growing the community of contributors and usrs including the addition of Red Hat along-side BlackRock as a partner in governing and running the project. On behalf of the Argo Project team, we believe that Argo is ready for graduation.

## Description

The Argo Project is a set of Kubernetes-native tools for deploying and running jobs and applications on Kubernetes. All the Argo tools are implemented as controllers and custom resources. These tools can be used independently but are even more powerful when used together. As a CNCF graduated project, all top level projects must meet graduation maturity requirements.

**Argo Workflows** enables creation of complex parallel workflows as Kubernetes resources and is used in many different use cases from CI/CD pipelines to DAG-based ML training workflows. It is the workflow engine behind the open source Kubeflow Pipelines.

**Argo Events** provides declarative management of event-based dependencies and triggers for Kubernetes resources based on various event sources. A common use of Argo Events is to trigger Argo Workflows and to generate events for long-lived services deployed using Argo CD.

**Argo CD** supports declarative GitOps-based deployment of any Kubernetes resource, including Argo Events, services and deployments across multiple k8s clusters.

**Argo Rollouts** provides declarative progressive delivery of application resources using deployment strategies such as blue/green and canary for Kubernetes.

Each of these tools is built to be Kubernetes native and are implemented as controllers and Custom Resources.  These tools can be used independently, but there is great benefit in using them together to create complex applications. Argo Events, for example, can kick off Argo Workflows which can generate and queue additional Argo Events which are processed by long-lived services deployed using Argo CD that use Argo Rollouts to control the deployment process.

Different Argo tools have been presented at Kubernetes community meetings and KubeCon conferences.

* KubeCon: https://www.youtube.com/watch?v=yeVkTTO9nOA
* KubeCon: https://www.youtube.com/watch?v=OdzH82VpMwI&feature=youtu.be
* KubeCon: https://www.youtube.com/watch?v=ZK510prml8o
* KubeCon: https://www.youtube.com/watch?v=VXrGp5er1ZE&t=0s&index=135&list=PLj6h78yzYM2PZf9eA7bhWnIh_mK1vyOfU
* Sig Apps: https://www.youtube.com/watch?v=aWDIQMbp1cc
* K8s Community Meeting: https://www.youtube.com/watch?v=LRDoKOLOlf8
* K8s Community Meeting: https://www.youtube.com/watch?v=GeB50xG-gmc&feature=youtu.be&t=81
* TGIK by Joe Bedahttps://www.youtube.com/watch?v=M_rxPPLG8pU&start=859
xxx nned to update

## Statement on alignment with CNCF mission

The Argo project is well-aligned with the CNCF’s mission to make cloud native computing ubiquitous. We are completely aligned to "empower organizations to build and run scalable applications" including the adoption of Kubernetes and declarative APIs. All the Argo tools are implemented as controllers and custom resources. They use/integrate with other CNCF projects like gRPC, Prometheus, NATS, Helm..

#### Sponsors / Advisors from TOC
* TBD

#### Project name
* Argo

#### Unique identifier
* argo, argoproj

#### Preferred maturity level
* graduated

#### The Argo Community is looking for the following by becoming a CNCF graduated project:

* Promote public visibility to add value to the CNCF mission.
* Foster collaborative development to further the overall CNCF mission.
* Closer integration and collaboration with other CNCF projects.
* Reassurance for the Argo Community that the project will be a permanent part of the CNCF ecosystem well into the future.

#### License
* Apache License 2.0

#### Source control repositories

* https://github.com/argoproj/argo
* https://github.com/argoproj/argo-events
* https://github.com/argoproj/argo-cd
* https://github.com/argoproj/argo-rollouts

#### External Dependencies

Argo depends on the following external software components:

* Kubernetes (Apache Software License 2.0)
* Dex (Apache Software License 2.0)
* Redis (BSD)
* React (MIT)
* GRPC (Apache Software License 2.0)
* Golang (Apache Software License 2.0)

#### Initial Committers (leads)

* Alex Collins (Intuit)
* Alexander Matyushentsev (Intuit)
* Jann Fischer (Red Hat)
* Jesse Suen (Intuit)
* Jonathan West (Red Hat)
* Vaibhav Page (BlackRock)

#### Infrastructure requests (CI / CNCF Cluster)

* None

#### Communication Channels

* Slack: https://argoproj.slack.com/
  * To join: https://join.slack.com/t/argoproj/shared_invite/enQtMzExODU3MzIyNjYzLTA5MTFjNjI0Nzg3NzNiMDZiNmRiODM4Y2M1NWQxOGYzMzZkNTc1YWVkYTZkNzdlNmYyZjMxNWI3NjY2MDc1MzI
* Mailing List: https://groups.google.com/forum/#!forum/argoproj 
* Community Meeting Doc: https://docs.google.com/document/d/16aWGQ1Te5IRptFuAIFtg3rONRQqHC1Z3X9rdDHYhYfE 

#### Issue tracker

* https://github.com/argoproj/argo/issues 
* https://github.com/argoproj/argo-events/issues
* https://github.com/argoproj/argo-cd/issues
* https://github.com/argoproj/argo-rollouts/issues

#### Website
* https://argoproj.github.io/ 

#### Release methodology and mechanics

* Major feature release about four times per year with additional minor/patch releases
* Some users also run HEAD of master particularly for trying and testing release candidates.

#### Social media accounts

* Twitter: @argoproj

#### Existing sponsorship
* CNCF, Intuit, Red Hat and Blackrock are the manin sponsors of Argo

#### Community size

Argoproj

* 7100 stars
* 1470 forks
* 540 contributors

#### Production usage

Argo is known to be actively used in production by the following organizations:

* https://github.com/argoproj/argo/blob/master/USERS.md
* https://github.com/argoproj/argo-cd/blob/master/USERS.md

## Graduation State Criteria

#### Have committers from at least two organizations

The Argo steering committee consists of members from Intuit, Red Hat and Blackrock. Committers are represented from a much broader set of organizations.

#### Have achieved and maintained a [Core Infrastructure Initiative Best Practices Badge](https://bestpractices.coreinfrastructure.org/)

xxx

#### Have completed an independent and third party security audit with results published of similar scope and quality as [this example](https://github.com/envoyproxy/envoy#security-audit) which includes all critical vulnerabilities and all critical vulnerabilities need to be addressed before graduation

Currently in progress with Trail of Bits as the 3rd party auditor.

#### Explicitly define a project governance and committer process

* https://github.com/argoproj/argoproj/blob/master/community/GOVERNANCE.md
* https://github.com/argoproj/argoproj/blob/master/community/membership.md

xxx

#### Have a public list of project adopters for at least the primary repo (e.g., ADOPTERS.md or logos on the project website)

* https://github.com/argoproj/argo/blob/master/OWNERS
* https://github.com/argoproj/argo-events/blob/master/OWNERS
* https://github.com/argoproj/argo-cd/blob/master/OWNERS
* https://github.com/argoproj/argo-rollouts/blob/master/OWNERS

