---
description: InstallValidate 動作會確認成本已屬性化的所有磁片區都有足夠的空間可進行安裝。 如果有任何磁片區是磁碟空間不足的情況，InstallValidate 動作就會結束安裝，併發生嚴重錯誤。
ms.assetid: 1c55794d-1ecc-43bf-956f-96afc5f36964
title: InstallValidate 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650ce136ac3b1b62e41ce34f79f5d28540d1292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194546"
---
# <a name="installvalidate-action"></a><span data-ttu-id="491f8-104">InstallValidate 動作</span><span class="sxs-lookup"><span data-stu-id="491f8-104">InstallValidate Action</span></span>

<span data-ttu-id="491f8-105">InstallValidate 動作會確認 [*成本*](c-gly.md)已屬性化的所有 [*磁片*](v-gly.md)區都有足夠的空間可進行安裝。</span><span class="sxs-lookup"><span data-stu-id="491f8-105">The InstallValidate action verifies that all [*volumes*](v-gly.md) to which [*cost*](c-gly.md) has been attributed have sufficient space for the installation.</span></span> <span data-ttu-id="491f8-106">如果有任何磁片區是磁碟空間不足的情況，InstallValidate 動作就會結束安裝，併發生嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="491f8-106">The InstallValidate action ends the installation with a fatal error if any volume is short of disk space.</span></span>

