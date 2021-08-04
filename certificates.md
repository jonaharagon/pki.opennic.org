---
layout: page
title: Certificates
---

{% include beta.html %}

## Root Certificate Authorities

You can test whether your products are compatible with our roots by following the test links for each root.

<table class="table table-bordered">
  <thead>
    <tr>
      <th scope="col">Name (<code>CN</code>)</th>
      <th scope="col">Primary Operator</th>
      <th scope="col">Key</th>
      <th scope="col">Fingerprint (SHA1)</th>
      <th scope="col">Expiration</th>
      <th scope="col">Download</th>
      <th scope="col">Test</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">OpenNIC Root CA X1</th>
      <td><a href="mailto:jonah@opennic.org">Jonah Aragon</a></td>
      <td>ECDSA P-384</td>
      <td>05:89:EA:FA:2D:A6:E4:77:3A:EA:83:B3:6F:FC:A4:AF:C0:C0:E4:69</td>
      <td>2026-08-23</td>
      <td>crt pem txt</td>
      <td>Valid Expired Revoked</td>
    </tr>
    <tr>
      <th scope="row">OpenNIC Root CA X2</th>
      <td><a href="mailto:jonah@opennic.org">Jonah Aragon</a></td>
      <td>ECDSA P-384</td>
      <td>05:89:EA:FA:2D:A6:E4:77:3A:EA:83:B3:6F:FC:A4:AF:C0:C0:E4:69</td>
      <td>2026-08-23</td>
      <td>crt pem txt</td>
      <td>Valid Expired Revoked</td>
    </tr>
    <tr>
      <th scope="row">OpenNIC Root CA X3</th>
      <td><a href="mailto:jonah@opennic.org">Jonah Aragon</a></td>
      <td>RSA 4096</td>
      <td>05:89:EA:FA:2D:A6:E4:77:3A:EA:83:B3:6F:FC:A4:AF:C0:C0:E4:69</td>
      <td>2026-08-23</td>
      <td>crt pem txt</td>
      <td>Valid Expired Revoked</td>
    </tr>
    <tr>
      <th scope="row">OpenNIC Root CA X4</th>
      <td><a href="mailto:jonah@opennic.org">Jonah Aragon</a></td>
      <td>RSA 4096</td>
      <td>05:89:EA:FA:2D:A6:E4:77:3A:EA:83:B3:6F:FC:A4:AF:C0:C0:E4:69</td>
      <td>2026-08-23</td>
      <td>crt pem txt</td>
      <td>Valid Expired Revoked</td>
    </tr>
  </tbody>
</table>

## Tier 1 Subordinate CAs

The following CAs have been created to support direct or indirect certificate issuance. They have lifetimes of 1-4 years, have strict name constraints configured, and can issue DV certificates directly or create shorter-lived subordinate CA certificates for issuance.

<table class="table table-bordered caption-top">
  <caption>Issued By: OpenNIC Root CA X1</caption>
  <thead>
    <tr>
      <th scope="col">Name (<code>CN</code>)</th>
      <th scope="col">Organization (<code>O</code>)</th>
      <th scope="col">Key</th>
      <th scope="col">Fingerprint (SHA1)</th>
      <th scope="col">Expiration</th>
      <th scope="col">Download</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Aragon Authority E1</th>
      <td><a href="mailto:jonah@triplebit.net">Aragon Ventures LLC</a></td>
      <td>ECDSA P-384</td>
      <td>05:89:EA:FA:2D:A6:E4:77:3A:EA:83:B3:6F:FC:A4:AF:C0:C0:E4:69</td>
      <td>2024-08-23</td>
      <td>crt pem txt</td>
    </tr>
  </tbody>
</table>

<table class="table table-bordered caption-top">
  <caption>Issued By: OpenNIC Root CA X3</caption>
  <thead>
    <tr>
      <th scope="col">Name (<code>CN</code>)</th>
      <th scope="col">Organization (<code>O</code>)</th>
      <th scope="col">Key</th>
      <th scope="col">Fingerprint (SHA1)</th>
      <th scope="col">Expiration</th>
      <th scope="col">Download</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Aragon Authority R1</th>
      <td><a href="mailto:jonah@triplebit.net">Aragon Ventures LLC</a></td>
      <td>RSA 2048</td>
      <td>05:89:EA:FA:2D:A6:E4:77:3A:EA:83:B3:6F:FC:A4:AF:C0:C0:E4:69</td>
      <td>2024-08-23</td>
      <td>crt pem txt</td>
    </tr>
  </tbody>
</table>

## Tier 2 Subordinate CAs

The following CAs have been created to support direct certificate issuance. They have lifetimes of 6 months, are expected to be cycled every 3 months by the issuing organization, and have strict name constraints configured.

<table class="table table-bordered caption-top">
  <caption>Issued By: OpenNIC Root CA X2</caption>
  <thead>
    <tr>
      <th scope="col">Name (<code>CN</code>)</th>
      <th scope="col">Organization (<code>O</code>)</th>
      <th scope="col">Key</th>
      <th scope="col">Fingerprint (SHA1)</th>
      <th scope="col">Expiration</th>
      <th scope="col">Download</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td colspan="6"><em>There are currently no subordinate CAs issued by OpenNIC Root CA X2.</em></td>
    </tr>
  </tbody>
</table>

<table class="table table-bordered caption-top">
  <caption>Issued By: OpenNIC Root CA X4</caption>
  <thead>
    <tr>
      <th scope="col">Name (<code>CN</code>)</th>
      <th scope="col">Organization (<code>O</code>)</th>
      <th scope="col">Key</th>
      <th scope="col">Fingerprint (SHA1)</th>
      <th scope="col">Expiration</th>
      <th scope="col">Download</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row"></th>
      <td><a href="mailto:opennic@eckner.net">Erich Eckner</a></td>
      <td>RSA 4096</td>
      <td>05:89:EA:FA:2D:A6:E4:77:3A:EA:83:B3:6F:FC:A4:AF:C0:C0:E4:69</td>
      <td>2022-02-03</td>
      <td>crt pem txt</td>
    </tr>
  </tbody>
</table>

## Third-Party Root CAs

The following Root CAs are operated by members of the OpenNIC community, however they are <strong>not</strong> signed by the OpenNIC Root CA. Inclusion in this list is <strong>not</strong> an indication of their trustworthiness. We provide this information for <strong>informational purposes only</strong>, and have <strong>not</strong> evaluated any of these providers.

*There are currently no well-known alternative Root CAs serving OpenNIC.*

## Historical Root CAs

The following Root CAs have been depreciated.

<table class="table table-bordered">
  <thead>
    <tr>
      <th scope="col">Name (<code>CN</code>)</th>
      <th scope="col">Organization (<code>O</code>)</th>
      <th scope="col">Key</th>
      <th scope="col">Fingerprint (SHA1)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">OpenNIC Root CA</th>
      <td><a href="mailto:opennic@eckner.net">Erich Eckner</a></td>
      <td>RSA 4096</td>
      <td>05:89:EA:FA:2D:A6:E4:77:3A:EA:83:B3:6F:FC:A4:AF:C0:C0:E4:69</td>
    </tr>
  </tbody>
</table>

## Revoked Subordinate CAs

*We do not currently have any revoked subordinate CAs.*
