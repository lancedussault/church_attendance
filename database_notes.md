# member_attendance database

## member table
- id, first_name, last_name, is_member, is_admin

## attendance table
- member_id(foreign key), specific_date (present/absent), total=SUM(specific_date)

## visitors table
- id, date, unique_identifier (e.g. "the Brazilians"), count, total=(SUM(count) WHERE date=specific_date )
- Capability of merging 2 unique_identifiers into one visitor profile
- Capability of moving visitors to members

## attendance_total table 
- SUM(member_attendance + visitors_count(foreign_key))
- How to do the above opperation 



