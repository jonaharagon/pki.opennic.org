---
layout: page
---

{% include beta.html %}

<div class="p-5 mb-4 bg-light rounded-3">
  <div class="container-fluid py-5">
    <h1 class="display-5 fw-bold">TLS/SSL for OpenNIC</h1>
    <p class="col-md-8 fs-4">OpenNIC PKI is a democratic collection of Certificate Authorities issuing certificates for the OpenNIC network as well as OpenNIC peers. Trusting our certificates requires installing our Root Certificate Authorities on your system.</p>
    <a href="install.html" class="btn btn-primary btn-lg" type="button"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-box-seam" viewBox="0 0 19 19">
  <path d="M8.186 1.113a.5.5 0 0 0-.372 0L1.846 3.5l2.404.961L10.404 2l-2.218-.887zm3.564 1.426L5.596 5 8 5.961 14.154 3.5l-2.404-.961zm3.25 1.7-6.5 2.6v7.922l6.5-2.6V4.24zM7.5 14.762V6.838L1 4.239v7.923l6.5 2.6zM7.443.184a1.5 1.5 0 0 1 1.114 0l7.129 2.852A.5.5 0 0 1 16 3.5v8.662a1 1 0 0 1-.629.928l-7.185 2.874a.5.5 0 0 1-.372 0L.63 13.09a1 1 0 0 1-.63-.928V3.5a.5.5 0 0 1 .314-.464L7.443.184z"/>
</svg> Install Now</a>
    <a href="certificates.html" class="btn btn-outline-primary btn-lg" type="button"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-patch-check" viewBox="0 0 19 19">
  <path fill-rule="evenodd" d="M10.354 6.146a.5.5 0 0 1 0 .708l-3 3a.5.5 0 0 1-.708 0l-1.5-1.5a.5.5 0 1 1 .708-.708L7 8.793l2.646-2.647a.5.5 0 0 1 .708 0z"/>
  <path d="m10.273 2.513-.921-.944.715-.698.622.637.89-.011a2.89 2.89 0 0 1 2.924 2.924l-.01.89.636.622a2.89 2.89 0 0 1 0 4.134l-.637.622.011.89a2.89 2.89 0 0 1-2.924 2.924l-.89-.01-.622.636a2.89 2.89 0 0 1-4.134 0l-.622-.637-.89.011a2.89 2.89 0 0 1-2.924-2.924l.01-.89-.636-.622a2.89 2.89 0 0 1 0-4.134l.637-.622-.011-.89a2.89 2.89 0 0 1 2.924-2.924l.89.01.622-.636a2.89 2.89 0 0 1 4.134 0l-.715.698a1.89 1.89 0 0 0-2.704 0l-.92.944-1.32-.016a1.89 1.89 0 0 0-1.911 1.912l.016 1.318-.944.921a1.89 1.89 0 0 0 0 2.704l.944.92-.016 1.32a1.89 1.89 0 0 0 1.912 1.911l1.318-.016.921.944a1.89 1.89 0 0 0 2.704 0l.92-.944 1.32.016a1.89 1.89 0 0 0 1.911-1.912l-.016-1.318.944-.921a1.89 1.89 0 0 0 0-2.704l-.944-.92.016-1.32a1.89 1.89 0 0 0-1.912-1.911l-1.318.016z"/>
</svg> Certificate List</a>
  </div>
</div>

## Intro &amp; Benefits

<p class="lead">Encryption is a vital part of the modern internet, but traditional Certificate Authorities are not permitted to issue certificates to domains outside of the ICANN root zone, such as for OpenNIC, New Nations, or FurNIC domains. OpenNIC PKI enables a collection of independent OpenNIC-focused Certificate Authorities to issue certificates under the OpenNIC Root CA, so that OpenNIC users can authenticate and encrypt traffic to OpenNIC websites.</p>

OpenNIC PKI is being built with a security-first mentality, and we are making best-efforts to conform to CA industry standards wherever possible. Another primary goal of OpenNIC PKI is enabling democratic and decentralized control of Certificate Authorities in the network. Any OpenNIC member is eligible to operate a Subordinate CA, however there are strict requirements and restrictions on doing so to balance this decentralization with security. Much of the rest of this website is technical details on how we wish to accomplish this.

