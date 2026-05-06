# Erreur JWT Secret trop court
Date    : 2026-05-06
Projet  : task-manager
Erreur  : IDX10720 key size must be greater than 256 bits
Fix     : dotnet user-secrets set "JWT:Secret" "{32+ chars}"
