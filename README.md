# SVN Backup Script

Performs a full or incremental backup if the last full or incremental backup revision is older than the current HEAD revision.

## Requirements

- mail
- md5sum`
- rsync (rsyncbakcup only)
- ssh  (rsyncbakcup only)
- svn
- svnadmin
- svnlook

## Usage

## svnbackup

    svnbackup [options...]

Options:

- `-b --backup`             Folder where store backups. It will be created if it not exists.
- `-h --help`               Show this help ad exit.
- `-i --incremental`        Perform incremental backup.
- `-f --full`               Perform full backup.
- `-m --mailto`             Comma separated list of mail address.
- `-r --repository`         Folder of the repository to backup.
- `--version`               Show svnbackup version and exit.

Example:

    svnbackup --full -r /var/repo/myrepo -b /var/backup/myrepo

## rsyncbackup

    rsyncbackup <BACKUP FOLDER> <REMOTE FOLDER>

Example:

    rsyncbackup /var/backup/myrepo remoteuser@remotehost:/pub/repo/backup
