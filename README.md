# TestRep-

Releasing and Git Flow (General Availability via App Store)

All new feature work should be based off of develop and submitted back with a pull request.
At the end of a development cycle, a release branch, such as release/2023.1.0, should be created, and the release workflow should be triggered. These steps should be done using Runway.
The marketing version on develop can now be incremented to reflect that any net-new functionality merged from that point forward will be included as part of a new App Store release.
When bugs are discovered in the release candidate, bug fixes should be made in branches based from the release branch and submitted back to the release branch with a pull request to that branch.
Once all bugs have been resolved, the release workflow should be triggered again using Runway. This will cause a new build of the projected release version to be generated so that the testing cycle can repeat.
After the version has been approved for release by the QA team and App Review and it has shipped to customers in the App Store, the head commit of the release branch should be tagged with the version of the release, and any changes made to that release branch since it divered from develop should be submitted back into develop with a pull request (this will normally just be some small bugfixes). This can be automated by Runway.
