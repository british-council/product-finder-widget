# Product Finder Exams List Widget

## How to add widget to Solas pages?

To make widget working properly you have to include following HTML markup somewhere in your page:
```html
<body>
  <!--  Your page content... --->

  <!--  It is important to have <div> with id="pf-root" --->
  <div id="pf-root">
    <!--  Inside this tag place correct config options. Available values are described below in the table --->
    <script type="text/props">
      {
        "countryName": "Poland",
        "isoCode": "pl",
        "addStructuredData": true,
        "addSolasCSS": false,
        "addPolyfills": false
      }
    </script>
  </div>
  <!-- Main script including widget and all its logic. -->
  <script
    defer="defer"
    src="https://bccdn.azureedge.net/product-finder/pf-bundle.js"
  ></script>
</body>
```

### Configuration object
You can configure your widget using folowing option:

| Key               | Description                                            | Default value                     |
| ----------------  | -----------                                            | -----------                       |
| countryName       | Full country name. It shows up in the districts list   | None, you must provide it         |
| isoCode           | Country ISO code (e.g. "pl", "tr", "de", etc)          | None, you must provide it         |
| addStructuredData | Generate rich Google serach results with exam dates    | true                              |
| addSolasCSS       | Add link to Solas CSS if you don't use it already on your page | false                             |
| addPolyfills      | Set to true if you care about older browsers like IE11 (can slow down the page) | false    |
| apiUrl            | Development purpose only. Do not use it if you are only adding this widget to the solas page  | pfapi.britishcouncil.org          |

**Please note:** Last item in the configuration object must **not** includes trailing comma! See example above.