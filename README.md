
Documentation at https://developer.android.com/guide/topics/manifest/queries-element states:

syntax:
```
<queries>
    <package android:name="string" />
    <intent>
        ...
    </intent>
    <provider android:authorities="list" />
    ...
</queries>
```

It seems omitting android:name makes the build fail. Either the documentation should make note of 
the requirement of adding android:name or the merger should work with it omitted. Considering adding
it requires an additional addition to tools:ignore="MissingClass" it is likely better from a 
consumer standpoint to make the merger work with android:name omitted.
