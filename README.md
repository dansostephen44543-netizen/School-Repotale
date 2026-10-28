# School Results Portal — upgraded demo

A responsive HTML/CSS/JavaScript school results portal demo. Open `index.html` in a modern browser.

## Demo sign-ins
- Teacher: `teacher` / `demo123`
- School Admin: `schooladmin` / `admin123`
- Sample student result checker: Student ID `STU2026001`, PIN `123456`

## Features
- Academic periods support school years from 2020/2021 through 2035/2036, First Term, Second Term and Third Term, and JHS 1–3 / SHS 1–3 classes.
- Student result checking using Student ID and result PIN.
- Result sheet shows the registered student photo, full name, ID, date of birth, exam and grades.
- School Admin can add, edit, search and delete student profiles with name, unique ID, date of birth and uploaded photo.
- Uploaded images are resized/compressed in the browser before storage.
- Teachers can enter and update results for a combined JHS and SHS core/elective subject list, with each subject optional; at least one valid score (0–100) is required.
- Teachers can set a pass mark for each student result (default 50/100). Pass status follows a WASSCE-style grade label: A1–C6 = CREDIT PASS, D7–E8 = PASS (NON-CREDIT), and F9 = FAIL. The configured school pass mark is shown for reference only and does not control this status. The raw-score-to-grade thresholds are a simplified school-portal convention, not an official WAEC conversion; WAEC grades are not assigned using a universal fixed raw-score threshold.
- Blank subject scores display as a dash and do not receive a grade.
- Teacher dashboard includes totals, published/draft counts, student profile count, searchable records and CSV export.
- School Admin can search the student directory and export its details as CSV.
- Print a result slip or download individual/all results as CSV. Date of birth is included in the result exports.
- Draft and published result states.
- Responsive layout for phones, tablets and desktops.

## Important limitations
This is a front-end demonstration only. It stores data in the current browser using `localStorage`; profiles, photos and results are not synced across devices. The demo usernames and passwords are visible in the JavaScript and are not real security. Do not use it to store real student data or passwords. A real school deployment needs a secure backend, a database, authenticated accounts, role-based permissions, backups, and protected photo storage. This is not an official WAEC website and is not connected to WAEC systems.


## Global website search

The header-area search can find portal pages, instructions, features, supported subjects and suggested Ghanaian school names. Selecting a result opens the relevant portal section. While signed in, teachers and school administrators can also search their own selected school's records in the global search; private records are not added to global search for signed-out visitors. Use Ctrl+K (or Command+K on Mac) to focus the search box.


### Student thank-you message
After a student successfully checks their published result, the portal displays “Thank you for using our service!”. After they select Download result, the message updates to confirm that the results download has started.


## Ghana JHS and SHS school-name suggestions

The portal supports JHS 1–3 and SHS 1–3, with separate academic-year and term selections. The school picker combines JHS/basic-school examples and a broad selection of SHS names, but it is **not a verified complete list of every JHS and SHS in Ghana**. Ghana has tens of thousands of schools and registers change. The school-name fields accept free text, so a teacher, admin, or student can enter any school name even when it is not in the suggestions.

For official/current school lookup, use the [Ghana Education Service School Directory](https://ges.gov.gh/schools.php) or the [NaSIA School Licensing Directory](https://www.nasia.gov.gh/nasiadashboard/index.php). The school suggestions in this demo are examples, not an official nationwide register.

### Saving and displaying student results
- When a teacher saves or publishes a result, the student record and entered raw scores are saved in this browser’s local storage and remain after refresh/reopening on the same browser/device.
- The student result slip, CSV download, and printable result show only subjects with scores entered by the teacher; each entered score is labelled as a raw score out of 100, with its grade and WASSCE-style credit-pass / non-credit-pass / fail status. Blank subjects are not shown.
- This demo does not sync results between different devices or browsers. A shared online database and secure server authentication are needed for school-wide access.


## Result printing and downloads
- Student result pages provide a CSV download and a standalone printable HTML file.
- The Print result button opens a clean print view; if the browser blocks pop-ups, it falls back to printing the current result page.
- Teacher result exports and student-directory CSV exports use the shared CSV download helper.
- On Android, if the browser asks for permission, allow downloads. To create a PDF, open the printable HTML file and choose Print, then Save as PDF.


Creator credit: Made by shadowchaser2234.
