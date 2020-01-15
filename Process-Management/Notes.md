# Process Management:
#### Concepts:
* The app should be executed in the execution env (container, usually) as one or more processes.
* Processes are stateless and share nothing.
* Any data that needs to persist is stored in a stateful backing service (database).
* Never assume anything cached in memory or on disk will be available for a future request.
#### Action Items:
* ALWAYS:
  * Use services like redis for ephemeral storage.
  * Use services like cockroachdb for persistent storage.
