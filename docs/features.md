# Features

In this article, features available across all Spryte platforms are described. Anything which doesn't fit neatly into one of the other articles is explained here.

## Custom E-Mail

### Introduction

Historically, when sending e-mails via the Spryte Labs platform, e-mails were sent from `noreply@sprytelabs.com`. Whilst this is fine for most use cases, it lacks the personal touch that many customers prefer. To address this, Spryte Labs has rolled out the ability to send e-mails from one's own e-mail address. Following the steps below, one can configure one's own e-mail address to be used when sending e-mails via the Spryte Labs platform. If a custom address is not configured, e-mails will continue to be sent from `noreply@sprytelabs.com`.

### Background: App Passwords

Whenever one logs into any site, one is asked for an e-mail and a password. This is done to ascertain the identity of the user. Therefore, to send e-mails on one's behalf, Spryte Labs needs to know the user's username and password. Google, however, does not allow for a user's password to be used to send e-mails. Instead, Google requires that a user generate an "app password" which can be used to send e-mails.

An app password is functionally equivalent to a password, granting access to one's account, except that it can be revoked at any time, after which it will no longer work. Say, heaven forfend, a data leak occurs. If a real password is leaked, the user will have to change their password. If an app password is leaked, the user can simply revoke it, and generate a new one. This is the reason why Google requires that app passwords be used to send e-mails.

Hence, to send e-mails from one's own e-mail address, one must generate an app password.

### Background: Two-Factor Authentication

Broadly speaking, when attempting to verify the identity of a user, three key categories of authentication may be used:

