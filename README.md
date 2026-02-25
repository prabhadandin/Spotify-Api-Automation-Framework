 Spotify API Automation & Testing Framework 
API testing suite designed for the **Spotify Web API**.
This framework demonstrates industry-standard automation practices, including dynamic variable passing, secure environment management, and tiered-access validation.

Key Features
End-to-End Automation: Automatically captures and persists `user_id` to drive playlist creation and item management without manual input.
Advanced JavaScript Testing: Post-response scripts validate status codes (200/201), JSON schema integrity, and data consistency.
Secure Environment Architecture: Zero hardcoded credentials. All secrets (`client_id`, `client_secret`) are handled via parameterized variables.
OAuth 2.0 Integration**: Uses a single-collection approach to manage multiple scopes and authentication tokens efficiently.

 API Tier & Scope 
- Free Plan Compatibility: This suite is optimized for **Spotify Free** users. 
- trategic Scopes: Uses a unified scope string (e.g., `playlist-modify-public`) to ensure full CRUD functionality within the limitations of a standard account.
- Excluded Features: Playback controls (Premium-only) were intentionally excluded to maintain a 100% test pass rate across all account types.

 Setup & Configuration
1. Import Files
Import both the `spotify_collection.json` and the `spotifyenv.json` into Postman.
2. Configure Environment
Populate the following variables in your **Postman Environment** (Current Value column):
- 'baseurl'  : https://api.spotify.com/v1
- `client_id`: Your Spotify App Client ID.
- `client_secret`: Your Spotify App Client Secret.
- `access_token`: Generated via the Collection's Authorization tab.
3. Execution
Run the collection using the **Postman Collection Runner** or via **Newman** for CLI execution.
Test Scenarios
- GET Profile: Validates account access and captures the dynamic `user_id`.
- POST Create Playlist: Validates successful creation (201 Created) and confirms the response metadata matches the request payload.
- Dynamic Persistence: passing data (IDs) between disparate API requests.
- Resilience & Negative Testing (Shift-Left Approach)identifying potential
 failures early in the development lifecycle—this suite includes intentional negative test cases:
 Invalid PlaylistID: Validates that the system gracefully handles malformed
 or non-existent IDs by confirming a `404 Not Found` status and verifying the presence of a descriptive error message.
 Project Summary
This project was developed to maintain and showcase technical proficiency 
in **API Lifecycle Management** and **Automated Quality Assurance**. 
It reflects a deep understanding of modern authentication protocols (OAuth 2.0)
 and the ability to build robust, secure, and well-documented testing frameworks.
