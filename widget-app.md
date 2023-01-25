# WidgetApp

##  User guide

### What’s new

* You can now work on the same Thing as your teammates at the same time. We’ll publish your changes as quickly as possible so that your teammates can see your work.

## Administrator guide

### What’s new

* Multiple users can now work on the same Thing at the same time, supported by our new Streaming API. Some things to be aware of:
  * The Streaming frontend and API processes add to your server load, so you may want to monitor these for excessive resource use. To learn more, see the Streaming API docs (add hyperlink). 
  * External developers connect to the API using the following URL: wss://www.widgetapp.com/_stream. The API uses OAuth2.0 access tokens for authorization, so you’ll need to manage these user groups. To learn more, see the authorization docs (add hyperlink). 

## API guide

### What’s new

* Our new Streaming API enables multiple users to work on the same Thing at the same time. The API runs over WebSockets, and you can use the same connection for different services. Some things to be aware of:
  * The Streaming API uses OAuth2.0 access tokens for authorization. 
  * Authorized connections that use the Streaming API are handled by the Streaming frontend, which manages the session in a similar way to the WidgetApp frontend, but with added Streaming API capabilities. Existing API requests are still handled by the WidgetApp frontend.
  * If your external systems use the Streaming frontend, they’ll need to listen on port 200 for stream messages.
  
  To learn more about the Streaming API capabilities, including how to connect and interact with it, see the Streaming API docs (add hyperlink).
  
## My approach

I read through the notes to find the main feature of the new API, and which notes, if any, applied to all users (end users, administrators and API developers). End users being able to work on the same Thing at the same time seemed like the main feature of the API and relevant to all users. I used this information as the starting point for each section.

I decided which section to put the remaining notes in by reading them from each user’s point of view — to identify the different types of information and make assumptions on what I thought was relevant for each user. 

Once I split the notes into the three sections, I read through them again and removed information that I thought belonged elsewhere in the documentation — and not in a What’s new section — including:

* Details on how to handle server load 
* Details on how to manage authorization
* Details on how to interact with the API
* Details of stream messages

I added “To learn more…” prompts where I would link out to this information. I then edited and tailored the sections to each user, and made the tone more conversational.

To consider whether these sections are complete, I would like to understand more about the following:

* “Most user actions, like search or scrolling, work by calling _ajax/ 
endpoints” — whether this applies to any of these user groups, or whether this information is more relevant to Anonymous's web interface developer team.
* “Authentication is unchanged from previous versions - managed through the existing WidgetApp frontend (WFE)” — whether we need to add this if nothing has changed.
* “Streaming API is authorized only for approved user groups - managed through OAuth2.0 access tokens” — whether my assumption that the end user does not need to interact with OAuth2.0 access tokens is correct.
* Our style guide for naming conventions, in particular, whether “Streaming” needs to be capitalized in “Streaming frontend”. 
