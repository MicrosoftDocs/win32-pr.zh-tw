---
description: 為了啟用應用程式檔的傳輸，COMREPL 會在來源和目標上自動管理檔系統資料夾的集合。 這些 COMREPL 資料夾全都以% systemdir% com 複寫為根目錄 \\ \\ 。
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: '檔案管理 (元件服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e785b8fd39d94bcf623810bca950862d22ec8762
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510518"
---
# <a name="file-management"></a><span data-ttu-id="f876f-104">檔案管理</span><span class="sxs-lookup"><span data-stu-id="f876f-104">File Management</span></span>

<span data-ttu-id="f876f-105">為了啟用應用程式檔的傳輸，COMREPL 會在來源和目標上自動管理檔系統資料夾的集合。</span><span class="sxs-lookup"><span data-stu-id="f876f-105">To enable the transfer of application files, COMREPL automatically manages sets of file system folders on the source and target.</span></span> <span data-ttu-id="f876f-106">這些 COMREPL 資料夾全都以% systemdir% com 複寫為根目錄 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="f876f-106">These COMREPL folders are all rooted in %systemdir%\\com\\replication.</span></span>

## <a name="source-folders"></a><span data-ttu-id="f876f-107">來源資料夾</span><span class="sxs-lookup"><span data-stu-id="f876f-107">Source folders</span></span>



| <span data-ttu-id="f876f-108">資料夾</span><span class="sxs-lookup"><span data-stu-id="f876f-108">Folder</span></span>                   | <span data-ttu-id="f876f-109">目的</span><span class="sxs-lookup"><span data-stu-id="f876f-109">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f876f-110">ReplicaSource</span><span class="sxs-lookup"><span data-stu-id="f876f-110">ReplicaSource</span></span><br/> | <span data-ttu-id="f876f-111">在準備階段期間匯出的應用程式會儲存在這裡。</span><span class="sxs-lookup"><span data-stu-id="f876f-111">Applications exported during the prepare phase are stored here.</span></span><br/> <span data-ttu-id="f876f-112">每次針對指定的來源電腦執行準備階段時，就會覆寫此資料夾。</span><span class="sxs-lookup"><span data-stu-id="f876f-112">This folder is overwritten each time the prepare phase is executed against a given source computer.</span></span> <span data-ttu-id="f876f-113">此資料夾永遠不會明確刪除，因此在來源準備好之後，可以隨時進行複寫。</span><span class="sxs-lookup"><span data-stu-id="f876f-113">This folder is never explicitly deleted, so replication to targets can take place at any time after the source is prepared.</span></span><br/> <span data-ttu-id="f876f-114">每個應用程式都會儲存在它自己的子資料夾中，名為 <appName> + <appID> 。</span><span class="sxs-lookup"><span data-stu-id="f876f-114">Each application is stored in its own subfolder named <appName>+<appID>.</span></span><br/> |



 

## <a name="target-folders"></a><span data-ttu-id="f876f-115">目標資料夾</span><span class="sxs-lookup"><span data-stu-id="f876f-115">Target folders</span></span>



| <span data-ttu-id="f876f-116">資料夾</span><span class="sxs-lookup"><span data-stu-id="f876f-116">Folder</span></span>                    | <span data-ttu-id="f876f-117">目的</span><span class="sxs-lookup"><span data-stu-id="f876f-117">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f876f-118">ReplicaNew</span><span class="sxs-lookup"><span data-stu-id="f876f-118">ReplicaNew</span></span><br/>     | <span data-ttu-id="f876f-119">複製階段會將來源上 ReplicaSource 中的所有檔案和子資料夾複製到目標上的 ReplicaNew。</span><span class="sxs-lookup"><span data-stu-id="f876f-119">The copy phase copies all files and subfolders from ReplicaSource on the source to ReplicaNew on the target.</span></span> <span data-ttu-id="f876f-120">每次針對指定的目標執行複製階段時，就會刪除任何先前的 ReplicaNew 內容。</span><span class="sxs-lookup"><span data-stu-id="f876f-120">Any previous contents of ReplicaNew are deleted each time the copy phase is run against a given target.</span></span><br/> <span data-ttu-id="f876f-121">只有當複寫程式正在執行時，這個資料夾才會存在。</span><span class="sxs-lookup"><span data-stu-id="f876f-121">This folder exists only while the replication process is running.</span></span> <span data-ttu-id="f876f-122"> (參閱 ReplicaCurrent。 ) </span><span class="sxs-lookup"><span data-stu-id="f876f-122">(See ReplicaCurrent.)</span></span><br/>           |
| <span data-ttu-id="f876f-123">ReplicaCurrent</span><span class="sxs-lookup"><span data-stu-id="f876f-123">ReplicaCurrent</span></span><br/> | <span data-ttu-id="f876f-124">目前安裝在目標上的已複寫應用程式會儲存在這裡。</span><span class="sxs-lookup"><span data-stu-id="f876f-124">The replicated applications currently installed on the target are stored here.</span></span><br/> <span data-ttu-id="f876f-125">當安裝階段開始時，ReplicaNew 資料夾會重新命名為 ReplicaCurrent。</span><span class="sxs-lookup"><span data-stu-id="f876f-125">When the install phase is started, the ReplicaNew folder is renamed to ReplicaCurrent.</span></span> <span data-ttu-id="f876f-126">如果有現有的 ReplicaCurrent 資料夾，則會重新命名為 ReplicaOld。</span><span class="sxs-lookup"><span data-stu-id="f876f-126">If there is an existing ReplicaCurrent folder, it is renamed to ReplicaOld.</span></span> <span data-ttu-id="f876f-127">如果有現有的 ReplicaOld 資料夾，則會刪除其內容。</span><span class="sxs-lookup"><span data-stu-id="f876f-127">If there is an existing ReplicaOld folder, its contents are deleted.</span></span><br/> |
| <span data-ttu-id="f876f-128">ReplicaOld</span><span class="sxs-lookup"><span data-stu-id="f876f-128">ReplicaOld</span></span><br/>     | <span data-ttu-id="f876f-129">儲存在上一次複寫期間安裝的應用程式檔。</span><span class="sxs-lookup"><span data-stu-id="f876f-129">Saves the application files installed during the next to last replication.</span></span> <span data-ttu-id="f876f-130">這些檔案只會儲存供備份之用。</span><span class="sxs-lookup"><span data-stu-id="f876f-130">These files are saved for backup purposes only.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="f876f-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="f876f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f876f-132">記錄和錯誤報表</span><span class="sxs-lookup"><span data-stu-id="f876f-132">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="f876f-133">複寫階段</span><span class="sxs-lookup"><span data-stu-id="f876f-133">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="f876f-134">使用 COMREPL</span><span class="sxs-lookup"><span data-stu-id="f876f-134">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="f876f-135">複寫的內容</span><span class="sxs-lookup"><span data-stu-id="f876f-135">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 




