---
_build:
  publishResources: false
  render: never
  list: never
---

1. Log in to the [Cloudflare dashboard](https://dash.cloudflare.com/login).
2. Select **Spectrum**.
3. Select **Create an Application**. If this is your first time using Spectrum, the **Create an Application** modal appears.
4. Select your **[Application Type](/spectrum/reference/configuration-options/#application-type)**.
5. Under **Domain**, enter the domain that will use Spectrum.
6. Under **Edge Port**, enter the port Cloudflare should use for your application.
7. Under **Origin**, select **Load Balancer**.
8. Select the load balancer you want to use from the dropdown. Disabled load balancers will not show on the **Load Balancer** menu.
9. Select **Add**.