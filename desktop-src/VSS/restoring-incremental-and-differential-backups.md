---
description: 還原 VSS 下的增量或差異備份，與任何其他 VSS 還原作業並無太大差異。
ms.assetid: 67143f6f-0bb8-4740-9289-8bbfeb7caadf
title: 還原增量和差異備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 639919ea24f12fbc036116bd89b1630321cbae54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513129"
---
# <a name="restoring-incremental-and-differential-backups"></a><span data-ttu-id="703b7-103">還原增量和差異備份</span><span class="sxs-lookup"><span data-stu-id="703b7-103">Restoring Incremental and Differential Backups</span></span>

<span data-ttu-id="703b7-104">還原 VSS 下的增量或差異備份，與任何其他 VSS 還原作業並無太大差異。</span><span class="sxs-lookup"><span data-stu-id="703b7-104">Restoring an incremental or differential backup under VSS is not significantly different from any other VSS restore operation.</span></span>

<span data-ttu-id="703b7-105">寫入器可以修改還原目標或要求導向目標，要求者必須處理替代位置對應和新目標，就像任何其他還原一樣。</span><span class="sxs-lookup"><span data-stu-id="703b7-105">A writer can modify restore targets or request directed targeting, and a requester must handle alternate location mappings and new targets, just as with any other restore.</span></span> <span data-ttu-id="703b7-106">不過，在處理增量或差異備份的還原時，有兩個重要的問題要注意：額外的還原和備份戳記。</span><span class="sxs-lookup"><span data-stu-id="703b7-106">There are, however, two significant issues to be aware of in handling the restore of an incremental or differential backup: additional restores and backup stamps.</span></span>

## <a name="additional-restores"></a><span data-ttu-id="703b7-107">額外的還原</span><span class="sxs-lookup"><span data-stu-id="703b7-107">Additional Restores</span></span>

<span data-ttu-id="703b7-108">第一個問題是額外的還原。</span><span class="sxs-lookup"><span data-stu-id="703b7-108">The first issue is that of additional restores.</span></span> <span data-ttu-id="703b7-109">備份操作員可能需要使用初始完整和後續增量或差異備份媒體作為來源，來執行數個還原作業。</span><span class="sxs-lookup"><span data-stu-id="703b7-109">A backup operator may need to run several restore operations using an initial full and subsequent incremental or differential backup media as a source.</span></span>

<span data-ttu-id="703b7-110">有些寫入器通常是使用 [**CVssWriter：： OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)處理 [*PostRestore*](vssgloss-p.md)事件的一部分，使用已還原的檔案來執行目前在磁片上的資料更新。</span><span class="sxs-lookup"><span data-stu-id="703b7-110">Some writers, typically as part of their handling of a [*PostRestore*](vssgloss-p.md) event using [**CVssWriter::OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), use restored files to perform updates of data currently on disk.</span></span> <span data-ttu-id="703b7-111">對於這些寫入器的某些寫入器效率很低（或危險），以重複更新還原檔案中的磁片資料。</span><span class="sxs-lookup"><span data-stu-id="703b7-111">For some of these writers it is inefficient—or dangerous—to repeatedly update on-disk data from restored files.</span></span>

<span data-ttu-id="703b7-112">因此，備份應用程式必須藉由呼叫 [**>ivssbackupcomponents：： SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores)來指出元件或元件的設定何時可能需要後續還原。</span><span class="sxs-lookup"><span data-stu-id="703b7-112">Therefore, it is important that backup applications indicate when a component or component set may require subsequent restores by calling [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores).</span></span>

<span data-ttu-id="703b7-113">寫入器會呼叫 [**>ivsscomponent：： GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) ，以判斷備份操作員是否計畫對元件或元件集進行更多的還原。</span><span class="sxs-lookup"><span data-stu-id="703b7-113">A writer would call [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) to determine whether the backup operator planned more restores of the component or component set.</span></span>

