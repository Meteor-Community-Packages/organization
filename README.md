# Meteor Community Packages

This organization unites packages that are important to the [Meteor](https://www.meteor.com) community to gurantee their long term maintenance and advance community initiatives.

This repository serves to resolve governance issues and establish shared practices and patterns.

## Associated organizations/projects

* [Meteor testing](https://github.com/meteortesting) - Focuses on testing in Meteor
* [Blaze](https://github.com/meteor/blaze) - Maintains the original view layer of Meteor

## Community Resources

* [Awesome Meteor](https://github.com/urigo/awesome-meteor) - A curated, community driven list of awesome Meteor packages, libraries, resources and shiny things.

* [Awesome Blaze](https://github.com/arggh/awesome-blaze) - A curated list of awesome things related to Blaze.

## Organization

### Teams

Each repository should have at least one corresponding [GitHub team](https://github.com/orgs/Meteor-Community-Packages/teams), containing all maintainers of the repository. It is suggested that team's name match repository's name, unless team is used for multiple repositories.

Each repository should also have a corresponding Meteor organization, you can [create it here](https://www.meteor.com/account-settings) under `Organizations` tab. After that you can add Meteor users to it, using web interface, or:

```bash
meteor admin members <organization name> --add <username>
```

Add that Meteor organization then as maintainer of the corresponding Meteor package:

```bash
meteor admin maintainers <package name> --add <organization name>
```

There is also a special Meteor organization `communitypackages` which consist of trusted community members who have permissions to publish any community package. This is a fallback measure to assure no package ends up without a maintainer. Make sure you add it as maintainer as well.

### Organization on NPM

We have an [NPM organization](https://www.npmjs.com/org/meteor-community), to maintain Meteor packages that live on  [NPM](https://www.npmjs.com/). The organization is same as on Atmosphere with the difference that instead of multiple organizations handling specific package(s), NPM uses teams under the organization for that purpose.

For adding packages under our organization see [section bellow](#npm) about this topic.

## Communication

There are three main routes of communication, each serving a separate and distinct purpose.

### Issues

Communication relating to individual repositories should be kept within the issue tracker of that particular repo.

### Project Boards

Organization level project boards should be used to communicate areas that need work outside of the scope of any individual repo. For example, things we can do to help progress Meteor Core.

You can find the project boards [here](https://github.com/orgs/Meteor-Community-Packages/projects).

### Slack

Slack should be used for more general communication of ideas and discussion about the progression about the community and as a general community meeting space.

Much of the happenings of our GitHub repositories are published to specific channels in Slack as well. This can allow you to subscribe to more real time updates about specific issues and efforts in a fine grained way.

Channels that have specific GitHub integration are as follows:

* #packages - Updates about the packages that are maintained by the community.

* #organization - Updates about the structure of the community organization.

* #website - Updates specific to the groups website

* #packoshpere - Updates specific to the Packosphere. The community alternative to Atmosphere.

Please feel free to join us in the Slack workspace by clicking this [invite link](https://join.slack.com/t/meteor-community/shared_invite/enQtODA0NTU2Nzk5MTA3LWY5NGMxMWRjZDgzYWMyMTEyYTQ3MTcwZmU2YjM5MTY3MjJkZjQ0NWRjOGZlYmIxZjFlYTA5Mjg4OTk3ODRiOTc).

## Package maintenance

## Process of adding a package

(Not yet complete.)

* (... Come to a decision of existing repository being adopted or if it is being forked. ...)
* Move existing repository to the organization **or** create a fork into the organization.
* If you obtained permission by original Meteor package maintainer to maintain it, continue to use that Meteor package name,
  otherwise decide on a new package name. You can use `communitypackages` Meteor organization.
* Create a [GitHub team](https://github.com/orgs/Meteor-Community-Packages/teams) **or** reuse an existing one.
  It should contain all maintainers of the repository, so configure it to have admin permissions on the repository.
* Create a Meteor organization for maintainers of the corresponding Meteor package, you can
  [create it here](https://www.meteor.com/account-settings) under `Organizations` tab.
  Or reuse an existing one.

* Add that Meteor organization then as maintainer of the corresponding Meteor package:

  ```bash
  meteor admin maintainers <package name> --add <organization name>
  ```

* Add `communitypackages` Meteor organization as a maintainer of the new Meteor package:

  ```bash
  meteor admin maintainers <package name> --add communitypackages`
  ```

* If repository has been moved, do not forget to update the URL to the repository in `package.js`.

### NPM

For transferring packages that live on [NPM](https://www.npmjs.com/), please contact [@StorytellerCZ](https://github.com/StorytellerCZ), who will add you to the [NPM organization](https://www.npmjs.com/org/meteor-community) and create a team for you package. After that you will be able to add the team as a maintainer for the package.
