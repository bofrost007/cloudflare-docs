---
pcx-content-type: concept
title: Challenge Solve Rate (CSR)
weight: 2
---

# Challenge Solve Rate (CSR)

The Challenge Solve Rate (CSR) is the percentage of issued challenges — Legacy CAPTCHA, JS Challenge, or Managed Challenge actions — that were solved. You can find the CSR of a rule by going to **Security** > **Firewall rules**.

```sql
CSR = number of challenges solved / number of challenges issued
```

This metric helps you evaluate your rule's effectiveness, as well as whether you need to make any adjustments to the rule's criteria or action.

## Common scenarios

The CSR provides an indication of automated traffic:

- If you see a high CSR (above **3%**), you might want to reevaluate the criteria of your rule to prevent human visitors from receiving challenges.
- If you see a low CSR (below **3%**), you likely do not need to adjust your rule but may still want to review its CSR periodically.
- If the rate is close to **0%**, your rule is only acting on automated traffic. Consider changing the rule action to _Block_.

{{<Aside type="warning" header="Important">}}

For customers on a Free plan, any rules configured with the _Legacy CAPTCHA_ action now use Managed Challenges. For more information, see [Understanding Cloudflare Captchas and Challenge Passage](https://support.cloudflare.com/hc/articles/200170136#managed-challenge).

{{</Aside>}}
