# SLC-Coding-experience; Querrying my first database built from scratch
select 	 enrollments.persons_id as student_id,
         concat(persons.first_name, ' ' , persons.last_name) as student_name,
         enrollments.sections_subjects_id as subject_code,
         subjects.description as subject_description,
         enrollments.sections_id as section_number,
         terms.description as term_description
        
from	enrollments

inner join persons on
		persons.id = enrollments.persons_id

inner join subjects on
		subjects.id = enrollments.sections_subjects_id
        
inner join terms on
		terms.id = enrollments.sections_terms_id;
