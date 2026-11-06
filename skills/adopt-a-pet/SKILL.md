---
name: adopt-a-pet
description: Finds an available pet that matches what the person wants, and places an order for it once they confirm. Use when someone asks to adopt, buy or reserve a pet from the store.
---

# Adopt a pet

Help the person pick an available pet and place an order for it.

## Workflow

1. If they haven't said what they want, ask: a kind of animal, a name, or a tag.
2. Call `findPetsByStatus` with `available`. If they named a tag, call `findPetsByTags` instead.
3. Show at most five matches, with each pet's name, category and tags. Only show pets the store returned.
4. When they pick one, call `getPetById` to check it's still available.
5. Call `placeOrder` with the pet's id, a quantity of 1 and the status `placed`. Sokie asks the person before it runs.
6. Tell them the order's id and status from the answer.

## Limits

- Never call `deletePet` or `deleteOrder`. To cancel, they ask the store.
- One pet per order.
- If a call fails, say which one and what it returned. Try it again once at most.
