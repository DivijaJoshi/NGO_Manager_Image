# NGO_Manager_Image
Image For Copy Right


```
  graph TD
    %% Styling Definitions
    classDef external fill:#FFE5D9,stroke:#FF7043,stroke-width:2px
    classDef process fill:#E3F2FD,stroke:#1976D2,stroke-width:2px
    classDef database fill:#F3E5F5,stroke:#7B1FA2,stroke-width:2px
    classDef subgraphStyle fill:#F5F5F5,stroke:#9E9E9E,stroke-width:2px
    classDef flow fill:#E8F5E9,stroke:#2E7D32,stroke-width:2px

    %% External Entities
    User((User))
    Admin((Admin))
    EmailService[[Email Service]]

    %% Data Stores
    UserStore[(User DB)]
    TaskStore[(Task DB)]
    EventStore[(Event DB)]
    IdeaStore[(Idea DB)]
    NotificationStore[(Notification DB)]
    DomainStore[(Domain DB)]

    %% Smart Matching System
    subgraph SmartMatching
        direction TB
        InputProcessing[Input Processing]
        DomainMatching[Domain Matching]
        WorkloadAnalysis[Workload Analysis]
        ProfileAnalysis[Profile Analysis]
        ScoringSystem[Scoring System]
        MatchGeneration[Match Generation]
        
        InputProcessing -.-> DomainMatching
        InputProcessing -.-> ProfileAnalysis
        InputProcessing -.-> WorkloadAnalysis
        DomainMatching -.-> ScoringSystem
        ProfileAnalysis -.-> ScoringSystem
        WorkloadAnalysis -.-> ScoringSystem
        ScoringSystem -.-> MatchGeneration
    end

    %% Authentication Flow
    subgraph Authentication
        direction TB
        Login[Login]
        Register[Register]
        ProfileUpdate[Profile Update]
        TokenValidation[Token Validation]
        
        Login -.-> TokenValidation
        Register -.-> UserStore
        ProfileUpdate -.-> UserStore
        TokenValidation -.-> AuthProcess
    end

    %% Task Management Flow
    subgraph TaskManagement
        direction TB
        TaskCreate[Create Task]
        TaskAssign[Assign Task]
        TaskUpdate[Update Status]
        SmartMatch[Smart Match]
        
        TaskCreate -.-> TaskStore
        UserStore -.-> SmartMatch
        SmartMatch -.-> TaskAssign
        TaskAssign -.-> TaskStore
        TaskUpdate -.-> TaskStore
        TaskUpdate -.-> NotificationProcess
    end

    %% Notification Flow
    subgraph Notifications
        direction TB
        NotifGenerate[Generate]
        BirthdayNotif[Birthday]
        TaskNotif[Task]
        EventNotif[Event]
        
        UserStore -.-> BirthdayNotif
        TaskStore -.-> TaskNotif
        EventStore -.-> EventNotif
        BirthdayNotif -.-> NotifGenerate
        TaskNotif -.-> NotifGenerate
        EventNotif -.-> NotifGenerate
        NotifGenerate -.-> NotificationStore
    end

    %% Analytics Flow
    subgraph Analytics
        direction TB
        ETL[Process]
        AnalyticsProcess[Analyze]
        Visualization[Dashboard]
        
        UserStore -.-> ETL
        TaskStore -.-> ETL
        EventStore -.-> ETL
        IdeaStore -.-> ETL
        ETL -.-> AnalyticsProcess
        AnalyticsProcess -.-> Visualization
        Visualization -.-> User
        Visualization -.-> Admin
    end

    %% Main Processes
    AuthProcess[Auth]
    TaskProcess[Tasks]
    EventProcess[Events]
    IdeaProcess[Ideas]
    NotificationProcess[Notify]
    ReportingProcess[Reports]

    %% Main Flow Connections
    User -.->|Login| AuthProcess
    AuthProcess -.->|Token| User
    AuthProcess -.->|Validate| UserStore
    UserStore -.->|Profile| AuthProcess

    User -.->|Tasks| TaskProcess
    Admin -.->|Assign| TaskProcess
    TaskProcess -.->|Store| TaskStore
    TaskStore -.->|Info| TaskProcess
    TaskProcess -.->|Notify| NotificationProcess
    UserStore -.->|Skills| TaskProcess
    TaskProcess -.->|Matches| User

    User -.->|Events| EventProcess
    EventProcess -.->|Store| EventStore
    EventStore -.->|Info| EventProcess
    EventProcess -.->|Notify| NotificationProcess
    EventProcess -.->|Updates| User

    User -.->|Ideas| IdeaProcess
    IdeaProcess -.->|Store| IdeaStore
    IdeaStore -.->|Info| IdeaProcess
    IdeaProcess -.->|Updates| User

    NotificationProcess -.->|Alerts| User
    NotificationProcess -.->|Store| NotificationStore
    NotificationStore -.->|Data| NotificationProcess
    NotificationProcess -.->|Emails| EmailService
    EmailService -.->|Status| NotificationProcess

    Admin -.->|Reports| ReportingProcess
    ReportingProcess -.->|Data| Admin
    UserStore -.->|Activity| ReportingProcess
    TaskStore -.->|Stats| ReportingProcess
    EventStore -.->|Stats| ReportingProcess
    IdeaStore -.->|Stats| ReportingProcess

    User -.->|Profile| AuthProcess
    DomainStore -.->|Info| TaskProcess
    AuthProcess -.->|Domains| DomainStore

    %% Smart Matching Connections
    TaskProcess -.->|Task Data| InputProcessing
    UserStore -.->|User Data| InputProcessing
    TaskStore -.->|Task History| InputProcessing
    MatchGeneration -.->|Matches| SmartMatch
    DomainStore -.->|Domain Info| DomainMatching

    %% Apply Styling
    class User,Admin,EmailService external
    class AuthProcess,TaskProcess,EventProcess,IdeaProcess,NotificationProcess,ReportingProcess process
    class UserStore,TaskStore,EventStore,IdeaStore,NotificationStore,DomainStore database
    class Authentication,TaskManagement,Notifications,Analytics,SmartMatching subgraphStyle
    class Login,Register,ProfileUpdate,TokenValidation,TaskCreate,TaskAssign,TaskUpdate,SmartMatch,NotifGenerate,BirthdayNotif,TaskNotif,EventNotif,ETL,AnalyticsProcess,Visualization,InputProcessing,DomainMatching,WorkloadAnalysis,ProfileAnalysis,ScoringSystem,MatchGeneration flow

    %% Layout Adjustments
    linkStyle default interpolate basis
```
___

