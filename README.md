# Tech-Interviews-MY

Tech Interviews MY is a Malaysia (Kuala Lumpur) based community dedicated to creating opportunities for participants to join for a mock technical (leetcode style) interview. This app serves to facilitate key problems like matching interviewers to interviewees during the event.

## Functional requirements
1. In the landing page, user should provide a unique alias. This alias should be unique to the current event only - if this alias was used in a previous event, the alias shouldn't be disqualified. Write this alias to DB. 
2. User's alias should be kept in local storage with a time to live of 2 hours at most. If a user reenters the web app, step (1) shouldn't be prompted anymore and skip directly to step (3)/(6).
3. User shall be navigated to a page where they can choose if they want to
   - Interview someone 
   - Get interviewed
   - Neither. Just here for networking
4. In the same page as (3), if their selection is to interview / get interviewed, they should specifiy the type of interview (Leetcode / System Design) and difficulty level (Easy / Medium / Hard) they desire to ask / get asked.
5. Upon selection, this information should again be stored into local storage like in step (2). Write this selection to DB. 
6. Depending on selection in stage 4: 
   - If the user chose to interview someone, they should see interviewees with a similar interview type and difficulty level
   - If the user chose to get interviewed, they should see interviewers with similar interview type and difficulty level
   - If the user chose networking, they should only see other people wanting to network
7. Interviewees choose who they want to be their interviewer. After an interviewee selects an interviewer, they'll pair up. Finding each other in person is the job of the pair. (Sticky note name tag?)
8. Everybody's application automatically refreshes every 30 seconds. As such, some latency between interviewee selecting an interviewer is expected. 
9. Everybody has a counter on their device that shows the number of interviewers, interviewees, and networking people available. Users may also go back to step (3) and (4) to change their preference.