<span data-ttu-id="703b7-114">如果要求者未呼叫 [**>ivssbackupcomponents：： SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores)，則 [**>ivsscomponent：： GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) 會傳回 false，而寫入器可以執行所需的任何還原後處理。</span><span class="sxs-lookup"><span data-stu-id="703b7-114">If the requester had not called [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores), then [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) returns false, and the writer can perform any post-restore processing it needs to.</span></span>

<span data-ttu-id="703b7-115">如果已呼叫 [**>ivssbackupcomponents：： SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) ， [**>ivsscomponent：： GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) 會傳回 **true**，而寫入器應該決定如何處理還原後的作業，例如，寫入器可能會選擇不更新其在磁片上的資料。</span><span class="sxs-lookup"><span data-stu-id="703b7-115">If [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) had been called, then [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) returns **true**, and a writer should decide how to handle post-restore operations—for instance, the writer may choose not to update its on-disk data.</span></span>

## <a name="backup-stamps"></a><span data-ttu-id="703b7-116">備份戳記</span><span class="sxs-lookup"><span data-stu-id="703b7-116">Backup Stamps</span></span>

<span data-ttu-id="703b7-117">在上一次完整備份操作的過程中，寫入器可能已在要求者的備份元件檔中儲存備份戳記。</span><span class="sxs-lookup"><span data-stu-id="703b7-117">As part of the previous full backup operation, a writer may have stored a backup stamp in the requester's Backup Components Document.</span></span>

<span data-ttu-id="703b7-118">備份戳記會儲存為字串，且其格式和資訊不會智慧型給要求者。</span><span class="sxs-lookup"><span data-stu-id="703b7-118">The backup stamp is stored as a string, and its format and information are not intelligible to the requester.</span></span> <span data-ttu-id="703b7-119">因此，要求者無法直接使用備份戳記資訊。</span><span class="sxs-lookup"><span data-stu-id="703b7-119">Therefore, the requester cannot make direct use of the backup stamp information.</span></span>

<span data-ttu-id="703b7-120">相反地，其工作是在產生增量備份的 [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)事件之前，先呼叫 [**>ivssbackupcomponents：： SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)方法，以將該資訊提供給寫入器。</span><span class="sxs-lookup"><span data-stu-id="703b7-120">Instead, its task is to make that information available to the writer, by calling the [**IVssBackupComponents::SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) method prior to the generation of a [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) event for an incremental backup.</span></span>

<span data-ttu-id="703b7-121">要求者會以元件為基礎來執行此操作。</span><span class="sxs-lookup"><span data-stu-id="703b7-121">The requester does this on a component-by-component basis.</span></span> <span data-ttu-id="703b7-122">要求者會使用 [**>ivsscomponent：： GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)檢查預存元件或元件集的備份戳記資訊。</span><span class="sxs-lookup"><span data-stu-id="703b7-122">A requester examines stored component or component set backup stamp information using [**IVssComponent::GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp).</span></span>

<span data-ttu-id="703b7-123">如果備份戳記資訊適用于正在進行的還原類型，則會使用 [**>ivssbackupcomponents：： SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) 方法，讓它成為元件最後一次備份的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="703b7-123">If backup stamp information is appropriate to the type of restore the requester is undertaking, it makes it available as the time stamp of the last backup of a component with the [**IVssBackupComponents::SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) method.</span></span>

<span data-ttu-id="703b7-124">寫入器會使用 [**>ivsscomponent：： GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)來復原備份戳記資訊。</span><span class="sxs-lookup"><span data-stu-id="703b7-124">A writer recovers the backup stamp information using [**IVssComponent::GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp).</span></span> <span data-ttu-id="703b7-125">此類別的寫入器產生了初始備份戳記，因此寫入器能夠將此戳記解碼並使用資訊。</span><span class="sxs-lookup"><span data-stu-id="703b7-125">A writer of this class generated the initial backup stamp, so the writer is able to decode this stamp and use the information.</span></span> <span data-ttu-id="703b7-126">根據這一點，在處理 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) 事件時，寫入器可以選擇採取動作，例如變更還原目標或要求導向目標。</span><span class="sxs-lookup"><span data-stu-id="703b7-126">Based on this, while handling a [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) event, a writer may choose to take actions such as changing restore targets or requesting directed targeting.</span></span>

 

 



