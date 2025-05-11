```mermaid
flowchart TD
    A[Login Page<br>index.html]
    B{User Type}
    C[Dashboard<br>dashboard.html]
    D[Management Page<br>management.html]
    Z[Login Error<br>or Message]
    L[Logout]

    %% Regular user pages
    E[Add Transaction<br>add-transaction.html]
    F[View Transactions<br>view-transactions.html]
    G[Rejected Transactions<br>view-rejected.html]

    %% Admin pages
    H[All Approved Transactions<br>view-all-approved.html]
    I[All Rejected Transactions<br>view-rejected.html]
    J[All Users<br>view-all-users.html]
    K[Pending Transactions<br>view-pending.html]

    %% Arrows
    A --> B
    B -- Regular --> C
    B -- foodgod --> D
    B -- Not Found --> Z
    Z --> A

    %% Regular dashboard
    C --> E
    C --> F
    C --> G
    C --> L

    %% Add Transaction page
    E --> C

    %% Regular transactions page
    F --> C

    %% Rejected transactions page
    G --> C

    %% Admin management page
    D --> H
    D --> I
    D --> J
    D --> K
    D --> L

    %% Approved transactions page
    H --> D

    %% All users page
    J --> D

    %% Pending transactions page
    K --> D

    %% Logout
    L --> A
