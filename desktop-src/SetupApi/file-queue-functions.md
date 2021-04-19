---
description: 下列函式會與檔案佇列一起使用。
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: 檔案佇列函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acaf1fb1fbd2dc4f020577a1ae68d6ec9b2e95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000296"
---
# <a name="file-queue-functions"></a><span data-ttu-id="ea015-103">檔案佇列函式</span><span class="sxs-lookup"><span data-stu-id="ea015-103">File Queue Functions</span></span>

<span data-ttu-id="ea015-104">下列函式會與檔案佇列一起使用。</span><span class="sxs-lookup"><span data-stu-id="ea015-104">The following functions are used with file queues.</span></span>



| <span data-ttu-id="ea015-105">函式</span><span class="sxs-lookup"><span data-stu-id="ea015-105">Function</span></span>                                                             | <span data-ttu-id="ea015-106">描述</span><span class="sxs-lookup"><span data-stu-id="ea015-106">Description</span></span>                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea015-107">**SetupCloseFileQueue**</span><span class="sxs-lookup"><span data-stu-id="ea015-107">**SetupCloseFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | <span data-ttu-id="ea015-108">終止佇列。</span><span class="sxs-lookup"><span data-stu-id="ea015-108">Terminates the queue.</span></span> <span data-ttu-id="ea015-109">未認可任何剩餘的交易。</span><span class="sxs-lookup"><span data-stu-id="ea015-109">Any remaining transactions are not committed.</span></span>                                   |
| [<span data-ttu-id="ea015-110">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="ea015-110">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | <span data-ttu-id="ea015-111">認可所有已排入佇列的交易。</span><span class="sxs-lookup"><span data-stu-id="ea015-111">Commits all queued transactions.</span></span>                                                                      |
| [<span data-ttu-id="ea015-112">**SetupOpenFileQueue**</span><span class="sxs-lookup"><span data-stu-id="ea015-112">**SetupOpenFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | <span data-ttu-id="ea015-113">初始化並傳回檔案佇列的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ea015-113">Initializes and returns a handle to the file queue.</span></span>                                                   |
| [<span data-ttu-id="ea015-114">**SetupPromptReboot**</span><span class="sxs-lookup"><span data-stu-id="ea015-114">**SetupPromptReboot**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | <span data-ttu-id="ea015-115">視需要提示使用者重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="ea015-115">Prompts the user to reboot his or her computer, if necessary.</span></span>                                         |
| [<span data-ttu-id="ea015-116">**SetupQueueCopy**</span><span class="sxs-lookup"><span data-stu-id="ea015-116">**SetupQueueCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | <span data-ttu-id="ea015-117">將檔案複製排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="ea015-117">Queues a file copy.</span></span>                                                                                   |
| [<span data-ttu-id="ea015-118">**SetupQueueCopySection**</span><span class="sxs-lookup"><span data-stu-id="ea015-118">**SetupQueueCopySection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | <span data-ttu-id="ea015-119">將 [INF 複製檔案] 區段中的檔案排入佇列。</span><span class="sxs-lookup"><span data-stu-id="ea015-119">Queues the files in an INF Copy Files section.</span></span>                                                        |
| [<span data-ttu-id="ea015-120">**SetupQueueDefaultCopy**</span><span class="sxs-lookup"><span data-stu-id="ea015-120">**SetupQueueDefaultCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | <span data-ttu-id="ea015-121">使用 INF 檔案中指定的預設資訊，將 INF 複製檔案區段中的檔案排入佇列。</span><span class="sxs-lookup"><span data-stu-id="ea015-121">Queues the files in an INF Copy Files section using the default information specified in an INF file.</span></span> |
| [<span data-ttu-id="ea015-122">**SetupQueueDelete**</span><span class="sxs-lookup"><span data-stu-id="ea015-122">**SetupQueueDelete**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | <span data-ttu-id="ea015-123">將檔案刪除排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="ea015-123">Queues a file deletion.</span></span>                                                                               |
| [<span data-ttu-id="ea015-124">**SetupQueueDeleteSection**</span><span class="sxs-lookup"><span data-stu-id="ea015-124">**SetupQueueDeleteSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | <span data-ttu-id="ea015-125">將 INF [刪除檔案] 區段中的檔案排入佇列。</span><span class="sxs-lookup"><span data-stu-id="ea015-125">Queues the files in an INF Delete Files section.</span></span>                                                      |
| [<span data-ttu-id="ea015-126">**SetupQueueRename**</span><span class="sxs-lookup"><span data-stu-id="ea015-126">**SetupQueueRename**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | <span data-ttu-id="ea015-127">將檔案重新命名為佇列。</span><span class="sxs-lookup"><span data-stu-id="ea015-127">Queues a file rename.</span></span>                                                                                 |
| [<span data-ttu-id="ea015-128">**SetupQueueRenameSection**</span><span class="sxs-lookup"><span data-stu-id="ea015-128">**SetupQueueRenameSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | <span data-ttu-id="ea015-129">在 [INF 重新命名檔案] 區段中將檔案排入佇列。</span><span class="sxs-lookup"><span data-stu-id="ea015-129">Queues the files in an INF Rename Files section.</span></span>                                                      |
| [<span data-ttu-id="ea015-130">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="ea015-130">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | <span data-ttu-id="ea015-131">掃描檔案佇列。</span><span class="sxs-lookup"><span data-stu-id="ea015-131">Scans the file queue.</span></span>                                                                                 |
| [<span data-ttu-id="ea015-132">**SetupSetPlatformPathOverride**</span><span class="sxs-lookup"><span data-stu-id="ea015-132">**SetupSetPlatformPathOverride**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | <span data-ttu-id="ea015-133">設定平臺路徑覆寫。</span><span class="sxs-lookup"><span data-stu-id="ea015-133">Sets the platform path override.</span></span>                                                                      |



 

 

 



