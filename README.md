<br>

The Jakarta Mail API provides a platform-independent and
protocol-independent framework to build mail and messaging
applications.
The Jakarta Mail API is available as an optional package for use with the
[Java SE platform](http://www.oracle.com/technetwork/java/javase/index.html)
and is also included in the
[Jakarta EE platform](http://jakarta.ee) and the
[Java EE platform](http://www.oracle.com/technetwork/java/javaee/index.html).

# Table of Contents
* [Latest News](#Latest_News)
* [Download Jakarta Mail Release](#Download_Jakarta_Mail_Release)
* [API Documentation](#API_Documentation)
* [Samples](#Samples)
* [Help](#Help)
* [Bugs](#Bugs)
* [Development Releases](#Development_Releases)
* [Jakarta Mail for Android](#Jakarta_Mail_for_Android)
* [Project Documentation](#Project_Documentation)

# <a name="Latest_News"></a>Latest News

## March 10, 2020 - Jakarta Mail 1.6.5 Final Release ##

The 1.6.5 release is (hopefully) the last release of the Jakarta Mail project
in the 1.x line, and includes several bug fixes and enhancements.
The main jar file is located at
[com.sun.mail:jakarta.mail](https://repo1.maven.org/maven2/com/sun/mail/jakarta.mail/1.6.5/jakarta.mail-1.6.5.jar).

Jakarta Mail, like other parts of [Jakarta EE](https://jakarta.ee),
is moving to the `jakarta.*` package namespace.
This is a major change, and so the next release will be Jakarta Mail 2.0.0,
which will be included in Jakarta EE 9.
Applications should be able to switch to this new version fairly easily
by just changing all imports that use `javax.mail.*` to instead use
`jakarta.mail.*`.
Note that SNAPSHOT and Release Candidate versions of Jakarta Mail 2.0.0
are already available.

## August 28, 2019 - Jakarta Mail 1.6.4 Final Release ##

The 1.6.4 release is the first release of the Jakarta Mail project using the
[Jakarta EE Specification Process](https://jakarta.ee/about/jesp/)
and includes several bug fixes and enhancements.
The main jar file is located at
[com.sun.mail:jakarta.mail](https://repo1.maven.org/maven2/com/sun/mail/jakarta.mail/1.6.4/jakarta.mail-1.6.4.jar).

## July 3, 2019 - Jakarta Mail is the new name for JavaMail ##

The JavaMail technology contributed to the Eclipse Foundation has been renamed
to "Jakarta Mail" to reflect its role in the
[Jakarta EE platform](https://jakarta.ee/).

## November 26, 2018 - JavaMail 1.6.3 Final Release ##

The 1.6.3 release is the first release of the Eclipse project for JavaMail
and includes no bug fixes or enhancements. It does include changes
to the Maven coordinates. The main jar file is now located at
[com.sun.mail:jakarta.mail](https://repo1.maven.org/maven2/com/sun/mail/jakarta.mail/1.6.3/jakarta.mail-1.6.3.jar).

## September 14, 2018 - JavaMail project moves to the Eclipse Foundation! ##

The JavaMail project is now hosted at the Eclipse Foundation as part of
the [EE4J project](https://projects.eclipse.org/projects/ee4j).

By contributing to this project, you agree to these additional terms of
use, described in [CONTRIBUTING](CONTRIBUTING.md).

# <a name="Download_Jakarta_Mail_Release"></a>Download Jakarta Mail Release

The latest release of Jakarta Mail is 1.6.5.

The following table provides easy access to the latest release. Most
people will only need the main Jakarta Mail implementation in the
jakarta.mail.jar file.

|Item|Description|
|:---|:----------|
|[jakarta.mail.jar](https://github.com/eclipse-ee4j/mail/releases/download/1.6.5/jakarta.mail.jar)|The Jakarta Mail implementation, including the SMTP, IMAP, and POP3 protocol providers|
|[README.txt](docs/README.txt)|Overview of the release|
|[NOTES.txt](docs/NOTES.txt)|Additional notes about using Jakarta Mail|
|[SSLNOTES.txt](docs/SSLNOTES.txt)|Notes on using SSL/TLS with Jakarta Mail|
|[NTLMNOTES.txt](docs/NTLMNOTES.txt)|Notes on using NTLM authentication with Jakarta Mail|
|[CHANGES.txt](docs/CHANGES.txt)|Changes since the previous release|
|[COMPAT.txt](docs/COMPAT.txt)|Important notes about compatibility|


In addition, the Jakarta Mail jar files are published to the Maven repository.
The main Jakarta Mail jar file, which is all most applications will need,
can be included using this Maven dependency:
```
        <dependencies>
            <dependency>
                <groupId>com.sun.mail</groupId>
                <artifactId>jakarta.mail</artifactId>
                <version>1.6.5</version>
            </dependency>
        </dependencies>
```
You can find all of the Jakarta Mail jar files in
[Maven Central](http://search.maven.org).


|jar file|groupId|artifactId|Description|
|:-------|:------|:---------|:----------|
|[jakarta.mail.jar](https://repo1.maven.org/maven2/com/sun/mail/jakarta.mail/1.6.5/jakarta.mail-1.6.5.jar)|com.sun.mail|jakarta.mail|The Jakarta Mail implementation jar file, including the SMTP, IMAP, and POP3 protocol providers|
|[jakarta.mail-api.jar](https://repo1.maven.org/maven2/jakarta/mail/jakarta.mail-api/1.6.5/jakarta.mail-api-1.6.5.jar)|jakarta.mail|jakarta.mail-api|The Jakarta Mail API definitions only, suitable for compiling against; use only with a Maven "provided" dependency scope|
|[mailapi.jar](https://repo1.maven.org/maven2/com/sun/mail/mailapi/1.6.5/mailapi-1.6.5.jar)|com.sun.mail|mailapi|The Jakarta Mail implementation with no protocol providers; use with one of the following providers|
|[smtp.jar](https://repo1.maven.org/maven2/com/sun/mail/smtp/1.6.5/smtp-1.6.5.jar)|com.sun.mail|smtp|The SMTP protocol provider|
|[imap.jar](https://repo1.maven.org/maven2/com/sun/mail/imap/1.6.5/imap-1.6.5.jar)|com.sun.mail|imap|The IMAP protocol provider|
|[pop3.jar](https://repo1.maven.org/maven2/com/sun/mail/pop3/1.6.5/pop3-1.6.5.jar)|com.sun.mail|pop3|The POP3 protocol provider|
|[gimap.jar](https://repo1.maven.org/maven2/com/sun/mail/gimap/1.6.5/gimap-1.6.5.jar)|com.sun.mail|gimap|An EXPERIMENTAL Gmail IMAP protocol provider that supports Gmail-specific features|
|[dsn.jar](https://repo1.maven.org/maven2/com/sun/mail/dsn/1.6.5/dsn-1.6.5.jar)|com.sun.mail|dsn|Support for parsing and creating messages containing Delivery Status Notifications|
|[logging-mailhandler.jar](https://repo1.maven.org/maven2/com/sun/mail/logging-mailhandler/1.6.5/logging-mailhandler-1.6.5.jar)|com.sun.mail|logging-mailhandler|A java.util.logging handler that uses Jakarta Mail, suitable for use in Google App Engine.|

# <a name="API_Documentation"></a>API Documentation

The Jakarta Mail 1.6 API is defined through the
[Jakarta EE Specification Process](https://jakarta.ee/about/jesp/).

The Jakarta Mail 1.6 specification and API documentation are available
[here](https://jakarta.ee/specifications/mail/1.6/).

Note that Jakarta Mail 1.6 is identical to JavaMail 1.6.

The JavaMail 1.6 and earlier API is defined through the Java Community Process as
[JSR 919](http://jcp.org/en/jsr/detail?id=919).

The following documents summarize the API changes in each release of
the JavaMail API specification:

-   [JavaMail 1.6](docs/JavaMail-1.6-changes.txt)
-   [JavaMail 1.5](docs/JavaMail-1.5-changes.txt)
-   [JavaMail 1.4](docs/JavaMail-1.4-changes.txt)
-   [JavaMail 1.3](docs/JavaMail-1.3-changes.txt)
-   [JavaMail 1.2](docs/JavaMail-1.2-changes.txt)
-   [JavaMail 1.1](docs/JavaMail-1.1-changes.txt)

# <a name="Samples"></a>Samples

Some sample programs showing how to use the Jakarta Mail APIs are available
[here](https://github.com/eclipse-ee4j/mail/releases/download/1.6.5/jakartamail-samples.zip).

# <a name="Help"></a>Help

Please read the
[Jakarta Mail FAQ](FAQ.html)!
Read it again. Tell everyone you know to read it. Thank you!

You can post questions to the
[mail-dev mailing list](https://accounts.eclipse.org/mailing-list/mail-dev).

Or, post a question on [Stack Overflow](http://stackoverflow.com/) using the
[javamail](http://stackoverflow.com/questions/tagged/javamail) tag.

# <a name="Bugs"></a>Bugs

Jakarta Mail bugs are tracked in the
[GitHub Jakarta Mail project issue tracker](https://github.com/eclipse-ee4j/mail/issues).

# <a name="Development_Releases"></a>Development Releases

From time to time snapshot releases of the next version of Jakarta Mail
under development are published to the
[Jakarta Sonatype OSS repository](http://jakarta.oss.sonatype.org).
These snapshot releases have received only minimal testing, but may
provide previews of bug fixes or new features under development.

For example, you can download the jakarta.mail.jar file from the Jakarta Mail
2.0.0-SNAPSHOT release
[here](https://jakarta.oss.sonatype.org/content/repositories/snapshots/com/sun/mail/jakarta.mail/2.0.0-SNAPSHOT/).
Be sure to scroll to the bottom and choose the jar file with the most
recent time stamp.

You'll need to add the following configuration to your Maven ~/.m2/settings.xml
to be able to use these with Maven:

```
    <profiles>
        <!-- to allow loading Jakarta snapshot artifacts -->
        <profile>
            <id>jakarta-snapshots</id>
            <pluginRepositories>
                <pluginRepository>
                    <id>jakarta-snapshots</id>
                    <name>Jakarta Snapshots</name>
                    <snapshots>
                        <enabled>true</enabled>
                        <updatePolicy>always</updatePolicy>
                        <checksumPolicy>fail</checksumPolicy>
                    </snapshots>
                    <url>https://jakarta.oss.sonatype.org/content/repositories/snapshots/</url>
                    <layout>default</layout>
                </pluginRepository>
            </pluginRepositories>
        </profile>
    </profiles>
```

And then when you build use `mvn -Pjakarta-snapshots ...`.

If you want the plugin repository to be enabled all the time so you don't need the -P, add:

```
    <activeProfiles>
        <activeProfile>jakarta-snapshots</activeProfile>
    </activeProfiles>
```

# <a name="Jakarta_Mail_for_Android"></a>Jakarta Mail for Android

The latest release includes support for Jakarta Mail on Android.
See the [Android](Android) page for details.

# <a name="Project_Documentation"></a>Project Documentation

You'll find more information about the protocol providers supported by
Jakarta Mail on the following pages:

-   [ smtp ](SMTP-Transport)
-   [ imap ](IMAP-Store)
-   [ pop3 ](POP3-Store)
-   [ mbox ](Mbox-Store)
-   [ pop3remote ](POP3-Remote-Store)

If you're interested in writing your own protocol provider (most people
won't need to), you can find more documentation on protocol providers
[here](https://javaee.github.io/javamail/docs/Providers.pdf).

The use of
[OAuth2 authentication](https://developers.google.com/gmail/xoauth2_protocol)
with Jakarta Mail is described [here](OAuth2).

The following pages provide hints and tips for using particular mail servers:

-   [Gmail](Gmail)
-   [ Yahoo! Mail ](Yahoo)
-   [ Exchange and Office 365 ](Exchange)
-   [ Outlook.com ](Outlook)

The following pages provide hints and tips for using Jakarta Mail on
particular operating systems or environments:

-   [Windows](Windows)
-   [Google App Engine](Google-App-Engine)

See [Build Instructions](Build-Instructions) for instructions on how to
download and build the most recent Jakarta Mail source code. You can also
find a bundle of the source code for the most recent Jakarta Mail release
in the [Releases](https://github.com/eclipse-ee4j/mail/releases) area of
this project.

If you're interested in contributing to Jakarta Mail, see the
[Contributions](Contributions) page.

You can find a list of products related to Jakarta Mail on the
[Third Party Products](ThirdPartyProducts) page.

Please see our page of
[links to additional information about Jakarta Mail and Internet email](Links)
and our list of
[books about Jakarta Mail and Internet email](Books).

To understand the Jakarta Mail license, see the [License](JakartaMail-License) page.