https://divijajoshi.github.io/NGO_Manager_Image/
___
https://kroki.io/mermaid/svg/eNqNWG1v2zYQ_p5fIWAokABMsSbL0vTDAKeWtwDJMNRu90HwB8aibc2KZIh0Whf68SOP7y-SkwCJyHt05N09Ot5x0-H9NltMzzL-8-5dNmfHumo22ZSsq6ZiVdtQEK1qTCmfzMgPRroG19m6qutPv8xm-c30DlHWtTsihre__nathpffq5JtP13tf_gq9l27IpQqDfn17Go2NRo-3N3-Pr06oaHEDD9jSvQmrvOb2Y1RcXv_YTY5pYIenjfCdmGw0XMzc_Xc5eL3hJ513X7Xlnyc3eTWF1f57fQ6sQ3t6lx7Mm8Y9zSRjv5KSXd-Lv5eXMDEpHypmvNz-Kem8hdc1XPSvVYrUhQwytRwuTT6p9xJPJ5t52iGYQHqs-n9xRIEC0x3SiAerSB_JQ1TEni2ooeSYCURj1bwd8uqdbXCgjoK4E5Z4LTl-9YQOZBCQ8UX3LHsCbPVVjByfqSMvIBQx05CNAJE4qesOrKCxRb3ZvKh2R_YP5J5HFzAOLMTS4OUe9FaC7U1Pba4f9tuV7e4nPAYHmlFCz2R6RmL5etwjhADVeMEcr5qO76MtLZQI2W8RcFu_iQN6cCrBYwzO2GRQw7ILt9f_hHYOo4NbBgHh84Z8K4EezYP-WwMGq42hvVmJTDwJkBJUxomTg5sy9mvKTzjn7zPQx8wTsTHdlM1Bfy1UfpCNhXfT1foh4g6X_c86RFDHDm0qAXPMc03XFelJASMMzuRIARsQTogeDvalkSZBJLe2xAoUC5hwmOKM5G7IQk94QZvyItIOrG_BcICxv0tsJ87Ipwn_8HM0pNPOHM3TSH_JeTK-crOOcPs4H6yJgsVTs5KeNxuRbldJ16DMN5TDDaaE4tZHXLfCYuGlrE2vRXh5vChuHl5Pg6aK6bjMQOo-iBJoR-sR--rjm1LfARcoUd-zKTMjyUcYlIAj4kYBRHwVvL0OyCznL-Qg7ALp21wnKytjY0ZA9kFxlDebBxYSwEv-4mkynMbTSU-LRuPZ754LBRrrMvNu0pSwMRPJ8zfKnrgeeOnTGlTTLfPLe7K01Hj6w3FyhVFUXJkpsBJvLZ4VEkssGDQNAn3zEkbaXPomBxqwShOT6JMUQuqks_JsoV4tvWenhXP1Kn29DwMqK319Lx4pnGlp8Uwpz7EL2TfdowftVooJ-jS37EgVfa5bRpJG1urgq09nFJ9dF44Y4mDU6a3rosA6gQifXBE-dTp1ZHmrxjsCZzWu360lbpEyPQbQ5yxBMLKfZCAfcr2D826fYMq6ft-MFUHhs53vGmhb9ALhw2hyreBKyRPeo88EZs8U-1Hd5b4BpWxb1B3ytz4DXmeDRgCxO5drofc96ww6eEsThbKhpOqEvtJGKMIVZOOUYffg0i1wXRej2blO6JVHPbk4FLQeYrgO_1o1KDqXYmaKb1G-PGoPNFHGSSZVlwLbGIMyD7hueW1YscBncEHJzY7tHzI1zFsQIshaMDEZAYKOuaxxBBlPvkeX9lRMNRlh4k4ygbyhgC8HTR-Kb_Li4ZBdOB30P0X7zja7ph-IejUggQVlMuRv1QrL90WtL6m2tnv66O-BrNXPWAYAn4hj936PsyBOgFAjv-Qm5GQkw1Q4qNAEc33TojtlsA6ZPyILD2RYR-KvnrkukZfpgUW2H4W-e2Wp44iU-sg7zbGv2BzdMOBjnRnibwWEgW9IrIdE7JdDbLNibMm8opb5JXXyNTQyBbKiNdxKKzUkFduoYCDyCcNCu8dUHBngbzLBhSyV9wdGuI94mN7YDyF_XegTPhZhprTcCfvKEuyxoeaZVXD_bZva1HC87hV9H-Ddv01
