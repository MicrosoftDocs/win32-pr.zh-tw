---
description: 下列通知會與檔案佇列一起使用。 如需有關通知格式和使用的詳細資訊，請參閱通知。
ms.assetid: 4a171b4a-8623-4be3-81ee-99081fe23034
title: 檔案佇列通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b674dee015c4c9408ff5dc853d5d3b2412e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027084"
---
# <a name="file-queue-notifications"></a><span data-ttu-id="f00be-104">檔案佇列通知</span><span class="sxs-lookup"><span data-stu-id="f00be-104">File Queue Notifications</span></span>

<span data-ttu-id="f00be-105">下列通知會與檔案佇列一起使用。</span><span class="sxs-lookup"><span data-stu-id="f00be-105">The following notifications are used with file queues.</span></span> <span data-ttu-id="f00be-106">如需有關通知格式和使用的詳細資訊，請參閱 [通知](notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="f00be-106">For more information about the format and use of notifications, see [Notifications](notifications.md).</span></span>



| <span data-ttu-id="f00be-107">通知</span><span class="sxs-lookup"><span data-stu-id="f00be-107">Notification</span></span>                                                      | <span data-ttu-id="f00be-108">Description</span><span class="sxs-lookup"><span data-stu-id="f00be-108">Description</span></span>                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f00be-109">**SPFILENOTIFY \_ COPYERROR**</span><span class="sxs-lookup"><span data-stu-id="f00be-109">**SPFILENOTIFY\_COPYERROR**</span></span>](spfilenotify-copyerror.md)         | <span data-ttu-id="f00be-110">檔案複製作業期間發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="f00be-110">An error occurred during a file copying operation.</span></span>                                                  |
| [<span data-ttu-id="f00be-111">**SPFILENOTIFY \_ DELETEERROR**</span><span class="sxs-lookup"><span data-stu-id="f00be-111">**SPFILENOTIFY\_DELETEERROR**</span></span>](spfilenotify-deleteerror.md)     | <span data-ttu-id="f00be-112">檔案刪除作業期間發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="f00be-112">An error occurred during a file deletion operation.</span></span>                                                 |
| [<span data-ttu-id="f00be-113">**SPFILENOTIFY \_ ENDCOPY**</span><span class="sxs-lookup"><span data-stu-id="f00be-113">**SPFILENOTIFY\_ENDCOPY**</span></span>](spfilenotify-endcopy.md)             | <span data-ttu-id="f00be-114">檔案複製作業已結束。</span><span class="sxs-lookup"><span data-stu-id="f00be-114">A file copying operation has ended.</span></span>                                                                 |
| [<span data-ttu-id="f00be-115">**SPFILENOTIFY \_ ENDDELETE**</span><span class="sxs-lookup"><span data-stu-id="f00be-115">**SPFILENOTIFY\_ENDDELETE**</span></span>](spfilenotify-enddelete.md)         | <span data-ttu-id="f00be-116">檔案刪除操作已結束。</span><span class="sxs-lookup"><span data-stu-id="f00be-116">A file deletion operation has ended.</span></span>                                                                |
| [<span data-ttu-id="f00be-117">**SPFILENOTIFY \_ ENDQUEUE**</span><span class="sxs-lookup"><span data-stu-id="f00be-117">**SPFILENOTIFY\_ENDQUEUE**</span></span>](spfilenotify-endqueue.md)           | <span data-ttu-id="f00be-118">佇列已完成認可。</span><span class="sxs-lookup"><span data-stu-id="f00be-118">The queue has finished committing.</span></span>                                                                  |
| [<span data-ttu-id="f00be-119">**SPFILENOTIFY \_ ENDRENAME**</span><span class="sxs-lookup"><span data-stu-id="f00be-119">**SPFILENOTIFY\_ENDRENAME**</span></span>](spfilenotify-endrename.md)         | <span data-ttu-id="f00be-120">檔案重新命名作業已結束。</span><span class="sxs-lookup"><span data-stu-id="f00be-120">A file rename operation has ended.</span></span>                                                                  |
| [<span data-ttu-id="f00be-121">**SPFILENOTIFY \_ ENDSUBQUEUE**</span><span class="sxs-lookup"><span data-stu-id="f00be-121">**SPFILENOTIFY\_ENDSUBQUEUE**</span></span>](spfilenotify-endsubqueue.md)     | <span data-ttu-id="f00be-122">子佇列 (複製、重新命名或刪除) 已結束。</span><span class="sxs-lookup"><span data-stu-id="f00be-122">A subqueue (either copy, rename or delete) has ended.</span></span>                                               |
| [<span data-ttu-id="f00be-123">**SPFILENOTIFY \_ FILEOPDELAYED**</span><span class="sxs-lookup"><span data-stu-id="f00be-123">**SPFILENOTIFY\_FILEOPDELAYED**</span></span>](spfilenotify-fileopdelayed.md) | <span data-ttu-id="f00be-124">檔案已在使用中，而且目前的操作已延遲，直到系統重新開機為止。</span><span class="sxs-lookup"><span data-stu-id="f00be-124">The file was in use, and the current operation has been delayed until the system is rebooted.</span></span>       |
| [<span data-ttu-id="f00be-125">**SPFILENOTIFY \_ LANGMISMATCH**</span><span class="sxs-lookup"><span data-stu-id="f00be-125">**SPFILENOTIFY\_LANGMISMATCH**</span></span>](spfilenotify-langmismatch.md)   | <span data-ttu-id="f00be-126">目前操作的語言與系統語言不符。</span><span class="sxs-lookup"><span data-stu-id="f00be-126">The language of the current operation does not match the system language.</span></span>                           |
| [<span data-ttu-id="f00be-127">**SPFILENOTIFY \_ NEEDMEDIA**</span><span class="sxs-lookup"><span data-stu-id="f00be-127">**SPFILENOTIFY\_NEEDMEDIA**</span></span>](spfilenotify-needmedia.md)         | <span data-ttu-id="f00be-128">需要新的來源媒體。</span><span class="sxs-lookup"><span data-stu-id="f00be-128">New source media is needed.</span></span>                                                                         |
| [<span data-ttu-id="f00be-129">**SPFILENOTIFY \_ QUEUESCAN**</span><span class="sxs-lookup"><span data-stu-id="f00be-129">**SPFILENOTIFY\_QUEUESCAN**</span></span>](spfilenotify-queuescan.md)         | <span data-ttu-id="f00be-130">已掃描檔案佇列中的節點。</span><span class="sxs-lookup"><span data-stu-id="f00be-130">A node in the file queue has been scanned.</span></span> <span data-ttu-id="f00be-131"> ( 僅限 [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)) </span><span class="sxs-lookup"><span data-stu-id="f00be-131">( [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) only)</span></span> |
| [<span data-ttu-id="f00be-132">**SPFILENOTIFY \_ RENAMEERROR**</span><span class="sxs-lookup"><span data-stu-id="f00be-132">**SPFILENOTIFY\_RENAMEERROR**</span></span>](spfilenotify-renameerror.md)     | <span data-ttu-id="f00be-133">檔案重新命名作業期間發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="f00be-133">An error occurred during a file renaming operation.</span></span>                                                 |
| [<span data-ttu-id="f00be-134">**SPFILENOTIFY \_ STARTCOPY**</span><span class="sxs-lookup"><span data-stu-id="f00be-134">**SPFILENOTIFY\_STARTCOPY**</span></span>](spfilenotify-startcopy.md)         | <span data-ttu-id="f00be-135">檔案複製作業已啟動。</span><span class="sxs-lookup"><span data-stu-id="f00be-135">A file copy operation has started.</span></span>                                                                  |
| [<span data-ttu-id="f00be-136">**SPFILENOTIFY \_ STARTDELETE**</span><span class="sxs-lookup"><span data-stu-id="f00be-136">**SPFILENOTIFY\_STARTDELETE**</span></span>](spfilenotify-startdelete.md)     | <span data-ttu-id="f00be-137">檔案刪除作業已啟動。</span><span class="sxs-lookup"><span data-stu-id="f00be-137">A file delete operation has started.</span></span>                                                                |
| [<span data-ttu-id="f00be-138">**SPFILENOTIFY \_ STARTQUEUE**</span><span class="sxs-lookup"><span data-stu-id="f00be-138">**SPFILENOTIFY\_STARTQUEUE**</span></span>](spfilenotify-startqueue.md)       | <span data-ttu-id="f00be-139">佇列已開始認可。</span><span class="sxs-lookup"><span data-stu-id="f00be-139">The queue has started to commit.</span></span>                                                                    |
| [<span data-ttu-id="f00be-140">**SPFILENOTIFY \_ STARTRENAME**</span><span class="sxs-lookup"><span data-stu-id="f00be-140">**SPFILENOTIFY\_STARTRENAME**</span></span>](spfilenotify-startrename.md)     | <span data-ttu-id="f00be-141">檔案重新命名作業已啟動。</span><span class="sxs-lookup"><span data-stu-id="f00be-141">A file rename operation has started.</span></span>                                                                |
| [<span data-ttu-id="f00be-142">**SPFILENOTIFY \_ STARTSUBQUEUE**</span><span class="sxs-lookup"><span data-stu-id="f00be-142">**SPFILENOTIFY\_STARTSUBQUEUE**</span></span>](spfilenotify-startsubqueue.md) | <span data-ttu-id="f00be-143">子佇列 (複製、重新命名或刪除) 已開始。</span><span class="sxs-lookup"><span data-stu-id="f00be-143">A subqueue (either copy, rename or delete) has started.</span></span>                                             |
| [<span data-ttu-id="f00be-144">**SPFILENOTIFY \_ TARGETEXISTS**</span><span class="sxs-lookup"><span data-stu-id="f00be-144">**SPFILENOTIFY\_TARGETEXISTS**</span></span>](spfilenotify-targetexists.md)   | <span data-ttu-id="f00be-145">目標上已有指定檔案的複本。</span><span class="sxs-lookup"><span data-stu-id="f00be-145">A copy of the specified file already exists on the target.</span></span>                                          |
| [<span data-ttu-id="f00be-146">**SPFILENOTIFY \_ TARGETNEWER**</span><span class="sxs-lookup"><span data-stu-id="f00be-146">**SPFILENOTIFY\_TARGETNEWER**</span></span>](spfilenotify-targetnewer.md)     | <span data-ttu-id="f00be-147">目標上有較新版本的指定檔案。</span><span class="sxs-lookup"><span data-stu-id="f00be-147">A newer version of the specified file exists on the target.</span></span>                                         |



 

 

 



