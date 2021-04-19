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
# <a name="calling-the-default-queue-callback-routine"></a>呼叫預設佇列回呼常式

如果呼叫 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 時，預設佇列回呼常式已初始化並指定，則佇列會在內部呼叫預設佇列回呼常式，您只需要執行其他動作。

如果您建立的篩選回呼常式依賴預設佇列回呼常式來處理佇列通知的子集，則您的篩選回呼常式必須明確呼叫 [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) 。

> [!IMPORTANT]
> 當您明確呼叫 [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) 時，您必須傳入 [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) 或 [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)所傳回的 void 指標。

 

> [!Note]  
> 其中一種方式是建立自訂回呼常式的內容結構，其包含 [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) 或 [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)所傳回的 void 指標作為其成員之一。

 

 

 



