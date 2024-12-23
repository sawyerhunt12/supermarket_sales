# Supermarket Sales
## Project Overview
This project analyzes a supermarket sales dataset using SQL to gain insights into sales performance, customer behavior, and other key metrics. The focus is on understanding trends in sales, payment methods, branch performance, and other aspects relevant to supermarket operations.

The analysis was conducted entirely using SQL queries for data exploration, aggregation, and deriving insights. The analysis can be viewed here: [Link](https://csvfiddle.io/#JTdCJTIyaXNUYWJsZU1ldGFkYXRhT3BlbiUyMiUzQWZhbHNlJTJDJTIyaXNOZXdUYWJsZUZvcm1PcGVuJTIyJTNBZmFsc2UlMkMlMjJpc0NvbmZpcm1EZWxldGVRdWVyeU9wZW4lMjIlM0FmYWxzZSUyQyUyMmlzQ29uZmlybURyb3BUYWJsZU9wZW4lMjIlM0FmYWxzZSUyQyUyMmlzU2hhcmVEaWFsb2dPcGVuJTIyJTNBZmFsc2UlMkMlMjJkYlJlYWR5JTIyJTNBZmFsc2UlMkMlMjJ0YWJsZXMlMjIlM0ElNUIlN0IlMjJuYW1lJTIyJTNBJTIyc3VwZXJtYXJrZXRfc2FsZXMlMjIlMkMlMjJ1cmwlMjIlM0FudWxsJTJDJTIyY29sdW1ucyUyMiUzQSU1QiU1RCU3RCU1RCUyQyUyMnF1ZXJpZXMlMjIlM0ElN0IlMjIxNzMzMDcwMDA2LjMwNjc2MzIlMjIlM0ElN0IlMjJpZCUyMiUzQTE3MzMwNzAwMDYuMzA2NzYzMiUyQyUyMnRpdGxlJTIyJTNBJTIyQWxsJTIwZmllbGRzJTIyJTJDJTIyYm9keSUyMiUzQSUyMi0tQSUyMGxvb2slMjBhdCUyMHRoZSUyMGRhdGFzZXQtLSU1Q24lNUNuc2VsZWN0JTIwKiU1Q25mcm9tJTIwc3VwZXJtYXJrZXRfc2FsZXMlNUNubGltaXQlMjAxNSU1Q24lM0IlMjIlMkMlMjJyZXN1bHQlMjIlM0ElNUIlNUQlMkMlMjJlcnJvciUyMiUzQW51bGwlN0QlMkMlMjIxNzMzMDcxMTg1LjY5MDQwMTglMjIlM0ElN0IlMjJpZCUyMiUzQTE3MzMwNzExODUuNjkwNDAxOCUyQyUyMnRpdGxlJTIyJTNBJTIyMS4wJTIwVG90YWwlMjBzYWxlcyUyMHBlciUyMGJyYW5jaCUyMiUyQyUyMmJvZHklMjIlM0ElMjItLVRvdGFsJTIwc2FsZXMlMjBwZXIlMjBicmFuY2gtLSU1Q24lNUNuc2VsZWN0JTIwQnJhbmNoJTJDJTIwcm91bmQoc3VtKFRvdGFsKSUyQyUyMDIpJTIwYXMlMjB0b3RhbF9zYWxlcyUyQyUyMHJvdW5kKHN1bShjb2dzKSUyQyUyMDIpJTIwYXMlMjB0b3RhbF9jb3N0X29mX2dvb2RzJTJDJTIwcm91bmQoc3VtKCU1QyUyMmdyb3NzJTIwaW5jb21lJTVDJTIyKSUyQyUyMDIpJTIwYXMlMjBncm9zc19pbmNvbWUlNUNuZnJvbSUyMHN1cGVybWFya2V0X3NhbGVzJTVDbmdyb3VwJTIwYnklMjBCcmFuY2glNUNub3JkZXIlMjBieSUyMHRvdGFsX3NhbGVzJTIwZGVzYyU1Q24lM0IlMjIlMkMlMjJyZXN1bHQlMjIlM0ElNUIlNUQlMkMlMjJlcnJvciUyMiUzQW51bGwlN0QlMkMlMjIxNzMzMTc5NjAxLjU2NzY5OCUyMiUzQSU3QiUyMmlkJTIyJTNBMTczMzE3OTYwMS41Njc2OTglMkMlMjJ0aXRsZSUyMiUzQSUyMjEuMSUyMEF2ZyUyMGN1c3RvbWVyJTIwcmF0aW5nJTIwcGVyJTIwYnJhbmNoJTIyJTJDJTIyYm9keSUyMiUzQSUyMi0tQXZlcmFnZSUyMGN1c3RvbWVyJTIwcmF0aW5nJTIwcGVyJTIwYnJhbmNoLS0lNUNuJTVDbnNlbGVjdCUyMHJvdW5kKGF2ZyhSYXRpbmcpJTJDJTIwMiklMjBhcyUyMGF2Z19yYXRpbmclMkMlMjBCcmFuY2glNUNuZnJvbSUyMHN1cGVybWFya2V0X3NhbGVzJTVDbmdyb3VwJTIwYnklMjBCcmFuY2glNUNub3JkZXIlMjBieSUyMGF2Z19yYXRpbmclMjBkZXNjJTVDbiUzQiUyMiUyQyUyMnJlc3VsdCUyMiUzQSU1QiU1RCUyQyUyMmVycm9yJTIyJTNBbnVsbCU3RCUyQyUyMjE3MzMyNDU5MTcuNjc0NjAwNCUyMiUzQSU3QiUyMmlkJTIyJTNBMTczMzI0NTkxNy42NzQ2MDA0JTJDJTIydGl0bGUlMjIlM0ElMjIxLjIlMjBCcmVha2Rvd24lMjBvZiUyMHBheW1lbnQlMjBtZXRob2RzJTIyJTJDJTIyYm9keSUyMiUzQSUyMi0tQnJlYWtkb3duJTIwb2YlMjBwYXltZW50JTIwbWV0aG9kcyUyMGJ5JTIwYnJhbmNoLS0lNUNuJTVDbnNlbGVjdCUyMEJyYW5jaCUyQyUyMFBheW1lbnQlMkMlMjBjb3VudCgqKSUyMGFzJTIwcGF5bWVudF9icmVha2Rvd24lNUNuZnJvbSUyMHN1cGVybWFya2V0X3NhbGVzJTVDbmdyb3VwJTIwYnklMjBQYXltZW50JTJDJTIwQnJhbmNoJTVDbm9yZGVyJTIwYnklMjBCcmFuY2glNUNuJTNCJTIyJTJDJTIycmVzdWx0JTIyJTNBJTVCJTVEJTJDJTIyZXJyb3IlMjIlM0FudWxsJTdEJTJDJTIyMTczMzM1MjA2NC4zNTM0NjI3JTIyJTNBJTdCJTIyaWQlMjIlM0ExNzMzMzUyMDY0LjM1MzQ2MjclMkMlMjJ0aXRsZSUyMiUzQSUyMjIuMCUyMFRvdGFscyUyMGJ5JTIwcHJvZHVjdCUyMGxpbmUlMjBncm91cGVkJTIwYnklMjBnZW5kZXIlMjIlMkMlMjJib2R5JTIyJTNBJTIyLS1Ub3RhbHMlMjBieSUyMHByb2R1Y3QlMjBsaW5lJTIwZ3JvdXBlZCUyMGJ5JTIwZ2VuZGVyLS0lNUNuJTVDbnNlbGVjdCUyMCU1QyUyMlByb2R1Y3QlMjBsaW5lJTVDJTIyJTJDJTIwR2VuZGVyJTJDJTIwcm91bmQoc3VtKFRvdGFsKSUyQyUyMDIpJTIwYXMlMjBwcm9kdWN0X2xpbmVfdG90YWwlMkMlMjBjb3VudCgqKSUyMGFzJTIwcHVyY2hhc2VfY291bnQlNUNuZnJvbSUyMHN1cGVybWFya2V0X3NhbGVzJTVDbmdyb3VwJTIwYnklMjAlNUMlMjJQcm9kdWN0JTIwbGluZSU1QyUyMiUyQyUyMEdlbmRlciU1Q25vcmRlciUyMGJ5JTIwJTVDJTIyUHJvZHVjdCUyMGxpbmUlNUMlMjIlMkMlMjBwcm9kdWN0X2xpbmVfdG90YWwlMjBkZXNjJTVDbiUzQiUyMiUyQyUyMnJlc3VsdCUyMiUzQSU1QiU1RCUyQyUyMmVycm9yJTIyJTNBbnVsbCU3RCUyQyUyMjE3MzQyMTU3MzQuMTAyMDQ1OCUyMiUzQSU3QiUyMmlkJTIyJTNBMTczNDIxNTczNC4xMDIwNDU4JTJDJTIydGl0bGUlMjIlM0ElMjIyLjElMjBQZWFrJTIwc2hvcHBpbmclMjBob3VycyUyMiUyQyUyMmJvZHklMjIlM0ElMjItLVBlYWslMjBzaG9wcGluZyUyMGhvdXJzLS0lNUNuJTVDbndpdGglMjBob3VybHlfc2FsZXMlMjBhcyUyMCglNUNuJTIwJTIwJTIwJTIwc2VsZWN0JTIwbGVmdChUaW1lJTJDJTIwMiklMjBhcyUyMGhvdXIlMkMlMjBjb3VudCgqKSUyMGFzJTIwdHJhbnNhY3Rpb25fY291bnQlMkMlMjByb3VuZChzdW0oVG90YWwpJTJDJTIwMiklMjBhcyUyMHRvdGFsX3JldmVudWUlNUNuJTIwJTIwJTIwJTIwZnJvbSUyMHN1cGVybWFya2V0X3NhbGVzJTVDbiUyMCUyMCUyMCUyMGdyb3VwJTIwYnklMjBob3VyJTVDbiklNUNuJTVDbnNlbGVjdCUyMColNUNuZnJvbSUyMGhvdXJseV9zYWxlcyU1Q25vcmRlciUyMGJ5JTIwdHJhbnNhY3Rpb25fY291bnQlMjBkZXNjJTVDbiUzQiUyMiUyQyUyMnJlc3VsdCUyMiUzQSU1QiU1RCUyQyUyMmVycm9yJTIyJTNBbnVsbCU3RCUyQyUyMjE3MzQyOTU4NTMuNzEwOTkyJTIyJTNBJTdCJTIyaWQlMjIlM0ExNzM0Mjk1ODUzLjcxMDk5MiUyQyUyMnRpdGxlJTIyJTNBJTIyMi4yJTIwTW9zdCUyMHBvcHVsYXIlMjBwcm9kdWN0JTIwbGluZSUyMGZvciUyMGVhY2glMjBicmFuY2glMjIlMkMlMjJib2R5JTIyJTNBJTIyLS1Nb3N0JTIwcG9wdWxhciUyMHByb2R1Y3QlMjBsaW5lJTIwZm9yJTIwZWFjaCUyMGJyYW5jaC0tJTVDbiU1Q253aXRoJTIwYWdncmVnYXRlZF90b3RhbCUyMGFzJTIwKCU1Q24lMjAlMjAlMjAlMjBzZWxlY3QlMjBCcmFuY2glMkMlMjAlNUMlMjJQcm9kdWN0JTIwbGluZSU1QyUyMiUyQyUyMHJvdW5kKHN1bShUb3RhbCklMkMlMjAyKSUyMGFzJTIwdG90YWxfcmV2ZW51ZSU1Q24lMjAlMjAlMjAlMjBmcm9tJTIwc3VwZXJtYXJrZXRfc2FsZXMlNUNuJTIwJTIwJTIwJTIwZ3JvdXAlMjBieSUyMEJyYW5jaCUyQyUyMCU1QyUyMlByb2R1Y3QlMjBsaW5lJTVDJTIyJTVDbiklMkMlNUNucmFua2VkX3NhbGVzJTIwYXMlMjAoJTVDbiUyMCUyMCUyMCUyMHNlbGVjdCUyMEJyYW5jaCUyQyU1Q24lMjAlMjAlMjAlMjAlNUMlMjJQcm9kdWN0JTIwbGluZSU1QyUyMiUyQyU1Q24lMjAlMjAlMjAlMjB0b3RhbF9yZXZlbnVlJTJDJTVDbiUyMCUyMCUyMCUyMHJhbmsoKSUyMG92ZXIlMjAocGFydGl0aW9uJTIwYnklMjBCcmFuY2glMjBvcmRlciUyMGJ5JTIwdG90YWxfcmV2ZW51ZSUyMGRlc2MpJTIwYXMlMjByYW5rJTVDbiUyMCUyMCUyMCUyMGZyb20lMjBhZ2dyZWdhdGVkX3RvdGFsJTVDbiklMjAlMjAlMjAlMjAlNUNuJTVDbnNlbGVjdCUyMEJyYW5jaCUyQyUyMCU1QyUyMlByb2R1Y3QlMjBsaW5lJTVDJTIyJTJDJTIwdG90YWxfcmV2ZW51ZSU1Q25mcm9tJTIwcmFua2VkX3NhbGVzJTVDbndoZXJlJTIwcmFuayUyMCUzRCUyMDElNUNub3JkZXIlMjBieSUyMEJyYW5jaCU1Q24lM0IlMjIlMkMlMjJyZXN1bHQlMjIlM0ElNUIlNUQlMkMlMjJlcnJvciUyMiUzQW51bGwlN0QlMkMlMjIxNzM0MzA2MDc4LjQyMjIwMTQlMjIlM0ElN0IlMjJpZCUyMiUzQTE3MzQzMDYwNzguNDIyMjAxNCUyQyUyMnRpdGxlJTIyJTNBJTIyMy4wJTIwTW9udGhseSUyMHNhbGVzJTIwYnklMjBicmFuY2glMjIlMkMlMjJib2R5JTIyJTNBJTIyLS0lMjBNb250aGx5JTIwc2FsZXMlMjBieSUyMGJyYW5jaCUyMGFuZCUyMGJlc3QlMjBzZWxsaW5nJTIwcHJvZHVjdCUyMGxpbmUtLSU1Q24lNUNud2l0aCU1Q24lNUNuLS0lMjBNb250aGx5JTIwc2FsZXMlMjBieSUyMGJyYW5jaC0tJTVDbiU1Q25tb250aGx5X3NhbGVzJTIwYXMoJTVDbiUyMCUyMCUyMCUyMHNlbGVjdCUyMEJyYW5jaCUyQyUyMG1vbnRoKERhdGUpJTIwYXMlMjBtb250aCUyQyUyMHJvdW5kKHN1bShUb3RhbCklMkMlMjAyKSUyMGFzJTIwdG90YWxfc2FsZXMlNUNuJTIwJTIwJTIwJTIwZnJvbSUyMHN1cGVybWFya2V0X3NhbGVzJTVDbiUyMCUyMCUyMCUyMGdyb3VwJTIwYnklMjBCcmFuY2glMkMlMjBtb250aCU1Q24pJTJDJTVDbiU1Q24tLU1vbnRobHklMjBzYWxlcyUyMGJ5JTIwcHJvZHVjdCUyMGxpbmUlMjBmb3IlMjBlYWNoJTIwYnJhbmNoLS0lNUNuJTVDbnByb2R1Y3RfbGluZV9zYWxlcyUyMGFzJTIwKCU1Q24lMjAlMjAlMjAlMjBzZWxlY3QlMjBCcmFuY2glMkMlMjBtb250aChEYXRlKSUyMGFzJTIwbW9udGglMkMlMjAlNUMlMjJQcm9kdWN0JTIwbGluZSU1QyUyMiUyQyUyMHJvdW5kKHN1bShUb3RhbCklMkMlMjAyKSUyMGFzJTIwcHJvZHVjdF9saW5lX3RvdGFsJTVDbiUyMCUyMCUyMCUyMGZyb20lMjBzdXBlcm1hcmtldF9zYWxlcyU1Q24lMjAlMjAlMjAlMjBncm91cCUyMGJ5JTIwQnJhbmNoJTJDJTIwbW9udGglMkMlMjAlNUMlMjJQcm9kdWN0JTIwbGluZSU1QyUyMiU1Q24pJTJDJTVDbiU1Q24tLSUyMElkZW50aWZ5JTIwdGhlJTIwYmVzdCUyMHNlbGxpbmclMjBwcm9kdWN0JTIwbGluZSUyMHBlciUyMGJyYW5jaCUyMHBlciUyMG1vbnRoLS0lNUNuJTVDbnJhbmtlZF9wcm9kdWN0X2xpbmVzJTIwYXMlMjAoJTVDbiUyMCUyMCUyMCUyMHNlbGVjdCUyMEJyYW5jaCUyQyU1Q24lMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjBtb250aCUyQyU1Q24lMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlNUMlMjJQcm9kdWN0JTIwbGluZSU1QyUyMiUyQyU1Q24lMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjBwcm9kdWN0X2xpbmVfdG90YWwlMkMlNUNuJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwcmFuaygpJTIwb3ZlciUyMChwYXJ0aXRpb24lMjBieSUyMEJyYW5jaCUyQyUyMG1vbnRoJTIwb3JkZXIlMjBieSUyMHByb2R1Y3RfbGluZV90b3RhbCUyMGRlc2MpJTIwYXMlMjByYW5rJTVDbiUyMCUyMCUyMCUyMGZyb20lMjBwcm9kdWN0X2xpbmVfc2FsZXMlNUNuKSU1Q24lNUNuLS1Db21iaW5lJTIwbW9udGhseSUyMHNhbGVzJTIwd2l0aCUyMHRoZSUyMGJlc3QlMjBzZWxsaW5nJTIwcHJvZHVjdCUyMGxpbmVzLS0lNUNuJTVDbnNlbGVjdCU1Q24lMjAlMjAlMjAlMjBtcy5CcmFuY2glMkMlNUNuJTIwJTIwJTIwJTIwbXMubW9udGglMkMlNUNuJTIwJTIwJTIwJTIwbXMudG90YWxfc2FsZXMlMkMlNUNuJTIwJTIwJTIwJTIwcnBsLiU1QyUyMlByb2R1Y3QlMjBsaW5lJTVDJTIyJTIwYXMlMjBiZXN0X3NlbGxpbmdfcHJvZHVjdF9saW5lJTJDJTVDbiUyMCUyMCUyMCUyMHJwbC5wcm9kdWN0X2xpbmVfdG90YWwlMjBhcyUyMGJlc3Rfc2VsbGluZ19wcm9kdWN0X2xpbmVfc2FsZXMlMkMlNUNuJTIwJTIwJTIwJTIwcmFuaygpJTIwb3ZlciUyMChwYXJ0aXRpb24lMjBieSUyMG1zLm1vbnRoJTIwb3JkZXIlMjBieSUyMG1zLnRvdGFsX3NhbGVzJTIwZGVzYyklMjBhcyUyMHJhbmslNUNuZnJvbSUyMG1vbnRobHlfc2FsZXMlMjBhcyUyMG1zJTVDbmxlZnQlMjBqb2luJTIwcmFua2VkX3Byb2R1Y3RfbGluZXMlMjBhcyUyMHJwbCU1Q25vbiUyMG1zLkJyYW5jaCUyMCUzRCUyMHJwbC5CcmFuY2glMjBhbmQlMjBtcy5tb250aCUyMCUzRCUyMHJwbC5tb250aCUyMGFuZCUyMHJwbC5yYW5rJTIwJTNEJTIwMSU1Q25vcmRlciUyMGJ5JTIwbXMuQnJhbmNoJTJDJTIwbXMubW9udGglNUNuJTNCJTIyJTJDJTIycmVzdWx0JTIyJTNBJTVCJTVEJTJDJTIyZXJyb3IlMjIlM0FudWxsJTdEJTJDJTIyMTczNDMwOTgyOC4yODk2NiUyMiUzQSU3QiUyMmlkJTIyJTNBMTczNDMwOTgyOC4yODk2NiUyQyUyMnRpdGxlJTIyJTNBJTIyMy4xJTIwU2FsZXMlMjBieSUyMGN1c3RvbWVyJTIwdHlwZSUyMG92ZXIlMjB0aW1lJTIyJTJDJTIyYm9keSUyMiUzQSUyMi0tJTIwU3BlbmRpbmclMjBieSUyMGN1c3RvbWVyJTIwdHlwZSUyMG92ZXIlMjB0aW1lJTIwLS0lNUNuJTVDbi0tJTIwY3RlJTIwdG8lMjBhZ2dyZWdhdGUlMjBtb250aGx5JTIwc3BlbmQlMkMlMjBncm91cCUyMGJ5JTIwY3VzdG9tZXIlMjB0eXBlJTIwYW5kJTIwbW9udGglMkMlMjBjYXNlJTIwc3RhdGVtZW50JTIwdG8lMjBsYWJlbCUyMG1vbnRocyUyMC0tJTVDbndpdGglMjBtb250aHNfbGFiZWxlZCUyMGFzJTIwKCU1Q24lMjAlMjAlMjAlMjBzZWxlY3QlMjAlNUMlMjJDdXN0b21lciUyMHR5cGUlNUMlMjIlMkMlMjByb3VuZChhdmcoVG90YWwpJTJDJTIwMiklMjBhcyUyMG1vbnRobHlfc3BlbmQlMkMlMjBtb250aChEYXRlKSUyMGFzJTIwbW9udGhfbnVtZXJpY2FsJTJDJTVDbiUyMCUyMCUyMCUyMGNhc2UlNUNuJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwd2hlbiUyMG1vbnRoKERhdGUpJTIwJTNEJTIwMSUyMHRoZW4lMjAnSmFudWFyeSclNUNuJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwd2hlbiUyMG1vbnRoKERhdGUpJTIwJTNEJTIwMiUyMHRoZW4lMjAnRmVicnVhcnknJTVDbiUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMHdoZW4lMjBtb250aChEYXRlKSUyMCUzRCUyMDMlMjB0aGVuJTIwJ01hcmNoJyU1Q24lMjAlMjAlMjAlMjBlbmQlMjBhcyUyMG1vbnRocyU1Q24lMjAlMjAlMjAlMjBmcm9tJTIwc3VwZXJtYXJrZXRfc2FsZXMlNUNuJTIwJTIwJTIwJTIwZ3JvdXAlMjBieSUyMCU1QyUyMkN1c3RvbWVyJTIwdHlwZSU1QyUyMiUyQyUyMG1vbnRoX251bWVyaWNhbCU1Q24pJTVDbiU1Q25zZWxlY3QlMjAqJTVDbmZyb20lMjBtb250aHNfbGFiZWxlZCU1Q25vcmRlciUyMGJ5JTIwbW9udGhfbnVtZXJpY2FsJTIwYXNjJTVDbiUzQiUyMiUyQyUyMnJlc3VsdCUyMiUzQSU1QiU1RCUyQyUyMmVycm9yJTIyJTNBbnVsbCU3RCUyQyUyMjE3MzQ4MTQ5MzEuMjU0MzkxJTIyJTNBJTdCJTIyaWQlMjIlM0ExNzM0ODE0OTMxLjI1NDM5MSUyQyUyMnRpdGxlJTIyJTNBJTIyMy4yJTIwQ3VzdG9tZXIlMjBMaWZldGltZSUyMFZhbHVlJTIyJTJDJTIyYm9keSUyMiUzQSUyMi0tJTIwQ3VzdG9tZXIlMjBsaWZldGltZSUyMHZhbHVlJTIwKENMViklMjAtLSU1Q24lNUNud2l0aCUyMGN1c3RvbWVyX2xpZmV0aW1lX3ZhbHVlJTIwYXMlMjAoJTVDbiUyMCUyMCUyMCUyMHNlbGVjdCUyMCU1QyUyMkN1c3RvbWVyJTIwdHlwZSU1QyUyMiUyQyU1Q24lMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjBCcmFuY2glMkMlNUNuJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwcm91bmQoc3VtKCU1QyUyMmdyb3NzJTIwaW5jb21lJTVDJTIyKSUyQyUyMDIpJTIwYXMlMjB0b3RhbF9saWZldGltZV92YWx1ZSUyQyU1Q24lMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjBjb3VudCgqKSUyMGFzJTIwdHJhbnNhY3Rpb25zJTJDJTVDbiUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMHJvdW5kKHN1bSglNUMlMjJncm9zcyUyMGluY29tZSU1QyUyMiklMjAlMkYlMjBjb3VudCgqKSUyQyUyMDIpJTIwYXMlMjBhdmdfdHJhbnNhY3Rpb25fdmFsdWUlNUNuJTIwJTIwJTIwJTIwZnJvbSUyMHN1cGVybWFya2V0X3NhbGVzJTVDbiUyMCUyMCUyMCUyMGdyb3VwJTIwYnklMjAlNUMlMjJDdXN0b21lciUyMHR5cGUlNUMlMjIlMkMlMjBCcmFuY2glNUNuKSU1Q24lNUNuc2VsZWN0JTIwJTVDJTIyQ3VzdG9tZXIlMjB0eXBlJTVDJTIyJTJDJTIwQnJhbmNoJTJDJTIwdG90YWxfbGlmZXRpbWVfdmFsdWUlMkMlMjB0cmFuc2FjdGlvbnMlMkMlMjBhdmdfdHJhbnNhY3Rpb25fdmFsdWUlNUNuZnJvbSUyMGN1c3RvbWVyX2xpZmV0aW1lX3ZhbHVlJTVDbm9yZGVyJTIwYnklMjB0b3RhbF9saWZldGltZV92YWx1ZSUyMGRlc2MlNUNuJTNCJTIyJTJDJTIycmVzdWx0JTIyJTNBJTVCJTVEJTJDJTIyZXJyb3IlMjIlM0FudWxsJTdEJTdEJTJDJTIyYWN0aXZlUXVlcnlJZCUyMiUzQTE3MzQyMTU3MzQuMTAyMDQ1OCUyQyUyMmFjdGl2ZVRhYmxlTWV0YWRhdGFDb2x1bW5zJTIyJTNBJTVCJTVEJTJDJTIybG9jYWxUYWJsZXNUb1dhcm4lMjIlM0ElNUIlNUQlMkMlMjJpc1F1ZXJ5SW5Qcm9ncmVzcyUyMiUzQWZhbHNlJTJDJTIyZGlkQWRkTmV3VGFibGVTdWNjZWVkJTIyJTNBbnVsbCUyQyUyMmFkZE5ld1RhYmxlRXJyb3IlMjIlM0FudWxsJTJDJTIyZHJvcFRhYmxlTmFtZSUyMiUzQSUyMnN1cGVybWFya2V0X3NhbGVzJTIyJTJDJTIyZGVsZXRlUXVlcnlJZCUyMiUzQTE3MzQ5MTMyMzEuMDczMjY3JTdE)


## Objectives
Identify overall sales trends across branches and product lines.

Examine payment method preferences.

Determine sales performance by branch, gender, and product line.

Explore customer behavior through metrics like ratings and quantity purchased.

## Key Insights
**Total Sales by Branch:**

Sales were calculated for each branch, revealing the top-performing branches.
  
**Customer Ratings:**

The average customer rating was analyzed by city to assess customer satisfaction trends.

**Payment Methods:**

The most frequently used payment methods were identified for each branch.

**Gender-Based Sales:**

Total sales were grouped by gender and branch to uncover purchasing patterns.

**Product Line Analysis:**

The best-selling product lines and their sales distributions were explored by branch.

**Monthly Sales Trends:**

Monthly sales totals were calculated to identify seasonal trends.

**Peak Shopping Hours:**

Peak hours for transactions were identified using timestamps.

**Most Popular Products:**

The most popular product lines were ranked for each branch based on sales totals.

## How to Reproduce the Analysis

Import the supermarket_sales.csv file located in this repository into a relational database or SQL tool of your choice.

Use the provided SQL queries to analyze the data.

Additionally, you can import the supermarket_sales.csv file into the csv fiddle site at the link above where the queries are already saved.

## Conclusion

This analysis provides actionable insights for supermarket management to optimize operations, improve sales strategies, and enhance customer experience.

This data was sourced from Kaggle, which can be found here: https://www.kaggle.com/datasets/aungpyaeap/supermarket-sales/data
