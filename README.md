GeocoderDemo
================

Demo that illustrates a problem with the Android Geocoder when geocoding with a bounding box.

See https://code.google.com/p/android/issues/detail?id=75575

**Usage:**

 * Run the project
 * Enter a search term (or use the default term)
 * Tap "Run Geocoder w/ bounding box" to see results using a bounding box, or tap 
   "Run Geocoder (no bounding box) to see results without using a bounding box.

**What I see:**

When running the Geocoder with the bounding box, the same small set of very generic results are 
always shown no matter what you enter in the search box.

**Expected behavior:**

When running the Geocoder with the bounding box, you should see different results depending on the
search term.

**Workaround:**

Running the Geocoder without a bounding box provides the expected behavior, in that the results 
differ depending on the search term.  However, these results are global.  If I enter `airport` 
in Tampa, FL, I get results from the opposite side of the world, which isn't usable without further 
filtering.

**Device:**

I've tested this using a Samsung Galaxy S3 with Android 4.4.4.

**Notes:**

The `Geocoder.isPresent` value will be output to Logcat.  In my tests, this always shows `true`.