1. Something the user knows (e.g. a password to log into a site);
2. Something the user has (e.g. a phone to receive a text message to confirm a bank transfer);
3. Something the user is (e.g. a fingerprint to unlock one's phone).

These are often called "factors" of authentication. Currently, the most common form of authentication is the first: something the user knows. This is because it is the easiest to implement. However, it is also the least secure. If a user's password is leaked, the user's account is compromised.

The term "two-factor authentication" refers to the use of two factors of authentication. For example, to complete a bank transfer one may be asked to enter a password, and then to confirm the transfer by receiving a text message on one's phone.

To generate an app password, one must enable two-factor authentication.

### Setting Up E-Mail

As mentioned above, to send e-mails from one's own e-mail address, one must first set up two-factor authentication, generate an app password, and then enter one's details on the Spryte Labs platform.

#### Setting Up Two-Factor Authentication

##### Instructions

To set up two-factor authentication, one must log into one's Google account, and then follow the steps below. To assist with this, the steps are also shown in the screenshots below.

1. Go to [https://myaccount.google.com/security](https://myaccount.google.com/security).
2. Set up two-factor authentication:
   1. Scroll down to the "How you sign in to Google" section - [find this section](#two-factor-authentication-image-1);
   2. Click on "2-Step Verification" - [you should then see this screen](#two-factor-authentication-image-2);
   3. Click on "Get Started" - [you should then see this screen](#two-factor-authentication-image-3);
   4. Re-enter your password - [you should then see this screen](#two-factor-authentication-image-4);
   5. Click on "Continue" - [you should then see this screen](#two-factor-authentication-image-5);
   6. Confirm your phone number;
   7. Click on "Send" - [you should then see this screen](#two-factor-authentication-image-6);
   8. Enter the code sent to your phone;
   9. Click on "Next" - [you should then see this screen](#two-factor-authentication-image-7);
   10. Click on "Turn on" - [you should then see this screen](#two-factor-authentication-image-8);
   11. Drink an espresso to celebrate.
3. Go to [https://myaccount.google.com/security](https://myaccount.google.com/security).
4. Confirm that two-factor authentication is enabled:
   1. Scroll down to the "How you sign in to Google" section - [find this section](#two-factor-authentication-image-9);
   2. Click on "2-Step Verification";
   3. Confirm that "2-Step Verification" is "On" - [you should then see this screen](#two-factor-authentication-image-8);
   4. If it is not, repeat steps 1.1.1 to 1.1.11.
5. Go to [https://myaccount.google.com/apppasswords](https://myaccount.google.com/apppasswords) - [you should then see this screen](#app-password-image-1).
6. Create an app password:
   1. Click on "Select app" - [an image for this step is shown below](#app-password-image-2);
   2. Select "Mail" - [an image for this step is shown below](#app-password-image-2);
   3. Click on "Select device" - [an image for this step is shown below](#app-password-image-3);
   4. Select "Other" - [an image for this step is shown below](#app-password-image-3);
   5. Enter a name for the app password (e.g. "spryte-mail") - [an image for this step is shown below](#app-password-image-4);
   6. Click on "Generate" - [an image for this step is shown below](#app-password-image-4);
   7. Your app password is now shown. Copy the app password, as it will not be shown again and you will need it in the next section - [an image for this step is shown below](#app-password-image-5);
   8. Click on "Done" once you have copied the app password - [an image for this step is shown below](#app-password-image-5).
7. Set up e-mail forwarding on the Spryte Labs platform:
   1. Go to [https://spryte-chat.web.app](https://spryte-labs.com) - [you should then see this screen](#e-mail-forwarding-image-1);
   2. Click the Spryte Labs logo - [you should then see this screen](#e-mail-forwarding-image-2);
   3. Log into your account - [you should then see this screen](#e-mail-forwarding-image-3);
   4. Click on your profile picture, represented here by a mosaic depicting the Emperor Justinian. It is highlighted in [this image](#e-mail-forwarding-image-3) and [you should then see this screen](#e-mail-forwarding-image-4);
   5. Fill in your e-mail address and press "Save" - [here is an image for this step](#e-mail-forwarding-image-5);
   6. Fill in your app password and press "Save" - remember, this is the password we generated in step 6.7.7, NOT your actual password - [here is an image for this step](#e-mail-forwarding-image-6);
   7. Fill in the server address and press "Save" - this will typically be "smtp.gmail.com" - [here is an image for this step](#e-mail-forwarding-image-7);
   8. Fill in the server port and press "Save" - this will typically be "465" - [here is an image for this step](#e-mail-forwarding-image-8);
   9. Click the checkbox next to "Email Forwarding" - [here is an image for this step](#e-mail-forwarding-image-9).
8. Done! E-mail forwarding is now set up. You can now send e-mails from the Spryte Labs platform from your own e-mail address.

##### Screenshots

###### Two-Factor Authentication: Image 1

[Return to Instructions](#instructions)

![How You Sign In](_media/Features/Custom%20E-Mail/Two%20Factor%20Authentication%20-%20I.png)

###### Two-Factor Authentication: Image 2

[Return to Instructions](#instructions)

![Protect Your Account](_media/Features/Custom%20E-Mail/Two%20Factor%20Authentication%20-%20II.png)

###### Two-Factor Authentication: Image 3

[Return to Instructions](#instructions)

![Log-In Screen](_media/Features/Custom%20E-Mail/Two%20Factor%20Authentication%20-%20III.png)

###### Two-Factor Authentication: Image 4

[Return to Instructions](#instructions)

![Use Your Phone](_media/Features/Custom%20E-Mail/Two%20Factor%20Authentication%20-%20IV.png)

###### Two-Factor Authentication: Image 5

[Return to Instructions](#instructions)

![Confirm Your Number](_media/Features/Custom%20E-Mail/Two%20Factor%20Authentication%20-%20V.png)

###### Two-Factor Authentication: Image 6

[Return to Instructions](#instructions)

![Enter Confirmation Code](_media/Features/Custom%20E-Mail/Two%20Factor%20Authentication%20-%20VI.png)

###### Two-Factor Authentication: Image 7

[Return to Instructions](#instructions)

![Turn On Two Factor](_media/Features/Custom%20E-Mail/Two%20Factor%20Authentication%20-%20VII.png)

###### Two-Factor Authentication: Image 8

[Return to Instructions](#instructions)

![Two Factor Screen](_media/Features/Custom%20E-Mail/Two%20Factor%20Authentication%20-%20VIII.png)

###### Two-Factor Authentication: Image 9

[Return to Instructions](#instructions)

![How You Sign In](_media/Features/Custom%20E-Mail/Two%20Factor%20Authentication%20-%20VIIII.png)

###### App Password: Image 1

[Return to Instructions](#instructions)

![App Passwords](_media/Features/Custom%20E-Mail/App%20Password%20-%20I.png)

###### App Password: Image 2

[Return to Instructions](#instructions)

![Select App](_media/Features/Custom%20E-Mail/App%20Password%20-%20II.png)

###### App Password: Image 3

[Return to Instructions](#instructions)

![Select Device](_media/Features/Custom%20E-Mail/App%20Password%20-%20III.png)

###### App Password: Image 4

[Return to Instructions](#instructions)

![Enter Name](_media/Features/Custom%20E-Mail/App%20Password%20-%20IV.png)

###### App Password: Image 5

**Note:** The app password in the screenshot below is no longer valid.

[Return to Instructions](#instructions)

![Copy Password](_media/Features/Custom%20E-Mail/App%20Password%20-%20V.png)

###### E-Mail Forwarding: Image 1

[Return to Instructions](#instructions)

![Spryte Labs Homepage](_media/Features/Custom%20E-Mail/Spryte%20Chat%20-%20I.png)

###### E-Mail Forwarding: Image 2

[Return to Instructions](#instructions)

![Spryte Labs Login Screen](_media/Features/Custom%20E-Mail/Spryte%20Chat%20-%20II.png)

###### E-Mail Forwarding: Image 3

[Return to Instructions](#instructions)

![Spryte Labs Landing Screen](_media/Features/Custom%20E-Mail/Spryte%20Chat%20-%20III.png)

###### E-Mail Forwarding: Image 4

[Return to Instructions](#instructions)

![Spryte Labs Settings](_media/Features/Custom%20E-Mail/Spryte%20Chat%20-%20IV.png)

###### E-Mail Forwarding: Image 5

[Return to Instructions](#instructions)

![Spryte Labs Settings - E-Mail](_media/Features/Custom%20E-Mail/Spryte%20Chat%20-%20V.png)

###### E-Mail Forwarding: Image 6

[Return to Instructions](#instructions)

![Spryte Labs Settings - Credentials](_media/Features/Custom%20E-Mail/Spryte%20Chat%20-%20VI.png)

###### E-Mail Forwarding: Image 7

[Return to Instructions](#instructions)

![Spryte Labs Settings - Server](_media/Features/Custom%20E-Mail/Spryte%20Chat%20-%20VII.png)

###### E-Mail Forwarding: Image 8

[Return to Instructions](#instructions)

![Spryte Labs Settings - Port](_media/Features/Custom%20E-Mail/Spryte%20Chat%20-%20VIII.png)

###### E-Mail Forwarding: Image 9

[Return to Instructions](#instructions)

![Spryte Labs Settings - Checkbox](_media/Features/Custom%20E-Mail/Spryte%20Chat%20-%20VIIII.png)