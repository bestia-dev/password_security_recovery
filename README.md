<!-- markdownlint-disable MD041 -->
[//]: # (auto_md_to_doc_comments segment start A)

# password_security_recovery

[//]: # (auto_cargo_toml_to_md start)

**How I manage my passwords, security and recovery**  
***version: 2023 date: 2023-11-17 author: [bestia.dev](https://bestia.dev) repository: [GitHub](https://github.com/bestia-dev/password_security_recovery)***  

**WARNING!!! This is a public repository: never write or save secrets here!!!**

[//]: # (auto_cargo_toml_to_md end)

 ![tutorial](https://img.shields.io/badge/tutorial-yellow)
 ![work_in_progress](https://img.shields.io/badge/work_in_progress-yellow)
 ![password_security_recovery](https://bestia.dev/webpage_hit_counter/get_svg_image/1196500460.svg)

Hashtags: #tutorial  
My projects on GitHub are more like a tutorial than a finished product: [bestia-dev tutorials](https://github.com/bestia-dev/tutorials_rust_wasm).

## Public and private

Like in normal life in our digital life, we have public and private things.

Many things in life are public. Everybody can use them. For example, a website like Google search is public. Nobody will get jealous if somebody else uses Google search. It is public.  

But some things are private. For example, my email is private. I don't want anybody to read my emails. It is not important why, this is a philosophical question. It is simply in human nature that we don't want to share everything with everybody else.  

And sometimes there is mix of this two. We allow guests to use our bathroom but we don't want them to go into our bedroom.

To protect our private things we use keys, passwords or similar mechanisms.  
Only with that "key" we can access our private things. That way if a thief wants to open a door, he cannot do it without the key. At least not easily and quietly.  

Let's go down the rabbit hole!

## Passwords

Passwords are easy. Everybody understands passwords.  
But many don't understand that passwords don't live alone. Passwords are always tightly coupled with a username and a "service".  
A very simple analogy is that:

- the "service" is like a house
- the username is like a specific door in that house
- the password is like the key to that door of that house

Many synonyms for password mean roughly the same thing: passkey, passcode, passphrase, ... These words are not exclusive for only one security technique, but often they are used to make soft distinctions around different techniques.

## Good practice

All door keys are different in real life. You cannot open all the doors in a street with the same key. The same should apply for passwords too. Most of the passwords must be unique, never reuse the same password for different things. The danger is that if a hacker finds one of your passwords, he will try it on every service. If the password is the same, he will have access to everything. If the passwords are different he will have access limited just to one single service. At least for the most important passwords make them different.  

Security is never 100%. Everything can be hacked eventually. The difference is how difficult it is to hack. If it is too damn difficult, the hacker will just leave it and find an easier target. More important the secrets are, the more resources will the hackers deploy. Cracking two passwords one after the other is more difficult than cracking only one to access an important secret. Security is like an onion, it has layers.

## First class passwords

Not all passwords are equal. It depends how important is the private thing that is protecting.

The password for our bank account is *very important*. If a thief finds this password he can steal all our money. That would be very bad.  

But a password for a free service like "free cooking recipes" is *not very important*. If the password is hacked, nothing terrible will happen. There is no money involved.

Then there is the *very important* password that protects our "digital identity". For example, if we forget the "cooking recipe" password, we can recover it easily. These kinds of services have a "forgot password" button and they send a link to recover it to your primary email.  
**Aha! "To your email"!**  
This means that our primary email must not be compromised. If a thief can access our primary email, he can change all passwords of our less important services. That is not good. So simply put our email is our "digital identity".  

The "first-class" passwords are used to protect:  

- bank accounts, digital wallets, debit card PINs and anything around money
- digital identity (emails, Google account, Facebook account, government-issued certificates, smartphone pin, windows login)
- password managers for "second-class" passwords
- encrypted private files (VeraCrypt, Cryptomator, ...)
- normal private files (Dropbox, GDrive, OneDrive, Windows account)

Fortunately, there are not a lot of these "first-class" passwords.
These passwords are so important that you MUST learn them by heart and never forget them. The easiest way to learn is by using them often. If you use a password once a week you will not forget it. If you use it once a year it is 100% sure you will forget it. Never use any password manager to store them, because that way you will forget them and it is dangerously prone to hacking.

You must somehow be able to store these super important passwords but never do it in a digital form because it can be hacked. Write them on a piece of paper and store them in a bank vault or hide them really really good. Like your life depends on it!

Obfuscate the passwords in this list. Make it look like they are not passwords at all. Don't write for what service they are using near them. Be mysterious. Be an 007 spy agent.  

## Second class passwords

And then there are "second-class" passwords. You can relax here. They don't protect anything valuable. You can use a "password manager" for them. There is a lot of these passwords, more then 100. Everywhere on the internet you create an account and use the password manager to store it. But always ask yourself if you are creating a "second-class" or a "first-class" password. The answer to this question must be precise. If there is a danger to loose money if hacked then this is a "first-class" password and must not go into the password manager.

## Password managers

Password managers are great for "second-class" passwords. When creating a new account for a service that does not involve money or digital identity, let the password manager create a new random password. It is a bunch of letters and numbers that nobody can remember. And you don't have to. You will always use the password manager to login to these services. That way all the passwords will be different and very difficult to crack.

But be aware that also password managers can be hacked. It is difficult but possible. So refrain from storing "first-class" passwords in them. These passwords are too important!

There are many different password managers: Dashlane, 1Password, Keeper, Bitwarden, even Google and probably Microsoft have their own password managers. I don't know which one to recommend. Try reading the reviews on the internet. Security is hard and you don't know whom to trust.

Some password managers can also store files. If not, then you will need an encrypted vault.

## Encrypted vault for files

Passwords are not the only secrets we have. There are files that we want to store securely away from the reach of hackers. For that, we use encrypted vaults like VeraCrypt, Cryptomator or similar. I cannot recommend any specific one, because I don't know whom to trust. It is your job to read reviews on the internet and choose the one you feel you can trust. Security is hard.

In the encrypted vault you can store for example the certificates from the government in the *.p12 files or configuration from programs that store passwords for FTP. Or maybe that photos from last summer that you don't want anybody to see. You can even store the backup of the password manager in there. Sure, it is already encrypted but 2 passwords are better security than one password. You can store important documents from your bank. You don't want to leave them lying around.

Once the files are encrypted you can store the vault in Dropbox, OneDrive or GDrive. Nobody will see the files hidden in it.

Warning: never forget the password for the encrypted vault. This is a "first-class" password. Super important. Never save it in a password manager. So try to use it often to refresh your memory.

## Primary email, other emails and recovery email

It is quite normal to have more than one email address. For example, these are serious emails with "first-class" passwords and 2FA enabled.

- personal email for friends and personal stuff (primary email)
- work email
- official email for communication with banks and the government

Then you need one or more non-serious emails that have a "second-class" password and don't need 2FA.

- funny email is for experimenting things on the internet without using "serious emails"

I recommend adding one more email just for recovery of the primary email. That email is also a "first-class" but must not have 2FA enabled. This email will be used only for recovery, nothing else.
It is important to remember the password because, in case of a catastrophic disaster, this is the starting point to revive your digital identity.

## Password recovery

Most of the "second-class" passwords are super easy to recover if we forget them. Usually, there is a button "forgot password". By clicking on it, the website sends a recovery link to your primary email. Click on it and you can assign a new password. Easy and fast. The security assumption is that your email is not compromised by a hacker.

But there are some places you cannot do that because they are too damn important. If you forget the password to your bank account you should probably go personally to the bank to recover it.  
If you forget the password to your encrypted vault there is no way to recover it. Nobody can help you.  
Some password managers have also no way to recover a forgotten master password. If you forget you cannot use it anymore.

This is good because recovering these passwords is extremely dangerous. These are "first-class" passwords. But also forgetting the password is very dangerous. You loose everything! Take notice! Errors are not tolerated here.

Don't despair. Just learn to live with the passwords in mind. It becomes second nature.

## Google account password recovery

Google account is really important. Under the same password, you have your Gmail, Gdrive, Chrome profile, even a password manager and much more. This is a "first-class" password. Google has come up with many different recovery methods for their password.  

But please don't use that! This is a "first-class" password. It is dangerous to use any digital online recovery methods. Instead, find and read the password from your secret hidden physical paper. You don't want a hacker to digitally intercept your recovery method.

And of course, if you use this password regularly, you will never forget it. This is the best way for "first-class" passwords.

## 2FA - two-factor authentication

Oh, how easy was life before 2FA two-factor authentication! You just remember the password. On any computer in the world, you could sit down, browse your preferred internet website and type the password. Boom. Done!

But that was dangerous. What if this password was somehow cracked? There are many ways to crack it. (The explanation is not in the scope of this tutorial.) The hacker could just use the password and you are hacked! If the service is your bank account, bye-bye your savings. Terrific!

We need something more. Something that the hacker cannot have. A second authentication that is not stored anywhere. Or it is temporarily limited to just one minute and cannot be reused later. Enter 2FA - two factor authentication. It is complicated.

## Email

This method is rarely used. After entering the password, the web site would send you a verification email with a short secret code. You copy and paste this code into the second authentication. This is ok, because the hacker can have your password but probably it does not have access to your email. Or has he?
This short code is time limited and after a minute or so, you cannot reuse it.

## SMS

We have now more smartphone in the world then computers. Virtually everybody have a smartphone today. Smartphones and even dumb phones can receive SMS text messages.

After entering the password, the web site would send you a verification SMS with a short secret code to your phone. You type this code into the second authentication. This is ok, because the hacker can have your password but probably it does not have access to your phone. Or has he?
This short code is time limited and after a minute or so, you cannot reuse it.
But sometimes your phone had exhausted the battery or there is no signal coverage.

## Pushed notification

Modern smartphones can receive pushed notification from a web service. For example, Google will send a notification that opens in your smartphone and ask you if it was you to login to their service. This looks nice but you need a smartphone with the possibility of pushed notification and a mobile internet signal.

If you loose you phone or don't have signal coverage, this method will not work.

## authenticator

Authenticators are little apps that calculate a short OTP one-time password that is time limited. They can run on the smartphone or on the computer. One example is Google Authenticator.

You need to initialize the authenticator using the codes from the service. That makes the service and the local authenticator share the same secret. You must also use the same date and time but all smartphones are already in sync with the atomic clocks.

For 2FA you use the code from the Authenticator app. You don't need internet access or mobile signal for that.

This is ok, because the hacker can have your password but probably it does not have access to your authenticator app. Or has he?
This short code is time limited and after a minute or so, you cannot reuse it.
But sometimes you loose your phone, or it breaks, or malfunction or is stolen, or falls in the water,...

## 2FA recovery

For most services today we have 2FA. It means we can still remember the password but we can loose access to the second authentication code. This can happen in a moment. You loose or break your phone. Probably it is the only device with your 2FA method. Without it, you cannot login to your service.

We need a way to recover from this. When you activate 2FA on any service, you have always an option to recover. You need to read it carefully and stay focused. There are different ways that are offered from different services.

### Google account 2FA

You should turn on 2FA for important passwords. This is a must today. If not, you risk your password to be cracked and your services to be hacked.  

Go to Manage your Google account - Security

Before you turn on 2FA set the "recovery email" and "recovery phone" to your best friend, to somebody you can trust 100%. Don't use your phone or your second email because when you loose access to your primary email, you will also loose access to your secondary email. And in the same moment your phone will be broken or stolen or lost. Choose your best friend email and phone.

Now choose 2-Step Verification - TURN ON

Then define second step after entering your password.

1. Google prompts (to your phone) - needs phone and internet connection
2. Authenticator app (install it on your phone) - needs phone
3. Text message (to your phone) - needs phone and mobile connection
4. Backup codes (download and save into your password manager. But be 100% sure that you don't have the password in the same place. The "first-class" passwords must not be in the password manager)








## Digital identity

## Certificates

## SSH keys and passphrases

## What to do when you lose everything

We will try to imagine the disaster scenario when you lose everything: your phone, laptop, tablet, everything. How to recover your digital identity from there. This will make clear why and how we set the security, passwords, 2FA and recovery on our services.

It is very bad to recover your digital life from a cyber cafe. This is not a secure environment and can lead to problems.

The best way to start is to buy a new phone and connect it to the internet. You can use mobile data or a Wifi. Later buy a new laptop when possible.

@startuml

title "Recovery of 2FA with codes"

participant "FirstClassPasswords\na_few_to_remember_by_heart\nwrite_on_hidden_paper" as FCP
participant "FirstPassManager\nwith_2FA\nonly_passwords" as FPM
participant "SecondPassManager\nNO_2FA\nonly_2FA_codes" as SPM
participant "PrimaryEmail\n2FA" as PE
participant "OnlineStorage\n2FA" as OS
participant "EncryptedVault\nNO_2FA" as EV

participant "OnlineServices\n2FA" as OOS2
participant "OnlineServices\nNO_2FA" as OOSN

FCP->SPM: 1st class password

FCP->FPM: 1st class password
SPM -> FPM: 2FA recovery codes

FCP->PE: 1st class password
SPM -> PE: 2FA recovery codes

FCP->OS: 1st class password
SPM -> OS: 2FA recovery codes

FCP->EV: 1st class password

FPM->OOS2: 2nd class password
SPM -> OOS2: 2FA recovery codes

FPM->OOSN: 2nd class password
OOSN -> PE: recovery email

@enduml

1. Open the special "recovery email", which we set on purpose without 2FA. You must know the password by heart! It is used only for the recovery of our primary Google account.
2. Open the primary email. We must know the password by heart. Then 

Special gmail for recovery only that has NO 2FA. And you must never forget the password to that, because it makes all other services with 2FA recoverable.

## Open-source and free as a beer

My open-source projects are free as a beer (MIT license).  
I just love programming.  
But I need also to drink. If you find my projects and tutorials helpful, please buy me a beer by donating to my [PayPal](https://paypal.me/LucianoBestia).  
You know the price of a beer in your local bar ;-)  
So I can drink a free beer for your health :-)  
[Na zdravje!](https://translate.google.com/?hl=en&sl=sl&tl=en&text=Na%20zdravje&op=translate) [Alla salute!](https://dictionary.cambridge.org/dictionary/italian-english/alla-salute) [Prost!](https://dictionary.cambridge.org/dictionary/german-english/prost) [Nazdravlje!](https://matadornetwork.com/nights/how-to-say-cheers-in-50-languages/) 🍻

[//bestia.dev](https://bestia.dev)  
[//github.com/bestia-dev](https://github.com/bestia-dev)  
[//bestiadev.substack.com](https://bestiadev.substack.com)  
[//youtube.com/@bestia-dev-tutorials](https://youtube.com/@bestia-dev-tutorials)  

[//]: # (auto_md_to_doc_comments segment end A)
