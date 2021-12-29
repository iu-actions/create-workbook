# create-workbook

[![GitHub issues](https://img.shields.io/github/issues/iu-actions/create-workbook)](https://github.com/iu-actions/create-workbook/issues)

This action creates an IU Workbook.

## Found a bug? 💁‍♀️

Thanks for letting us know! Please [file an issue](../../issues/new?assignees=&labels=&template=bug_report.md&title=) and we should reply shortly.

## Configuration

This action requires the presence of inputs, which are listed below.

### Inputs
- `first_name`: The first name of the student. (**required**)
- `last_name`: The last name of the student. (**required**)
- `email`: The email of the student. (**required**)
- `id`: The id of the student. (**required**)
- `degree`: The degree pursued by the student. (**required**)

- `workbook`: Path to the `workbook.md`. (**required**)

- `course_name`: The name of the course. (**required**)
- `course_id`: The id/number of the course. (**required**)
- `professor`: The professor of the course. (**required**)
- `tutor`: The tutor of the course. (**required**)

*Note*: The following files must be present at the specified location and contain the appropriate variables.

- `content_format_doc`: Path to the Microsoft Word template of the content. (**required**) → [Learn more](https://pandoc.org/MANUAL.html#option--reference-doc)
- `cover_format_doc`: Path to the Microsoft Word template of the cover page. (**required**) → [Learn more](https://pandoc.org/MANUAL.html#option--reference-doc)
- `cover_template_doc`: Path to the Markdown template of the cover page to define the structure. (**required**) → [Learn more](https://pandoc.org/MANUAL.html#option--template)

## Example

Below you will find an example of how you can use this action.

```yaml
uses: iu-actions/create-workbook@main
  with:
    # student details
    first_name: John
    last_name: Doe
    email: john.doe@example.edu
    id: 12345678
    degree: B. Sc. Computer Science

    # course details
    course_name: Linear Algebra I
    course_id: LA101
    professor: Prof. Dr. Gilbert Strang
    tutor: Jane Doe
          
    # workbook details
    workbook: exam/workbook.md

    # configuration details
    content_format_doc: .workbook/content/format.docx
    cover_format_doc: .workbook/cover/format.docx
    cover_template_doc: .workbook/cover/template.md
  ```
