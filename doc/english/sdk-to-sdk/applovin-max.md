# Track AppLovin MAX ad revenue with Adjust SDK

[Adjust Unity SDK README][unity-readme]

Minimum SDK version required for this feature:

- **Adjust SDK v4.29.0**

If you want to track your ad revenue with the AppLovin MAX SDK, you can use our SDK-to-SDK integration to pass this information to the Adjust backend. To do this, you will need to construct an Adjust ad revenue object containing the information you wish to record, then pass the object to the `trackAdRevenue` method.

> Note: If you have any questions about ad revenue tracking with AppLovin MAX, please contact your dedicated account manager or send an email to [support@adjust.com](mailto:support@adjust.com).

### Example

```cs
// initialise with AppLovin MAX source
AdjustAdRevenue adjustAdRevenue = new AdjustAdRevenue(AdjustConfig.AdjustAdRevenueSourceAppLovinMAX);

// set revenue and currency
adjustAdRevenue.setRevenue(6.66, "USD");

// optional parameters
adjustAdRevenue.setAdRevenueNetwork("network");
adjustAdRevenue.setAdRevenueUnit("unit");
adjustAdRevenue.setAdRevenuePlacement("placement");

// track ad revenue
Adjust.trackAdRevenue(adjustAdRevenue);

```

[unity-readme]:    ../../../README.md
