---
description: 當 SetupCommitFileQueue 函式認可檔案佇列時，它會依下列連續處理檔案作業：檔案刪除作業、檔案重新命名作業，最後是檔案複製作業。
ms.assetid: 23aae815-ff1a-435d-b14d-3c62a3355a1b
title: 佇列承諾的順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f261b1e42631e35146dc3d11f848ff543c999c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849600"
---
# <a name="order-of-queue-commitment"></a><span data-ttu-id="d1fe2-103">佇列承諾的順序</span><span class="sxs-lookup"><span data-stu-id="d1fe2-103">Order of Queue Commitment</span></span>

<span data-ttu-id="d1fe2-104">當 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 函式認可檔案佇列時，它會依下列連續處理檔案作業：檔案刪除作業、檔案重新命名作業，最後是檔案複製作業。</span><span class="sxs-lookup"><span data-stu-id="d1fe2-104">When the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function commits the file queue, it processes the file operations in the following order: file deletion operations, then file renaming operations, and finally, file copying operations.</span></span> <span data-ttu-id="d1fe2-105">下列大綱說明佇列的承諾用量流程的生命週期。</span><span class="sxs-lookup"><span data-stu-id="d1fe2-105">The following outline illustrates the life cycle of a queue's commitment process.</span></span>

 

-   <span data-ttu-id="d1fe2-106">啟動刪除子佇列</span><span class="sxs-lookup"><span data-stu-id="d1fe2-106">start the delete subqueue</span></span>
    -   <span data-ttu-id="d1fe2-107">開始 < 的檔案刪除作業--為每個作業重複</span><span class="sxs-lookup"><span data-stu-id="d1fe2-107">start a file delete operation <-- repeat for each</span></span>
    -   <span data-ttu-id="d1fe2-108">完成檔案刪除作業 <--已排入佇列的檔案刪除</span><span class="sxs-lookup"><span data-stu-id="d1fe2-108">finish a file delete operation <-- queued file delete</span></span>
-   <span data-ttu-id="d1fe2-109">完成刪除子佇列</span><span class="sxs-lookup"><span data-stu-id="d1fe2-109">finish the delete subqueue</span></span>

<!-- -->

-   <span data-ttu-id="d1fe2-110">啟動重新命名子佇列</span><span class="sxs-lookup"><span data-stu-id="d1fe2-110">start the rename subqueue</span></span>
    -   <span data-ttu-id="d1fe2-111">開始重新命名作業 <--為每個動作重複</span><span class="sxs-lookup"><span data-stu-id="d1fe2-111">start a file rename operation <-- repeat for each</span></span>
    -   <span data-ttu-id="d1fe2-112">完成檔案刪除作業 <--已排入佇列的檔案重新命名</span><span class="sxs-lookup"><span data-stu-id="d1fe2-112">finish a file delete operation <-- queued file rename</span></span>
-   <span data-ttu-id="d1fe2-113">完成重新命名子佇列</span><span class="sxs-lookup"><span data-stu-id="d1fe2-113">finish the rename subqueue</span></span>

<!-- -->

-   <span data-ttu-id="d1fe2-114">啟動複製 subque</span><span class="sxs-lookup"><span data-stu-id="d1fe2-114">start the copy subque</span></span>
    -   <span data-ttu-id="d1fe2-115">開始檔案複製作業 <--為每個作業重複</span><span class="sxs-lookup"><span data-stu-id="d1fe2-115">start a file copy operation <-- repeat for each</span></span>
    -   <span data-ttu-id="d1fe2-116">完成檔案複製作業 <--已排入佇列的檔案複製</span><span class="sxs-lookup"><span data-stu-id="d1fe2-116">finish a file copy operation <-- queued file copy</span></span>
    -   <span data-ttu-id="d1fe2-117">完成複製子佇列</span><span class="sxs-lookup"><span data-stu-id="d1fe2-117">finish the copy subqueue</span></span>
-   <span data-ttu-id="d1fe2-118">完成佇列</span><span class="sxs-lookup"><span data-stu-id="d1fe2-118">finish the queue</span></span>

 

<span data-ttu-id="d1fe2-119">在每個步驟中，或如果發生錯誤， [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 函式會將通知傳送給回呼常式。</span><span class="sxs-lookup"><span data-stu-id="d1fe2-119">At each step, or if an error occurs, the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function sends a notification to the callback routine.</span></span> <span data-ttu-id="d1fe2-120">回呼常式可以使用佇列所傳送的資訊來追蹤安裝進度，並視需要與使用者互動。</span><span class="sxs-lookup"><span data-stu-id="d1fe2-120">The callback routine can use the information sent by the queue to track the installation progress and, if necessary, interact with the user.</span></span>

<span data-ttu-id="d1fe2-121">例如，如果檔案複製作業需要目前路徑無法使用的原始程式檔， [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 會將 SPFILENOTIFY \_ NEEDMEDIA 通知傳送給回呼常式，以及所需的檔案和媒體的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1fe2-121">For example, if a file copy operation needed a source file that was not available at the current path, [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) would send a SPFILENOTIFY\_NEEDMEDIA notification to the callback routine, along with information about the file and media required.</span></span> <span data-ttu-id="d1fe2-122">回呼常式可以使用此資訊來產生對話方塊，以提示使用者透過呼叫 SetupPromptForDisk 來插入下一個磁片[ ](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)</span><span class="sxs-lookup"><span data-stu-id="d1fe2-122">The callback routine could use this information to generate a dialog box that prompts the user to insert the next disk by calling [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)</span></span>

<span data-ttu-id="d1fe2-123">預設佇列回呼常式 [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)會隨附于安裝程式 API。</span><span class="sxs-lookup"><span data-stu-id="d1fe2-123">A default queue callback routine, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), is included with the Setup API.</span></span> <span data-ttu-id="d1fe2-124">此常式會處理佇列通知，並產生安裝的錯誤對話方塊和進度列。</span><span class="sxs-lookup"><span data-stu-id="d1fe2-124">This routine handles queue notifications and generates error dialog boxes and progress bars for the installation.</span></span> <span data-ttu-id="d1fe2-125">您可以使用預設佇列回呼常式，或撰寫篩選回呼常式來處理通知的子集，並將其他通知傳遞至預設佇列回呼常式。</span><span class="sxs-lookup"><span data-stu-id="d1fe2-125">You can use the default queue callback routine as it is, or write a filter callback routine to handle a subset of the notifications and pass the others on to the default queue callback routine.</span></span>

<span data-ttu-id="d1fe2-126">如果回呼常式的任何功能都不符合您的需求，您可以撰寫獨立的自訂回呼常式，而不會呼叫預設佇列回呼常式。</span><span class="sxs-lookup"><span data-stu-id="d1fe2-126">If none of the functionality of the callback routine suits your needs, you can write a self-contained custom callback routine that does not call the default queue callback routine.</span></span>

<span data-ttu-id="d1fe2-127">如需佇列回呼常式的詳細資訊，請參閱 [預設佇列回呼常式](default-queue-callback-routine.md)和 [建立自訂佇列回呼常式](creating-a-custom-queue-callback-routine.md)。</span><span class="sxs-lookup"><span data-stu-id="d1fe2-127">For more information about queue callback routines, see [Default Queue Callback Routine](default-queue-callback-routine.md), and [Creating a Custom Queue Callback Routine](creating-a-custom-queue-callback-routine.md).</span></span>

 

 



