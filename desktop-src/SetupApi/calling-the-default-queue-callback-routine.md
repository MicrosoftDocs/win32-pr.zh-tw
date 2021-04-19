---
description: 如果呼叫 SetupCommitFileQueue 時，預設佇列回呼常式已初始化並指定，則佇列會在內部呼叫預設佇列回呼常式，您只需要執行其他動作。
ms.assetid: a976c275-f128-490d-a544-efbfc6fd87f4
title: 呼叫預設佇列回呼常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24449fc1fcd92d8041de6f104092f45925a495b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978400"
---
# <a name="calling-the-default-queue-callback-routine"></a><span data-ttu-id="0fe3a-103">呼叫預設佇列回呼常式</span><span class="sxs-lookup"><span data-stu-id="0fe3a-103">Calling the Default Queue Callback Routine</span></span>

<span data-ttu-id="0fe3a-104">如果呼叫 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 時，預設佇列回呼常式已初始化並指定，則佇列會在內部呼叫預設佇列回呼常式，您只需要執行其他動作。</span><span class="sxs-lookup"><span data-stu-id="0fe3a-104">If the default queue callback routine is initialized and specified when [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) is called, the queue calls the default queue callback routine internally and you need do nothing more.</span></span>

<span data-ttu-id="0fe3a-105">如果您建立的篩選回呼常式依賴預設佇列回呼常式來處理佇列通知的子集，則您的篩選回呼常式必須明確呼叫 [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) 。</span><span class="sxs-lookup"><span data-stu-id="0fe3a-105">If you create a filter callback routine that relies on the default queue callback routine to handle a subset of the queue notifications, your filter callback routine must call [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitly.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0fe3a-106">當您明確呼叫 [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) 時，您必須傳入 [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) 或 [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)所傳回的 void 指標。</span><span class="sxs-lookup"><span data-stu-id="0fe3a-106">When you call [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitly, you must pass in the void pointer returned by either [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span>

 

> [!Note]  
> <span data-ttu-id="0fe3a-107">其中一種方式是建立自訂回呼常式的內容結構，其包含 [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) 或 [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)所傳回的 void 指標作為其成員之一。</span><span class="sxs-lookup"><span data-stu-id="0fe3a-107">One way to do this is to create a context structure for your custom callback routine that includes as one of its members the void pointer returned by [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span>

 

 

 



