# OSSRH-72656 - Publish to SonaType

## Links

- [Setup guide from Juxt](https://www.juxt.pro/blog/maven-central)
- [Setup GPG](https://central.sonatype.org/publish/requirements/gpg/)
- [ticket for verification with SonaType](https://issues.sonatype.org/browse/OSSRH-72656)
- [Publish Guide/deployment](https://central.sonatype.org/publish/publish-guide/#deployment)
- [Publish Guide/release](https://central.sonatype.org/publish/release/)
- [SonaType Lift](https://links.sonatype.com/products/lift/github-integration)
- [List of open issues](https://issues.sonatype.org/projects/OSSRH/issues/OSSRH-72199?filter=allopenissues)
- [Use github as coordinates](https://central.sonatype.org/publish/requirements/coordinates/)
- [Use your custom domain](https://central.sonatype.org/faq/how-to-set-txt-record/)
 - [namecheap.com](https://www.namecheap.com/support/knowledgebase/article.aspx/317/2237/how-do-i-add-txtspfdkimdmarc-records-for-my-domain/)
 - Check TXT record

 ```sh
 #
 host -t txt yourdomain.com
 #
 dig -t txt yourdomain.com
 ```

## Misc outputs

```
io.github.burinc has been prepared, now user(s) b12n can:
Publish snapshot and release artifacts to s01.oss.sonatype.org
Have a look at this section of our official guide for deployment instructions:
https://central.sonatype.org/publish/publish-guide/#deployment

Depending on your build configuration, your first component(s) might be released automatically after a successful deployment.
If that happens, you will see a comment on this ticket confirming that your artifact has synced to Maven Central.

If you do not see this comment within an hour or two, you can follow the steps in this section of our guide:
https://central.sonatype.org/publish/release/

######

As part of our efforts to improve the security and quality posture of the open source supply chain,
we plan to enable additional scanning of dependencies for security alerts soon. Since you're already
hosting your source code in Github, you can get these insights today by enabling Sonatype Lift.
Sonatype Lift is free forever on public repositories! Lift tells you about open source vulnerabilities
during code review, and goes beyond open source to scan your code for both code quality and security issues,
providing feedback right in your pull requests.
More information can be found at https://links.sonatype.com/products/lift/github-integration
 ```

 ## Setup project

 You will probably need to also create [User Token](https://oss.sonatype.org/#profile;User%20Token) via [Nexus UI](https://oss.sonatype.org/)

 ```
 ;; ~/.lein/credentials.clj.gpg
 {#"https://oss\.sonatype\.org/.*"
  {:username "..." ;;
   :password "..."}}
 ```

 ### Setup GPG

 - [How to setup GPG (SonarType)](https://central.sonatype.org/publish/requirements/gpg/)

 ## References

 - https://central.sonatype.org/publish/publish-guide/#create-a-ticket-with-sonatype
 - https://central.sonatype.org/publish/requirements/coordinates/
