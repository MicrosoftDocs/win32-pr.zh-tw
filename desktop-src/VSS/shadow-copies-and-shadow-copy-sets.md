---
description: 陰影複製是磁片區的快照集，該磁片區會在一段妥善定義的瞬間內，複製該磁片區上保留的所有資料。 VSS 會依持續性 GUID 來識別每個陰影複製。
ms.assetid: 8ef2478a-c8bc-4517-9a14-e1d9226ec4cd
title: 陰影複製和陰影複製集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18709842b1fb0fbf6d6cce2557b51042dfb024ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993081"
---
# <a name="shadow-copies-and-shadow-copy-sets"></a><span data-ttu-id="5fa55-104">陰影複製和陰影複製集</span><span class="sxs-lookup"><span data-stu-id="5fa55-104">Shadow Copies and Shadow Copy Sets</span></span>

<span data-ttu-id="5fa55-105">[*陰影複製*](vssgloss-s.md)是磁片區的快照集，該磁片區會在一段妥善定義的瞬間內，複製該磁片區上保留的所有資料。</span><span class="sxs-lookup"><span data-stu-id="5fa55-105">A [*shadow copy*](vssgloss-s.md) is a snapshot of a volume that duplicates all of the data that is held on that volume at one well-defined instant in time.</span></span> <span data-ttu-id="5fa55-106">VSS 會依持續性 GUID 來識別每個陰影複製。</span><span class="sxs-lookup"><span data-stu-id="5fa55-106">VSS identifies each shadow copy by a persistent GUID.</span></span>

<span data-ttu-id="5fa55-107">[*陰影複製組*](vssgloss-s.md)是所有不同磁片區的陰影複製集合，全都採用相同的時間。</span><span class="sxs-lookup"><span data-stu-id="5fa55-107">A [*shadow copy set*](vssgloss-s.md) is a collection of shadow copies of various volumes all taken at the same time.</span></span> <span data-ttu-id="5fa55-108">VSS 會依持續性 GUID 來識別每個陰影複製集。</span><span class="sxs-lookup"><span data-stu-id="5fa55-108">VSS identifies each shadow copy set by a persistent GUID.</span></span>

<span data-ttu-id="5fa55-109">特定硬體或軟體廠商選擇如何選擇執行陰影複製，完全是自行決定。</span><span class="sxs-lookup"><span data-stu-id="5fa55-109">How a particular hardware or software vendor chooses to implement shadow copies is completely at its discretion.</span></span> <span data-ttu-id="5fa55-110">一旦建立陰影複製，系統就會有可供系統使用的陰影複製磁片區的兩個映射：可供使用的原始磁片區;也可以透過 VSS API 來存取複製的資料。</span><span class="sxs-lookup"><span data-stu-id="5fa55-110">Once a shadow copy is created, there are effectively two images of the shadow-copied volume available to the system: the original volume, which can be accessed conventionally; and the copied data, which can be accessed through the VSS API.</span></span>

<span data-ttu-id="5fa55-111">如此一來，就可以同時執行兩組活動：</span><span class="sxs-lookup"><span data-stu-id="5fa55-111">This allows two sets of activities to take place at the same time:</span></span>

-   <span data-ttu-id="5fa55-112">系統上的一般應用程式可以使用原始磁片區快速繼續或繼續，並更新磁片上的資料。</span><span class="sxs-lookup"><span data-stu-id="5fa55-112">Ordinary applications on the system can quickly continue or resume using the original volume, updating data on the disk.</span></span>
-   <span data-ttu-id="5fa55-113">使用 VSS 要求者 API 來存取陰影複製之磁片區的應用程式，可以執行備份或類似的作業。</span><span class="sxs-lookup"><span data-stu-id="5fa55-113">Applications that are using the VSS requester API to access the shadow-copied volume can perform backups or similar operations.</span></span>

