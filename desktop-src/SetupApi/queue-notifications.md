---
description: 藉由呼叫 SetupCommitFileQueue 來認可佇列之後，它就會開始處理已排入佇列的作業。 在每個步驟中，佇列會將通知傳送至呼叫 SetupCommitFileQueue 時所指定的回呼常式。
ms.assetid: 866e1066-b6e0-43d3-8af4-bd37fbc024e2
title: 佇列通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06858eeb5c6e9abe200792f83edcc83503270ed2706450d35ef36d5dddc80d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665488"
---
# <a name="queue-notifications"></a>佇列通知

藉由呼叫 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)來認可佇列之後，它就會開始處理已排入佇列的作業。 在每個步驟中，佇列會將通知傳送至呼叫 **SetupCommitFileQueue** 時所指定的回呼常式。

以下是 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 用來傳送通知給回呼常式的語法。

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

*Param1* 和 *Param2* 的值包含與傳送至回呼常式之通知相關的其他資訊。 檔案 [佇列通知](file-queue-notifications.md)中會詳細說明每個通知、其 *Param1* 和 *Param2* 值，以及預設佇列回呼常式處理該通知的方式。

 

 



