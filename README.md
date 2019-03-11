This sample project demonstrates lint issues with the mapbox sdk.

Instructions:

Run lint: `./gradlew lintDebug`

This produces a lint report in `app/build/reports/lint-results-debug.html`

The report contains two issues:

`ObsoleteLintCustomCheck`:
>
>jetified-mapbox-android-sdk-7.2.0.aar/.../lint.jar: Lint found an issue registry (com.mapbox.mapboxsdk.lint.MapboxIssueRegistry) which did not specify the Lint API version it was compiled with.
>
>This means that the lint checks are likely not compatible.

`PrivateResource`:
>../../src/main/res/values/strings.xml:2: Overriding @string/app_name which is marked as private in com.mapbox.mapboxsdk:mapbox-android-sdk. If deliberate, use tools:override="true", otherwise pick a different name.
```
 1 <resources>
 2     <string name="app_name">MapboxAppNameLintIssue</string>                                         
 3 </resources>
```

