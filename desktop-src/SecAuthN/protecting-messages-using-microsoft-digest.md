---
Description: 'Explains how to protect messages using Microsoft Digest.'
ms.assetid: '15509d51-80c0-4d5c-aa24-4dc17de3f12c'
title: Protecting Messages Using Microsoft Digest
---

# Protecting Messages Using Microsoft Digest

## HTTP and SASL

As a means of detecting certain types of security violations, the client and server use the [security support provider interface](sspi.md) (SSPI) message [*integrity*](security.i_gly#-security-integrity-gly) functions [**MakeSignature**](makesignature.md) and [**VerifySignature**](verifysignature.md) to protect messages.

A client calls the [**MakeSignature**](makesignature.md) function to sign a message using its [*security context*](security.s_gly#-security-security-context-gly). The server uses the [**VerifySignature**](verifysignature.md) function to verify the message's origin. In addition to verifying the [*signature*](security.d_gly#-security-digital-signature-gly) that accompanies the message, the **VerifySignature** function also checks that the [*nonce*](security.n_gly#-security-nonce-gly) count (specified by the nc directive) is one greater than the last count sent for the nonce. If this is not the case, the **VerifySignature** function returns an SEC\_OUT\_OF\_SEQUENCE error code.

## SASL Only

The [**EncryptMessage (General)**](encryptmessage--general-.md) and [**DecryptMessage (General)**](decryptmessage--general-.md) functions supply confidentiality for post-authentication messages exchanged between client and server.

In order to use the message confidentiality functions, the server and client must have established a [*security context*](security.s_gly#-security-security-context-gly) with the following attributes:

-   Quality of protection, specified by the qop directive, must be "auth-conf".
-   An encryption mechanism must have been specified by means of the cipher directive.

 

 


