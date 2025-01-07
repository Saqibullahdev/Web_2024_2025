## Team Schema
The `Team` schema is defined in `models/team.js` with the following attributes:

- `picture`: String (required) - URL of the team member's picture.
- `name`: String (required) - Name of the team member.
- `designation`: String (required) - Designation of the team member.
- `years`: String (required) - Years of experience or association.
- `priority`: Number (optional) - Priority level of the team member.
- `team`: String (optional) - Team name or identifier.


# Team API Documentation

## Create Team
**POST** `http://localhost:3000/api/team`
- Creates a new team
- Request body should contain team data
```json
{
    "picture": "https://example.com/picture.jpg",
    "name": "John Doe",
    "designation": "Software Engineer",
    "year": "2022"
}
```
- This should be sent in form-data from the front end

like this
```javascript
const form = new FormData();
form.append('picture', 'https://example.com/picture.jpg');
form.append('name', 'John Doe');
form.append('designation', 'Software Engineer');
form.append('year', '2022');
```


## Get Teams by Year
**GET** `http://localhost:3000/api/team/:year`
- Retrieves all teams for a specific year
- Replace `:year` with the desired year (e.g., `http://localhost:3000/api/team/2023`)

## Update Team
**PATCH** `http://localhost:3000/api/team/:id`
- Updates an existing team
- Replace `:id` with the team ID
- Request body should contain fields to update

## Delete Team
**DELETE** `http://localhost:3000/api/team/:id`
- Deletes a team
- Replace `:id` with the team ID
