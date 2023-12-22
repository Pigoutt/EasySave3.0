# .NET-Backup-Projet-G3 - EasySaveApp

### Group 3 :
- Corentin PIGOUT
- Brad BITANGANE
- Martin CHADES

### UML diagrams :
https://drive.google.com/drive/folders/1HRngIXlfq6Ax6Fj-5cRUCp2SlZux4-iZ?usp=sharing
Sequence, UseCase, Class, Activity




### Class details for the project :

BackupLog:
    - Purpose: Represents log information for backup operations.
    - Responsibilities:
        - Stores timestamped details of backup actions, including job name, source, destination, file size, and transfer time.

BackupJob:
    - Purpose: Represents a backup job definition.
    - Responsibilities:
        - Defines a backup job with a name, source directory, target directory, type (full or differential), and state.
        - Executes the backup job.

JobState:
    - Purpose: Represents the state of a backup job at a specific moment.
    - Responsibilities:
        - Stores information about the current status, progress, and details of a backup job.
        - Used by BackupJob to track and manage its state.

RealTimeStateFile:
    - Purpose: Manages real-time state information for the application.
    - Responsibilities:
        - Contains a list of JobState instances, providing a historical record of job states.

LanguageManager:
    - Purpose: Manages language-related operations for the application.
    - Responsibilities:
        - Handles setting and retrieving localized strings based on the selected language.

EasySaveAppViewModel:
    - Purpose: Serves as the ViewModel orchestrating interactions between the View and Model components.
    - Responsibilities:
        - Manages instances of BackupJob, BackupLog, RealTimeStateFile, and LanguageManager.
        - Provides methods for creating backup jobs, executing jobs, generating logs, and language management.

BackupType (enumeration):
    - Purpose: Enumerates types of backup (Full, Differential).
    - Responsibilities:
        - Defines two constants representing different types of backup operations.

EasySaveAppView:
    - Purpose: Represents the user interface and handles user interactions.
    - Responsibilities:
        - Displays prompts and interacts with the user.
        - Depends on EasySaveAppViewModel for handling user interactions.

These classes collectively adhere to the MVVM pattern, where the Model classes (BackupLog, BackupJob, JobState, RealTimeStateFile, BackupType) encapsulate data and state, the ViewModel (EasySaveAppViewModel) manages application logic, and the View (EasySaveAppView) handles user interface interactions. The LanguageManager assists in language-related functionalities throughout the application.
