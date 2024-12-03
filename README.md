# Average Project Scores SQL Query

This SQL script calculates the average score for each project, but only includes projects where more than one team member has provided a score.

## Script Details

- **Filename**: `average_project_scores.sql`
- **Functionality**:
  - Groups scores by `project_id`.
  - Calculates the average score for each project.
  - Filters out projects with only one score.

## Query Example
```sql
SELECT 
    project_id,
    AVG(score) AS average_score
FROM 
    project_scores
GROUP BY 
    project_id
HAVING 
    COUNT(score) > 1;
