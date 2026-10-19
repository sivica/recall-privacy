# Recall privacy and account deletion

Effective 19 October 2026. Recall is developed by Ivica Stojanoski. For privacy questions or account deletion, contact s.ivica@gmail.com.

## Your choices

You can study as a guest without an account. Guest study stays in Recall's private storage on your device. Signing in does not upload guest study. Copying guest study into the private account workspace is an explicit action; saving that workspace to your account is a separate action.

## Account and saved study data

Google sign-in supplies account identity information to Recall's authentication service, including a Google identifier, email address and profile information Google provides, such as display name or picture. This identifies your account and lets the same account access its saved study on another device.

When you choose **Save to account**, Recall sends a checkpoint containing personal deck/card text, review dates, the saved session queue and ratings, completion state and operation identifiers. Checkpoints are retained as revision history until you delete the account. Recall does not automatically upload study in the background. Loading a saved copy replaces the private workspace on that device and keeps one previous local copy for recovery.

Recall uses Google for sign-in and Nhost authentication, Hasura and PostgreSQL hosted on Railway for account storage. Connections use HTTPS. The app includes no advertising or analytics SDK. Access controls restrict study checkpoints to their account owner; this is not end-to-end encryption. Authentication credentials are encrypted with Android Keystore on the device, and app data is excluded from Android backup.

## Deletion and sign-out

**Account → Delete Recall account → Delete account** requests removal of the account and its cloud checkpoint history and removes that device's private workspace. Guest study remains. Other devices may retain their own offline copies; clear Recall's app storage or uninstall it on those devices to remove those copies. A deleted identity cannot save more checkpoints.

Signing out hides the private workspace but keeps its unsaved local changes so the same account can recover them later. Signing out does not delete cloud data.

If the deletion response is lost, the app labels cloud deletion as unconfirmed and allows retry. The local private copy is still removed. If authentication can no longer reconcile the request, contact the developer for verification. Hosting providers may retain technical service logs or backups under their configured retention policies; deleted records are no longer available through Recall's active account APIs.

## Request deletion without the app

Email s.ivica@gmail.com with the subject “Recall account deletion” and the Google email used for Recall. You can make this request without installing or opening the app. Do not send passwords or tokens. The developer will verify account ownership before deleting the account and its live cloud checkpoint history. You can also use this contact to check an unconfirmed deletion request or ask a privacy question.
