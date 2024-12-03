# GPT Notes

--- 
## Tech to Use

1. Front End
- React.js 
- React Native if I'm feeling *spicy*
- Tailwind CSS for *style*

2. Back End
- Flask or Django b/c I'm comfortable with Python
- Node.js + Express.js maybe, idk I'm pretty out of my depth here

3. Database
- PostgreSQL to work w/ relational databases 

4. Hosting
- IDK, I'll figure this out later 
- Vercel for Front End and AWS for Back End & Database 

---
## Features and Techniques 
1. Key Features 
- Mark attendance... kind of the whole point. Maybe create a swipe feature like Quizlet
- Track attendence over time. Create a report and send to pastors for check in's
- Visitor tracking
- Export data to a csv file would be pretty cool

2. Database Design 
- Families Table: id, family_name, members (relation)
- Members Table: id, family_id(from Families), first_name, is_admin(from Admin)
- Visitors Table: id, identifier, count
- Attendance Table: id, member_id(from Members), status(present/absent), visitor_count(from Visitors)
- Admin Table: id, username, password_hash, role

3. Considerations
- Scalability
- Security: HTTPS, store passwords securely w/ hashing alorgithms 
- Performance: Cache frequently accessed data using Redis(?)
- Backup and recovery of data

---
## Step-By-Step
1. Define Requirements
- Core Functionality -- Mark members as present/absent & account for visitors in total attendance
- Additional Features -- Generate reports 
- Sketch out UI

2. Plan Architecture 
- Front End-- What I'll interact with; think "easy to use" & "sleek"
- Back End-- Handle Front End requests, authentification, & permissions
- Database-- How to store & update data
- API-- How to connect Front End & Back End; REST or GraphQL(?)

3. Set Up Environment 
- Install necessary tools 
- Choose frameworks 
- Set up project on GitHub (checkity-check-check)

4. Build the Database
- Tables for church members, families, attendance, admin roles...
- Relationships-- church members will have foreign key to families, attendace will have a foreign key to members & dates 
- Create migrations to define schema(?)

5. Develop the Back End-- Django Approach (Although I might go with Flask)
- Handle user authentification & permissions
- Create Models(?) for Member, Family, Attendance, and Admin User
- Use Django's admin panel(?) for data management
- Build API Endpoints w/ Django REST Framework for marking attendance, fetching reports, and managing members and families

6. Develope the Front End 
- Use React or Vue 
- Use Axios or Fetch API(?) to connect Front End with Back End APIs 

7. Add Key Features 
- Mark Attendance-- Create forms to select members & mark present/absent & create an option to increment visitor count
- Track Attendance Over Time-- A page the shows trends for members &/or families (use chart.js or D3.js)
- Generate PDF or CSV Reports 

8. Test Application
- Unit tests for Back End logic (APIs, database queries)
- Integration tests to make sure front end & back end talk nice 
- User testing on mobile and desktop
- Use tools like Postman(?) to test API endpoints

9. Deploy the App
### Hosting Providers
- Backend-- deploy Django on Heroku, AWS, or DigitalOcean(?)
- Frontend-- Vercel, Netlify(?)
- Database-- Heroku Postgres, AWS RDS, or MongoDB Atlas
### Production Environment
- Configure environment variables for security (database credentials, API keys(?))
- Use gunicorn or uwsgi (???) w/ a reverse proxy (Nginx) to serve app (?)
- Enable HTTPS w/ services like Let's Encrypt(?)

10. Maintain & Improve 
- Regularly backup database
- Monitor app performance & debug as necessary 
- Gather user feedback from me, myself, and I and iteratively add new features

---
## Development Workflow Abridged 
1. Backend Development-- Create models, APIs, andauthentification
2. Frontend Development-- Create a user-friendly interface & connect to APIs 
3. Integration-- Test frontend & backend together
4. Deployment-- launch app & let the little bird fly on its own
