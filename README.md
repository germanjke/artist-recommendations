### Little bit about Data Preparation

### Base approach:
1. Filter sessions by `numtracks > 5` and `playcount > 900` 
2. Only tracks with `playtime > 60`
3. Build user-item sparse matrix, where values is `count` of listenings of artist

### Upgrade approach:

Same as Base, but with advantage by likes (`count *= 10`) if `user-track` pair contains in `like dataframe`

### Algorithm:
ALS

### Metric:
Mean Average Precision at k