<span data-ttu-id="5fa55-114">針對每個檔案、目錄或磁片區，不需要以相同的方式來執行陰影複製。</span><span class="sxs-lookup"><span data-stu-id="5fa55-114">Shadow copies need not be implemented in the same way for every file, directory, or volume.</span></span> <span data-ttu-id="5fa55-115">不同的陰影複製機制執行 ([*提供者*](vssgloss-p.md)) 可能會使用不同的方法來建立陰影複製。</span><span class="sxs-lookup"><span data-stu-id="5fa55-115">Different implementations of the shadow copy mechanism ([*providers*](vssgloss-p.md)) may use different approaches to creating a shadow copy.</span></span> <span data-ttu-id="5fa55-116">不過，對於使用 VSS API 的所有應用程式，所有陰影複製都應該相同。</span><span class="sxs-lookup"><span data-stu-id="5fa55-116">However, to all applications that are using the VSS API, all shadow copies should appear the same.</span></span>

<span data-ttu-id="5fa55-117">如需預設 Windows 提供者執行的詳細資訊，請參閱 [系統提供者](providers.md)。</span><span class="sxs-lookup"><span data-stu-id="5fa55-117">For information on the default Windows provider implementation, see [System Provider](providers.md).</span></span>

## <a name="default-shadow-copy-state"></a><span data-ttu-id="5fa55-118">預設陰影複製狀態</span><span class="sxs-lookup"><span data-stu-id="5fa55-118">Default Shadow Copy State</span></span>

<span data-ttu-id="5fa55-119">雖然檔案系統會在建立陰影複製之前排清所有 i/o 緩衝區，但這並不確定已正確處理未完成的 i/o。</span><span class="sxs-lookup"><span data-stu-id="5fa55-119">Even though the file system flushes all I/O buffers prior to creating a shadow copy, this will not ensure that incomplete I/O is properly handled.</span></span>

<span data-ttu-id="5fa55-120">因此，假設系統沒有具備 VSS 功能的應用程式，則陰影複製中的資料會被視為處於損 [*毀一致的狀態*](vssgloss-c.md)。</span><span class="sxs-lookup"><span data-stu-id="5fa55-120">Therefore, assuming that the system has no VSS-enabled applications, the data in a shadow copy is said to be in a [*crash-consistent state*](vssgloss-c.md).</span></span> <span data-ttu-id="5fa55-121">處於損毀一致狀態的陰影複製包含磁片的映射，這與在嚴重系統關機後仍存在的磁片映射相同。</span><span class="sxs-lookup"><span data-stu-id="5fa55-121">A shadow copy in a crash-consistent state contains an image of the disk that is the same as that which would exist following a catastrophic system shutdown.</span></span> <span data-ttu-id="5fa55-122">所有開啟的檔案仍會存在於磁片區，但不保證不會有不完整的 i/o 作業或資料損毀。</span><span class="sxs-lookup"><span data-stu-id="5fa55-122">All files that were open will still exist on the volume, but they are not guaranteed to be free of incomplete I/O operations or data corruption.</span></span>

<span data-ttu-id="5fa55-123">雖然當機時保持一致的狀態不會完全處理與定義穩定備份組相關的所有問題 (請參閱 [常見的磁片區備份問題](common-volume-backup-issues.md)) ，它有幾個優點，是傳統備份作業必須使用的備份組：</span><span class="sxs-lookup"><span data-stu-id="5fa55-123">While the crash-consistent state does not fully deal with all the issues associated with defining a stable backup set (see [Common Volume Backup Issues](common-volume-backup-issues.md)), it has several advantages over the backup set that conventional backup operations would have to use:</span></span>

-   <span data-ttu-id="5fa55-124">包含在陰影複製中的磁片區（即使處於損毀一致狀態）仍會包含所有檔案。</span><span class="sxs-lookup"><span data-stu-id="5fa55-124">A volume contained in a shadow copy, even in a crash-consistent state, still contains all files.</span></span> <span data-ttu-id="5fa55-125">建立時不含陰影複製的備份組，將不會包含在備份時開啟的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="5fa55-125">A backup set created without a shadow copy would not contain all files open at the time of the backup.</span></span> <span data-ttu-id="5fa55-126">備份作業會從備份中排除在備份作業時保持開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="5fa55-126">Files held open at the time of the backup operation are excluded from the backup.</span></span>
-   <span data-ttu-id="5fa55-127">磁片區的陰影複製會在一段時間內立即建立，而不是藉由找出使用中的檔案系統，這通常需要更多時間。</span><span class="sxs-lookup"><span data-stu-id="5fa55-127">The shadow copy of the volume is created at one instant in time, and not by traversing an active file system, which typically requires much more time.</span></span>

