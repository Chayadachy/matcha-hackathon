# Requirements Document



## Introduction



Matcha is a social platform designed to connect users based on shared interests, preferences, and compatibility. The platform facilitates meaningful connections through personalized profiles, a sophisticated matching system, real-time communication, and event-based meetups. This document outlines the requirements for the Matcha social platform, focusing on user profiles, matching algorithms, communication features, interest categorization, and event organization.



## Requirements



### 1. User Profile Management



**User Story:** As a user, I want to create and manage a personalized profile, so that I can share information about myself and attract compatible connections.



#### Acceptance Criteria



1. WHEN a user registers for the platform THEN the system SHALL create a new user profile.

2. WHEN a user accesses their profile THEN the system SHALL display editable fields for personal information.

3. WHEN a user updates their profile THEN the system SHALL save and immediately reflect these changes.

4. WHEN a user adds information to their profile THEN the system SHALL allow inclusion of:

   - Basic information (name, age, location)

   - Short biography

   - Personal interests

   - Preferences for matching

5. IF a user uploads a profile picture THEN the system SHALL validate the image format and size before saving.

6. WHEN a user views another user's profile THEN the system SHALL display only the information marked as public.



### 2. Matching System



**User Story:** As a user, I want to discover and connect with compatible users through various matching methods, so that I can form meaningful relationships based on shared interests and preferences.



#### Acceptance Criteria



1. WHEN a user enters the matching section THEN the system SHALL present potential matches based on the configured matching algorithms.

2. WHEN the system generates matches THEN it SHALL prioritize users with similar ranked interests.

3. IF a user sets age preferences THEN the system SHALL filter potential matches to include only users within the specified age range.

4. WHEN an initial match is established THEN the system SHALL present customizable compatibility questions to both users.

5. IF both users provide compatible answers to confirmation questions THEN the system SHALL confirm the match and enable communication.

6. WHEN a user receives a match THEN the system SHALL send a notification.

7. IF a user rejects a match THEN the system SHALL not present that user as a potential match again for a defined period.

8. WHEN the matching algorithm runs THEN the system SHALL consider the user's interest rankings as a primary factor in determining compatibility.

9. IF both users mutually express interest THEN the system SHALL confirm the match.

10. IF no suitable matches are found THEN the system SHALL suggest relaxing some criteria or offer alternative recommendations.





### 3. Chat System



**User Story:** As a user, I want to communicate with my matches through a real-time messaging system, so that I can build connections and plan meetups.



#### Acceptance Criteria



1. WHEN a match is confirmed THEN the system SHALL create a private chat room for the matched users.

2. WHEN a user sends a message THEN the system SHALL deliver it to the recipient in real-time.

3. WHEN a user receives a message THEN the system SHALL display a notification.

4. IF a user creates a group chat THEN the system SHALL allow them to add multiple participants.

5. WHEN a user joins an interest-based group chat THEN the system SHALL display the chat history.

6. IF a user connects their social networking accounts THEN the system SHALL offer integration options for sharing content or contacts.

7. WHEN a user is offline THEN the system SHALL store unread messages and deliver them when the user returns online.

8. IF a user blocks another user THEN the system SHALL prevent further communication between them.

9. IF a user reports abusive behavior in chat THEN the system SHALL flag the chat and notify moderators for review.

10. WHEN a user sends an image or sticker THEN the system SHALL support media attachments subject to content policies.



### 4. 4. Interest Ranking System (Expanded)

User Story:

As a user, I want to select and rank my interests during the onboarding process, so that the system can recommend better matches and personalize my experience from the start.



Onboarding Flow & Structure

The Interest Ranking System is introduced during the account creation process, spanning across three pages:



Page 1: User Personal Information



First Name / Last Name: Text input



Preferred Name / Nickname: Text input



Gender: [Male] / [Female] / [Trans] (Button selection)



Birthday: Dropdown (DD/MM/YYYY)



Job: Text input



City: Search-based input