<span data-ttu-id="491f8-107">InstallValidate 動作也會在使用中進程目前正在使用一或多個要覆寫或移除的檔案時，通知使用者。</span><span class="sxs-lookup"><span data-stu-id="491f8-107">The InstallValidate action also notifies the user if one or more files to be overwritten or removed are currently in use by an active process.</span></span> <span data-ttu-id="491f8-108">如需詳細資訊，請參閱 [系統重新開機](system-reboots.md)。</span><span class="sxs-lookup"><span data-stu-id="491f8-108">For more information, see [System Reboots](system-reboots.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="491f8-109">順序限制</span><span class="sxs-lookup"><span data-stu-id="491f8-109">Sequence Restrictions</span></span>

<span data-ttu-id="491f8-110">[CostFinalize](costfinalize-action.md)動作和任何 UI 對話方塊序列，可讓使用者修改選取狀態和（或）目錄，應該在 InstallValidate 動作之前排序。</span><span class="sxs-lookup"><span data-stu-id="491f8-110">The [CostFinalize](costfinalize-action.md) action and any UI dialog box sequences that allow the user to modify selection states and/or directories should be sequenced before the InstallValidate action.</span></span>

<span data-ttu-id="491f8-111">變更功能或元件安裝狀態的[自訂動作](custom-actions.md)必須在 InstallValidate 動作之前排序。</span><span class="sxs-lookup"><span data-stu-id="491f8-111">[Custom actions](custom-actions.md) that change the installation state of features or components must be sequenced before the InstallValidate action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="491f8-112">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="491f8-112">ActionData Messages</span></span>

<span data-ttu-id="491f8-113">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="491f8-113">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="491f8-114">備註</span><span class="sxs-lookup"><span data-stu-id="491f8-114">Remarks</span></span>

<span data-ttu-id="491f8-115">一般來說，當使用者嘗試起始檔案的複製時，較早的 UI 對話方塊順序應該與 InstallValidate 動作執行相同的驗證。</span><span class="sxs-lookup"><span data-stu-id="491f8-115">Typically, an earlier UI dialog box sequence should perform the same verification as the InstallValidate action when the user attempts to initiate the copying of files.</span></span> <span data-ttu-id="491f8-116">如果選取的磁片區沒有足夠的空間可進行安裝，此 UI 對話方塊順序應該會顯示 [ **磁碟空間不足** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="491f8-116">This UI dialog box sequence should present an **Out of Disk Space** dialog box if the volumes selected do not have enough space for the installation.</span></span> <span data-ttu-id="491f8-117">如果磁碟空間不足，則應該以防止使用者繼續安裝的方式來撰寫 UI 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="491f8-117">The UI dialog boxes should be authored in a way to prevent the user from proceeding with the installation if there is insufficient disk space.</span></span> <span data-ttu-id="491f8-118">在無訊息安裝的情況下，沒有任何使用者介面，且如果磁碟空間不足，InstallValidate 動作就會終止安裝。</span><span class="sxs-lookup"><span data-stu-id="491f8-118">In the case of a quiet installation, there is no user interface and the InstallValidate action terminates the installation if there is insufficient disk space.</span></span> <span data-ttu-id="491f8-119">如果啟用記錄功能，則會在記錄檔中記錄提前終止的原因。</span><span class="sxs-lookup"><span data-stu-id="491f8-119">The cause of the premature termination is recorded in the log file if logging is enabled.</span></span>

<span data-ttu-id="491f8-120">如果在檔案的任何程式中開啟檔案以供執行或修改，則會將專案加入至內部 FilesInUse [*資料表。*](c-gly.md)</span><span class="sxs-lookup"><span data-stu-id="491f8-120">An entry is added to an internal FilesInUse table if any file is overwritten or removed while it is open for execution or modification by any process during file [*costing*](c-gly.md).</span></span> <span data-ttu-id="491f8-121">FilesInUse 資料表包含檔案的名稱和完整路徑的資料行。</span><span class="sxs-lookup"><span data-stu-id="491f8-121">The FilesInUse table contains columns for the name and full path of the file.</span></span> <span data-ttu-id="491f8-122">當 InstallValidate 動作執行時，安裝程式會查詢 FilesInUse 資料表中的專案，並使用該檔案來決定進程的名稱。</span><span class="sxs-lookup"><span data-stu-id="491f8-122">When the InstallValidate action executes, the installer queries the FilesInUse table for entries and determines the name of the process using the file.</span></span> <span data-ttu-id="491f8-123">InstallValidate 動作會針對此查詢所識別的每個唯一程式，將一筆記錄加入 [ListBox](listbox-table.md) 使用者介面資料表中。</span><span class="sxs-lookup"><span data-stu-id="491f8-123">The InstallValidate action adds one record to the [ListBox](listbox-table.md) user interface table for each unique process identified by this query.</span></span> <span data-ttu-id="491f8-124">記錄包含每個資料行中的下列值：</span><span class="sxs-lookup"><span data-stu-id="491f8-124">The record contains the following values in each column:</span></span>

<span data-ttu-id="491f8-125">**屬性**： FileInUseProcess</span><span class="sxs-lookup"><span data-stu-id="491f8-125">**Property**: FileInUseProcess</span></span>

 

<span data-ttu-id="491f8-126">**值**： *進程的名稱*</span><span class="sxs-lookup"><span data-stu-id="491f8-126">**Value**: *Name of process*</span></span>

 

<span data-ttu-id="491f8-127">**Text**： *流程主視窗標題中包含的文字*</span><span class="sxs-lookup"><span data-stu-id="491f8-127">**Text**: *Text contained in the caption of the main window of the process*</span></span>

<span data-ttu-id="491f8-128">InstallValidate 動作接著會顯示 [ **使用中** 的檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="491f8-128">The InstallValidate action then displays the **Files In Use** dialog box.</span></span> <span data-ttu-id="491f8-129">此對話方塊會顯示必須關閉的處理常式，以避免重新開機系統以取代使用中檔案的需求。</span><span class="sxs-lookup"><span data-stu-id="491f8-129">This dialog box displays the processes that must be shut down to avoid the requirement of restarting the system to replace files in use.</span></span>

<span data-ttu-id="491f8-130">InstallValidate 動作會使用 [保留名稱[FilesInUse](filesinuse-dialog.md) ] 對話方塊來查詢已撰寫之對話方塊的[對話方塊](dialog-table.md)資料表，並加以顯示。</span><span class="sxs-lookup"><span data-stu-id="491f8-130">The InstallValidate action queries the [Dialog](dialog-table.md) table for an authored dialog box with the reserved name [FilesInUse](filesinuse-dialog.md) dialog and displays it.</span></span> <span data-ttu-id="491f8-131">此對話方塊必須包含與名為 FileInUseProcess 的屬性系結的 [ListBox](listbox-control.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="491f8-131">This dialog box must contain a [ListBox](listbox-control.md) control that is tied to a property named FileInUseProcess.</span></span> <span data-ttu-id="491f8-132">依照慣例，這個對話方塊會有 [結束 **]、[\*\*\*\*重試**] 或 [**略** 過] 按鈕，但這是由 UI 作者所撰寫。</span><span class="sxs-lookup"><span data-stu-id="491f8-132">By convention, this dialog box has an **Exit**, **Retry**, or **Ignore** button, but this is up to the UI author.</span></span> <span data-ttu-id="491f8-133">每個按鈕都應系結至[ControlEvent](controlevent-table.md)資料表中的[EndDialog](enddialog-controlevent.md) ControlEvent。</span><span class="sxs-lookup"><span data-stu-id="491f8-133">Each button should be tied to an [EndDialog](enddialog-controlevent.md) ControlEvent in the [ControlEvent](controlevent-table.md) table.</span></span> <span data-ttu-id="491f8-134">InstallValidate 動作會依照下列其中一個[EndDialog](enddialog-controlevent.md)引數（與使用者推送的按鈕相關聯）的指示，以下列方式回應[dataadapter.doaction](doaction-controlevent.md) ControlEvent 所傳回的值：</span><span class="sxs-lookup"><span data-stu-id="491f8-134">The InstallValidate action responds as follows to the value returned by the [DoAction](doaction-controlevent.md) ControlEvent, as dictated by one of these [EndDialog](enddialog-controlevent.md) arguments associated with the button pushed by the user:</span></span>

<span data-ttu-id="491f8-135">**重試**：已清除新增至 [ListBox](listbox-table.md) 資料表的所有值，並重複整個檔案 [*成本*](c-gly.md) 程式，重新檢查仍在使用中的檔案。</span><span class="sxs-lookup"><span data-stu-id="491f8-135">**Retry**: All values added to the [ListBox](listbox-table.md) table are cleared, and the entire file [*costing*](c-gly.md) procedure is repeated, rechecking for files that are still in use.</span></span> <span data-ttu-id="491f8-136">如果有一或多個進程仍識別為使用要覆寫或刪除的檔案，則會重複此程式;否則，InstallValidate 會將控制權傳回給安裝程式，其狀態為 msiDoActionStatusSuccess。</span><span class="sxs-lookup"><span data-stu-id="491f8-136">If one or more processes are still identified as using files to be overwritten or deleted, the process repeats; otherwise, InstallValidate returns control to the installer with a status of msiDoActionStatusSuccess.</span></span>

<span data-ttu-id="491f8-137">**Exit**： InstallValidate 動作會立即將控制權傳回給安裝程式，其狀態為 msiDoActionStatusUserExit。</span><span class="sxs-lookup"><span data-stu-id="491f8-137">**Exit**: The InstallValidate action immediately returns control to the installer with a status of msiDoActionStatusUserExit.</span></span> <span data-ttu-id="491f8-138">這會結束安裝。</span><span class="sxs-lookup"><span data-stu-id="491f8-138">This terminates the installation.</span></span>

<span data-ttu-id="491f8-139">**任何其他傳回值**： InstallValidate 動作會立即將控制權傳回給安裝程式，其狀態為 msiDoActionStatusSuccess。</span><span class="sxs-lookup"><span data-stu-id="491f8-139">**Any other return value**: The InstallValidate action immediately returns control to the installer with a status of msiDoActionStatusSuccess.</span></span> <span data-ttu-id="491f8-140">在此情況下，因為有一或多個檔案仍在使用中，所以後續的 [InstallFiles](installfiles-action.md) 和/或 [InstallAdminPackage](installadminpackage-action.md) 動作必須排程在系統重新開機時，要取代或刪除) 的 (使用中檔案。</span><span class="sxs-lookup"><span data-stu-id="491f8-140">In this case, since one or more files are still in use, the subsequent [InstallFiles](installfiles-action.md) and/or [InstallAdminPackage](installadminpackage-action.md) actions must schedule the in-use file(s) to be replaced or deleted when the system is restarted.</span></span>

<span data-ttu-id="491f8-141">如果資料庫中沒有 [ListBox](listbox-table.md) 資料表，InstallValidate 會以無訊息方式結束，而不會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="491f8-141">If there is no [ListBox](listbox-table.md) table in the database, InstallValidate exits silently without an error.</span></span>

<span data-ttu-id="491f8-142">分號是轉換、來源和修補程式的清單分隔符號，不應該用在這些檔案名或路徑中。</span><span class="sxs-lookup"><span data-stu-id="491f8-142">The semicolon is the list delimiter for transforms, sources, and patches, and should not be used in these file names or paths.</span></span>

<span data-ttu-id="491f8-143">在唯讀位置中標示為唯讀的檔案永遠不會被安裝程式使用。</span><span class="sxs-lookup"><span data-stu-id="491f8-143">Files marked read-only in a read-only location are never considered in use by the installer.</span></span>

<span data-ttu-id="491f8-144">如果使用者介面層級為「基本」，則會向使用者顯示包含「**中止**」和「**重試**」按鈕的預設 [**磁碟空間不足**] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="491f8-144">A default **Out of Disk Space** dialog box containing **Abort** and **Retry** buttons is presented to the user if the user interface level is basic.</span></span>

 

 



