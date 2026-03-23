```mermaid
gitGraph
    commit id: "Initial commit"

    %% Feature
    branch feature/123
    checkout feature/123
    commit id: "feat: add feature"

    %% Bug
    checkout main
    branch bug/145
    checkout bug/145
    commit id: "fix: bug"

    %% Improvement
    checkout main
    branch improvement/167
    checkout improvement/167
    commit id: "refactor: improvement"

    %% Release
    checkout main
    branch release/1.0.0
    checkout release/1.0.0
    merge feature/123
    merge bug/145
    merge improvement/167
    commit id: "chore: prepare release"

    checkout main
    merge release/1.0.0 tag: "v1.0.0"

    %% Hotfix
    branch hotfix/1.0.1
    checkout hotfix/1.0.1
    commit id: "fix: critical bug"

    checkout main
    merge hotfix/1.0.1 tag: "v1.0.1"