---
description: 藉由呼叫 SetupCommitFileQueue 來認可佇列之後，它就會開始處理已排入佇列的作業。 在每個步驟中，佇列會將通知傳送至呼叫 SetupCommitFileQueue 時所指定的回呼常式。
ms.assetid: 866e1066-b6e0-43d3-8af4-bd37fbc024e2
title: 佇列通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842a3ebc82640789fdb6e730e881d6790a0d642b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997871"
---
# <a name="queue-notifications"></a><span data-ttu-id="598c8-104">佇列通知</span><span class="sxs-lookup"><span data-stu-id="598c8-104">Queue Notifications</span></span>

<span data-ttu-id="598c8-105">藉由呼叫 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)來認可佇列之後，它就會開始處理已排入佇列的作業。</span><span class="sxs-lookup"><span data-stu-id="598c8-105">After a queue is committed by calling [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), it will begin to process the queued operations.</span></span> <span data-ttu-id="598c8-106">在每個步驟中，佇列會將通知傳送至呼叫 **SetupCommitFileQueue** 時所指定的回呼常式。</span><span class="sxs-lookup"><span data-stu-id="598c8-106">At each step, the queue sends a notification to the callback routine specified in the call to **SetupCommitFileQueue**.</span></span>

<span data-ttu-id="598c8-107">以下是 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 用來傳送通知給回呼常式的語法。</span><span class="sxs-lookup"><span data-stu-id="598c8-107">Following is the syntax that [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) uses to send a notification to the callback routine.</span></span>

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

<span data-ttu-id="598c8-108">*Param1* 和 *Param2* 的值包含與傳送至回呼常式之通知相關的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="598c8-108">The values of *Param1* and *Param2* contain additional information relevant to the notification being sent to the callback routine.</span></span> <span data-ttu-id="598c8-109">檔案 [佇列通知](file-queue-notifications.md)中會詳細說明每個通知、其 *Param1* 和 *Param2* 值，以及預設佇列回呼常式處理該通知的方式。</span><span class="sxs-lookup"><span data-stu-id="598c8-109">Each notification, its *Param1* and *Param2* values, and how the default queue callback routine handles that notification, is described in detail in [File Queue Notifications](file-queue-notifications.md).</span></span>

 

 



