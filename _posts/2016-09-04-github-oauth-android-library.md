---
title: Github Oauth Android library
date: 2016-09-04 00:00:00 Z
permalink: "/android/using_oauthLibGithub_to_authenticate_user_on_android"
layout: post
---

Android library to authenticate user via Oauth 2.0 Github as provider.

To simplify the process of authentication using OAuth 2.0 protocol in Android mobile app development, this is primarily build to be used with github as authentication provider to that user can login to host app using github credentials.


Installation : 

`compile 'com.github.geniushkg:oauthLibGithub:1.0.1`

Add  to manifest file :

` <uses-permission android:name="android.permission.INTERNET"/> `

` <activity android:name="com.hardikgoswami.oauthLibGithub.OauthActivity"/> `
								
								
							
							
## Github Auth Flow
Initialise new Auth instance with credentials

Sample initialization given below , you can also set debug(true) for inspection  purpose.

Suppose you want to start authentication process by button click then initialise as below,
Important that you provide next activity where to redirect after login successfull.



**Sample initialization :**


        // Github ID and secret are generated in github.com profile
		// package name is your packagename
		// next activity is your activity with full name including package 
		// you can use debug(true) for logcat , use TAG = "github-oauth"

		loginButton.setOnClickListener(new View.OnClickListener() {

            @Override
            public void onClick(View v) {
                 GithubOauth
                        .Builder()
                        .withClientId(GITHUB_ID)
                        .withClientSecret(GITHUB_SECRET)
                        .withContext(context)
                        .packageName("com.hardikgoswami.github_oauth_lib")
                        .nextActivity("com.hardikgoswami.github_oauth_lib.UserActivity")
                        .debug(true)
                         .execute();
            }
        });

**Note :** Callback url can be as per your requirement or make it http://localhost while registering new Oauth application.


Execute will launch a new activity with webview and user token will be stored in shared preference


Shared preference name : **github_prefs**

String in preference :**oauth_token**

		// Sample to read logged in user oauth token
        public static final String PREFERENCE = "github_prefs";
		sharedPreferences = getSharedPreferences(PREFERENCE, 0);
        String oauthToken = sharedPreferences.getString("oauth_token", null);
        Log.d(TAG, "oauth token for github loged in user is :" + oauthToken);


