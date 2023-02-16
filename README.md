# Android and iOS Driver App-Git Release Process Flow



## Pre-release Git Flow (during TestFlight-only for iOS and Firebase-only for Android)

1. All new feature work and bug fixes should be based off of develop and submitted back with a pull request.
2. Once necessary enhancements and bug fixes have been implemented, the tip of develop should be merged into the existing release branch with a pull request. This will bring the latest changes up into the release pipeline to be built and deployed to TestFlight.
3. The release workflow should then be triggered via Runway to create a new build of the application for deployment in TestFlight.

[![](https://mermaid.ink/img/pako:eNqtk09rhDAQxb9KCIiXdXd1WwreWoTSQ3vpNZdZM2qoSSTG0iJ-92Zt3equ9g8sXsbhvd-8IUxLU82RxtTzWqGEjUlL_FzYewNV4fd_EoS6M6DS4gkkup7P8RVLXfldRzrPY2rQM0VIqqUU9lDtew8xWCLUuIm20W4drrdjUV8XmL7oxpIv6sjqOuEmSW4fgjDaBRmCbQyG0ylzdokmx0X3woCrQRKdYpck3xn-mWbMmaaJBsl1UGuJwb7JM_F2Sv5BNZfpb-mWoBPj3GMeCQPyfAxTMyveBKC0LdD8tuWs8AKLnnMvsSshB870oyvqnO6QuLu0ttdQN1gio7ErOWbQlJZRpjonhcbq53eV0jiDssYVbSoOFhMBuQF57CIXVpvHz_Ptr7j7AFkpShM?type=png)](https://mermaid.live/edit#pako:eNqtk09rhDAQxb9KCIiXdXd1WwreWoTSQ3vpNZdZM2qoSSTG0iJ-92Zt3equ9g8sXsbhvd-8IUxLU82RxtTzWqGEjUlL_FzYewNV4fd_EoS6M6DS4gkkup7P8RVLXfldRzrPY2rQM0VIqqUU9lDtew8xWCLUuIm20W4drrdjUV8XmL7oxpIv6sjqOuEmSW4fgjDaBRmCbQyG0ylzdokmx0X3woCrQRKdYpck3xn-mWbMmaaJBsl1UGuJwb7JM_F2Sv5BNZfpb-mWoBPj3GMeCQPyfAxTMyveBKC0LdD8tuWs8AKLnnMvsSshB870oyvqnO6QuLu0ttdQN1gio7ErOWbQlJZRpjonhcbq53eV0jiDssYVbSoOFhMBuQF57CIXVpvHz_Ptr7j7AFkpShM)

## Releasing and Git Flow (General Availability via App Store and Google Play Store)

1. All new feature work should be based off of develop and submitted back with a pull request.
2. At the end of a development cycle, a release branch, such as release/2023.1.0, should be created, and the release workflow should be triggered. These steps should be done using Runway.
The marketing version on develop can now be incremented to reflect that any net-new functionality merged from that point forward will be included as part of a new App Store release.
3. When bugs are discovered in the release candidate, bug fixes should be made in branches based from the release branch and submitted back to the release branch with a pull request to that branch.
4. Once all bugs have been resolved, the release workflow should be triggered again using Runway. This will cause a new build of the projected release version to be generated so that the testing cycle can repeat.
5. After the version has been approved for release by the QA team and App Review and it has shipped to customers in the App Store, the head commit of the release branch should be tagged with the version of the release, and any changes made to that release branch since it divered from develop should be submitted back into develop with a pull request (this will normally just be some small bugfixes). This can be automated by Runway.

[![](https://mermaid.ink/img/pako:eNqVk8FugzAMhl8lioS4lLbQ7cJtE9K0w3bZNReXGIhGEhSSaRPi3ZeBStsNqKYckli__dmO09Fcc6QpDYJOKGFT0pGwFPbJQFOFw02CUI8GVF69gkRvCzl-YK2bsO9JHwRMnfRM5VpKYc87U8fBkxisEVrcJfvksI23-wtphfm7dnZGMnl7YLzLsofnKE4OUaslRkdXFuLzwn1Ncxsl0ZS4FmM2l7sIlLYVmvV0ZmS_-vSvzP6Gu-b-vM0MYnqSFdi5xuREu4-0wkhqM_TimrQsmmA3gFN1i6Hmahu9lmdqXHRDvdCPL_fz3TFFCKO-bRIZTf2RYwGutowy1XspOKvfvlROU2scbqhrOFjMBJQGJE0LqFtvRS6sNi_jnxm-Tv8Nbzchpw?type=png)](https://mermaid.live/edit#pako:eNqVk8FugzAMhl8lioS4lLbQ7cJtE9K0w3bZNReXGIhGEhSSaRPi3ZeBStsNqKYckli__dmO09Fcc6QpDYJOKGFT0pGwFPbJQFOFw02CUI8GVF69gkRvCzl-YK2bsO9JHwRMnfRM5VpKYc87U8fBkxisEVrcJfvksI23-wtphfm7dnZGMnl7YLzLsofnKE4OUaslRkdXFuLzwn1Ncxsl0ZS4FmM2l7sIlLYVmvV0ZmS_-vSvzP6Gu-b-vM0MYnqSFdi5xuREu4-0wkhqM_TimrQsmmA3gFN1i6Hmahu9lmdqXHRDvdCPL_fz3TFFCKO-bRIZTf2RYwGutowy1XspOKvfvlROU2scbqhrOFjMBJQGJE0LqFtvRS6sNi_jnxm-Tv8Nbzchpw)
