---
description: 在所有所需的檔案作業都已排入佇列之後，必須認可佇列。 這會導致處理已排入佇列的檔案作業。
ms.assetid: 536f47f5-785e-4a83-a500-c769442e3e68
title: 認可佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d995f6811dbd19bba9e13f29bc119cdf2f471f74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695168"
---
# <a name="committing-a-queue"></a>認可佇列

在所有所需的檔案作業都已排入佇列之後，必須認可佇列。 這會導致處理已排入佇列的檔案作業。

檔案佇列在認可之後無法重複使用。 最佳做法是收集檔案佇列的所有必要檔案作業，並只認可一次佇列。 如果在認可佇列之後需要額外的處理，則應該關閉佇列的控制碼並建立新的檔案佇列。 若要認可檔案佇列，請呼叫 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 函數，並指定回呼常式。 當檔案作業已處理時，回呼常式將會從 **SetupCommitFileQueue** 接收通知。 如果您想要使用預設佇列回呼常式，您必須先呼叫 [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) 或 [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)來初始化所需的內容。 如需預設佇列回呼常式的詳細資訊，請參閱 [預設佇列回呼常式](default-queue-callback-routine.md)。

> [!Note]  
> [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 應該在關閉佇列之前呼叫。 呼叫 [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) 時未認可的任何作業都不會執行。

 

 

 