Languages Spoken: Multi-select checkbox



Page 2: Purpose of Use



You are looking for: [Friend] / [Dating] / [Casual] (Multi-select)



Who are you interested in connecting with?



[Men], [Women], [More Options]



If "More Options" selected: [Lesbian], [Gay], [Bisexual], [Trans women], [Trans men], [Non-binary], [Pansexual], [Asexual], [Queer], [Prefer not to say], [Type your own]



Age Range for Matching: Slide bar with optional “Open to all ages” checkbox



Page 3: Interest Selection & Ranking



Users are asked to select 5 topics that best represent themselves, and for each topic, choose top 3 favorites and optionally fill in more detail.



Interest Categories (Multi-select from list):



Hobby



Movies



Pop Culture



Music



Games



Foodie



Travel



Books



Podcast



Example: If User selects [Movies]



Choose sub-interests: [Drama], [Comedy], [Horror], etc.



Tell me more about [Movies]:



3 Movies I love: [Search box / Text input]



Favorite Actor/Director (optional)



Favorite Movie of All Time (optional)



Each selected category includes:



Sub-category multi-select



Free-text input for personalized favorites (e.g., "3 things I love")



Optional metadata: favorite artist/actor/platform/author, etc.



Acceptance Criteria (Extended)

1.WHEN a new user creates an account THEN the system SHALL guide them through a multi-page onboarding flow.

2.WHEN the user reaches the interest ranking page THEN the system SHALL require them to select up to 5 interest categories.

3.WHEN the user selects a category THEN the system SHALL present sub-categories as multi-select checkboxes.

4.WHEN the user selects sub-categories THEN the system SHALL ask for 3 personalized favorites per category using search-assisted input fields.

5.IF the user provides optional data (e.g., favorite artist, platform, location) THEN the system SHALL store and use this for more precise matching.

6.WHEN a user completes onboarding THEN the system SHALL generate an interest profile used for ranking-based matching.

7.IF a user returns to edit their interests THEN the system SHALL allow updates at any time via profile settings.



### 5. Event-Based Meeting Feature (Expanded)

User Story:

As a user, I want to create and join social events through the platform, so that I can meet people with similar interests in real-world settings and continue building relationships beyond the app.



Acceptance Criteria

1.WHEN a user accesses the events section

THEN the system SHALL display a list of upcoming events, categorized by:

- Type (e.g., travel, concert, meetup)

- Location (based on user’s current city or selected area)

- Recommended (based on user's interests)



2.WHEN a user creates an event

THEN the system SHALL collect the following required fields:



- Event type (e.g., Travel, Drinking Meetup, Concert, Café Hopping, Game Night)

- Date & time (start/end)

- Location (Searchable Map or Address)

- Description

- Participant limit (min/max)

- Visibility: [Public] / [Friends Only] / [Private with Link]



3.IF an event is created

THEN the system SHALL:



- Display it to compatible users (based on interest and location match)



- Tag it by topic for discovery (e.g., #Kpop #Boardgames)



4.WHEN a user joins an event

THEN the system SHALL:



- Add them to a dedicated event group chat



- Display other participants (profile preview)



- Notify the event host



5.IF an event reaches the participant limit

THEN the system SHALL:



- Mark the event as “Full”



- Optionally allow a waitlist



6.WHEN the event date approaches

THEN the system SHALL:



- Send a reminder notification 24 hours and 1 hour in advance



- Include location info and chat link



7.IF a user has joined an event

THEN the system SHALL provide sharing options:



- Share via SNS (LINE, Instagram, etc.)



- Copy invitation link (if event is public or private with link)



8.WHEN the event concludes

THEN the system SHALL:



- Prompt users to leave feedback or rate the event



- Suggest connections with participants they chatted with



9.IF a host edits the event details after creation

THEN the system SHALL notify all current participants about the changes



10.IF a user reports inappropriate behavior in an event

THEN the system SHALL forward the report to moderation for review and take appropriate action (e.g., warning, event removal)