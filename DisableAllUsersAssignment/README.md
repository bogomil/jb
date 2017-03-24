#YouTrack workflow plugin to disable the assignment an issue to ALL USERS

##code

```java

rule DisableAllusers

when <issue created or updated> {
 if(!loggedInUser.hasRole("dms-poweruser")) {
  if(issue.permittedGroup.changed) {
   issue.permittedGroup=issue.permittedGroup.oldValue;
   message("You are not allowed to change the group!");
  }
 }
}

```

