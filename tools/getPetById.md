---
operation: GET /pet/{petId}
title: Find pet by ID
risk: read
---

Looks up one pet by its numeric id and returns its name, category, tags, photo URLs and status: available, pending or sold. Use it after findPetsByStatus or findPetsByTags to check a pet before ordering it.
