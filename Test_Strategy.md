# Test Strategy

## Objective

To validate the critical user experience of the RNME Android application through end-to-end mobile UI automation from a real user perspective.

## Approach

A risk-based approach was used to prioritize high-impact features. Tests were designed to be independent, maintainable, and include both positive and negative scenarios.

## Test Coverage

## Preconditions

* The provided APK is stable and representative of the application.
* Test credentials remain valid.
* Internet connectivity is available for online scenarios.
  
### Authentication

* Valid login
* Invalid login
* Authentication validation
* Logout

### Movie Discovery

* Search for a movie
* View movie details
* Search with no results

### Favorites

* Add movie to Favorites
* Remove movie from Favorites
* Watch trailer navigation

### Profile

* Access Profile
* Change application theme (Light, Dark, System)

### Session Management

* Verify user remains logged in during app usage
* Verify session persists until explicit logout

### Offline Scenarios

* Validate login behavior without internet connectivity
* Verify application behavior when an logged in user goes offline

## Test Data


| Test Scenario       | Input Data / Action                                                              | Expected Flow / Module       |
| ------------------- | -------------------------------------------------------------------------------- | ---------------------------- |
| Invalid Login       | Email: [invalid@rnme.com](mailto:invalid@rnme.com)<br>Password: WrongPassword123 | Login Authentication         |
| Movie Search        | Search Query: Batman                                                             | Movie Search                 |
| Search – No Results | Search Query: xyzabc123                                                          | Search Results (Empty State) |
| Favorites           | Movie: The Batman                                                                | Add to Favorites             |
| Offline Scenarios   | Network disabled (Android Emulator)                                              | Offline Mode Handling        |
| Theme Validation    | Light, Dark, System themes                                                       | App Theme Settings           |

## Automation Approach

* Framework: Maestro
* Platform: Android
* Device: Pixel 8 Emulator (Android 14)
* Test Format: YAML


## Reusability

The automation suite is designed to be reusable and executable by any team member with the documented prerequisites. Once the Android Emulator, Maestro, and the RNME APK are set up, the tests can be executed without additional configuration or source code changes.

## Preconditions

Maestro installed<br>
Android Studio with an Android Emulator<br>
RNME APK installed on the emulator/device<br>
ADB configured and accessible from the command line<br>
Internet connectivity for online scenarios<br>
Execution<br>

##Run an individual test:

maestro test maestro/login.yaml

Run the complete test suite:

maestro test maestro/

## Future Improvements

* Accessibility testing
* Cross-device validation
* Network recovery scenarios
* CI/CD integration and reporting
* Performance testing
