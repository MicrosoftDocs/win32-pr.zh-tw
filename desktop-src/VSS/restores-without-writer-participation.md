---
description: VSS 備份中的寫入器參與設計，是為了讓應用程式能夠控制要如何使用其還原資料。
ms.assetid: 076b2e6f-c2ca-4129-8827-1b18a655d634
title: 不含寫入器參與的還原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89fd5ea855d2d91701d351e860bf966148be587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115148"
---
# <a name="restores-without-writer-participation"></a><span data-ttu-id="0b1ca-103">不含寫入器參與的還原</span><span class="sxs-lookup"><span data-stu-id="0b1ca-103">Restores without Writer Participation</span></span>

<span data-ttu-id="0b1ca-104">VSS 備份中的寫入器參與設計，是為了讓應用程式能夠控制要如何使用其還原資料。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-104">Writer participation in a VSS backup is designed to allow applications to control what and how their restore data is to be used.</span></span>

<span data-ttu-id="0b1ca-105">一般來說，如果系統上有寫入器，建議您不要將資料還原至其原始位置，而不需要撰寫參與。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-105">In general, if a writer is available on a system, it is never advisable to restore data to its original location without writer participation.</span></span> <span data-ttu-id="0b1ca-106">這樣的還原可能會遇到鎖定的目的地檔案，而且會造成損毀資料的重大風險。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-106">Such a restore would likely encounter locked destination files and runs a significant risk of corrupting data.</span></span>

<span data-ttu-id="0b1ca-107">不過，備份應用程式可能會想要或需要還原 VSS 備份而不需要撰寫參與的原因如下：</span><span class="sxs-lookup"><span data-stu-id="0b1ca-107">However, there are reasons why a backup application might want or need to restore a VSS backup without writer participation:</span></span>

-   <span data-ttu-id="0b1ca-108">資料是由不受 VSS 感知的應用程式所管理。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-108">Data is managed by VSS-unaware applications.</span></span> <span data-ttu-id="0b1ca-109">幾乎每個系統都有一些應用程式（文字編輯器、郵件讀取器、文字處理器等等）不是 VSS 感知。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-109">Almost every system will have some applications—text editors, mail readers, word processors, and so forth—that are VSS unaware.</span></span> <span data-ttu-id="0b1ca-110">無法使用寫入器參與來還原此資料。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-110">This data cannot be restored using writer participation.</span></span>

    <span data-ttu-id="0b1ca-111">一般而言，這種類型的資料不是系統或服務關鍵，而還原它應該不會有問題，或至少在傳統還原期間沒有任何問題。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-111">Generally, this type of data is not system- or service-critical, and restoring it should not be problematic, or at least no more problematic than during a conventional restore.</span></span>

    <span data-ttu-id="0b1ca-112">如同傳統還原的準備工作，還原操作員應該在啟動 VSS 還原之前，嘗試暫停或終止這類應用程式。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-112">As with preparations for conventional restores, if possible, restore operators should attempt to suspend or terminate such applications prior to starting a VSS restore.</span></span>

-   <span data-ttu-id="0b1ca-113">遺漏 VSS 寫入器。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-113">Missing VSS writers.</span></span> <span data-ttu-id="0b1ca-114">在還原損毀的系統狀態時，這種情況可能相當常見。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-114">This situation may be fairly common when restoring the state of a damaged system.</span></span> <span data-ttu-id="0b1ca-115">備份作業必須判斷是否需要還原遺失寫入器的檔案。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-115">A backup operation must determine whether it is desirable to restore files for missing writers.</span></span> <span data-ttu-id="0b1ca-116">如果需要還原，可以還原檔案，就像傳統備份會還原這些檔案一樣。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-116">If restoration is desirable, the files can be restored just as a conventional backup would restore them.</span></span>
-   <span data-ttu-id="0b1ca-117">寫入器資料的私用還原。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-117">A private restore of a writer's data.</span></span> <span data-ttu-id="0b1ca-118">要求者可以選擇將執行中的寫入器資料還原到某個私用位置，而不會通知寫入器。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-118">A requester may choose to restore the data of a running writer to some private location without notifying the writer.</span></span> <span data-ttu-id="0b1ca-119">其中一個範例可能會還原寫入器的資料，以支援離線比較。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-119">An example of this might be restoration of the writer's data to support offline comparison.</span></span> <span data-ttu-id="0b1ca-120">在這種情況下，要求者不會想要在進行還原時使用 [*新的目標位置*](vssgloss-n.md) ，因為它不希望寫入器存取資料。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-120">In this sort of situation, a requester would not want to use the [*new target location*](vssgloss-n.md) while doing the restore, because it does not want the writer to access the data.</span></span>
-   <span data-ttu-id="0b1ca-121">在還原過程中不會包含寫入器。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-121">A writer does not want to be involved during restore.</span></span> <span data-ttu-id="0b1ca-122">寫入器會藉由 \_ \_ 針對 [**IVssCreateWriterMetadata：： SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod)的 *writerRestore* 參數傳遞 VSS WRE，來指出這一點。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-122">A writer indicates this by passing in VSS\_WRE\_NEVER for the *writerRestore* parameter of [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).</span></span>
-   <span data-ttu-id="0b1ca-123">寫入器需要自訂的還原方法。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-123">A writer requires a custom restore method.</span></span> <span data-ttu-id="0b1ca-124">寫入器表示它需要自訂還原， \_ \_ 方法是針對 [**IVssCreateWriterMetadata：： SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod)的 *方法* 參數傳遞 VSS RME 自訂。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-124">A writer indicates that it requires a custom restore by passing in VSS\_RME\_CUSTOM for the *method* parameter of [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).</span></span> <span data-ttu-id="0b1ca-125">在此情況下，除非該寫入器的自訂還原檔另有指示，否則這個寫入器不應該參與還原程式。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-125">In this case, this writer should not be involved in the restore process unless the custom-restore documentation for that writer indicates otherwise.</span></span>

<span data-ttu-id="0b1ca-126">要求者牽涉到還原程式中的寫入器，方法是在呼叫 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)時指定其中一個寫入器的元件。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-126">A requester involves a writer in the restore process by specifying one of that writer's components in a call to [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).</span></span> <span data-ttu-id="0b1ca-127">在 **>ivssbackupcomponents：： SetSelectedForRestore** 的呼叫中不指定任何該寫入器的元件時，可以還原寫入器的資料而不涉及寫入器。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-127">A writer's data can be restored without involving the writer by simply not specifying any of that writer's components in a call to **IVssBackupComponents::SetSelectedForRestore**.</span></span> <span data-ttu-id="0b1ca-128">如果寫入器不預期有任何還原事件，則在還原程式中牽涉到該寫入器可能會造成該寫入器回報的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0b1ca-128">If a writer does not expect any restore events, involving that writer in the restore process can cause spurious errors to be reported for that writer.</span></span>

 

 



