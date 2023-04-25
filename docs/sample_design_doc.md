---
layout: default
title: Sample Design Doc
---

# Sample Design Document

## Introduction

- **Project Name:** [Project Name]
- **Project Description:** [Project Description]
- **Project Manager:** [Project Manager Name]
- **Designer:** [Designer Name]

## Design Goals

- [ ] [Design Goal]
- [ ] [Design Goal]
- [ ] [Design Goal]

## Design Requirements

- [ ] The design must be [Requirement].
- [ ] The design must be [Requirement].
- [ ] The design must be [Requirement].

## Design Approach

- [ ] [Design Approach]
- [ ] [Design Approach]
- [ ] [Design Approach]

## Design Details

### User Interface Design

<div class="mermaid">
    sequenceDiagram
    participant web as Web Browser
    participant blog as Blog Service
    participant account as Account Service
    participant mail as Mail Service
    participant db as Storage

    Note over web,db: The user must be logged in to submit blog posts
    web->>+account: Logs in using credentials
    account->>db: Query stored accounts
    db->>account: Respond with query result

    alt Credentials not found
        account->>web: Invalid credentials
    else Credentials found
        account->>-web: Successfully logged in

        Note over web,db: When the user is authenticated, they can now submit new posts
        web->>+blog: Submit new post
        blog->>db: Store post data

        par Notifications
            blog--)mail: Send mail to blog subscribers
            blog--)db: Store in-site notifications
        and Response
            blog-->>-web: Successfully posted
        end
    end
</div>
### System Architecture Design

- [ ] [System Architecture Design Detail]
- [ ] [System Architecture Design Detail]
- [ ] [System Architecture Design Detail]

### Data Storage Design

- [ ] [Data Storage Design Detail]
- [ ] [Data Storage Design Detail]
- [ ] [Data Storage Design Detail]

## Technical Considerations

- [ ] [Technical Consideration]
- [ ] [Technical Consideration]
- [ ] [Technical Consideration]

## Assumptions and Constraints

- [ ] [Assumption/Constraint]
- [ ] [Assumption/Constraint]
- [ ] [Assumption/Constraint]

## Acceptance Criteria

- [ ] [Acceptance Criterion]
- [ ] [Acceptance Criterion]
- [ ] [Acceptance Criterion]
