# WebhookBuilder

Example class to use in your proyect when trying to build webhook message.

## Use

Example of use: 
```java
 MessageBuilder webhook = new MessageBuilder(webhookUrl);
 webhook.setUsername("MyBotName");
 webhook.setTts(true);
 webhook.setContent("Message Received");
 webhook.addEmbed((new MessageBuilder.EmbedObject()).setTitle("Message from  " + message.getFrom())
         .addField("Header", "`" + message.getSubject() + "`", false)
         .addField("Message", "`" + (String) message.getContent() + "`", false)
         .setColor(Color.PINK));
 webhook.execute();
      
