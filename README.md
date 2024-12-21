# supermarket_sales
Data exploration on supermarket sales using SQL.
[Link] (https://csvfiddle.io/#JTdCJTIyaXNUYWJsZU1ldGFkYXRhT3BlbiUyMiUzQWZhbHNlJTJDJTIyaXNOZXdUYWJsZUZvcm1PcGVuJTIyJTNBZmFsc2UlMkMlMjJpc0NvbmZpcm1EZWxldGVRdWVyeU9wZW4lMjIlM0FmYWxzZSUyQyUyMmlzQ29uZmlybURyb3BUYWJsZU9wZW4lMjIlM0FmYWxzZSUyQyUyMmlzU2hhcmVEaWFsb2dPcGVuJTIyJTNBZmFsc2UlMkMlMjJkYlJlYWR5JTIyJTNBZmFsc2UlMkMlMjJ0YWJsZXMlMjIlM0ElNUIlN0IlMjJuYW1lJTIyJTNBJTIyc3VwZXJtYXJrZXRfc2FsZXMlMjIlMkMlMjJ1cmwlMjIlM0FudWxsJTJDJTIyY29sdW1ucyUyMiUzQSU1QiU1RCU3RCU1RCUyQyUyMnF1ZXJpZXMlMjIlM0ElN0IlMjIxNzMzMDcwMDA2LjMwNjc2MzIlMjIlM0ElN0IlMjJpZCUyMiUzQTE3MzMwNzAwMDYuMzA2NzYzMiUyQyUyMnRpdGxlJTIyJTNBJTIyQWxsJTIwZmllbGRzJTIyJTJDJTIyYm9keSUyMiUzQSUyMi0tQSUyMGxvb2slMjBhdCUyMHRoZSUyMGRhdGFzZXQtLSU1Q24lNUNuc2VsZWN0JTIwKiU1Q25mcm9tJTIwc3VwZXJtYXJrZXRfc2FsZXMlNUNubGltaXQlMjAxNSU1Q24lM0IlMjIlMkMlMjJyZXN1bHQlMjIlM0ElNUIlNUQlMkMlMjJlcnJvciUyMiUzQW51bGwlN0QlMkMlMjIxNzMzMDcxMTg1LjY5MDQwMTglMjIlM0ElN0IlMjJpZCUyMiUzQTE3MzMwNzExODUuNjkwNDAxOCUyQyUyMnRpdGxlJTIyJTNBJTIyMS4wJTIwVG90YWwlMjBzYWxlcyUyMHBlciUyMGJyYW5jaCUyMiUyQyUyMmJvZHklMjIlM0ElMjItLVRvdGFsJTIwc2FsZXMlMjBwZXIlMjBicmFuY2gtLSU1Q24lNUNuc2VsZWN0JTIwQnJhbmNoJTJDJTIwcm91bmQoc3VtKFRvdGFsKSUyQyUyMDIpJTIwYXMlMjB0b3RhbF9zYWxlcyUyQyUyMHJvdW5kKHN1bShjb2dzKSUyQyUyMDIpJTIwYXMlMjB0b3RhbF9jb3N0X29mX2dvb2RzJTJDJTIwcm91bmQoc3VtKCU1QyUyMmdyb3NzJTIwaW5jb21lJTVDJTIyKSUyQyUyMDIpJTIwYXMlMjBncm9zc19pbmNvbWUlNUNuZnJvbSUyMHN1cGVybWFya2V0X3NhbGVzJTVDbmdyb3VwJTIwYnklMjBCcmFuY2glNUNub3JkZXIlMjBieSUyMHRvdGFsX3NhbGVzJTIwZGVzYyU1Q24lM0IlMjIlMkMlMjJyZXN1bHQlMjIlM0ElNUIlNUQlMkMlMjJlcnJvciUyMiUzQW51bGwlN0QlMkMlMjIxNzMzMTc5NjAxLjU2NzY5OCUyMiUzQSU3QiUyMmlkJTIyJTNBMTczMzE3OTYwMS41Njc2OTglMkMlMjJ0aXRsZSUyMiUzQSUyMjEuMSUyMEF2ZyUyMGN1c3RvbWVyJTIwcmF0aW5nJTIwcGVyJTIwY2l0eSUyMiUyQyUyMmJvZHklMjIlM0ElMjItLUF2ZXJhZ2UlMjBjdXN0b21lciUyMHJhdGluZyUyMHBlciUyMGNpdHktLSU1Q24lNUNuc2VsZWN0JTIwcm91bmQoYXZnKFJhdGluZyklMkMlMjAyKSUyMGFzJTIwYXZnX3JhdGluZyUyQyUyMEJyYW5jaCU1Q25mcm9tJTIwc3VwZXJtYXJrZXRfc2FsZXMlNUNuZ3JvdXAlMjBieSUyMEJyYW5jaCU1Q25vcmRlciUyMGJ5JTIwYXZnX3JhdGluZyUyMGRlc2MlNUNuJTNCJTIyJTJDJTIycmVzdWx0JTIyJTNBJTVCJTVEJTJDJTIyZXJyb3IlMjIlM0FudWxsJTdEJTJDJTIyMTczMzI0NTkxNy42NzQ2MDA0JTIyJTNBJTdCJTIyaWQlMjIlM0ExNzMzMjQ1OTE3LjY3NDYwMDQlMkMlMjJ0aXRsZSUyMiUzQSUyMjEuMiUyMEJyZWFrZG93biUyMG9mJTIwcGF5bWVudCUyMG1ldGhvZHMlMjIlMkMlMjJib2R5JTIyJTNBJTIyLS1CcmVha2Rvd24lMjBvZiUyMHBheW1lbnQlMjBtZXRob2RzJTIwYnklMjBicmFuY2gtLSU1Q24lNUNuc2VsZWN0JTIwQnJhbmNoJTJDJTIwUGF5bWVudCUyQyUyMGNvdW50KCopJTIwYXMlMjBwYXltZW50X2JyZWFrZG93biU1Q25mcm9tJTIwc3VwZXJtYXJrZXRfc2FsZXMlNUNuZ3JvdXAlMjBieSUyMFBheW1lbnQlMkMlMjBCcmFuY2glNUNub3JkZXIlMjBieSUyMEJyYW5jaCU1Q24lM0IlMjIlMkMlMjJyZXN1bHQlMjIlM0ElNUIlNUQlMkMlMjJlcnJvciUyMiUzQW51bGwlN0QlMkMlMjIxNzMzMzUyMDY0LjM1MzQ2MjclMjIlM0ElN0IlMjJpZCUyMiUzQTE3MzMzNTIwNjQuMzUzNDYyNyUyQyUyMnRpdGxlJTIyJTNBJTIyMi4wJTIwVG90YWxzJTIwYnklMjBwcm9kdWN0JTIwbGluZSUyMGdyb3VwZWQlMjBieSUyMGdlbmRlciUyMiUyQyUyMmJvZHklMjIlM0ElMjItLVRvdGFscyUyMGJ5JTIwcHJvZHVjdCUyMGxpbmUlMjBncm91cGVkJTIwYnklMjBnZW5kZXItLSU1Q24lNUNuc2VsZWN0JTIwJTVDJTIyUHJvZHVjdCUyMGxpbmUlNUMlMjIlMkMlMjBHZW5kZXIlMkMlMjByb3VuZChzdW0oVG90YWwpJTJDJTIwMiklMjBhcyUyMHByb2R1Y3RfbGluZV90b3RhbCUyQyUyMGNvdW50KCopJTIwYXMlMjBwdXJjaGFzZV9jb3VudCU1Q25mcm9tJTIwc3VwZXJtYXJrZXRfc2FsZXMlNUNuZ3JvdXAlMjBieSUyMCU1QyUyMlByb2R1Y3QlMjBsaW5lJTVDJTIyJTJDJTIwR2VuZGVyJTVDbm9yZGVyJTIwYnklMjAlNUMlMjJQcm9kdWN0JTIwbGluZSU1QyUyMiUyQyUyMHByb2R1Y3RfbGluZV90b3RhbCUyMGRlc2MlNUNuJTNCJTIyJTJDJTIycmVzdWx0JTIyJTNBJTVCJTVEJTJDJTIyZXJyb3IlMjIlM0FudWxsJTdEJTJDJTIyMTczNDIxNTczNC4xMDIwNDU4JTIyJTNBJTdCJTIyaWQlMjIlM0ExNzM0MjE1NzM0LjEwMjA0NTglMkMlMjJ0aXRsZSUyMiUzQSUyMjIuMSUyMFBlYWslMjBzaG9wcGluZyUyMGhvdXJzJTIyJTJDJTIyYm9keSUyMiUzQSUyMi0tUGVhayUyMHNob3BwaW5nJTIwaG91cnMtLSU1Q24lNUNud2l0aCUyMGhvdXJseV9zYWxlcyUyMGFzJTIwKCU1Q24lMjAlMjAlMjAlMjBzZWxlY3QlMjBsZWZ0KFRpbWUlMkMlMjAyKSUyMGFzJTIwaG91ciUyQyUyMGNvdW50KCopJTIwYXMlMjB0cmFuc2FjdGlvbl9jb3VudCUyQyUyMHJvdW5kKHN1bShUb3RhbCklMkMlMjAyKSUyMGFzJTIwdG90YWxfcmV2ZW51ZSU1Q24lMjAlMjAlMjAlMjBmcm9tJTIwc3VwZXJtYXJrZXRfc2FsZXMlNUNuJTIwJTIwJTIwJTIwZ3JvdXAlMjBieSUyMGhvdXIlNUNuKSU1Q24lNUNuc2VsZWN0JTIwKiU1Q25mcm9tJTIwaG91cmx5X3NhbGVzJTVDbm9yZGVyJTIwYnklMjB0cmFuc2FjdGlvbl9jb3VudCUyMGRlc2MlNUNuJTNCJTIyJTJDJTIycmVzdWx0JTIyJTNBJTVCJTVEJTJDJTIyZXJyb3IlMjIlM0FudWxsJTdEJTJDJTIyMTczNDI5NTg1My43MTA5OTIlMjIlM0ElN0IlMjJpZCUyMiUzQTE3MzQyOTU4NTMuNzEwOTkyJTJDJTIydGl0bGUlMjIlM0ElMjIyLjIlMjBNb3N0JTIwcG9wdWxhciUyMHByb2R1Y3QlMjBsaW5lJTIwZm9yJTIwZWFjaCUyMGJyYW5jaCUyMiUyQyUyMmJvZHklMjIlM0ElMjItLU1vc3QlMjBwb3B1bGFyJTIwcHJvZHVjdCUyMGxpbmUlMjBmb3IlMjBlYWNoJTIwYnJhbmNoLS0lNUNuJTVDbndpdGglMjBhZ2dyZWdhdGVkX3RvdGFsJTIwYXMlMjAoJTVDbiUyMCUyMCUyMCUyMHNlbGVjdCUyMEJyYW5jaCUyQyUyMCU1QyUyMlByb2R1Y3QlMjBsaW5lJTVDJTIyJTJDJTIwcm91bmQoc3VtKFRvdGFsKSUyQyUyMDIpJTIwYXMlMjB0b3RhbF9yZXZlbnVlJTVDbiUyMCUyMCUyMCUyMGZyb20lMjBzdXBlcm1hcmtldF9zYWxlcyU1Q24lMjAlMjAlMjAlMjBncm91cCUyMGJ5JTIwQnJhbmNoJTJDJTIwJTVDJTIyUHJvZHVjdCUyMGxpbmUlNUMlMjIlNUNuKSUyQyU1Q25yYW5rZWRfc2FsZXMlMjBhcyUyMCglNUNuJTIwJTIwJTIwJTIwc2VsZWN0JTIwQnJhbmNoJTJDJTVDbiUyMCUyMCUyMCUyMCU1QyUyMlByb2R1Y3QlMjBsaW5lJTVDJTIyJTJDJTVDbiUyMCUyMCUyMCUyMHRvdGFsX3JldmVudWUlMkMlNUNuJTIwJTIwJTIwJTIwcmFuaygpJTIwb3ZlciUyMChwYXJ0aXRpb24lMjBieSUyMEJyYW5jaCUyMG9yZGVyJTIwYnklMjB0b3RhbF9yZXZlbnVlJTIwZGVzYyklMjBhcyUyMHJhbmslNUNuJTIwJTIwJTIwJTIwZnJvbSUyMGFnZ3JlZ2F0ZWRfdG90YWwlNUNuKSUyMCUyMCUyMCUyMCU1Q24lNUNuc2VsZWN0JTIwQnJhbmNoJTJDJTIwJTVDJTIyUHJvZHVjdCUyMGxpbmUlNUMlMjIlMkMlMjB0b3RhbF9yZXZlbnVlJTVDbmZyb20lMjByYW5rZWRfc2FsZXMlNUNud2hlcmUlMjByYW5rJTIwJTNEJTIwMSU1Q25vcmRlciUyMGJ5JTIwQnJhbmNoJTVDbiUzQiUyMiUyQyUyMnJlc3VsdCUyMiUzQSU1QiU1RCUyQyUyMmVycm9yJTIyJTNBbnVsbCU3RCUyQyUyMjE3MzQzMDYwNzguNDIyMjAxNCUyMiUzQSU3QiUyMmlkJTIyJTNBMTczNDMwNjA3OC40MjIyMDE0JTJDJTIydGl0bGUlMjIlM0ElMjIzLjAlMjBNb250aGx5JTIwc2FsZXMlMjBieSUyMGJyYW5jaCUyMiUyQyUyMmJvZHklMjIlM0ElMjItLSUyME1vbnRobHklMjBzYWxlcyUyMGJ5JTIwYnJhbmNoJTIwYW5kJTIwYmVzdCUyMHNlbGxpbmclMjBwcm9kdWN0JTIwbGluZS0tJTVDbiU1Q253aXRoJTVDbiU1Q24tLSUyME1vbnRobHklMjBzYWxlcyUyMGJ5JTIwYnJhbmNoLS0lNUNuJTVDbm1vbnRobHlfc2FsZXMlMjBhcyglNUNuJTIwJTIwJTIwJTIwc2VsZWN0JTIwQnJhbmNoJTJDJTIwbW9udGgoRGF0ZSklMjBhcyUyMG1vbnRoJTJDJTIwcm91bmQoc3VtKFRvdGFsKSUyQyUyMDIpJTIwYXMlMjB0b3RhbF9zYWxlcyU1Q24lMjAlMjAlMjAlMjBmcm9tJTIwc3VwZXJtYXJrZXRfc2FsZXMlNUNuJTIwJTIwJTIwJTIwZ3JvdXAlMjBieSUyMEJyYW5jaCUyQyUyMG1vbnRoJTVDbiklMkMlNUNuJTVDbi0tTW9udGhseSUyMHNhbGVzJTIwYnklMjBwcm9kdWN0JTIwbGluZSUyMGZvciUyMGVhY2glMjBicmFuY2gtLSU1Q24lNUNucHJvZHVjdF9saW5lX3NhbGVzJTIwYXMlMjAoJTVDbiUyMCUyMCUyMCUyMHNlbGVjdCUyMEJyYW5jaCUyQyUyMG1vbnRoKERhdGUpJTIwYXMlMjBtb250aCUyQyUyMCU1QyUyMlByb2R1Y3QlMjBsaW5lJTVDJTIyJTJDJTIwcm91bmQoc3VtKFRvdGFsKSUyQyUyMDIpJTIwYXMlMjBwcm9kdWN0X2xpbmVfdG90YWwlNUNuJTIwJTIwJTIwJTIwZnJvbSUyMHN1cGVybWFya2V0X3NhbGVzJTVDbiUyMCUyMCUyMCUyMGdyb3VwJTIwYnklMjBCcmFuY2glMkMlMjBtb250aCUyQyUyMCU1QyUyMlByb2R1Y3QlMjBsaW5lJTVDJTIyJTVDbiklMkMlNUNuJTVDbi0tJTIwSWRlbnRpZnklMjB0aGUlMjBiZXN0JTIwc2VsbGluZyUyMHByb2R1Y3QlMjBsaW5lJTIwcGVyJTIwYnJhbmNoJTIwcGVyJTIwbW9udGgtLSU1Q24lNUNucmFua2VkX3Byb2R1Y3RfbGluZXMlMjBhcyUyMCglNUNuJTIwJTIwJTIwJTIwc2VsZWN0JTIwQnJhbmNoJTJDJTVDbiUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMG1vbnRoJTJDJTVDbiUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCU1QyUyMlByb2R1Y3QlMjBsaW5lJTVDJTIyJTJDJTVDbiUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMHByb2R1Y3RfbGluZV90b3RhbCUyQyU1Q24lMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjByYW5rKCklMjBvdmVyJTIwKHBhcnRpdGlvbiUyMGJ5JTIwQnJhbmNoJTJDJTIwbW9udGglMjBvcmRlciUyMGJ5JTIwcHJvZHVjdF9saW5lX3RvdGFsJTIwZGVzYyklMjBhcyUyMHJhbmslNUNuJTIwJTIwJTIwJTIwZnJvbSUyMHByb2R1Y3RfbGluZV9zYWxlcyU1Q24pJTVDbiU1Q24tLUNvbWJpbmUlMjBtb250aGx5JTIwc2FsZXMlMjB3aXRoJTIwdGhlJTIwYmVzdCUyMHNlbGxpbmclMjBwcm9kdWN0JTIwbGluZXMtLSU1Q24lNUNuc2VsZWN0JTVDbiUyMCUyMCUyMCUyMG1zLkJyYW5jaCUyQyU1Q24lMjAlMjAlMjAlMjBtcy5tb250aCUyQyU1Q24lMjAlMjAlMjAlMjBtcy50b3RhbF9zYWxlcyUyQyU1Q24lMjAlMjAlMjAlMjBycGwuJTVDJTIyUHJvZHVjdCUyMGxpbmUlNUMlMjIlMjBhcyUyMGJlc3Rfc2VsbGluZ19wcm9kdWN0X2xpbmUlMkMlNUNuJTIwJTIwJTIwJTIwcnBsLnByb2R1Y3RfbGluZV90b3RhbCUyMGFzJTIwYmVzdF9zZWxsaW5nX3Byb2R1Y3RfbGluZV9zYWxlcyUyQyU1Q24lMjAlMjAlMjAlMjByYW5rKCklMjBvdmVyJTIwKHBhcnRpdGlvbiUyMGJ5JTIwbXMubW9udGglMjBvcmRlciUyMGJ5JTIwbXMudG90YWxfc2FsZXMlMjBkZXNjKSUyMGFzJTIwcmFuayU1Q25mcm9tJTIwbW9udGhseV9zYWxlcyUyMGFzJTIwbXMlNUNubGVmdCUyMGpvaW4lMjByYW5rZWRfcHJvZHVjdF9saW5lcyUyMGFzJTIwcnBsJTVDbm9uJTIwbXMuQnJhbmNoJTIwJTNEJTIwcnBsLkJyYW5jaCUyMGFuZCUyMG1zLm1vbnRoJTIwJTNEJTIwcnBsLm1vbnRoJTIwYW5kJTIwcnBsLnJhbmslMjAlM0QlMjAxJTVDbm9yZGVyJTIwYnklMjBtcy5CcmFuY2glMkMlMjBtcy5tb250aCU1Q24lM0IlMjIlMkMlMjJyZXN1bHQlMjIlM0ElNUIlNUQlMkMlMjJlcnJvciUyMiUzQW51bGwlN0QlMkMlMjIxNzM0MzA5ODI4LjI4OTY2JTIyJTNBJTdCJTIyaWQlMjIlM0ExNzM0MzA5ODI4LjI4OTY2JTJDJTIydGl0bGUlMjIlM0ElMjIzLjElMjBTYWxlcyUyMGJ5JTIwY3VzdG9tZXIlMjB0eXBlJTIwb3ZlciUyMHRpbWUlMjIlMkMlMjJib2R5JTIyJTNBJTIyLS0lMjBTcGVuZGluZyUyMGJ5JTIwY3VzdG9tZXIlMjB0eXBlJTIwb3ZlciUyMHRpbWUlMjAtLSU1Q24lNUNuLS0lMjBjdGUlMjB0byUyMGFnZ3JlZ2F0ZSUyMG1vbnRobHklMjBzcGVuZCUyQyUyMGdyb3VwJTIwYnklMjBjdXN0b21lciUyMHR5cGUlMjBhbmQlMjBtb250aCUyQyUyMGNhc2UlMjBzdGF0ZW1lbnQlMjB0byUyMGxhYmVsJTIwbW9udGhzJTIwLS0lNUNud2l0aCUyMG1vbnRoc19sYWJlbGVkJTIwYXMlMjAoJTVDbiUyMCUyMCUyMCUyMHNlbGVjdCUyMCU1QyUyMkN1c3RvbWVyJTIwdHlwZSU1QyUyMiUyQyUyMHJvdW5kKGF2ZyhUb3RhbCklMkMlMjAyKSUyMGFzJTIwbW9udGhseV9zcGVuZCUyQyUyMG1vbnRoKERhdGUpJTIwYXMlMjBtb250aF9udW1lcmljYWwlMkMlNUNuJTIwJTIwJTIwJTIwY2FzZSU1Q24lMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjB3aGVuJTIwbW9udGgoRGF0ZSklMjAlM0QlMjAxJTIwdGhlbiUyMCdKYW51YXJ5JyU1Q24lMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjB3aGVuJTIwbW9udGgoRGF0ZSklMjAlM0QlMjAyJTIwdGhlbiUyMCdGZWJydWFyeSclNUNuJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwd2hlbiUyMG1vbnRoKERhdGUpJTIwJTNEJTIwMyUyMHRoZW4lMjAnTWFyY2gnJTVDbiUyMCUyMCUyMCUyMGVuZCUyMGFzJTIwbW9udGhzJTVDbiUyMCUyMCUyMCUyMGZyb20lMjBzdXBlcm1hcmtldF9zYWxlcyU1Q24lMjAlMjAlMjAlMjBncm91cCUyMGJ5JTIwJTVDJTIyQ3VzdG9tZXIlMjB0eXBlJTVDJTIyJTJDJTIwbW9udGhfbnVtZXJpY2FsJTVDbiklNUNuJTVDbnNlbGVjdCUyMColNUNuZnJvbSUyMG1vbnRoc19sYWJlbGVkJTVDbm9yZGVyJTIwYnklMjBtb250aF9udW1lcmljYWwlMjBhc2MlNUNuJTNCJTIyJTJDJTIycmVzdWx0JTIyJTNBJTVCJTVEJTJDJTIyZXJyb3IlMjIlM0FudWxsJTdEJTJDJTIyMTczNDgxNDkzMS4yNTQzOTElMjIlM0ElN0IlMjJpZCUyMiUzQTE3MzQ4MTQ5MzEuMjU0MzkxJTJDJTIydGl0bGUlMjIlM0ElMjIzLjIlMjBDdXN0b21lciUyMExpZmV0aW1lJTIwVmFsdWUlMjIlMkMlMjJib2R5JTIyJTNBJTIyLS0lMjBDdXN0b21lciUyMGxpZmV0aW1lJTIwdmFsdWUlMjAoQ0xWKSUyMC0tJTVDbiU1Q253aXRoJTIwY3VzdG9tZXJfbGlmZXRpbWVfdmFsdWUlMjBhcyUyMCglNUNuJTIwJTIwJTIwJTIwc2VsZWN0JTIwJTVDJTIyQ3VzdG9tZXIlMjB0eXBlJTVDJTIyJTJDJTVDbiUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMEJyYW5jaCUyQyU1Q24lMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjAlMjByb3VuZChzdW0oJTVDJTIyZ3Jvc3MlMjBpbmNvbWUlNUMlMjIpJTJDJTIwMiklMjBhcyUyMHRvdGFsX2xpZmV0aW1lX3ZhbHVlJTJDJTVDbiUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMGNvdW50KCopJTIwYXMlMjB0cmFuc2FjdGlvbnMlMkMlNUNuJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwJTIwcm91bmQoc3VtKCU1QyUyMmdyb3NzJTIwaW5jb21lJTVDJTIyKSUyMCUyRiUyMGNvdW50KCopJTJDJTIwMiklMjBhcyUyMGF2Z190cmFuc2FjdGlvbl92YWx1ZSU1Q24lMjAlMjAlMjAlMjBmcm9tJTIwc3VwZXJtYXJrZXRfc2FsZXMlNUNuJTIwJTIwJTIwJTIwZ3JvdXAlMjBieSUyMCU1QyUyMkN1c3RvbWVyJTIwdHlwZSU1QyUyMiUyQyUyMEJyYW5jaCU1Q24pJTVDbiU1Q25zZWxlY3QlMjAlNUMlMjJDdXN0b21lciUyMHR5cGUlNUMlMjIlMkMlMjBCcmFuY2glMkMlMjB0b3RhbF9saWZldGltZV92YWx1ZSUyQyUyMHRyYW5zYWN0aW9ucyUyQyUyMGF2Z190cmFuc2FjdGlvbl92YWx1ZSU1Q25mcm9tJTIwY3VzdG9tZXJfbGlmZXRpbWVfdmFsdWUlNUNub3JkZXIlMjBieSUyMHRvdGFsX2xpZmV0aW1lX3ZhbHVlJTIwZGVzYyU1Q24lM0IlMjIlMkMlMjJyZXN1bHQlMjIlM0ElNUIlNUQlMkMlMjJlcnJvciUyMiUzQW51bGwlN0QlN0QlMkMlMjJhY3RpdmVRdWVyeUlkJTIyJTNBMTczNDgxNDkzMS4yNTQzOTElMkMlMjJhY3RpdmVUYWJsZU1ldGFkYXRhQ29sdW1ucyUyMiUzQSU1QiU1RCUyQyUyMmxvY2FsVGFibGVzVG9XYXJuJTIyJTNBJTVCJTVEJTJDJTIyaXNRdWVyeUluUHJvZ3Jlc3MlMjIlM0FmYWxzZSUyQyUyMmRpZEFkZE5ld1RhYmxlU3VjY2VlZCUyMiUzQW51bGwlMkMlMjJhZGROZXdUYWJsZUVycm9yJTIyJTNBbnVsbCUyQyUyMmRyb3BUYWJsZU5hbWUlMjIlM0ElMjJzdXBlcm1hcmtldF9zYWxlcyUyMiUyQyUyMmRlbGV0ZVF1ZXJ5SWQlMjIlM0ExNzM0MzA1ODE0LjY1ODI4NCU3RA==)
