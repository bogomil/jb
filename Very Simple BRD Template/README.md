#YouTrack workflow plugin for adding a very simple BRD template when requesting a new feature

##code

```java
rule A very simple BRD Template

when !isReported() && description == null && Type = {Feature} {
    description = "Describe objectives ans main purpose of this request:" + "\n\n" +
        "Describe how this request will help the specific customer group" + "\n\n" +
        "Describe the current solution (if any) and why is is not abequate:";
}
```

## Help
You can change the text to align with your project and/or you can add more points.
