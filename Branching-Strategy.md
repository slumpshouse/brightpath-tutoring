# BRANCHING-STRATEGY.md

BrightPath Tutoring – Branching Strategy

## Overview

Our team uses a structured Git branching strategy to keep the BrightPath application stable while allowing new features and fixes to be developed safely.

This strategy helps prevent broken updates and ensures production-ready code stays reliable.

---

## 1. Production Branch – `main`

**Purpose:**

The `main` branch contains production-ready code.

**Rules:**

- Only fully tested and approved code can be merged into `main`.
- Code must pass CI checks before merging.
- No direct commits are allowed to `main`.

**Why This Matters:**

This protects BrightPath from downtime by ensuring unstable code does not reach students or teachers.

---

## 2. Integration Branch – `develop`

**Purpose:**

The `develop` branch is where completed features are combined and tested together before going to production.

**Rules:**

- Feature branches are merged into `develop`.
- Integration testing happens here.
- This branch may contain new changes that are not yet in production.

**Why This Matters:**

This prevents new updates from immediately breaking the live system.


## 3. Feature Branches – `feature/*`

**Purpose:**

Feature branches are used to develop new functionality.

**Rules:**

- Created from `develop`
- Used for one specific feature
- Merged back into `develop` via Pull Request

**Why This Matters:**

Keeps new work isolated so unfinished features do not break other parts of the system.

---

## 4. Hotfix Branches – `hotfix/*`

**Purpose:**

Hotfix branches are used for urgent production issues.


**Rules:**

- Created from `main`
- Fix the issue quickly
- Merged back into both `main` and `develop`

**Why This Matters:**

Allows the team to quickly fix critical problems without disrupting ongoing feature development.