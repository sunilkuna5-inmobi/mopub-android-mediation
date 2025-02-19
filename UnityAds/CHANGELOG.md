## Changelog
  * 4.0.0.0
    * Update adapters to use latest Unity APIs and refactor event sending.
    * This version of the adapters has been certified with Untiy Ads 4.0.0 and MoPub SDK 5.18.0.

  * 3.7.5.1
    * Refactor adapters and update to use latest Unity Ads APIs.

  * 3.7.5.0
    * This version of the adapters has been certified with Unity Ads 3.7.5 and MoPub SDK 5.17.0.

  * 3.7.2.0
    * This version of the adapters has been certified with Unity Ads 3.7.2 and MoPub SDK 5.17.0.

  * 3.7.1.1
    * Remove mopub-sdk as a required dependency from POM file.

  * 3.7.1.0
    * Remove unnecessary callback in Rewarded Ad when SDK is not initialized.
    * This version of the adapters has been certified with Unity Ads 3.7.1 and MoPub SDK 5.16.4.

  * 3.6.0.1
    * Fix a bug where the rewarded video adapter fails to request a new ad after a show-related error happens.

  * 3.6.0.0
    * This version of the adapters has been certified with Unity Ads 3.6.0 and MoPub SDK 5.15.0.

  * 3.5.1.0
    * This version of the adapters has been certified with Unity Ads 3.5.1 and MoPub SDK 5.14.0.

  * 3.5.0.0
    * This version of the adapters has been certified with Unity Ads 3.5.0 and MoPub SDK 5.14.0.
    * Set automatic impression and click tracking on for banners.

  * 3.4.8.1
    * This version of the adapters has been certified with Unity Ads 3.4.8 and MoPub SDK 5.14.0.

  * 3.4.8.0
    * This version of the adapters has been certified with Unity Ads 3.4.8 and MoPub SDK 5.13.1.
    * Note that, this adapter version is not certified using Android API 30. For Android 11 compatibility, expect an upcoming adapter release.

  * 3.4.6.0
    * This version of the adapters has been certified with Unity Ads 3.4.6 and MoPub SDK 5.13.1.

  * 3.4.2.1
    * Refactor non-native adapter classes to use the new consolidated API from MoPub.
    * This and newer adapter versions are only compatible with 5.13.0+ MoPub SDK.

  * 3.4.2.0
    * This version of the adapters has been certified with Unity Ads 3.4.2.

  * 3.4.0.1
    * Log the Unity Ads placement ID in ad lifecycle events.

  * 3.4.0.0
    * This version of the adapters has been certified with Unity Ads 3.4.0.

  * 3.3.0.1
    * Update adapter to handle Unity Ads load behaviors seamlessly for fullscreen ads.
    * Remove deprecated `UnityBannerCallbackRouter` class.

  * 3.3.0.0
    * This version of the adapters has been certified with Unity Ads 3.3.0.
    * Update the banner adapter to use new load API.
    * Fix refresh logic for banner ads to render correctly.
    
  * 3.2.0.2
    * Fire a playback error callback when the rewarded video is unable to show.

  * 3.2.0.1
    * Add support for AndroidX. This is the minimum version compatible with MoPub 5.9.0.

  * 3.2.0.0
    * This version of the adapters has been certified with Unity Ads 3.2.0.
    * **Note**:On MoPub adunit refresh, Unity Banners may not render correctly and this issue will be fixed in the upcoming Unity SDK versions. This behavior is inconsistent and there is no suggested workaround at the moment 

  * 3.1.0.0
    * This version of the adapters has been certified with Unity Ads 3.1.0.
    * Add load API functionality via metadata API to prevent rewarded and interstitial placements from loading in UnityAds until `load` is called.

  * 3.0.3.0
    * This version of the adapters has been certified with Unity Ads 3.0.3.

  * 3.0.1.3
    * Make `placementId` not static in `UnityRewardedVideo` to fix missing callbacks for multiple rewarded video ad requests.

  * 3.0.1.2
    * Pass MoPub's log level to Unity Ads. To adjust Unity Ads' log level via MoPub's log settings, reference [this page](https://developers.mopub.com/publishers/android/test/#enable-logging).

  * 3.0.1.1
    * UnityAds Adapter will now be released as an Android Archive (AAR) file that includes manifest file for UnityAds.

  * 3.0.1.0
    * This version of the adapters has been certified with Unity Ads 3.0.1.
    
  * 3.0.0.1
    * **Note**: This version is only compatible with the 5.5.0+ release of the MoPub SDK.
    * Add the `UnityAdsAdapterConfiguration` class to: 
         * pre-initialize the Unity Ads SDK during MoPub SDK initialization process
         * store adapter and SDK versions for logging purpose
    * Streamline adapter logs via `MoPubLog` to make debugging more efficient. For more details, check the [Android Initialization guide](https://developers.mopub.com/docs/android/initialization/) and [Writing Custom Events guide](https://developers.mopub.com/docs/android/custom-events/).
    * Fix missing callbacks for subsequent rewarded videos. The adapter now registers Unity Ads listeners for every new ad request.
    * Allow supported mediated networks and publishers to opt-in to process a user’s personal data based on legitimate interest basis. More details [here](https://developers.mopub.com/docs/publisher/gdpr-guide/#legitimate-interest-support).

  * 3.0.0.0
    * This version of the adapters has been certified with UnityAds 3.0.0.
    * Add support for banner ad.
    * Update GDPR consent passing logic to use MoPub's `gdprApplies()` and `canCollectPersonalInfo`.
  
  * 2.3.0.2
    * Handle no-fill scenarios from Unity Ads. 

  * 2.3.0.1
    * Update the placement ID returned in the `getAdNetworkId` API (used to generate server-side rewarded video callback URL) to be non-null, and avoid potential NullPointerExceptions.

  * 2.3.0.0
    * This version of the adapters has been certified with Unity Ads 2.3.0.

  * 2.2.1.2
    * Update to share consent with Unity Ads only when user provides an explicit yes/no. In all other cases, Unity Ads SDK will collect its own consent per the guidelines published in https://unity3d.com/legal/gdpr

  * 2.2.1.1
    * Pass explicit consent to Unity Ads.

  * 2.2.1.0
    * This version of the adapters has been certified with Unity Ads 2.2.1.
    * General Data Protection Regulation (GDPR) update to support a way for publishers to determine GDPR applicability and to obtain/manage consent from users in European Economic Area, the United Kingdom, or Switzerland to serve personalize ads. Only applicable when integrated with MoPub version 5.0.0 and above.

  * 2.2.0.0
    * This version of the adapters has been certified with Unity Ads 2.2.0.
    * Pass the placement ID to Unity's isReady() checks.

  * 2.1.1.0
    * This version of the adapters has been certified with Unity Ads 2.1.1.

  * Initial Commit
  	* Adapters moved from [mopub-android-sdk](https://github.com/mopub/mopub-android-sdk) to [mopub-android-mediation](https://github.com/mopub/mopub-android-mediation/)
