# OSSRH-72656

Git project for verification with SonarType

- [Setup guide from Juxt](https://www.juxt.pro/blog/maven-central)
- [ticket for verification with SonarType](https://issues.sonatype.org/browse/OSSRH-72656)
- [list of open issues](https://issues.sonatype.org/projects/OSSRH/issues/OSSRH-72199?filter=allopenissues)
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
