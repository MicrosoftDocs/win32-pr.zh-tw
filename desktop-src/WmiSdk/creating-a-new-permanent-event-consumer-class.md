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
ms.openlocfilehash: 03f8ae8e1e83abcf3b340398d45aefde4c7141e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993075"
---
# <a name="creating-a-new-permanent-event-consumer-class"></a><span data-ttu-id="39b48-104">建立新的永久事件取用者類別</span><span class="sxs-lookup"><span data-stu-id="39b48-104">Creating a New Permanent Event Consumer Class</span></span>

<span data-ttu-id="39b48-105">建立永久事件取用者的第一個步驟是建立描述事件取用者的 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="39b48-105">One of the first steps in creating a permanent event consumer is to create the WMI class that describes the event consumer.</span></span> <span data-ttu-id="39b48-106">具體而言，永久事件取用者類別會定義實體取用者所執行之動作的參數。</span><span class="sxs-lookup"><span data-stu-id="39b48-106">Specifically, the permanent event consumer class defines the parameters of the action implemented by the physical consumer.</span></span>

<span data-ttu-id="39b48-107">下列程式描述如何建立永久性事件取用者類別。</span><span class="sxs-lookup"><span data-stu-id="39b48-107">The following procedure describes how to create a permanent event consumer class.</span></span>

<span data-ttu-id="39b48-108">**若要建立永久事件取用者類別**</span><span class="sxs-lookup"><span data-stu-id="39b48-108">**To create a permanent event consumer class**</span></span>

1.  <span data-ttu-id="39b48-109">從 [**\_ \_ EventConsumer**](--eventconsumer.md)系統類別衍生類別。</span><span class="sxs-lookup"><span data-stu-id="39b48-109">Derive a class from the [**\_\_EventConsumer**](--eventconsumer.md) system class.</span></span>
2.  <span data-ttu-id="39b48-110">執行處理事件通知所需的任何參數。</span><span class="sxs-lookup"><span data-stu-id="39b48-110">Implement any parameters necessary to process an event notification.</span></span>

<span data-ttu-id="39b48-111">下列範例顯示用來建立 SMTPConsumerEvent 類別的語法。</span><span class="sxs-lookup"><span data-stu-id="39b48-111">The following example shows the syntax used to create the SMTPConsumerEvent class.</span></span> <span data-ttu-id="39b48-112">您可以使用此範例來建立新類別。</span><span class="sxs-lookup"><span data-stu-id="39b48-112">You can use this as an example for creating your new class.</span></span> <span data-ttu-id="39b48-113">[**SMTPEventConsumer**](smtpeventconsumer.md)類別會在每次傳遞事件給它時，使用 Simple Mail Transfer PROTOCOL (SMTP) 傳送電子郵件訊息。</span><span class="sxs-lookup"><span data-stu-id="39b48-113">The [**SMTPEventConsumer**](smtpeventconsumer.md) class sends an email message by using Simple Mail Transfer Protocol (SMTP) each time an event is delivered to it.</span></span> <span data-ttu-id="39b48-114">此類別定義于 smtpcons 中。</span><span class="sxs-lookup"><span data-stu-id="39b48-114">This class is defined in smtpcons.mof.</span></span>

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

<span data-ttu-id="39b48-115">您應該能夠建立永久事件取用者類別的實例，以描述將事件傳送給實體取用者的一或多個方法。</span><span class="sxs-lookup"><span data-stu-id="39b48-115">You should be able to create instances of your permanent event consumer class to describe one or more ways to send events to your physical consumer.</span></span> <span data-ttu-id="39b48-116">如需詳細資訊，請參閱 [建立邏輯取用者](creating-a-logical-consumer.md)。</span><span class="sxs-lookup"><span data-stu-id="39b48-116">For more information, see [Creating a Logical Consumer](creating-a-logical-consumer.md).</span></span>

 

 



