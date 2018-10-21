# botsharp-channel-weixin
A channel module of BotSharp for Tencent Weixin

### How to integrate with Wechat 

```
git clone https://github.com/Oceania2018/BotSharp
```

Install packages for BotSharp.WebHost project
```
PM> Install-Package BotSharp.Platform.Dialogflow
PM> Install-Package BotSharp.Channel.Weixin
```

Check app.json to load Weixin and Dialogflow modules
```
{
  "version": "0.1.0",
  "assemblies": "BotSharp.Core",

  "platformModuleName": "DialogflowAi",

  "modules": [
    {
      "Name": "DialogflowAi",
      "Type": "BotSharp.Platform.Dialogflow"
    },
    {
      "Name": "WeixinChannel",
      "Type": "BotSharp.Channel.Weixin"
    }
  ]
}
```

Update channels.weixin.json to set the corresponding KEY
```
{
  "weixinChannel": {
    "token": "botsharp",
    "encodingAESKey": "",
    "appId": ""
  }
}
```

Refere (BotSharp docs)[https://botsharp.readthedocs.io] to design your chatbot.
