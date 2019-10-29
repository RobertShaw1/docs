---
layout: default
description: ArangoDB v3.6 Release Notes New Features
---
Features and Improvements in ArangoDB 3.6
=========================================

The following list shows in detail which features have been added or improved in
ArangoDB 3.6. ArangoDB 3.6 also contains several bug fixes that are not listed
here.

AQL
---

### SmartJoins for Views

In AQL queries views are now considered for SmartJoins. All rules for
collections apply unchanged. A view qualifies for a SmartJoin if the
following conditions are met: all collections forming the view are sharded
equally. One of those collections is picked to represent the view and must
fulfill the already known requirements with the join partner. The partner may be
a collection or another View.
