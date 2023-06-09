
# Instagram Unfollower Manager by Ibrahim Saleem
This code repository contains an application designed to help users manage their Instagram unfollowers. The application includes various components for searching users, displaying search results, managing whitelisted and non-whitelisted users, unfollowing users, and displaying unfollowing logs.

# Purpose
The purpose of this code is to provide a user-friendly interface for users to track and manage their Instagram unfollowers. It allows users to search for specific users, view search results, select users for unfollowing, manage whitelisted users, and track unfollowing actions through logs. The code aims to simplify the process of managing unfollowers on Instagram and provide a seamless user experience.

# Main Components
The main components in this code include:

App: The root component that orchestrates the application and renders other components.
SearchBar: A component responsible for accepting user input and triggering searches based on the entered query.
ResultsContainer: A component that displays search results and provides functionalities like selecting users for unfollowing.
UnfollowLogContainer: A component that displays the unfollowing log and allows users to filter and view past unfollowing actions.

# Functionality Overview
Unfollowing Users: The code provides an "UNFOLLOW" button that triggers an unfollow confirmation dialog. Upon confirmation, selected users are unfollowed, and the application state is updated accordingly. The unfollowing process involves updating the status, initializing the unfollowing log, and applying filter options.

Searching Users: The code includes a search bar that dynamically updates the search term in the application state as the user types. Search results are rendered in the ResultsContainer component, with filtering options applied based on the search term.

Copying User List: Clicking the "COPY LIST" button generates a list of usernames from the current search results, whitelisted users, and filter options. The generated list is copied to the clipboard for the user's convenience. The button is only functional during the "scanning" status.

Pagination: The code includes pagination functionality with previous and next buttons. Clicking these buttons updates the application state with the new page number, triggering a re-render of the search results component to display the corresponding page of results.

User Selection: Users in the search results can be selected or deselected by clicking on their respective checkboxes. The code updates the application state to reflect the selected users and modifies the checkbox's checked status accordingly.

Filtering Unfollowing Log: The UnfollowLogContainer component provides options to filter the unfollowing log based on success or failure status. Changing the filter options updates the application state and triggers a re-render of the log to display the filtered results.

# Developed By
This application was developed by Ibrahim Saleem. You can follow Ibrahim Saleem on Instagram @ibrahimmmm._ and connect on LinkedIn at linkedin.com/in/ibrahimsaleem91.

