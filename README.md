# California license plates

**Warning: this dataset contains vulgar and offensive language (quite a lot of it).**

`applications.csv` is a CSV of 23,463 personalized license plate applications the California DMV received from 2015-2016 and prepared by @veltman.

`applications2017.csv` is a CSV of 12,046 personalized license plate applications the California DMV received in 2017 (until the process and documentation changed in mid-July 2017) and prepared by @21five.

These do NOT represent all applications received by the DMV during that timeframe, only applications that were flagged for additional review by the Review Committee. The file includes the following columns:

- `plate`: the personalized license plate combination requested.
- `review_reason_code`: Reason code for the application being reviewed (see below for codes).
- `customer_meaning`: Meaning of the plate provided by the applicant.
- `reviewer_comments`: Comments from DMV reviewers.
- `status`: `Y` means the plate was approved, `N` means it was denied.

This data was parsed from a set of 458 (2015-16) and 165 (2017) Excel workbooks that the DMV prepared for other public records requests. These files were received as consolation prizes in response to related records requests, which would have cost upwards of \$2,000 each to fulfill otherwise.

## Notes

- In plate combinations, a `#` character indicates a hand symbol, a `$` character indicates the heart symbol, a `+` character indicates the plus symbol, and a `&` character indicates the star symbol. A space may indicate a half or full space.
- Some records are missing reason codes, customer meanings, reviewer comments, and/or statuses.
- A reviewer comment of "No micro" indicates that a paper application was submitted but was unavailable in the DMV's imaging system.
- A reviewer comment of "Quickweb unavailable" indicates that the DMV's application system was unavailable to the reviewer.
- In a few cases the reason code was some other character or word besides `Y` or `N`, possibly a typo. Most of the unambiguous ones were changed while all the rest were changed to "?".
- We tried to redact any records we found that seemed to include too much personal information about the applicant (about 50 in 2015-16 and 100 in 2017). This included full names from DMV records, home addresses or telephone numbers.
- Because the data is parsed from Excel workbooks that are not 100% consistent in structure, there may be some errors.
- The data is not sorted, but ordered by the date of the workbook (so earlier entries are from earlier dates, later entries are from later dates). The plates were alphabetized within each workbook.
- Review reason codes are described as follows:

```md
7(B) When a desired configuration is not available, a letter shall not be substituted for a number, nor shall a number be substituted for a letter, to create another configuration of a similar appearance.
7(D) The department shall refuse any configuration that may carry connotations offensive to good taste and decency, or which would be misleading, based on criteria which includes, but is not limited to, the following:
    1. The configuration has a sexual connotation or is a term of lust or depravity.
    2. The configuration is a vulgar term; a term of contempt, prejudice, or hostility; an insulting or degrading term; a racially degrading term; or an ethnically degrading term.
    3. The configuration is a swear word or term considered profane, obscene, or repulsive.
    4. The configuration has a negative connotation to a specific group.
    5. The configuration misrepresents a law enforcement entity.
    6. The configuration has been deleted from regular series license plates.
    7. The configuration is a foreign or slang word or term, or is a phonetic spelling or mirror image of a word or term falling into the categories described in subdivisions 1. through 6. above.
```
