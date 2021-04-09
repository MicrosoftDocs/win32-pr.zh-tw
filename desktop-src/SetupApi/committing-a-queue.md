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
# <a name="committing-a-queue"></a><span data-ttu-id="509bb-104">認可佇列</span><span class="sxs-lookup"><span data-stu-id="509bb-104">Committing a Queue</span></span>

<span data-ttu-id="509bb-105">在所有所需的檔案作業都已排入佇列之後，必須認可佇列。</span><span class="sxs-lookup"><span data-stu-id="509bb-105">After all the desired file operations have been queued, the queue must be committed.</span></span> <span data-ttu-id="509bb-106">這會導致處理已排入佇列的檔案作業。</span><span class="sxs-lookup"><span data-stu-id="509bb-106">This causes the enqueued file operations to be processed.</span></span>

<span data-ttu-id="509bb-107">檔案佇列在認可之後無法重複使用。</span><span class="sxs-lookup"><span data-stu-id="509bb-107">A file queue cannot be reused after it has been committed.</span></span> <span data-ttu-id="509bb-108">最佳做法是收集檔案佇列的所有必要檔案作業，並只認可一次佇列。</span><span class="sxs-lookup"><span data-stu-id="509bb-108">The best practice is to collect all the required file operations for the file queue and commit the queue only once.</span></span> <span data-ttu-id="509bb-109">如果在認可佇列之後需要額外的處理，則應該關閉佇列的控制碼並建立新的檔案佇列。</span><span class="sxs-lookup"><span data-stu-id="509bb-109">If additional processing of the queue is required after it has been committed, the handle to the queue should be closed and a new file queue created.</span></span> <span data-ttu-id="509bb-110">若要認可檔案佇列，請呼叫 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 函數，並指定回呼常式。</span><span class="sxs-lookup"><span data-stu-id="509bb-110">To commit the file queue, call the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function, specifying a callback routine.</span></span> <span data-ttu-id="509bb-111">當檔案作業已處理時，回呼常式將會從 **SetupCommitFileQueue** 接收通知。</span><span class="sxs-lookup"><span data-stu-id="509bb-111">The callback routine will receive notifications from **SetupCommitFileQueue** as the file operations are processed.</span></span> <span data-ttu-id="509bb-112">如果您想要使用預設佇列回呼常式，您必須先呼叫 [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) 或 [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)來初始化所需的內容。</span><span class="sxs-lookup"><span data-stu-id="509bb-112">If you want to use the default queue callback routine, you must first initialize the necessary context by calling either [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span> <span data-ttu-id="509bb-113">如需預設佇列回呼常式的詳細資訊，請參閱 [預設佇列回呼常式](default-queue-callback-routine.md)。</span><span class="sxs-lookup"><span data-stu-id="509bb-113">For more information about the default queue callback routine, see [Default Queue Callback Routine](default-queue-callback-routine.md).</span></span>

> [!Note]  
> <span data-ttu-id="509bb-114">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 應該在關閉佇列之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="509bb-114">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) should be called before the queue is closed.</span></span> <span data-ttu-id="509bb-115">呼叫 [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) 時未認可的任何作業都不會執行。</span><span class="sxs-lookup"><span data-stu-id="509bb-115">Any operations that are uncommitted when [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) is called will not be performed.</span></span>

 

 

 



