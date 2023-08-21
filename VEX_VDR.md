# Unconfusing VEX and VDR

Last update: 2023-06-27  
zmanion@protonmail.com

## Summary
Vulnerability Exploitability eXchange (VEX) and Vulnerability Disclosure Reports (VDR) are similar concepts that are sometimes conflated or confused. While both concepts are in relatively early stages of development and implementation, VEX is more clearly defined and has a more substantial history.

## VDR defined

### NIST SP 800-161r1

The concept of a Vulnerability Disclosure Report (VDR) was first introduced in [NIST SP 800-161r1](https://doi.org/10.6028/NIST.SP.800-161r1) *Cybersecurity Supply Chain Risk Management Practices for Systems and Organizations*. The final version of this SP was published in May 2022 and "VDR" does not appear in previous drafts. VDR is defined in Appendix A: C-SCRM Security Controls in the Risk Assessment family under RA-5 Vulnerability Monitoring and Scanning. Appendix A provides "Supplemental C-SCRM Guidance" to some of the controls defined in [NIST SP 800-53, Rev. 5](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53r5.pdf):

> This section is structured as an enhanced overlay of \[NIST SP 800-53, Rev. 5\]. It identifies and augments C-SCRM-related controls with additional supplemental guidance and provides new controls as appropriate.

VDR is described in SP 800-161r1, RA-5, page 132:

> Enterprises, where applicable and appropriate, may consider providing customers with a Vulnerability Disclosure Report (VDR) to demonstrate proper and complete vulnerability assessments for components listed in SBOMs. The VDR should include the analysis and findings describing the impact (or lack of impact) that the reported vulnerability has on a component or product. The VDR should also contain information on plans to address the CVE. Enterprises should consider publishing the VDR within a secure portal available to customers and signing the VDR with a trusted, verifiable, private key that includes a timestamp indicating the date and time of the VDR signature and associated VDR. Enterprises should also consider establishing a separate notification channel for customers in cases where vulnerabilities arise that are not disclosed in the VDR. Enterprises should require their prime contractors to implement this control and flow down this requirement to relevant sub-tier contractors.

RA-5 refers departments and agencies to Appendix F for additional guidance on [EO 14028](https://www.federalregister.gov/executive-order/14028). Appendix F in turn refers to NIST’s dedicated EO 14028 [web-based portal](https://www.nist.gov/itl/executive-order-14028-improving-nations-cybersecurity). Neither "vulnerability disclosure report" nor "VDR" appear in these additional sources.

### Draft NIST SP 800-216

"Vulnerability disclosure report" language (but not the VDR acronym) also appears in [Draft NIST SP 800-216](https://doi.org/10.6028/NIST.SP.800-216-draft) *Recommendations for Federal Vulnerability Disclosure Guidelines* published in June 2021. Neither "vulnerability disclosure report" nor "VDR" appear in the final version of SP 800-216 published in May 2023.

In Draft NIST SP 800-216, "vulnerability disclosure report" describes an incoming report to a department or agency's Vulnerability Disclosure Program Office (VDPO). This is different than the NIST SP 800-161r1 description of a VDR as a "...proper and complete vulnerability assessments for components listed in SBOMs."

## VEX defined
From [*Vulnerability-Exploitability eXchange (VEX) – An Overview*](https://ntia.gov/sites/default/files/publications/vex_one-page_summary_0.pdf) published in September 2021:

> The primary use cases for VEX are to provide users (e.g., operators, developers, and services providers) additional information on whether a product is impacted by a specific vulnerability in an included component and, if affected, whether there are actions recommended to remediate.

From [*Minimum Requirements for Vulnerability Exploitability eXchange (VEX)*](https://www.cisa.gov/sites/default/files/2023-04/minimum-requirements-for-vex-508c.pdf) published in April 2023:

> Vulnerability Exploitability eXchange (VEX) indicates the status of a software product or component with respect to a vulnerability. A common VEX use case is to indicate that software is or is not affected by a vulnerability.

## VEX and VDR together

Taking the NIST SP 800-161r1 definition of VDR, it seems reasonable that a VDR could consist of a set of VEX documents and statements.

VDR is sometimes described as providing postive acknowledgement that software is affected by a vulnerability, contrasted with VEX asserting that software is *not* affected by a vulnerability. VEX can convey that software is or is not affected by a vulnerability. From *Minimum Requirements*:

> \[status\] MUST be one of the following values, some of which have further requirements:
> * Not affected (“not\_affected”)
> * Affected (“affected”)
> * Fixed (“fixed”)
> * Under investigation (“under\_investigation”)
