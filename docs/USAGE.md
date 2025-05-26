# Usage

The API exposes the following types of annotations that can be used currently:

- `@Requires(lock)`
- `@Acquires(lock)`

## Breakdown

### Requires

A function may be annotated with `Requires` signifying that the thread that calls this function should already have the lock. The function should be able to then proceded and directly reference the critical section.

### Acquires

A function should be able to acquire the current lock.

### Return

A function will "return" a lock by maintaining it on return within the thread it is running in. 

## Todo

Ownership constraints like Rust maybe?
