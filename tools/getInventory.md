---
operation: GET /store/inventory
title: Returns pet inventories by status
risk: read
---

Counts the store's pets by status, as a map such as available: 12, pending: 3, sold: 7. Use it for totals; it doesn't list pets, so call findPetsByStatus to see which ones.
