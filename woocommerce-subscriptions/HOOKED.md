# Hooked actions

## `woocommerce_scheduled_subscription_payment`
> Args: `subscription_id`

1. `WC_Subscriptions_Manager::maybe_process_failed_renewal_for_repair`

   > Check if the subscription needs to use the failed payment process to repair its status after it incorrectly expired due to a date migration bug in upgrade process for 2.0.0 of Subscriptions (i.e. not 2.0.1 or newer). See WCS_Repair_2_0_2::maybe_repair_status() for more details.
   1. Priority: `0`
   1. Args: 1

1. `WC_Subscriptions_Manager::prepare_renewal`

   > Sets up renewal for subscriptions managed by Subscriptions. This function is hooked early on the scheduled subscription payment hook.
   1. Priority: `1`
   1. Args: 1

1. `WC_Subscriptions_Payment_Gateways::gateway_scheduled_subscription_payment`

   > Fire a gateway specific hook for when a subscription payment is due.
   1. Priority: `10`
   1. Args: 1