If you are a visitor to OpenNIC or a website operator, you will want to first <a href="install.html">install our Root CA</a> in your system in order to trust websites signed by our system.

{% assign accordion = "accordionIntroFAQ" %}
<div class="accordion" id="{{ accordion }}">
{% include accordion-item.html
  title="What are TLS/SSL certificates?"
  content='<p>TLS/SSL certificates are used to authenticate and establish secure connections to websites. Browsers use certificates to know that  information being transmitted is being sent to the right server, and that information to/from the server has not been read or modified in-transit. Certificates are issued and cryptographically signed by entities known as Certificate Authorities.</p>'
%}
{% include accordion-item.html
  title="What are self-signed certificates?"
  content='<p>It is possible to create and use a certificate on your website without involving a Certificate Authority. These self-signed certificates require no registration or fees, but they have some drawbacks. Visitors to your website will receive a large warning in their browsers stating that the certificate is not trusted by their system. It is also very difficult to validate whether a self-signed certificate is being legitimately provided by the server rather than a <abbr title="Man-in-the-Middle" class="initialism">MITM</abbr>, without manually comparing certificate fingerprints against a known-trusted source.</p>
  <p>The goal of OpenNIC PKI is to eliminate the need for self-signed certificates, while maintaining security and as much democracy and decentralization as possible under the current PKI/CA model.</p>'
%}
{% include accordion-item.html
  title="I run an OpenNIC domain name. Where do I get a certificate?"
  content='<p>OpenNIC website/server operators should visit <a href="https://wiki.opennic.org/opennic/tls">https://wiki.opennic.org/opennic/tls</a> for information on obtaining and installing a TLS certificate from a Subordinate CA provider. The information on this website is primarily useful for OpenNIC <em>visitors/users</em> and those seeking to operate a Subordinate CA themselves. We do not provide certificates to OpenNIC website operators directly from this website.</p>'
%}
</div>

## Project Goals and Overview

The intent of this project is to provide a single root authority for OpenNIC zones that can be trusted by OpenNIC users and domain operators alike. Currently, this single root authority takes the form of four Root CA certificates that must be trusted by your local computer system.

We will not be signing domain certificates with our Root CA certificates directly. Instead, we will sign **Subordinate CAs** that will be responsible for issuing domain-validated certificates on our behalf. Subordinate CAs can be run by many different individuals, alleviating a single-point-of-failure in our PKI model.

Subordinate CAs take two forms:

- **Tier 2 Subordinate CAs** are relatively short-lived, with 6 month expiration dates. They are intended to be rolled over every 3 months, enabling their use in an ACME-based certificate issuance system.
- **Tier 1 Subordinate CAs** are relatively long-lived, with expiration ranging from 1 to 3 years. Tier 1 Certificate Authorities have the ability to issue subordinate CAs of their own, effectively making them "mini Root CAs". The intended purpose of Tier 1 Certificate Authorities is to allow certain trusted individuals to create their own shorter-lived "Tier 2" CAs for use in an ACME-based issuance system without needing to request/negotiate a CA rollover with the central OpenNIC PKI Root CA every 3 months. Additionally, Tier 1 CAs can issue longer-lived server certificates, whereas Tier 2 CAs are practically limited to 30-day issuance.

{% assign accordion = "accordionGoalsFAQ" %}
<div class="accordion" id="{{ accordion }}">
{% include accordion-item.html
  title="Why distinguish between Tier 1 and 2?"
  content='<p>Decentralization is a primary goal of the OpenNIC PKI project, and we want to enable the creation of multiple issuing Certificate Authorities in the OpenNIC network. At the same time there is a need to maintain strict security standards.</p>
  <p>We believe that establishing a more limited Tier 2 Certificate Authority allows us to mitigate some of the risk of granting Certificate Authorities to less well-established individuals in the OpenNIC network. Tier 2 authorities need to regularly check in with OpenNIC PKI for re-issuance (every 3 months), and any potential breach will have shorter/limited impact.</p>'
%}
</div>

## Becoming a Certificate Authority

