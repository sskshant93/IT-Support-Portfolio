# Project 3 - Active Directory User Support

## Scenario

A user contacts the IT Service Desk because they are unable to sign in to their Windows account. The objective is to identify whether the issue is related to incorrect credentials, an account lockout, an expired password, or a disabled Active Directory account, and then restore access using the appropriate support procedure.

## Step 1 - Locate and Inspect the User Account

The first step is to locate the user's account in Active Directory Users and Computers (ADUC) and review the account status before making any changes.

### Initial Checks

Confirm the correct user account and review:

- Whether the account is enabled
- Whether the account is locked out
- Whether the password has expired
- Whether the user is required to change the password at next logon
- Whether any account expiration settings apply

No account changes should be made until the user's identity and the cause of the sign-in problem have been verified.

## Step 2 - Check for Account Lockout

If the user account is locked, determine whether the lockout is consistent with the organization's account lockout policy and investigate the likely cause before restoring access.

### Possible Causes

- Multiple incorrect password attempts
- Old credentials saved on another device or application
- Cached or stored credentials using an outdated password
- A service, scheduled task, or mapped resource using old credentials

### Support Action

After verifying the user's identity and following the organization's access-control procedures:

1. Confirm that the correct account is locked.
2. Investigate the likely source of repeated authentication failures.
3. Unlock the account if authorized.
4. Ask the user to attempt sign-in again.
5. Confirm that the account does not immediately lock again.
6. Document the action and outcome in the support ticket.

## Step 3 - Check Password Status and Reset if Required

If the account is not locked, investigate whether the sign-in problem is related to the user's password.

### Password Checks

Review whether:

- The password has expired
- The user has forgotten the password
- The user is required to change the password at next logon
- The account is subject to the organization's password policy

### Password Reset Procedure

If a password reset is required and authorized:

1. Verify the user's identity according to company policy.
2. Confirm that the correct Active Directory account has been selected.
3. Reset the password using the approved procedure.
4. Apply "User must change password at next logon" when required by organizational policy.
5. Have the user sign in using the temporary password.
6. Confirm that the user can successfully create a new password and access the account.
7. Document the password reset and successful validation in the support ticket.

Passwords should never be recorded in the support ticket or troubleshooting documentation.


## Step 4 - Check for a Disabled Account

If the account is not locked and the password is not the cause, check whether the Active Directory account is disabled.

### What to Check

- Confirm that the correct user account has been selected
- Check whether the account is currently disabled
- Review available ticket or account information for the reason
- Determine whether authorization is required before restoring access

### Support Action

If the account is disabled:

1. Do not automatically enable the account.
2. Verify the user's identity and confirm the account status.
3. Review the support request or available documentation.
4. Escalate or obtain authorization if required by organizational policy.
5. Enable the account only when authorized.
6. Have the user test their sign-in.
7. Document the action, authorization, and final result in the support ticket.

## Step 5 - Validate the Resolution

After the appropriate account action has been completed, confirm that the user's access has been restored.

### Validation

- Ask the user to sign in again
- Confirm that authentication is successful
- Verify that the account does not immediately lock again
- Confirm that the user can access the required Windows resources
- Ensure no additional authentication errors are reported

### Ticket Documentation

Document the troubleshooting process in the service desk ticket, including:

- User-reported issue
- Account status discovered
- Troubleshooting steps performed
- Action taken
- Required authorization or escalation
- Final validation and user confirmation

Do not document passwords or other sensitive authentication information in the ticket.


## Step 5 - Validate the Resolution

After the appropriate account action has been completed, confirm that the user's access has been restored.

### Validation

- Ask the user to sign in again
- Confirm that authentication is successful
- Verify that the account does not immediately lock again
- Confirm that the user can access the required Windows resources
- Ensure no additional authentication errors are reported

### Ticket Documentation

Document the troubleshooting process in the service desk ticket, including:

- User-reported issue
- Account status discovered
- Troubleshooting steps performed
- Action taken
- Required authorization or escalation
- Final validation and user confirmation

Do not document passwords or other sensitive authentication information in the ticket.


## Skills Demonstrated

- Active Directory Users and Computers (ADUC)
- User account troubleshooting
- Account lockout investigation
- Password reset support
- Disabled account investigation
- Identity verification and access-control procedures
- Windows authentication troubleshooting
- Service desk ticket documentation
- Post-resolution validation
