# Globus

Globus is a powerful tool for robustly and securely managing data transfers to and from collaborators and within UAB Research Computing. Globus is recommended for most single-use, day-to-day data transfer use-cases.

UAB Research Computing uses High Assurance Endpoints and Collections, meaning there are additional security measures in place to reduce risk and move toward HIPAA compliance. Generally speaking, if you have used Globus in the past, the data transfer interface has not changed, but there are a few new restrictions.

1. You will be prompted to prove authorization each time you access a UAB Research Computing endpoint, collection or attempt to download files to your local machine from such an endpoint or collection. If you are already logged in with Single Sign-On (SSO) the process is simple. If not, you will need to authenticate with SSO.
2. Bookmarks are not allowed in High Assurance endpoints and collections.

For more detailed information on High Assurance please see the Globus official pages below:

- [High Assurance Security Overview](https://docs.globus.org/security/high-assurance-overview/)
- [High Assurance Collections](https://docs.globus.org/high-assurance/)

## Setting up Globus Connect Personal

[Globus Connect Personal](https://www.globus.org/globus-connect-personal) is software meant to be installed on local machines such as laptops, desktops,
workstations and self-owned, local-scale servers. Globus maintains excellent documentation for installation on [MacOS](https://docs.globus.org/how-to/globus-connect-personal-mac/), [Linux](https://docs.globus.org/how-to/globus-connect-personal-linux) and [Windows](https://docs.globus.org/how-to/globus-connect-personal-windows).

To verify your installation is complete, please visit <https://app.globus.org> and log in. Click "Endpoints" in the left-hand navigation pane and then click the "Administered By You" tab. Look in the table for the endpoint you just created.

## Managing Identities

Globus Identities is a concept helping to map Globus Accounts (one per person) to institutions (one or more per person).

Most UAB researchers will have a single identity, their UAB identity, tied to their blazerid. Some researchers may have external collaborations or appointments that provide additional entities which need access to other endpoints on Globus.

To manage your identities, navigate to <https://app.globus.org/account/identities> and sign in.

<!-- markdownlint-disable MD046 -->
!!! important

    To use UAB Research Computing endpoints and collections, you will need to ensure you are using you UAB identity.
<!-- markdownlint-enable MD046 -->

## Moving Data Between Endpoints

1. Log in to the Globus App online at <https://app.globus.org> using UAB Single Sign-On (SSO). Start typing "University of Alabama at Birmingham" into the "Use your existing organizational login" text box and selected it when it appears in the list.

    ![!Globus login page with University of Alabama at Birmingham entered into the text box](./images/globus_001_login.png)

2. Click File Manager in the left-hand navigation pane.

    ![!Navigation pane with File Manager selected.](./images/globus_002_nav_pane_file_manager.png)

3. Ensure the center icon for the "Panels" selection is picked.

    ![!Panels selection widget with center icon selected. Center icon appears to be two side-by-side panes.](./images/globus_003_panels.png)

4. Click the "Search" icon in the "Collection" text box near the top-left or top-right of the page to locate an endpoint. There are multiple ways to find an endpoint. For some endpoints you may be asked to log in, which is true of all UAB endpoints. Some UAB endpoints may also require that you be on the UAB Campus VPN.

    ![!Globus File Manager interface with mouse pointer over left-hand Collection Search box.](./images/globus_004_search_bar.png)

    1. Begin typing in the box to search for an endpoint. To find UAB-related endpoints, search for "UAB". There are two Cheaha endpoints

        1. Cheaha cluster on-campus (UAB Science DMZ) for machines that are either on the UAB Campus Network, or connected to the UAB Campus VPN.
        2. Cheaha cluster off-campus (UAB Science DMZ) for machines that are _not_ on the UAB Campus Network and _not_ on the UAB Campus VPN.

    2. The "Recent" tab shows endpoints that have most recently been used.

        ![!Globus Collection Search Recent tab showing two endpoints.](./images/globus_005_recent_tab.png)

    3. The "Bookmarks" tab shows a list of endpoint bookmarks. Bookmarks may not reference folders within UAB Research Computing or other High Assurance endpoints or collections.

        ![!Globus Collection Search Bookmarks tab showing four bookmarks.](./images/globus_006_bookmarks_tab.png)

    4. The "Your Collections" tab shows all endpoints owned by you. For most researchers this will be one or more Globus Connect Personal endpoints.

        ![!Globus Collection Search Your Collections tab showing one endpoint.](./images/globus_007_your_collections_tab.png)

    5. The "Shared With You" tab shows any private endpoints that have
        been shared with you by other users, possibly collaborators.

    6. The "More Options" tab will show a brief text on installing
        Globus Connect Personal.

5. When an endpoint has been selected you will see a list of folders and files on the default path for that endpoint in the bottom box. You can use the "Path" box to type a path to find the files you are looking for.

    ![!Globus File Manager interface with one endpoint selected showing files of default directory.](./images/globus_010_one_endpoint_done.png)

6. Repeat the process of selecting an endpoint for the other "Collection" text box.

    ![!Globus File Manager interface with both endpoints selected showing files for both default directories.](./images/globus_011_two_endpoint_done.png)

7. When both endpoints have been selected and you have chosen the correct paths for each endpoint, select files and/or folders on the side you wish to transfer FROM. We will call this side the source endpoint, and the other side the target endpoint. Selections may be made by clicking the checkboxes that appear when you hover over each file or folder.

    ![!Globus File Manager interface with files selected in left endpoint.](./images/globus_012_selected_files.png)

8. When all files and folders have been selected from the source endpoint, click the "Start" button on the source endpoint side. This will start a transfer process from source to target. The files will be placed in the currently open path on the target endpoint.

    ![!Pop-up showing Transfer request submitted successfully. Pop-up contains link to View details.](./images/globus_013_popup.png)

9. A green pop-up notification will appear indicating the transfer has started. Click "View details \>" to be taken to the status of the transfer. You can also check on the status of any transfers by clicking the "Activity" button in the left-hand navigation pane.

<!-- markdownlint-disable MD046 -->
!!! note

    File permissions from the source will not be copied to the destination. Please read more at [this ask.ci FAQ](https://ask.cyberinfrastructure.org/t/why-cant-other-users-access-data-i-transferred-to-a-project-space-on-cheaha/2527/3).
<!-- markdownlint-enable MD046 -->

### Transfer and Sync Options

Between the two "Start" buttons on the "File Manager" page is a "Transfer & Sync Options" drop down menu. Click that button to change the options. More information on each option. A brief summary of the options are...

![!Transfer and Sync Options pane showing multiple options.](./images/globus_040_transfer_and_sync_options.png)

1. sync - Sync files only, rather than create new files.
2. delete files - Delete any files on the target that are not on the source. Useful for forcing identical filesystems when syncing.
3. preserve source - Copies file "modified time" metadata.
4. verify integrity - Verifies that checksums are identical on source and target after transfer completes. Highly recommended to have this checked.
5. encrypt transfer - Encrypts data before leaving source and decrypts after arriving at destination. Recommended for all transfers, required and enforced for all UAB endpoints.
6. skip files - Skips source files that cause errors during the transfer. Otherwise the entire transfer will stop when an error is encountered.
7. quota fail - Fails instead of retries when the target storage quota is exceeded.

### Common Errors

1. File Not Found - This may mean that a file was not readable by Globus. Check that the file hasn't moved or changed names during the transfer. It is recommended to not modify files while they are being transferred by Globus.
2. Permission Denied - Globus is not able to access the files because permissions do not allow it. For Globus Connect Personal, be sure the containing folder is on the "Accessible Folders" list. Be sure that your Cheaha account has access to read the file.

### Project Space Permissions

Globus does not preserve permissions nor ownership when data is transferred, instead using whatever permissions are default at the target location, and making the owner the authenticated user who initiated the transfer. Typically this is not an issue, but may cause problems for project directories. Please see our [Project Directory Permissions Section](../storage.md#project-directory-permissions) for more information.

### More Information

A [Globus FAQ](https://docs.globus.org/faq/globus-connect-endpoints/) is available for additional information on endpoints and transfers.

## Connectors

UAB Researcher Computing has subscriptions to connectors for cloud services and other types of filesystems.

### UAB Box Connector

To use the UAB Box Connector, [search for an endpoint](#moving-data-between-endpoints) like usual and enter "UAB Box" into the search box. Select the endpoint labeled "UAB Box". You should see a list of files and folders that are available to you at <https://uab.app.box.com>. File transfers work as they would with any other endpoint or collection.

### Long-term Storage S3 (LTS) Connector

<!-- markdownlint-disable MD046 -->
!!! important

    [LTS](../lts/lts.md) behaves differently from other file systems and comes with a few possible pitfalls. Keep in mind the following three rules: (1) all data must be in buckets, (2) buckets are only allowed in the root folder, and (3) buckets must have unique names.
<!-- markdownlint-enable MD046 -->

To use the UAB [LTS](../lts/lts.md) Connector, [search for an endpoint](#moving-data-between-endpoints) like usual and enter "UAB LTS" into the search box. Select the endpoint labeled "UAB Research Computing LTS (Long Term Storage aka S3)". If you have stored data within LTS already you should see a list of folders, otherwise you will see an empty space where folders may be placed. Each folder corresponds to a [bucket](../lts/lts.md#make-a-bucket) in [LTS](../lts/lts.md). To create a bucket, click "New Folder" in the "File Manager" window in Globus. Note that buckets must have globally unique names. Read on for more information about possible pitfalls.

#### Data Must be in Buckets

All data transferred to LTS must be placed in a bucket, and may _not_ be placed directly into the root directory. Attempting to move data to the root directory will result in an unhelpful error message in the "Activity" window.

![!unhelpful error message for data placed in the root LTS directory](images/globus_lts_no_bucket_error_001.png)

Clicking on the "view event log" link shows the following.

![!unhelpful event log message](images/globus_lts_no_bucket_error_002.png)

```text
Error (transfer)
Endpoint: UAB Research Computing LTS (Long Term Storage aka S3) (184408b4-d04b-4513-9912-8feeb6adcab3)
Server: m-a201b5.9ad93.a567.data.globus.org:443
Command: STOR /test.log
Message: The connection to the server was broken
---
Details: an end-of-file was reached\nglobus_xio: An end of file occurred\n
```

#### Buckets Must Have Globally Unique Names

When creating new buckets, the name must be unique across all buckets on the system. At first this may sound very restrictive, but it is quite simple to deal with in practice. See our LTS section on [good naming practice](../lts/lts.md#avoiding-duplicate-names) for how to avoid duplicate names.

If a duplicate bucket name is entered, a long error message will appear in a small space next to the new bucket name. The message reads like the following, expanded for readability.

![!large error message in small space](images/globus_lts_duplicate_name_error_001.png)

```text
Bad Gateway: Endpoint Error, Error (mkdir)
Endpoint: UAB Research Computing LTS (Long Term Storage aka S3) (184408b4-d04b-4513-9912-8feeb6adcab3)
Server: m-b81a79.9ad93.a567.data.globus.org:443
Command: MKD /test/
Message: Fatal FTP Response ---
Details: 553-
  GlobusError: v=1 c=PATH_EXISTS\r\n553-
  GridFTP-Path: (null)\r\n553-globus_gridftp_server_s3_base: S3
  Error accessing "": ErrorBucketAlreadyExists: ErrorBucketAlreadyExists: \r\n553 End.\r\n
```

## Using Bookmarks

To save a bookmark, use the File Manager interface to select an endpoint and navigate to a path on that endpoint. Then click the bookmark button as shown below.

![!Globus File Manager interface with mouse pointer hovering over Bookmark icon.](./images/globus_060_create_bookmark.png)

To manage bookmarks, click "Bookmarks" in the left-hand navigation pane. Click the "Pencil" icon to edit a bookmark. Click the "Trash Bin" icon to delete a bookmark.

![!Globus Bookmarks interface showing four bookmarks.](./images/globus_061_manage_bookmarks.png)

<!-- markdownlint-disable MD046 -->
!!! note

    It is not possible to create bookmarks within High Assurance Endpoints.
<!-- markdownlint-enable MD046 -->

## Managing Shared Collections from a Globus Connect Personal Endpoint

It is NOT RECOMMENDED to make Globus Connect Personal endpoints public as this is insecure. It is more difficult to manage access controls for the entire Globus Connect Personal endpoint than for a shared collection. Shared collections make it simpler to share different data with distinct collaborators, and to manage who has access to what data. Be secure, use shared collections!

### Creating a Shared Collection

1. Click "Endpoints" in the left-hand navigation pane.

2. Click the "Administered By You" tab.

    ![!Globus Endpoints page with Administered by You selected, showing two endpoints. One of the endpoints is a shared endpoint.](./images/globus_100_shared_admin_tab.png)

3. In the table, find the endpoint you wish to share data from and click its name. You will be taken to the page for that endpoint.

4. Click the "Collections" tab.

    ![!Globus UAB RC Work Laptop page with Guest Collections tab selected showing one collection.](./images/globus_101_shared_collections.png)

5. Click the "Add a Guest Collection" button.

6. Fill out the form.

    ![!Create New Guest Collection form.](./images/globus_102_shared_collection_form.png)

    1. Manually enter a path or click the Browse button to select a folder.
    2. Give a short but memorable name for your shared collection. This information will be useful for your collaborators.
    3. Optionally fill in a more detailed description of the shared collection for your records.
    4. Optionally fill in searchable keywords.

7. Click "Create Share" to move to the next step. You will be taken to the page for the newly created collection, which is now a full-fledged endpoint. Any further references to "an endpoint" will be about the newly created, shared collection.

8. Make sure you are on the "Permissions" tab. You should see a permissions table with your name in the first row.

    ![!Newly created test endpoint page with Permissions tab selected.](./images/globus_103_shared_permissions.png)

9. Click "Add Permissions -- Share With" to share your endpoint with other users.

10. Fill out the form.

    ![!Test endpoint Add Permissions Share With form.](./images/globus_104_shared_add_permissions.png)

    1. Optionally enter a path within the shared endpoint or use the Browse button. If you leave the path as just a slash, the entire shared endpoint will be shared with these users.
    2. Select who to share with.
        1. User - One or more users.
        2. Group - All members of a group.
        3. All Users - All globus users.

            <!-- markdownlint-disable MD046 -->
            !!! danger

                This will expose information to everyone on Globus!
            <!-- markdownlint-disable MD046 -->

    3. Search for users to add, or a group, depending on your choice above. You should be able to find any globus user using the search box.

        <!-- markdownlint-disable MD046 -->
        !!! warning

            Be certain of which user you are selecting! Check the email address domain.
        <!-- markdownlint-disable MD046 -->

    4. If adding users, optionally enter a message so they know why they are being added.
    5. Select permissions. Read is automatically selected and cannot be changed. Write permissions are optional.

11. Click "Add Permission" to add permissions for these users or groups.
    You will be returned to the page for the shared endpoint and should
    be on the "Permissions" tab and should see the user or group in the
    table.

### Deleting a Shared Collection

1. Click "Endpoints" in the left-hand navigation pane, then c

2. Click the "Administered By You" tab.

    ![!Globus Endpoints page with Administered by You tab selected, showing two endpoints.](./images/globus_100_shared_admin_tab.png)

3. Click the right caret ">" icon at the right side of the row with the endpoint you wish to delete. You will be taken to the information page for that endpoint.

4. Click "X Delete Endpoint" and a confirmation dialog will open at the top of the page. Respond to the dialog to delete the endpoint, or to cancel.

    ![!Delete Endpoint confirmation dialog banner.](./images/globus_105_shared_delete.png)
