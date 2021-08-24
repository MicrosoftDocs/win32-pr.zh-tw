---
description: 建立永久事件取用者的第一個步驟是建立描述事件取用者的 WMI 類別。 具體而言，永久事件取用者類別會定義實體取用者所執行之動作的參數。
ms.assetid: a5b6d0b9-8df1-47e3-bb3b-cc69db6d9c0e
ms.tgt_platform: multiple
title: 建立新的永久事件取用者類別
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f86f9e8ea4339eb76bdc77087780fcfa9be09f47c92a154c5f89109d90337b41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464278"
---
# <a name="creating-a-new-permanent-event-consumer-class"></a>建立新的永久事件取用者類別

建立永久事件取用者的第一個步驟是建立描述事件取用者的 WMI 類別。 具體而言，永久事件取用者類別會定義實體取用者所執行之動作的參數。

下列程式描述如何建立永久性事件取用者類別。

**若要建立永久事件取用者類別**

1.  從 [**\_ \_ EventConsumer**](--eventconsumer.md)系統類別衍生類別。
2.  執行處理事件通知所需的任何參數。

下列範例顯示用來建立 SMTPConsumerEvent 類別的語法。 您可以使用此範例來建立新類別。 [**SMTPEventConsumer**](smtpeventconsumer.md)類別會在每次傳遞事件給它時，使用 Simple Mail Transfer PROTOCOL (SMTP) 傳送電子郵件訊息。 此類別定義于 smtpcons 中。

``` syntax
class SMTPEventConsumer : __EventConsumer
{
  [key] string Name;
  [not_null] string SMTPServer;
  [Template] string Subject;
  [Template] string FromLine;
  [Template] string ReplyToLine;
  [Template] string Message;
  [Template] string ToLine;
  [Template] string CcLine;
  [Template] string BccLine;
  string HeaderFields[];
};
```

您應該能夠建立永久事件取用者類別的實例，以描述將事件傳送給實體取用者的一或多個方法。 如需詳細資訊，請參閱 [建立邏輯取用者](creating-a-logical-consumer.md)。

 

 