<span data-ttu-id="5fa55-128">系統上不是 VSS 感知的應用程式（字處理器、編輯器等等）可能會使其檔案處於損毀一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="5fa55-128">Applications on a system that are not VSS-aware—word processors, editors, and so on—will likely have their files left in a crash-consistent state.</span></span> <span data-ttu-id="5fa55-129">不過， (寫入器的 VSS 感知應用程式) 可以協調其動作，讓陰影複製中的檔案狀態妥善定義且一致。</span><span class="sxs-lookup"><span data-stu-id="5fa55-129">However, VSS-aware applications (writers) can coordinate their actions so that the state of their files in the shadow copy is well defined and consistent.</span></span>

## <a name="shadow-copy-freeze-and-thaw"></a><span data-ttu-id="5fa55-130">陰影複製凍結和解除凍結</span><span class="sxs-lookup"><span data-stu-id="5fa55-130">Shadow Copy Freeze and Thaw</span></span>

<span data-ttu-id="5fa55-131">建立每個 VSS 陰影複製作業的方式都是由 [*凍結*](vssgloss-f.md) 和 [*解除凍結*](vssgloss-t.md) 事件括住，而寫入器會在陰影複製之前用來將檔案放在穩定的狀態。</span><span class="sxs-lookup"><span data-stu-id="5fa55-131">The creation of every VSS shadow copy operation is bracketed by [*Freeze*](vssgloss-f.md) and [*Thaw*](vssgloss-t.md) events, which writers use to put their files in a stable state prior to shadow copy.</span></span>

<span data-ttu-id="5fa55-132">將凍結和解除凍結事件作為 VSS 模型的一部分，表示：</span><span class="sxs-lookup"><span data-stu-id="5fa55-132">Having Freeze and Thaw events as part of the VSS model means:</span></span>

-   <span data-ttu-id="5fa55-133">處理凍結事件表示開發寫入者的使用者在備份週期中必須有清楚的分隔點，以確保磁片的所有寫入作業都已停止，且檔案處於妥善定義的備份狀態。</span><span class="sxs-lookup"><span data-stu-id="5fa55-133">Handling the Freeze event means that those who are developing writers must have a clearly delineated point in the backup cycle where they ensure that all write operations to the disk are stopped and that files are in a well-defined state for backup.</span></span>
-   <span data-ttu-id="5fa55-134">處理解除凍結事件提供了一種機制，讓寫入器繼續寫入磁片，並清除任何暫存檔或其他與陰影複製建立關聯的暫時狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="5fa55-134">Handling the Thaw event provides the mechanism for writers to resume writes to the disk and clean up any temporary files or other temporary state information that were created in association with the shadow copy.</span></span>
-   <span data-ttu-id="5fa55-135">凍結和解除凍結事件之間的預設視窗很短 (通常是60秒) ;因此，寫入器提供的任何服務實際中斷都可以最小化。</span><span class="sxs-lookup"><span data-stu-id="5fa55-135">The default window between the Freeze and Thaw events is short (typically 60 seconds); therefore, actual interruption of any service that a writer provides can be minimized.</span></span>
-   <span data-ttu-id="5fa55-136"> (的其他事件（例如 PrepareForSnapshot) 前面和後續的凍結和解除凍結事件），提供必要的彈性，讓寫入器能夠完成複雜的作業以支援陰影複製。</span><span class="sxs-lookup"><span data-stu-id="5fa55-136">Handling of other events (such as PrepareForSnapshot) preceding and following the Freeze and Thaw events, respectively, provides the necessary flexibility to allow writers to complete complicated operations to support shadow copies.</span></span>

 

 



