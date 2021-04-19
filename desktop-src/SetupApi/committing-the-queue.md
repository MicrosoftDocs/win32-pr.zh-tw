---
description: 如果在佇列承諾期間將會呼叫預設回呼函式，則必須使用 SetupInitDefaultQueueCallback 或 SetupInitDefaultQueueCallbackEx 函式來初始化它的內容。
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: 認可佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ed721c60457a77a168218aa0294bf448889129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976942"
---
# <a name="committing-the-queue"></a><span data-ttu-id="be5d1-103">認可佇列</span><span class="sxs-lookup"><span data-stu-id="be5d1-103">Committing the Queue</span></span>

<span data-ttu-id="be5d1-104">如果在佇列承諾期間將會呼叫預設回呼函式，則必須使用 [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) 或 [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) 函式來初始化它的內容。</span><span class="sxs-lookup"><span data-stu-id="be5d1-104">If the default callback function is going to be called during the queue commitment, the context for it must be initialized using the [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) functions.</span></span> <span data-ttu-id="be5d1-105">如果您使用的自訂回呼函式永遠不會呼叫預設回呼函式，則不需要此步驟。</span><span class="sxs-lookup"><span data-stu-id="be5d1-105">If you are using a custom callback function that never calls the default callback function, this step is not necessary.</span></span>

<span data-ttu-id="be5d1-106">建立佇列並將處理佇列通知的回呼函式初始化之後，您可以呼叫 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 來認可已排入佇列的作業。</span><span class="sxs-lookup"><span data-stu-id="be5d1-106">After the queue is built and the callback function that will process queue notifications has been initialized, you can call [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to commit the operations that have been enqueued.</span></span>

<span data-ttu-id="be5d1-107">下列範例會使用 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 來認可使用預設回呼常式的佇列。</span><span class="sxs-lookup"><span data-stu-id="be5d1-107">The following example uses [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to commit the queue using the default callback routine.</span></span>

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

<span data-ttu-id="be5d1-108">在上述範例中，MyQueue 是要認可的佇列，OwnerWindow 是將擁有預設回呼常式所建立之任何對話方塊的視窗，SetupDefaultQueueCallback 會指定將使用預設的回呼函式，而 *內容* 則是上一次呼叫 [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)所傳回之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="be5d1-108">In the preceding example, MyQueue is the queue to commit, OwnerWindow is the window that will own any dialog boxes created by the default callback routine, SetupDefaultQueueCallback specifies that the default callback function will be used, and *Context* is a pointer to the structure returned by the previous call to [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).</span></span>

 

 



