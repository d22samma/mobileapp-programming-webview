
# Rapport

Rename App - Strings.
Fork the webview app and clone the fork from your own Github repository in Android Studio
Rename your App. Hint: `res/values/strings.xml`

Enabled Internet AndroidManifest
Enable Internet access for your App. Hint: `AndroidManifest.xml`

Create Webview - Actvity_Main
Create a WebView element in the layout file `content_main.xml` by replacing the existing `TextView`
Give the WebView an ID. Hint: `android:id="@+id/my_webview"`



For a passing grade (G) need to (in order):

Create a private member variable called `myWebView` of the type `WebView` and instantiate it in `onCreate()`. Hint: `findViewById()`
Locate the WebView element created in step 1 using the WebView ID
Create a new WebViewClient to attach to the WebView
Enable Javascript execution in your WebViewClient. Hint: `getSettings()` and `setJavaScriptEnabled()`
Add a html page as an asset.
Implement `showExternalWebPage()` and `showInternalWebPage()`. Hint: `loadUrl()`.
Call `showExternalWebPage()` and `showInternalWebPage()` when menu dropdown is clicked. Hint: `onOptionsItemSelected()`.
Write a short report where you explain the things that you have done. Include one (1) screenshot showing your internal web page and one (1) screenshot showing your external web page. Hint: This is a function built into the android virtual device. Make sure you include all other parts that are required in the report as described in the assignment requirements.
Submit all artifacts as described in the assignment requirements.

**Skriv din rapport här!**

_Du kan ta bort all text som finns sedan tidigare_.

## Följande grundsyn gäller dugga-svar:

- Ett kortfattat svar är att föredra. Svar som är längre än en sida text (skärmdumpar och programkod exkluderat) är onödigt långt.
- Svaret skall ha minst en snutt programkod.
- Svaret skall inkludera en kort övergripande förklarande text som redogör för vad respektive snutt programkod gör eller som svarar på annan teorifråga.
- Svaret skall ha minst en skärmdump. Skärmdumpar skall illustrera exekvering av relevant programkod. Eventuell text i skärmdumpar måste vara läsbar.
- I de fall detta efterfrågas, dela upp delar av ditt svar i för- och nackdelar. Dina för- respektive nackdelar skall vara i form av punktlistor med kortare stycken (3-4 meningar).

Programkod ska se ut som exemplet nedan. Koden måste vara korrekt indenterad då den blir lättare att läsa vilket gör det lättare att hitta syntaktiska fel.

```
function errorCallback(error) {
    switch(error.code) {
        case error.PERMISSION_DENIED:
            // Geolocation API stöds inte, gör något
            break;
        case error.POSITION_UNAVAILABLE:
            // Misslyckat positionsanrop, gör något
            break;
        case error.UNKNOWN_ERROR:
            // Okänt fel, gör något
            break;
    }
}
```

Bilder läggs i samma mapp som markdown-filen.

![](android.png)

Läs gärna:

- Boulos, M.N.K., Warren, J., Gong, J. & Yue, P. (2010) Web GIS in practice VIII: HTML5 and the canvas element for interactive online mapping. International journal of health geographics 9, 14. Shin, Y. &
- Wunsche, B.C. (2013) A smartphone-based golf simulation exercise game for supporting arthritis patients. 2013 28th International Conference of Image and Vision Computing New Zealand (IVCNZ), IEEE, pp. 459–464.
- Wohlin, C., Runeson, P., Höst, M., Ohlsson, M.C., Regnell, B., Wesslén, A. (2012) Experimentation in Software Engineering, Berlin, Heidelberg: Springer Berlin Heidelberg.
