# Java Server Faces and Okta

An example JSF application that demonstrates basic CRUD operations and security with Spring Security and Okta.

Please read [Build a Simple Application with JavaServer Faces](https://developer.okta.com/2019/09/27/build-a-crud-app-with-jsf)
for the full tutorial.

**Prerequisites:** [Java 8](https://adoptopenjdk.net/).

> [Okta](https://developer.okta.com/) has Authentication and User Management APIs that reduce development time with instant-on, scalable user infrastructure. Okta's intuitive API and expert support make it easy for developers to authenticate, manage and secure users and roles in any application.

* [Getting Started](#getting-started)
* [Links](#links)
* [Help](#help)
* [License](#license)

## Getting Started

To install this example application, run the following commands:

```bash
git clone https://github.com/oktadeveloper/okta-java-jsf-crud-example.git
cd okta-java-jsf-crud-example
```

### Create an Application in Okta

You will need to create an OIDC Application in Okta to get your values to perform authentication. 

Log in to your Okta Developer account (or [sign up](https://developer.okta.com/signup/) if you don’t have an account) and navigate to **Applications** > **Add Application**. Click **Web**, click **Next**, and give the app a name you’ll remember. Specify `http://localhost:8080/login/oauth2/code/okta` as a Login redirect URI. Click **Done**, then click **Edit** to edit General Settings then click **Save**.

#### Configuration

Set the `issuer` and copy the `clientId` and `clientSecret` into `src/main/resources/application.properties`. 

**NOTE:** The value of `{yourOktaDomain}` should be something like `dev-123456.oktapreview.com`. Make sure you don't include `-admin` in the value!

```properties
okta.issuer-uri=issuer-uri=https://{yourOktaDomain}/oauth2/default
okta.client-id={client-id}
okta.client-secret={client-secret}
```

## Build and Run the application
 
```bash
./mvn package tomee:run
```

## Links

This example uses the following open source libraries:

* [JSF](http://www.javaserverfaces.org/)
* [PrimeFaces](https://www.primefaces.org/)
* [Spring Security](https://spring.io/projects/spring-security)

## Help

Please post any questions as comments on the [blog post](https://developer.okta.com/2019/09/27/build-a-crud-app-with-jsf), or visit our [Okta Developer Forums](https://devforum.okta.com/). You can also email developers@okta.com if you'd like to create a support ticket.

## License

Apache 2.0, see [LICENSE](LICENSE).
