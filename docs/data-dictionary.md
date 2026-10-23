# Data dictionary: EPL 2024/25 prepared dataset

| Column   | Meaning                          | Type              | Allowed values / format |
|----------|----------------------------------|-------------------|-------------------------|
| Date     | Day the match was played         | date              | YYYY-MM-DD, 2024-08-16 to 2025-05-25 |
| HomeTeam | Club playing at its home ground  | text              | 20 club names |
| AwayTeam | Visiting club                    | text              | 20 club names |
| FTHG     | Full-time home-team goals        | non-negative int  | 0–7 in this season |
| FTAG     | Full-time away-team goals        | non-negative int  | 0–7 in this season |
| FTR      | Full-time result                 | code              | H = home win, D = draw, A = away win |
| HTHG     | Half-time home-team goals        | non-negative int  | |
| HTAG     | Half-time away-team goals        | non-negative int  | |
| Referee  | Match referee (initial + surname)| text              | 24 distinct referees |

Source: original 22-column CSV (DataHub, from Football-Data.co.uk), 380 rows.
Changes: 13 statistics columns removed; 2 referee names corrected with cited
evidence (row 241: K Kavanagh → C Kavanagh; row 319: O Oliver → M Oliver).
Full operation log: openrefine/preparation-history.json