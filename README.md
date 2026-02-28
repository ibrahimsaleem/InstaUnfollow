
# Instagram Unfollower Manager by Ibrahim Saleem
This code repository contains an application designed to help users manage their Instagram unfollowers. The application includes various components for searching users, displaying search results, managing whitelisted and non-whitelisted users, unfollowing users, and displaying unfollowing logs.

# Purpose
The purpose of this code is to provide a user-friendly interface for users to track and manage their Instagram unfollowers. It allows users to search for specific users, view search results, select users for unfollowing, manage whitelisted users, and track unfollowing actions through logs. The code aims to simplify the process of managing unfollowers on Instagram and provide a seamless user experience.

# Usage Instructions
Follow these steps to use the code:

Step 1:  Log in to your Instagram account on Laptop,PC etc.

Step 2:  Open the developer console in your web browser. You can do this by right-clicking on the page and selecting "Inspect" or by pressing Ctrl+Shift+J (Windows) or ⌘+⌥+I (Mac OS).

Step 3:  Copy the code from the file named "InstaUnfollowCode".
Link - https://github.com/ibrahimsaleem/InstaUnfollow/blob/main/InstaUnfollowCode

Step 4:  Paste the code into the developer console and press Enter.

A user interface will appear with an initial screen.

Click on the "RUN" button to start scanning for users who do not follow you back.

The code will start printing the users who do not follow you back.

Once the code finishes printing the users, the results screen will be displayed. This screen will show you the list of users who do not follow you back.

If you wish to unfollow any of these users, you can select one or more users by clicking the checkbox next to each user.

Tips:
- Use **Select all filtered (all pages)** to bulk-select every user currently matching your filters/search.
- Use **Clear selection** to instantly unselect everyone.
- Use the **Selected Only** filter to show only the accounts you’ve checked (useful for reviewing before unfollowing).
- Use **Public** / **Private** filters to narrow accounts by visibility.
- Use the per-user gender selector (**? / M / F**) to manually tag accounts, then filter using **Male / Female / Unknown**.- Use **AUTO-TAG GENDER** (requires a Gemini API key) to automatically predict M/F/Unknown for all untagged accounts using AI — manual tags are never overwritten.

# Gemini AI Auto-Tag Gender
The tool integrates the **Google Gemini REST API** to automatically classify gender associations from account names in batches of 50.

### How to use
1. Get a free API key at [Google AI Studio](https://aistudio.google.com/app/apikey).
2. Run the bookmarklet and complete a scan (click **RUN**).
3. In the left sidebar, find the **GEMINI AI** section and paste your key into the password field — it is saved to `localStorage` and persists across sessions.
4. Click **AUTO-TAG GENDER** — the tool processes all untagged accounts in batches and shows live progress toasts.

### Model fallback
Requests are tried in this order (cheapest/fastest first); if a model is unavailable or blocked, the next one is used automatically:
1. `gemini-3-flash-preview`
2. `gemini-3.1-flash-image-preview`
3. `gemini-3.1-pro-preview`
4. `gemini-3-pro-image-preview`

### Privacy
- The prompt is framed as *name-linguistics classification* — no personal data beyond display name/username is sent.
- Your API key is stored only in your browser's `localStorage` under the key `iu_gemini_api_key` and is never transmitted anywhere other than directly to `generativelanguage.googleapis.com`.
Please note that this code helps you identify users who do not follow you back on Instagram. The decision to unfollow any user is at your discretion.
# Main Components
The main components in this code include:

App: The root component that orchestrates the application and renders other components.
SearchBar: A component responsible for accepting user input and triggering searches based on the entered query.
ResultsContainer: A component that displays search results and provides functionalities like selecting users for unfollowing.
UnfollowLogContainer: A component that displays the unfollowing log and allows users to filter and view past unfollowing actions.

# Functionality Overview
Unfollowing Users: The code provides an "UNFOLLOW" button that triggers an unfollow confirmation dialog. Upon confirmation, selected users are unfollowed, and the application state is updated accordingly. The unfollowing process involves updating the status, initializing the unfollowing log, and applying filter options.

Note: The unfollow log now treats non-2xx responses as failures and may show an HTTP status code (for example, 429 when you’re temporarily rate-limited).

Searching Users: The code includes a search bar that dynamically updates the search term in the application state as the user types. Search results are rendered in the ResultsContainer component, with filtering options applied based on the search term.

Copying User List: Clicking the "COPY LIST" button generates a list of usernames from the current search results, whitelisted users, and filter options. The generated list is copied to the clipboard for the user's convenience. The button is only functional during the "scanning" status.

Pagination: The code includes pagination functionality with previous and next buttons. Clicking these buttons updates the application state with the new page number, triggering a re-render of the search results component to display the corresponding page of results.

User Selection: Users in the search results can be selected or deselected by clicking on their respective checkboxes. The code updates the application state to reflect the selected users and modifies the checkbox's checked status accordingly.

Filtering Unfollowing Log: The UnfollowLogContainer component provides options to filter the unfollowing log based on success or failure status. Changing the filter options updates the application state and triggers a re-render of the log to display the filtered results.

# Developed By
This application was developed by Ibrahim Saleem. You can follow Ibrahim Saleem on Instagram @ibrahimmmm._ and connect on LinkedIn at linkedin.com/in/ibrahimsaleem91.

