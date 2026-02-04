Outlook User-Initiated Automation

This repository captures a simple pattern for email-driven automation scenarios where user intent matters.

Many email automations assume a shared mailbox and background ingestion. That approach works well when every message should be handled the same way. But some workflows depend on an individual deciding that a specific email is actionable, adding context, and then allowing automation to continue.

This repo documents a lightweight way to support that pattern using Outlook as the starting point.

The Pattern

In this approach:

Outlook is the launch surface
The user acts on a specific email and indicates that it is actionable.

The add-in stays intentionally small
It does not run business logic or attempt to automate decisions. Its role is to capture intent and a small amount of structured input.

Everything else happens downstream
Validation, routing, persistence, notifications, and processing are handled by workflows and systems designed for those responsibilities.

The goal is not to replace existing automation patterns, but to recognize when a different starting point better reflects how people actually work.

When This Pattern Fits

This pattern is a good fit when:

The email itself is not the request, but the starting point for a decision
Individual users (often outside a single department) decide which messages matter
Context only becomes clear once the email is read
Shared mailboxes introduce extra handoffs rather than simplifying the work

It is not intended to replace shared mailbox automation for high-volume, repeatable intake scenarios.

What’s in This Repository

This repository is intentionally minimal.

It contains:

A conceptual reference for the pattern
A lightweight Outlook add-in shell (task pane + manifest)
No business logic
No opinionated workflows
No production configuration

It is meant as a reference, not a finished solution.

Related Reading

If you’re interested in the reasoning behind this pattern, see:

Why Some Email Automations Don’t Belong in a Shared Mailbox
[(Medium article link goes here)](https://medium.com/@sassyx/why-some-email-automations-dont-belong-in-a-shared-mailbox-0cf1f1aebf9e)

Notes

This is not a supported product
This is not a full sample application
This repo exists to illustrate design boundaries, not implementation detail
