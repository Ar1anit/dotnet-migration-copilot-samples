/speckit-constitution Modernize in small, reversible steps. Preserve observable behavior, record unknowns instead of guessing, add tests before replacing legacy dependencies, keep secrets out of code, and require build and test evidence before declaring completion.

/speckit-specify Define the behavior that must remain true when ContosoUniversity's legacy admin notifications are modernized. Cover create, update, and delete notifications for students, courses, instructors, and departments; user-visible message data; retrieval limits; and the rule that notification failure must not fail the business operation. Use existing code as evidence, mark unknowns, and do not choose a cloud technology.

/speckit-clarify Ask only questions that could change behavior or tests: delivery guarantees, ordering, duplicates, timestamp rules, authorization, failure visibility, and whether read state must persist.

/speckit-plan Plan a small, reversible migration from MSMQ to Azure Service Bus for Azure Container Apps. Select and justify a supported .NET LTS, preserve the approved notification contract, use managed identity, isolate the transport behind an interface, add contract tests, and include rollback.

/speckit-tasks Create dependency-ordered tasks for one vertical slice: characterize current behavior, add tests, introduce the transport boundary, add the Service Bus adapter, switch providers through configuration, validate failure behavior, and document rollback.

/speckit-analyze Check that every requirement has a task and test. Flag behavior drift, unsupported assumptions, missing identity or security work, missing rollback, and plan choices that are not traceable to the specification.

/speckit-implement Implement only the first independently testable task. Run its focused tests and build, show the diff and evidence, then stop.

/speckit-converge Compare the implementation and test evidence against the approved specification, plan, and tasks. Add only actionable gap tasks and report complete only when they align.