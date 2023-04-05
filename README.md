
# Assignment 2: WebView

## Rename App
Genom att döpa om text value inom `strings,xml` med `Id ` som motsvarar `app_name`.   
Text value hämtas från `strings.xml` till filen `AndoidManifest.xml` som anropar efter innehållet av `App_name` komponenten.
```java
    android:label="@string/app_name"
// Code from `Androidmanifest.xml`
```

``` java
    <string name="app_name"> My App </string>
    // Code from `string.xml`
```  

****
## Enable Internet
Genom att lägga till `<uses-permission android:name="android.permission. INTERNET" />` tillåter man att internet används.  
Denna koden används inom `AndroidManifest.xml` för att göra internet tillgängligt inom applikationen.

``` java
    <uses-permission android:name="android.permission.INTERNET" /> 
    // Code from `AndroidManifest.xml`
```

****
## Create Webview
Genom att ändra från text till webbview input. Istället för en textview komponent visas en webview upp istället. Med hjälp av `android:id="@+id/my_webview` ger man ett specifikt `id` till `Webview`.

``` java
<WebView
        android:id="@+id/my_webview"
        // Code from `MainActivity.java`

```

****
## Private Member

Lägger till en klass kallad `Webview` med ett attribut som kallas `myWebView`.

``` java
public class MainActivity extends AppCompatActivity {
    private WebView myWebView;
    ...
    // Code from `MainActivity.java`
```


Inom `onCreate()` anger man att `MyWebView` hämtar data från `id` som kallas `my_webview`
``` java
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Toolbar toolbar = findViewById(R.id.toolbar);
        setSupportActionBar(toolbar);
        myWebView = findViewById(R.id.my_webview);
        ...
        // Code from `MainActivity.java`
```


****
## WebviewClient with Enabled Javascript
Genom att skapa en klass kallad WebSettings med webSettings som attribut. motsvarar att hämta settings inom myWebView. Websettings sätts med hjälp av `webSettings.setJavaScriptEnabled(true)`.

``` java
        WebSettings webSettings = myWebView.getSettings();
        webSettings.setJavaScriptEnabled(true);
        // Code from `MainActivity.java`
```

****
## Html page
Jag skapade en html fil. Jag startade med att skapa en ny `assetfolder` inom mappen som kallas `app`. Jag skapa en ny fil inom mappen `asset` som heter `page.html`.
Inom `page.html`filen skapa jag en egen ´Html kod´ till min egna lokala sida.

``` html
<!Doctype html>
<html>
<h1>MyPage</h1>
<hr>
<p>Välkommen till min sida</p>
<p>Hoppas du har en trevlig dag</p>
</html>
<!-- Code from `page.html` -->
```

****
## Internal Page

Genom att hämta en websida som är lokaliserad inom den lokala mappen som projektet ligger inom motsvarar en `Intern sida`.
Som i detta fall motsvarar `page.html`.


``` java
public void showInternalWebPage()
{
    WebView myWebView = (WebView) findViewById(R.id.my_webview);
    myWebView.loadUrl("file:///android_asset/page.html");
}
// Code from `MainActivity.java`
```


``` java
if (id == R.id.action_internal_web) {
    showInternalWebPage();
    Log.d("==>","Will display internal web page");
    return true;
}
// Code from `MainActivity.java` 
```

![](Internal.png)
_Screenshot of `Internal Page`_

****
## External page

Genom att hämta en websida utanför den lokala mappen som projektet ligger inom, motsvarar en  `extern sida`.
I detta fall motsvarar `https://www.his.se`.

``` java
    public void showExternalWebPage(){
        WebView myWebView = (WebView) findViewById(R.id.my_webview);
        myWebView.loadUrl("https://www.his.se");
    }
// Code from `MainActivity.java`
```


``` java
if (id == R.id.action_external_web) 
{
    showExternalWebPage();
    Log.d("==>","Will display external web page");
    return true;
}
// Code from `MainActivity.java`
```

![](External.png)
_Screenshot of `External Page`_

