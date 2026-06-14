# RNME Mobile Automation Testing

## Application Setup

I used the pre-built APK provided in the repository (Option A) to test the application as a black-box Android application.

The APK was installed on an Android Emulator using:

adb install rnme/rnme.apk <br>
No source code or environment configuration is required


---

## Overview

This project contains UI automation tests for the RNME (Movie Explorer) Android application using Maestro.

### Covered Scenarios

Positive Scenarios

Login with valid credentials<br>
Search Movie<br>
View Movie Details<br>
Add to Favorites<br>
Remove from Favorites<br>
Watch Trailer<br>
Logout<br>
Theme Change (Light/Dark Mode)

Negative Scenarios<br>
Login with Invalid credentials<br>
Validation error message on login<br>
Session management <br>
Verify user session persists after navigation<br>
Vefiy logged in user remains logged in until logout<br>

---

## Framework

* Tool: Maestro
* Platform: Android
* Device: Pixel 8 Emulator (Android 14)
* Language: YAML

---
## Project Structure

maestro/<br>
login.yaml<br>
logout.yaml<br>
invalid-login.yaml<br>
search-movie.yaml<br>
search-no-result.yaml<br>
movie-detail.yaml<br>
favorites.yaml<br>
remove-favorite.yaml<br>
session.yaml<br>
offline.yaml<br>
offline-logged-in.yaml<br>
empty-credentials.yaml<br>
profile.yaml<br>


---

## Test Credentials

**Email:** [test@rnme.com](mailto:test@rnme.com)

**Password:** Test123$$

---

## Run Tests

Run a single test:

```bash
maestro test maestro/login.yaml
```

Run all tests:

```bash
maestro test maestro/
```

---

## Preconditions

* Android emulator is running
* RNME APK is installed
* Internet connection is available
* Test account remains active

---
## Use of AI Tools

ChatGPT was used to assist with test planning, coverage analysis, and documentation refinement. <br>
The automation scripts were implemented using Maestro Studio and executed on an Android emulator. Key functionalities were additionally verified through manual testing on a physical device.

---

## Manual Testing
All test were performed manually as well while working on automation script.
