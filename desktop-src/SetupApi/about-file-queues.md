---
description: 檔案佇列是一種檔案作業清單，會一次處理。 佇列中的檔案作業可能是複製、重新命名或刪除作業。 檔案佇列會依類型來組織檔案作業，建立複製、重新命名和刪除子佇列。
ms.assetid: 9ad42c37-1d6b-4f1b-8173-629e2d3678f2
title: 關於檔案佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af441a1195bad5116306ca93cfbe658be5b3efc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970976"
---
# <a name="about-file-queues"></a><span data-ttu-id="af3ad-105">關於檔案佇列</span><span class="sxs-lookup"><span data-stu-id="af3ad-105">About File Queues</span></span>

<span data-ttu-id="af3ad-106">檔案佇列是一種檔案作業清單，會一次處理。</span><span class="sxs-lookup"><span data-stu-id="af3ad-106">A file queue is a list of file operations that are processed at one time.</span></span> <span data-ttu-id="af3ad-107">佇列中的檔案作業可能是複製、重新命名或刪除作業。</span><span class="sxs-lookup"><span data-stu-id="af3ad-107">The file operations in the queue may be copy, rename, or delete operations.</span></span> <span data-ttu-id="af3ad-108">檔案佇列會依類型來組織檔案作業，建立複製、重新命名和刪除子佇列。</span><span class="sxs-lookup"><span data-stu-id="af3ad-108">The file queue organizes file operations by type, creating copy, rename, and delete subqueues.</span></span>

<span data-ttu-id="af3ad-109">這些作業可能會以任何順序傳送至佇列，而佇列進程不需要連續。</span><span class="sxs-lookup"><span data-stu-id="af3ad-109">These operations may be sent to the queue in any order, and the enqueuing process need not be contiguous.</span></span> <span data-ttu-id="af3ad-110">認可佇列時， [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 函式會依作業類型的順序來執行檔案作業。</span><span class="sxs-lookup"><span data-stu-id="af3ad-110">When the queue is committed, the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function performs file operations in order of the operation type.</span></span>

<span data-ttu-id="af3ad-111">一般來說，整個安裝所需的所有檔案作業都會排入檔案佇列中，然後在認可佇列時，于單一批次中處理。</span><span class="sxs-lookup"><span data-stu-id="af3ad-111">Typically, all of the file operations necessary for an entire installation are queued to the file queue, and then processed in a single batch when the queue is committed.</span></span>

<span data-ttu-id="af3ad-112">從 INF 檔案依區段將檔案作業排入佇列的優點之一，是您可以簡化安裝程式。</span><span class="sxs-lookup"><span data-stu-id="af3ad-112">One advantage of queuing file operations over installing files section-by-section from an INF file is that you can streamline the installation process.</span></span> <span data-ttu-id="af3ad-113">您可以在建立佇列時，從使用者取得安裝資訊，以取得要安裝的所有檔案，而不需要為每個要安裝的區段取得資訊。</span><span class="sxs-lookup"><span data-stu-id="af3ad-113">Instead of having to obtain information from the user for each section to be installed, you can obtain installation information from the user for all the files to be installed while building the queue.</span></span> <span data-ttu-id="af3ad-114">如此一來，當 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 函式處理時間密集的複製作業時，使用者就可以釋出其他活動。</span><span class="sxs-lookup"><span data-stu-id="af3ad-114">This frees the user to pursue other activities while the time-intensive copy operations are processed by the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function.</span></span>

<span data-ttu-id="af3ad-115">檔案佇列的另一個優點是您可以追蹤整個安裝的進度。</span><span class="sxs-lookup"><span data-stu-id="af3ad-115">Another advantage of file queues is that you can track the progress of the installation as a whole.</span></span> <span data-ttu-id="af3ad-116">從 INF 檔案逐步安裝區段時，進度列之類的進度指示器只會追蹤目前的 INF 區段。</span><span class="sxs-lookup"><span data-stu-id="af3ad-116">When installing section-by-section from an INF file, progress indicators such as progress bars can track only the current INF section.</span></span> <span data-ttu-id="af3ad-117">安裝下一個區段時，進度列就會從頭開始。</span><span class="sxs-lookup"><span data-stu-id="af3ad-117">When the next section is installed, the progress bar starts over.</span></span> <span data-ttu-id="af3ad-118">使用佇列時，在認可佇列之前，會先知道要在整個安裝期間處理的檔案總數，因此可以產生進度列來追蹤整個安裝。</span><span class="sxs-lookup"><span data-stu-id="af3ad-118">With a queue, the total number of files to be processed during the entire installation is known before the queue is committed, and thus, a progress bar can be generated to track the entire installation.</span></span>

<span data-ttu-id="af3ad-119">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="af3ad-119">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="af3ad-120">佇列承諾的順序</span><span class="sxs-lookup"><span data-stu-id="af3ad-120">Order of Queue Commitment</span></span>](order-of-queue-commitment.md)
-   [<span data-ttu-id="af3ad-121">佇列通知</span><span class="sxs-lookup"><span data-stu-id="af3ad-121">Queue Notifications</span></span>](queue-notifications.md)

 

 



