## Changelog
  * 20.3.0.0
    * This version of the adapters has been certified with AdMob 20.3.0 and MoPub 5.18.0.

  * 20.2.0.2
    * This version of the adapters has been certified with AdMob 20.2.0 and MoPub 5.18.0.
    * Refactor internal media layout to maintain compatibility with MoPub 5.18.0.

  * 20.2.0.1
    * Make native ad icon optional.

  * 20.2.0.0
    * This version of the adapters has been certified with AdMob 20.2.0 and MoPub 5.17.0.

  * 20.1.0.0
    * This version of the adapters has been certified with AdMob 20.1.0 and MoPub 5.16.4.

  * 20.0.0.2
    * Remove mopub-sdk as a required dependency from POM file.

  * 20.0.0.1
    * Set MediaView's scale type to `CENTER_CROP` to fix native ad alignment issues.

  * 20.0.0.0
    * This version of the adapters has been certified with AdMob 20.0.0 and MoPub 5.16.4.

  * 19.8.0.0
    * This version of the adapters has been certified with AdMob 19.8.0 and MoPub 5.16.3.
    * Align impression tracking for non-native ad formats based on Google's `onAdImpression()` callback.

  * 19.7.0.1
    * Service release. No code changes.

  * 19.7.0.0
    * This version of the adapters has been certified with AdMob 19.7.0 and MoPub 5.16.0.
    * Refactor interstitial, rewarded video, and native based on new API guidelines from Google. No action items for publishers.

  * 19.6.0.2
    * Make `GooglePlayServicesNativeAd.java` public, and update the deprecated usage of `setMediaAspectRatio()` and `NativeAdOptions` orientations.

  * 19.6.0.1
    * Fix a bug where the rewarded video adapter fails to request a new ad after a show-related error happens.

  * 19.6.0.0
    * This version of the adapters has been certified with AdMob 19.6.0 and MoPub 5.15.0.
    * Remove the deprecated `onAdLeftApplication()` callback. As a result, click is no longer tracked for interstitial (in addition to rewarded video).

  * 19.5.0.3
    * Fail rewarded video playback errors using `VIDEO_PLAYBACK_ERROR` so publishers can request for the next rewarded video.

  * 19.5.0.2
    * Migrate the `MediaLayout` implementation from using `com.mopub.nativeads.MediaLayout` to `com.mopub.nativeads.GooglePlayServicesMediaLayout`. Publishers must use the new `GooglePlayServicesMediaLayout` in their native ad XML.

  * 19.5.0.1
    * Prevent oversized banner ads from serving by failing the ad request if the creative's width or height is greater than the publishers-specified width or height.

  * 19.5.0.0
    * This version of the adapters has been certified with AdMob 19.5.0 and MoPub 5.14.0.

  * 19.4.0.1
    * Bind native ad resources via the dedicated `GooglePlayServicesViewBinder.java` instead of MoPub's `MediaViewBinder.java`. Publishers must use this new ViewBinder in their apps.

  * 19.4.0.0
    * This version of the adapters has been certified with AdMob 19.4.0 and MoPub 5.13.1.

  * 19.3.0.2
    * Fix native ad static images not displayed/clickable. This allows Google to manage the image asset within their `MediaView`.

  * 19.3.0.1
    * Add support for the new `onRewardedAdFailedToLoad(LoadAdError loadAdError)` to handle load failures. 

  * 19.3.0.0
    * This version of the adapters has been certified with AdMob 19.3.0 and MoPub 5.13.1.
    * All ad formats: Remove load failure callbacks that return an `int` (deprecated by Google) and use the equivalent (if any) that returns a `LoadAdError`.
    * Rewarded video: Remove `onRewardedAdFailedToShow(int)` (deprecated by Google) and use `onRewardedAdFailedToShow(AdError)`.

  * 19.2.0.1
    * Fix interstitial load listener usage.

  * 19.2.0.0
    * This version of the adapters has been certified with AdMob 19.2.0 and MoPub 5.13.0.

  * 19.1.0.1
    * Refactor non-native adapter classes to use the new consolidated API from MoPub.
    * Remove banner size mapping checks to fully take advantage of adaptive banner. 
    * This and newer adapter versions are only compatible with 5.13.0+ MoPub SDK.

  * 19.1.0.0
    * This version of the adapters has been certified with AdMob 19.1.0 and MoPub 5.12.0.
    * Remove calls to `MobileAds.initialize(Context context, String applicationCode)` (deprecated by Google) in favor of `MobileAds.initialize(Context context)`.

  * 19.0.1.0
    * This version of the adapters has been certified with AdMob 19.0.1 and MoPub 5.11.1.

  * 19.0.0.0
    * This version of the adapters has been certified with AdMob 19.0.0.
    * Deprecated `AdRequest.Builder.addTestDevice()` in favor of `RequestConfiguration.Builder.setTestDeviceIds()`.

  * 18.3.0.3
    * MoPub now collects GDPR consent on behalf of Google.

  * 18.3.0.2
    * Log the AdMob ad unit ID in ad lifecycle events.

  * 18.3.0.1
    * Make the adapter keys public.

  * 18.3.0.0
    * This version of the adapters has been certified with AdMob 18.3.0.
    * Allow publishers to reset previously-supplied npa without re-initializing the MoPub SDK. This change expands upon the one introduced in v18.2.0.4.

  * 18.2.0.4
    * Allow publishers to set a new npa without re-initializing the MoPub SDK.

  * 18.2.0.3
    * Map banner ad sizes starting from largest height x width.

  * 18.2.0.2
    * Prioritize reading data from `localExtras` and fall back to `MediationSettings` if necessary for GooglePlayServicesRewardedVideo.java.

  * 18.2.0.1
    * Read banner ad size from `localExtras` instead of `serverExtras`. To ensure an optimal ad experience, publishers should use the MoPub 5.8.0+ SDK and unified banner ad units. If you are using a pre-5.8.0 MoPub SDK or unable to pass the safe area in the 5.8.0 MoPub SDK, check your ad unit setup in the Advanced Options section on the MoPub UI (more info at https://developers.mopub.com/publishers/ui/apps/manage-ad-units/#create-an-ad-unit).

  * 18.2.0.0
    * This version of the adapters has been certified with AdMob 18.2.0.
    * Use `RequestConfiguration` in place of `AdRequest.Builder` to pass targeting data to Google. 

  * 17.2.1.1
    * Add support for AndroidX. This is the minimum version compatible with MoPub 5.9.0.

  * 17.2.1.0
    * This version of the adapters has been certified with AdMob 17.2.1.

  * 17.2.0.2
    * Move the `npa` from `MediationSettings` to `NetworkConfiguration`. [Click here](https://developers.mopub.com/publishers/mediation/networks/google/#instructions-for-passing-users-ad-preference-to-admob) for updated usage instructions.

  * 17.2.0.1
    * Refactor the `MediationSettings` implementation to maintain consistency with the MoPub Unity SDK.

  * 17.2.0.0
    * This version of the adapters has been certified with AdMob 17.2.0.
    * Update the rewarded ad adapter to use AdMob's new Rewarded Video API. For more details, check AdMob's [Rewarded Ads - New APIs guide](https://developers.google.com/admob/android/rewarded-ads).
    * The following mediation settings are now available, with two new additions:
         * `testDeviceId` to be used as a test device when making an ad request to AdMob.
         * `contentUrl` to be used as keyword targeting for applications that monetize content matching a webpage.
         * `npa` to indicate that ad requests should be personalized or not.
         * `tagForChildDirectedTreatment` to indicate that the application's content is child-directed.
         * `tagForUnderAgeOfConsent` to indicate that ad requests is to receive treatment for users in the European Economic Area (EEA) under the age of consent.
    * Mediation settings are now passed in a single `Bundle` object instead of using constructors to pass data separately.

  * 17.1.2.4
    * AdMob Adapter will now be released as an Android Archive (AAR) file that includes manifest file for AdMob.

  * 17.1.2.3
    * **Note**: This version is only compatible with the 5.5.0+ release of the MoPub SDK.
    * Add the `GooglePlayServicesAdapterConfiguration` class to: 
         * pre-initialize the AdMob SDK during MoPub SDK initialization process
         * store adapter and SDK versions for logging purpose
    * Streamline adapter logs via `MoPubLog` to make debugging more efficient. For more details, check the [Android Initialization guide](https://developers.mopub.com/docs/android/initialization/) and [Writing Custom Events guide](https://developers.mopub.com/docs/android/custom-events/).

  * 17.1.2.2
    * Allow publishers to pass test device IDs to the adapters (via localExtras) to get test ads from AdMob.
    * Guard against a NullPointerException for rewarded video.

  * 17.1.2.1
    * Add support for publishers to pass a content URL to AdMob's ad request via the localExtras (if set). For more information on content mapping for apps, see https://support.google.com/admob/answer/6270563?hl=en.

  * 17.1.2.0
    * This version of the adapters has been certified with AdMob 17.1.2.

  * 17.0.0.2
    * Add a null check when calling AdMob's `isLoaded()` for rewarded video ads.
    
  * 17.0.0.1
    * Fix a bug where AdMob's native ads disappear when scrolling through a ListView/RecyclerView using MoPub's Ad Placer technology.

  * 17.0.0.0
    * This version of the adapters has been certified with AdMob 17.0.0.

  * 15.0.1.0
    * This version of the adapters has been certified with AdMob 15.0.1.
    * Update the native ad adapter to use Google's MediaView and UnifiedNativeAd per requirements (https://developers.google.com/admob/android/native-unified).

  * 15.0.0.11
    * Remove manual impression tracking for banner, since AdMob does not have an equivalent callback for impressions (AdListener.onAdImpression() is only applicable for Google's native ads).

  * 15.0.0.10
    * Align MoPub's banner and interstitial impression tracking to that of AdMob.
        * `setAutomaticImpressionAndClickTracking` is set to `false`, and AdMob's `onAdImpression` and `onAdOpened` callbacks are leveraged to fire MoPub impressions. This change requires MoPub 5.3.0 or higher.

  * 15.0.0.9
    * Update the ad unit ID returned in the `getAdNetworkId` API (used to generate server-side rewarded video callback URL) to be non-null, and avoid potential NullPointerExceptions.

  * 15.0.0.8
    * Really fix the AdMob `isLoaded()` crash (15.0.0.3).

  * 15.0.0.7
    * Improve 15.0.0.5 to no longer call out to MoPub's rewarded video APIs to store and process the `npa` value.

  * 15.0.0.6
    * Guard against potential NPEs in 15.0.0.5.

  * 15.0.0.5
    * Append user's ad personalization preference via MoPub's GlobalMediationSettings to AdMob's ad requests. Publishers should work with Google to be GDPR-compliant and Google’s personalization preference does not MoPub’s consent.

  * 15.0.0.4
    * Append user's ad personalization preference from `localExtras` to AdMob's ad requests. [Deprecated]

  * 15.0.0.3
    * Forced AdMob's rewarded video's `isLoaded()` check to run on the main thread (in light of multithreading crashes when mediating AdMob on Unity).

  * 15.0.0.2
    * Resolved the previous Known Issue (AdMob's native ads are occasionally removed from the view hierarchy when a ListView/RecyclerView is scrolled).

  * 15.0.0.1
    * Removed an extra class from the JCenter jar. The adapter binaries on this GitHub repository are not affected.

  * 15.0.0.0
    * This version of the adapters has been certified with AdMob 15.0.0.
	* Implement AdMob's onRewardedVideoCompleted() callback. 
    * [Known Issue] AdMob's native ads are occasionally removed from the view hierarchy when a ListView/RecyclerView is scrolled.

  * 11.8.0.0
    * This version of the adapters has been certified with AdMob 11.8.0.
	
  * Initial Commit
  	* Adapters moved from [mopub-android-sdk](https://github.com/mopub/mopub-android-sdk) to [mopub-android-mediation](https://github.com/mopub/mopub-android-mediation/)
