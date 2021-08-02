# SVN Backup Script

Performs a full or incremental backup if the last full or incremental backup revision is older than the current HEAD revision.

## Usage

    svnbackup <REPO_NAME> -r <REPO_DIR> -b <BACKUP_DIR> --mail <MAILTO>
