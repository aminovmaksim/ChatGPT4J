# ChatGPT4J
ChatGPT Java SDK. Official OpenAI API.

[![Maven Central](https://img.shields.io/maven-central/v/io.github.aminovmaksim/chatgpt4j)](https://maven-badges.herokuapp.com/maven-central/io.github.aminovmaksim/chatgpt4j)
---
### How to install
#### Maven
```xml
<dependency>
    <groupId>io.github.aminovmaksim</groupId>
    <artifactId>chatgpt4j</artifactId>
    <version>1.0.2</version>
</dependency>
```
#### Gradle
```groovy
implementation 'io.github.aminovmaksim:chatgpt4j:1.0.2'
```
---
## How to use
- Initialize the client
```java
ChatGPTClient client = ChatGPTClient.builder()
        .apiKey("YOUR_KEY")
        .requestTimeout(30000L) // optional, default is 60000 ms
        .baseUrl("https://api.openai.com/v1") // optional
        .build();
```
You can get your api key [here](https://platform.openai.com/account/api-keys)

- Send a message
```java
ChatResponse response = client.sendChat(new ChatRequest("Hello"));

System.out.println(response.getChoices().get(0).getMessage().getContent());
```

---
## Disclaimers
Project currently in develop, feel free to contact me [@aminovmaksim](https://github.com/aminovmaksim)
