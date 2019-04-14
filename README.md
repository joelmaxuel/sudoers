# sudoers
## A configuration concept to pull back from the "all or nothing" approach

Joel Maxuel (joelmaxuel), 2019

## Introduction

Some time ago I have come across a moral challenge with the `sudo` command.  I have used it for years for a quick and convenient way to issue a few privileged commands, and continue along my way.

I seemed to recall when I first heard of it, I was surprised to hear that to gain root access, you enter your own password.  "Wait, what?"  I may have become comfortable with using the command over the years, but that initial reaction is now creeping back.

To be frank, there is no right answer.  One could use `sudo` as it came out of the box, and if an attacker got access to your system, all it would need is your password.
One could make a small adjustment by setting the `rootpw` default flag - but now there is little to no difference between a `sudo` and a `su -c`.
Ultimately, avoiding `sudo` altogether results in overusing the root privilege, which may result in an unknowingly exposed password down the line.

However my assertion is that the greatest problem with `sudo` is not what it is (legitimately) used for, rather that way more often that not, no work has been done to personalize or lock down the "wide open" policy.

Enter this concept.

## A few steps closer to your balanced approach

As I have already said there is no right answer, I am not going to claim this is for you, much less to "just copy the files in and walk away".  No, your needs are (likely) much different than mine, once you get past the idea of being able to "do anything" with your system while ensuring a stranger can "do nothing".

I would consider this somewhat useful for scenarios ranging from a family computer to a small team managing a similarly small number of systems.

What makes this strategy different is the use of a password from an arbitrary account.  As in, for a user to complete a privileged command, she must enter a password that is neither her own nor root's.  Further, what *is* allowed, is boiled down to what is beneficial.  Finally (useful in a shared environment), user error (which could also be attempts of attack) are fiercely logged.

## Take a look

I will add more context in this README at a later time; in the meantime take a look at what a balancing act each component can be.

If you have suggestions on how to improve a specific scenario (admittedly yes, there are problems with every approach - come help mitigate or even solve some of these loopholes), please make a pull request.

Cheers.
