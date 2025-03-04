# Project Development Protocol

This document defines the standard development protocol for project execution. Adherence to this protocol is critical for consistent, efficient, and successful project outcomes.

## Core Development Cycle: Task-Based Approach

Development follows a task-based paradigm. For each discrete task:

1.  **Define Tests:**  Write automated tests *before* implementation. Tests must explicitly specify expected functionality and acceptance criteria for the task.
2.  **Implement Code:** Develop code to satisfy task requirements and pass all defined tests. Code must adhere to project coding standards.
3.  **Execute Tests:** Run all relevant tests post-implementation. Verify successful test completion to confirm functional correctness.

**Requirement Acquisition: README.md Reference**

Project requirements and feature specifications are documented in the `README.md` file. **Mandatory compliance**:  Consult `README.md` *prior* to commencing any development activity.  This is fundamental for aligning development with project objectives.

**Feature Sequencing: Ordered Implementation**

Implement features sequentially, as defined in project documentation. Begin with the initial feature and proceed in listed order. This promotes structured and manageable development progression.

**Project State Persistence: Memory File (`memory.md`)**

Maintain a `memory.md` file within the project repository for state persistence and inter-session context retention.

*   **File Purpose:** `memory.md` serves as the central repository for project state, critical notes, and persistent data required between development sessions.
*   **Content Management:**  Actively update `memory.md` to reflect the current project state. Ensure information is accurate and current.
*   **Task Tracking Separation:** Task completion status is managed in a dedicated To-Do list. **Do not** duplicate task completion tracking within `memory.md`.

## Protocol Evolution: Adaptive Guidelines

This development protocol is designed to be adaptable.  Incorporate learnings and process improvements discovered during development. **Protocol updates are encouraged** to reflect enhanced methodologies or refined understanding of project needs.  Modify this document as necessary to maintain its relevance and efficacy.

---

## Social Feature Module: Finance Application Enhancement

This section details the integration of social media features into the finance application, designed to enhance user engagement and platform interactivity.

**Social Feature Specification:**

The following social features are designated for implementation:

1.  **User Profiles:**
    *   Functionality:  Personalized profiles for users to present investment history, trading style, and biographical information.
    *   Data Points: Portfolio performance metrics, trading activity summaries, investment philosophy description, follower/following counts, achievement indicators.
2.  **Follower/Following System:**
    *   Functionality: Users can follow other users to track investment strategies and activities.
    *   Data Model:  Establish relationships between users to represent follower/following connections.
3.  **Activity Feed:**
    *   Functionality:  Aggregated feed displaying recent trading activities and portfolio changes from followed users.
    *   Content Source: Real-time updates from the trading system and user portfolio management modules.
4.  **Investment Groups/Communities:**
    *   Functionality: Platform for users to form or join groups focused on investment strategy discussion and knowledge sharing.
    *   Features: Group creation, membership management, discussion forums, resource sharing.
5.  **Trade Sharing:**
    *   Functionality:  Users can share completed trades with optional commentary on strategy and rationale.
    *   Content Output: Shared trades become entries in the activity feed, enriching social content.
6.  **Performance Leaderboards:**
    *   Functionality: Ranking of users based on portfolio growth percentage or other key performance indicators (KPIs).
    *   Metrics:  Portfolio growth, risk-adjusted returns, or other quantifiable investment performance metrics.
7.  **Comment and Reaction System:**
    *   Functionality:  Users can comment on shared trades and react using emojis or text-based responses.
    *   Interaction Type:  Textual comments, emoji reactions, threaded discussions.

---

## Social Feature Implementation Plan: Phased Approach

Implementation will proceed in a structured, phased manner. Phases are sequential and build upon preceding phases.

**Implementation Phases:**

1.  **Phase 1: Database Schema Modification:**
    *   Task: Extend the database schema to support social features.
    *   Artifacts:  Creation of new tables: `profiles`, `followers`, `posts`, `comments`, `likes`, `groups`, `group_members`.
    *   Output: Updated database schema definition (SQL DDL or ORM schema).
2.  **Phase 2: Route Implementation (API Endpoints):**
    *   Task:  Implement new API routes in the Flask application to expose social features.
    *   Routes:  `/profile`, `/profile/{username}`, `/feed`, `/follow/{username}`, `/unfollow/{username}`, `/post/new`, `/post/{post_id}`, `/groups`, `/group/{group_id}`, `/leaderboard`.
    *   Output:  Flask route definitions and corresponding controller logic.
3.  **Phase 3: User Profile Enhancement (Data Model & Presentation):**
    *   Task: Enhance user registration and profile management to include social profile data.
    *   Components:  Data model updates, profile page template development, data persistence logic.
    *   Output: Enhanced user profile data model and user interface components.
4.  **Phase 4: Frontend Integration (UI/UX):**
    *   Task: Develop and integrate frontend user interfaces for social features within the application.
    *   UI Elements: Social feed component, user profile display components, post creation forms, comment sections, navigation updates.
    *   Output: Frontend templates and UI logic integrated into the application.
5.  **Phase 5: Trade Sharing Functionality (Core Feature):**
    *   Task: Implement core trade sharing functionality, linking trades to the social feed.
    *   Integration Points: Trade execution module, activity feed generation, user notification mechanisms.
    *   Output: Functional trade sharing feature integrated with social components.
6.  **Phase 6: Group and Leaderboard Implementation (Community Features):**
    *   Task: Implement group creation, management, and leaderboard functionality.
    *   Features: Group management interfaces, leaderboard generation algorithms, ranking display components.
    *   Output:  Functional group and leaderboard features integrated into the application.

## Immediate Action Items: Next Steps for Execution

For immediate progression, execute the following steps in sequence:

1.  **Initiate Database Schema Extension:** Begin the process of modifying the database schema as defined in Phase 1.
2.  **Develop User Profile Enhancement:** Implement the data model and UI updates for enhanced user profiles (Phase 3).
3.  **Implement Follower/Following System:** Develop the core logic for the follower/following functionality (Phase 2 routes and Phase 3 data model).
4.  **Construct Activity Feed Component:**  Build the initial framework for the social activity feed (Phase 4 UI and Phase 2 routes).
5.  **Develop Posting and Commenting Features:** Implement the core posting and commenting functionalities (Phase 2 routes and Phase 4 UI).
6.  **Implement Group and Leaderboard Features:** Develop the group and leaderboard functionalities as defined (Phase 6).

Proceed with database schema modifications as the initial action. Confirm readiness to commence Phase 1.
