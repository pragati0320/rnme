1. Test Structure

The test suite is organized into separate, independent YAML files for each user flow (login, search, favorites, offline, etc.). This makes it easy to scale, maintain, and add new tests without affecting existing ones. Each test can run independently.

2. Element Strategy

I used stable selectors like visible text and consistent UI elements using maestro studio. This helps the tests survive minor UI changes.

3. Test Prioritization

I focused first on critical user experiences:

Login and session handling
Movie search and discovery
Invalid login
Favorites feature
remove-favorites
Offline behavior
and theme behavior

This ensures the core app value is tested first, followed by edge cases.

4. Usability

The suite is designed so anyone can run it easily. With a simple setup (Maestro + emulator + APK), tests can be executed in under 15-30 minutes without extra member's effort.

5. Overall Focus

The goal was to prioritize real user flows, keep tests stable, and build a clean structure that can scale as the application grows.