In line with our open and democratic nature, the ability to become a Certificate Authority under this system is a right granted to all OpenNIC members. However, there are requirements to be met before you can be issued a Tier 1 or 2 Subordinate CA:

 - You must **already** have an automated certificate issuance solution that is tested and working properly.
   - Your solution must somehow validate that the requestor is permitted to receive a domain-validated certificate from you. We recommend using ACME challenges to validate these requests.
   - Some existing ACME solutions that may prove useful to you include [Let's Encrypt Boulder](https://github.com/letsencrypt/boulder), [Smallstep step-ca](https://github.com/smallstep/certificates), and [acme2certifier](https://github.com/grindsa/acme2certifier).
 - You must issue domain-validated certificates to the public, for free. The OpenNIC Root does not sign any paid-only nor internal-use-only CAs.
 - You must maintain a <attr title="certificate revocation list" class="initialism">CRL</attr> accessible at an `http://` endpoint defined in your CA certificate. It must be updated at least monthly, and the `nextUpdate` field must not be greater than 1 month. It must be updated within 24 hours of revoking a subscriber's certificate.
   - Additionally, it is strongly recommended to maintain an OCSP responder, although not a requirement at this time.
 - You must only issue certificates with RSA keys with a modulus size of at least 2048 bits; or ECDSA keys on the NIST P-256, NIST P-384, or NIST P-521 elliptic curve.
   - If you generate private keys on the subscriber's behalf, you must not archive the private key after delivery.
 - You may not issue certificates for greater than 397 days, or for longer than the expiry of your CA and any CA in the chain of trust.
   - You should not issue certificates for the maximum permissible time. It is strongly recommended to implement a system which enabled automatic key rollover such as ACME, and only issue 30-day certificates.

Those seeking to operate a Tier 1 CA must additionally meet the following requirements:

 - You must utilize hardware security (i.e. HSM/SmartCard technology) to store your CA's private key. Your CA's private key must not exist in a readable format anywhere else.
   - This is recommended for Tier 2 CAs as well, but not strictly a requirement at this time due to the short-lived nature of Tier 2 CAs, and quirks regarding the technical implementation of some domain issuance systems.
   - It is recommended to generate the key on the HSM/SmartCard itself to minimize the risk of mistakes. However, it is acceptable to generate a key on an offline, airgapped computer, provided that this computer is never connected to a network and the key is securely wiped from the machine after generation. This is useful to import the key onto multiple HSM/SmartCards for backup/redundancy purposes, for example.
 - You must have an intended use-case for your Certificate Authority that a Tier 2 Subordinate CA certificate would not be able to support.
   - We strongly recommend the use of Tier 2 CAs wherever possible, as they facilitate frequent key rollover.

{% assign accordion = "accordionCAFAQ" %}
<div class="accordion" id="{{ accordion }}">
{% include accordion-item.html
  title="Who can apply to run a Subordinate CA?"
  content='<p>Technically, the ability to operate a CA is open to anybody wishing to contribute. However, generally Tier 1 Certificate Authorities should be operated by <a href="https://servers.opennicproject.org/?tier=1">Tier 1 DNS Server Operators</a>. Tier 1 Subordinate CAs are primarily intended for people who wish to tightly integrate an SSL solution with one or more TLDs on the OpenNIC network, which typically means the operator would also have to operate that TLD in the first place. Members who are unaffiliated with an OpenNIC domain registry are strongly encouraged to utilize ACME to issue certificates, and the Tier 2 CA system is best suited for that use-case.</p>'
%}
{% include accordion-item.html
  title="What if I want to create my own Root CA instead?"
  content='<p>You can do so, but you would not benefit from automatic trust by users that have installed the OpenNIC PKI Team\'s Root CAs in their system.</p>
  <p>That being said, this website aims to be a central resource of all TLS/SSL/PKI related information in the OpenNIC universe. If you operate a well-established independent Root CA, you can add its information to the <em>Third-Party Root CAs</em> <a href="certificates.html">list</a>. Your Root CA would <strong>not</strong> be added to any official OpenNIC CA packages available on the installation page of this website.</p>'
%}
</div>

## Subordinate CA Issuance
