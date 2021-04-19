---
description: COMREPL 會在三個階段中執行其工作。
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: 複寫階段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc180e7864f05eb1be60262ee54dd4b71df53bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966645"
---
# <a name="replication-phases"></a><span data-ttu-id="65eab-103">複寫階段</span><span class="sxs-lookup"><span data-stu-id="65eab-103">Replication Phases</span></span>

<span data-ttu-id="65eab-104">COMREPL 會在三個階段中執行其工作。</span><span class="sxs-lookup"><span data-stu-id="65eab-104">COMREPL does its work in three phases.</span></span> <span data-ttu-id="65eab-105">複寫程式分成不同的階段，原因有下列兩個：</span><span class="sxs-lookup"><span data-stu-id="65eab-105">The replication process is divided into distinct phases for the following two reasons:</span></span>

-   <span data-ttu-id="65eab-106">將完成的工作與每個目標上完成的工作進行分隔，以準備來源</span><span class="sxs-lookup"><span data-stu-id="65eab-106">To separate work done to prepare the source from work that is done on each target</span></span>
-   <span data-ttu-id="65eab-107">延遲修改目標，直到從來源取得所有資料為止</span><span class="sxs-lookup"><span data-stu-id="65eab-107">To delay modification of the target until all data has been acquired from the source</span></span>

<span data-ttu-id="65eab-108">複寫階段如下所示。</span><span class="sxs-lookup"><span data-stu-id="65eab-108">The replication phases are as follows.</span></span>



| <span data-ttu-id="65eab-109">階段</span><span class="sxs-lookup"><span data-stu-id="65eab-109">Phase</span></span>         | <span data-ttu-id="65eab-110">描述</span><span class="sxs-lookup"><span data-stu-id="65eab-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65eab-111">準備階段</span><span class="sxs-lookup"><span data-stu-id="65eab-111">Prepare phase</span></span> | <span data-ttu-id="65eab-112">將所有已安裝的應用程式匯出到來源電腦上的本機。</span><span class="sxs-lookup"><span data-stu-id="65eab-112">Exports all the installed applications locally on the source computer.</span></span> <span data-ttu-id="65eab-113">這個階段不會接觸任何目標的設定。</span><span class="sxs-lookup"><span data-stu-id="65eab-113">This phase does not touch the configuration of any targets.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="65eab-114">複製階段</span><span class="sxs-lookup"><span data-stu-id="65eab-114">Copy phase</span></span>    | <span data-ttu-id="65eab-115">將資料複製到目的電腦。</span><span class="sxs-lookup"><span data-stu-id="65eab-115">Copies data to a target computer.</span></span> <span data-ttu-id="65eab-116">來源上匯出的所有應用程式都會複製到目標。</span><span class="sxs-lookup"><span data-stu-id="65eab-116">All applications exported on the source are copied to the target.</span></span> <span data-ttu-id="65eab-117">這是檔案複製作業。</span><span class="sxs-lookup"><span data-stu-id="65eab-117">This is a file copy operation.</span></span> <span data-ttu-id="65eab-118"> (請參閱檔案 [管理](file-management.md)。 ) 此步驟也會從來源電腦取得未封裝在匯出應用程式檔內的一些資料 (例如，應用程式識別) 。</span><span class="sxs-lookup"><span data-stu-id="65eab-118">(See [File Management](file-management.md).) This step also acquires some data from the source computer that is not encapsulated within exported application files (for example, application identities).</span></span> <span data-ttu-id="65eab-119">這項資料會保留在 COMREPL 內的記憶體中。</span><span class="sxs-lookup"><span data-stu-id="65eab-119">This data is held in memory within COMREPL.</span></span> <span data-ttu-id="65eab-120">這個階段不會接觸任何目的電腦的設定。</span><span class="sxs-lookup"><span data-stu-id="65eab-120">This phase does not touch the configuration of any target computers.</span></span>                                                                               |
| <span data-ttu-id="65eab-121">安裝階段</span><span class="sxs-lookup"><span data-stu-id="65eab-121">Install phase</span></span> | <span data-ttu-id="65eab-122">在目的電腦上安裝來原始目錄。</span><span class="sxs-lookup"><span data-stu-id="65eab-122">Installs source catalog on a target computer.</span></span> <span data-ttu-id="65eab-123">當這個步驟起始時，重新設定目標所需的所有資料都位於目的檔案系統的應用程式檔內，或在 COMREPL 中保留為實例資料。</span><span class="sxs-lookup"><span data-stu-id="65eab-123">When this step is initiated, all data required to reconfigure the target is within application files in the target's file system or is held as instance data within COMREPL.</span></span> <span data-ttu-id="65eab-124">這個階段將會刪除目標 (上已安裝的所有應用程式，但在安裝從來源複製的應用程式之前，會先 [複寫) 中](what-gets-replicated.md) 所述的應用程式。</span><span class="sxs-lookup"><span data-stu-id="65eab-124">This phase will delete all the installed applications on the target (except the applications described in [What Gets Replicated](what-gets-replicated.md)) prior to installing the applications copied from the source.</span></span> <span data-ttu-id="65eab-125">COMREPL 會使用每個目標的安裝執行緒，同時在多個目標上安裝。</span><span class="sxs-lookup"><span data-stu-id="65eab-125">COMREPL installs on multiple targets concurrently by using an install thread per target.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="65eab-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="65eab-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65eab-127">檔案管理</span><span class="sxs-lookup"><span data-stu-id="65eab-127">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="65eab-128">記錄和錯誤報表</span><span class="sxs-lookup"><span data-stu-id="65eab-128">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="65eab-129">使用 COMREPL</span><span class="sxs-lookup"><span data-stu-id="65eab-129">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="65eab-130">複寫的內容</span><span class="sxs-lookup"><span data-stu-id="65eab-130">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



