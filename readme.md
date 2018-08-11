# SAML SSO with ADFS Provision Manual

## 1. AD / ADFS Architecture

![](https://lh3.googleusercontent.com/-zar5_s7BfPA/W21f99XRQ4I/AAAAAAAAJGQ/qvPLzQIvUjYXNNEahYudJGR-NcrL9CKWQCHMYCw/I/15115101530194.jpg)

## 2. How to Add User in AD

### 2.1 Create User

Choose [Active Directory Users and Computers] in start menu

![](https://lh3.googleusercontent.com/-DGs38AqQrHg/W21f-pHGDRI/AAAAAAAAJGU/6WVWqd8fBHEx89zcR4z2kC1yXcaVWx8vgCHMYCw/I/15115053615964.jpg)

Choose [Splashtop SSO] in Active Directory Users and Computers

![](https://lh3.googleusercontent.com/-UpnwxIcyZlI/W21f-5ajcjI/AAAAAAAAJGY/OuoD4svNxtctxBvMA66S9Et3IJQC7qtwACHMYCw/I/15115053942279.jpg)

Add new User to Splashtop SSO

![](https://lh3.googleusercontent.com/-cF1lNjpFddE/W21f_TTMYDI/AAAAAAAAJGc/CucsR5JDEi4OXr-3bxLiGYhU43IA_DbgQCHMYCw/I/15115054159264.jpg)

Enter User Name, then press [Next]

![](https://lh3.googleusercontent.com/-qw_38USad5Y/W21f__xRh9I/AAAAAAAAJGg/nh1V3r8wVdAePQTfQgWedTntPYndMlNOgCHMYCw/I/15115055786886.jpg)

1. password must have at least 1 uppercase, 1 downcase ,1 digit and length larger than 8.
2. choose [Password never expires]
3. press [Next]

![](https://lh3.googleusercontent.com/-CsRb6od1bzo/W21gAcahA6I/AAAAAAAAJGk/jzdPrmbHmmk_6PsbrHDvszCIRnCj2HvvACHMYCw/I/15115057375626.jpg)

![](https://lh3.googleusercontent.com/-2ui2daA4RrY/W21gA3T-a_I/AAAAAAAAJGo/Q0xb_eRSObgidye6sVX95sExR23IH1pLQCHMYCw/I/15115062961374.jpg)

### 2.2 Add User to SSO group

Choose [Add to a group]

![](https://lh3.googleusercontent.com/-VrVQPMTWdyY/W21gBeSsMBI/AAAAAAAAJGs/ILfp_DpGdbwi2dnAENCBjsZu3uZn9ptOQCHMYCw/I/15115063844544.jpg)

![](https://lh3.googleusercontent.com/-Cd-x0bRDiCo/W21gB0mnT-I/AAAAAAAAJGw/q1qKqM26XmACcazmrIHeyqbkVmjWHIlZgCHMYCw/I/15115066589025.jpg)

![](https://lh3.googleusercontent.com/-GZlhy0K5nPE/W21gCfVRSKI/AAAAAAAAJG0/0uO-eXSNEtQwdGYEUmIwDNpsyRGNBjTqgCHMYCw/I/15115066789464.jpg)

### 2.3 Add Email to User

Double click user that you created.

![](https://lh3.googleusercontent.com/-NeRk4jS--20/W21gCjzJglI/AAAAAAAAJG4/VhgmevQpb4YCqkt_SwTLGekMFcBVoPqIQCHMYCw/I/15115069654817.jpg)

Fill email field then press [OK]

![](https://lh3.googleusercontent.com/-UBcfk0KEw_o/W21gC2I0LLI/AAAAAAAAJG8/mJcEwn6a3-kIAyUE_EmLW4MngWwfNQkEQCHMYCw/I/15115068465646.jpg)



## 3. SSO

### 3.1 set ADFS HOST / DNS

```
IP_ADDRESS_YOUR_ADFS  esADFS01.es.lab
```

### 3.2 SSO

open webpage https://your-adfs-url/saml and click login.

![](https://lh3.googleusercontent.com/-5mlvlwoGlcA/W21gDRgYHyI/AAAAAAAAJHA/xL_-ByRxP_8nnKRlP7nGgqvCgk3fUr0fACHMYCw/I/15115108237849.jpg)

Choose Sign in to one of the following sites and select Great ADFS SSO.

![](https://lh3.googleusercontent.com/-mydaeAm92d8/W21gDiLYULI/AAAAAAAAJHE/cmPGaZOpVDk9CRBfwKyUGS9gjvCEb8vwwCHMYCw/I/15115078380573.jpg)

Enter username and password.

![](https://lh3.googleusercontent.com/-cCA0cDKuIz4/W21gEKUclbI/AAAAAAAAJHI/wu4h-xYuzUIJONF5GfuPAMarlkqVlVoEgCHMYCw/I/15115081135173.jpg)

Login Success!!

![](https://lh3.googleusercontent.com/-tlGIWeTMrp0/W21gH515YeI/AAAAAAAAJHo/MNCREuCwNmEk8dPU8hjR0DHEm2xInkBUgCHMYCw/I/15115081389508.jpg)

## 4. Introduce to ADFS

### 4.1 Select Relying Party

![](https://i.imgur.com/XIO339E.png)

metadata

![](https://i.imgur.com/GlMrHch.png)


identifier

![](https://i.imgur.com/rRnOBJu.png)

Assertion Comsumer

![](https://i.imgur.com/3M8XYQ0.png)

## 4.2 Claim

![](https://i.imgur.com/uyx8qbA.png)

rule 1 - get email from AD
rule 2 - email to SAML NameID

![](https://i.imgur.com/B2SNvGn.png)

![](https://lh3.googleusercontent.com/-tlGIWeTMrp0/W21gH515YeI/AAAAAAAAJHo/MNCREuCwNmEk8dPU8hjR0DHEm2xInkBUgCHMYCw/I/15115081389508.jpg)

### 4.3 Provision ADFS from Zero

[Configuring ADFS 3.0 to Communicate with SAML 2.0 - ServiceNow Wiki](http://wiki.servicenow.com/index.php?title=Configuring_ADFS_3.0_to_Communicate_with_SAML_2.0#gsc.tab=0)



