# member_attendance database

## member table
- id, first_name, last_name, is_member, is_admin

## attendance table
- member_id(foreign key), specific_date (present/absent)

## visitors table
- id, unique_identifier (e.g. "the Brazilians"), count
- Capability of merging 2 unique_identifiers into one visitor profile
- Capability of moving visitors to members

## attendance_total table 
- SUM(member_attendance + visitors_count(foreign_key))
- How to do the above opperation 



