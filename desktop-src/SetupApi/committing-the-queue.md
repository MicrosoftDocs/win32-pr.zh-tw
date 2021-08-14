---
description: 如果在佇列承諾期間將會呼叫預設回呼函式，則必須使用 SetupInitDefaultQueueCallback 或 SetupInitDefaultQueueCallbackEx 函式來初始化它的內容。
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: 認可佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67c19b91cc25e5107f91fbd241d96147137a38b8544568e57ea3bbbd58981a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887519"
---
# <a name="committing-the-queue"></a>認可佇列

如果在佇列承諾期間將會呼叫預設回呼函式，則必須使用 [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) 或 [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) 函式來初始化它的內容。 如果您使用的自訂回呼函式永遠不會呼叫預設回呼函式，則不需要此步驟。

建立佇列並將處理佇列通知的回呼函式初始化之後，您可以呼叫 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 來認可已排入佇列的作業。

下列範例會使用 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 來認可使用預設回呼常式的佇列。

``` syntax
test = SetupCommitFileQueue (
     OwnerWindow,          //window that will own dialog boxes
                           //created by the callback routine
     MyQueue,              //the queue to commit
  
                           //use the default callback routine
     SetupDefaultQueueCallback,  
  
     Context               //context information that will be 
                           //  used by the callback routine
);
```

在上述範例中，MyQueue 是要認可的佇列，OwnerWindow 是將擁有預設回呼常式所建立之任何對話方塊的視窗，SetupDefaultQueueCallback 會指定將使用預設的回呼函式，而 *內容* 則是上一次呼叫 [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)所傳回之結構的指標。

 

 



