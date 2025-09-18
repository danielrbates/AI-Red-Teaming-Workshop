# Examine AI evaluations and Defender alerts

> **Avg review time: ~15 min**

This guide provides instructions for examining the AI red teaming agent results across areas relevant to different personas protecting the GenAI application. One of the byproducts of running the AI red team agent is that it can produce security alerts due to it's attack strategy techniques employed on risk category content. Defender for AI Services will generate secuirty alerts that can be found where the persona is.

## Azure AI Foundry project red team evaluations

Security alerting from Defender for AI Services can be found in the left navigation blade of Azure AI Foundry.  Here, the data analyst or application owner can find if an alert was recently issued and view some basic information on the alert and affected resource, including some remediation steps. The user is invited to review the alert in more detail and evidence in Defender for Cloud.

![AI Foundry Alert](../images/aifoundalert.png)

![AI Foundry Alert Details](../images/aifoundalert2.png)

## Defender for Cloud

The security alert is also in Defender for Cloud and in the left navigation Security Alerts. The alert itself contains additional security context including aspects of the sucpicious prompt that triggered the alert. 

![MDC Alert](../images/mdcalert.png)

![MDC Alert](../images/mdcalertdetails1.png)

Some of those aspects include:

- MITRE ATT&CK® Tactics
- IP address
- Geo information
- The model involved in the attack

![MDC Alert](../images/mdcalertdetails2.png)

We can see even more rich data within the "Supporting evidence events" section by clicking "Show events" in the bottom right:

- Suspicious prompt segemnt
- User agent involved with browser or application
- Confidence score

![MDC Alert](../images/mdcalertdetails3.png)

## Defender XDR alerting

Finally, the Defender for AI Services alerting is available in the Defender XDR portal, and can also be correlated with other suspicious or malicious activity around similar patterns. The following below shows a Jailbreak attempt as part of a correlated larger attack story. The same evidence and information is available in different tiles, including the same information we saw in the Defender for Cloud alert such as Prompt Suspicious Segment.

![XDR Alert](../images/xdralert.png)

## AI-SPM within Azure AI Foundry and Defender for Cloud

Security Recommendations are also generated to reduce attack surfaces and harden Azure Services including Azure AI Foundry. These results can be found across areas relevant to different personas protecting the GenAI application. These recommendations are surfaced at Azure AI Foundry Project -> Guardrails + controls -> Security Recommendations. By clicking on a recommendation, you can get some additional details and a pivot link for more information found in Defender for Cloud.

![AI recommendation](../images/aispmrec.png)

The same recommendation appears in Defender for Cloud -> Recomendations:

![MDC recommendation](../images/mdcspmrec.png)

Defender for Cloud will have additional context involving the MITRE ATT&CK® Tactics involved with the attack surface, any additional risk factors, and a top suggested active user for assignment for remediation.
