# Project 1 - Windows Disk Space Troubleshooting

## Scenario

A Windows user reports that the C: drive is running low on available storage space. The objective is to identify what is consuming disk space, safely recover unnecessary storage, and verify that sufficient free space is available afterward.

## Initial Investigation

Before making changes, I would first verify the available disk space and identify what is consuming storage.

### Windows Storage

Navigate to:

Settings > System > Storage

Review storage categories such as installed applications, temporary files, documents, and other system files.

### Command Prompt

Basic Command Prompt commands can be used to gather information about the computer before troubleshooting.

```cmd
whoami
```
Identifies the currently logged-in user.

```cmd
hostname
```
Identifies the computer being troubleshot.

```cmd
systeminfo
```
Displays Windows version and general system information.

```cmd
chkdsk C:
```
Checks the C: drive file system and reports detected file-system problems.

## Troubleshooting Process

1. Confirm the amount of free space available on the C: drive.
2. Review Windows Storage to identify the largest storage categories.
3. Check temporary files and unnecessary system files.
4. Review installed applications for unused software.
5. Empty the Recycle Bin when appropriate.
6. Remove only files confirmed to be safe to delete.
7. Recheck available disk space after cleanup.

## Validation

After troubleshooting:

- Confirm that available C: drive space has increased.
- Verify that Windows and applications are operating normally.
- Confirm that important user files were not affected.
- Document the actions performed and the final result.

## Skills Demonstrated

- Windows 10/11 troubleshooting
- Command Prompt
- Disk space analysis
- Windows Storage
- End-user support
- Troubleshooting methodology
- Technical documentation
- Post-resolution validation
