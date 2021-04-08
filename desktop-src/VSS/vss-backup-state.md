---
description: 在備份作業期間，要求者會使用 >ivssbackupcomponents：： SetBackupState 來定義進行中的作業類型。
ms.assetid: 43dcdac7-ed8e-4150-83eb-585e0e92f13c
title: VSS 備份狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aa9250139aee9f48f9880fd4a657fa7c6c4991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690460"
---
# <a name="vss-backup-state"></a><span data-ttu-id="b216f-103">VSS 備份狀態</span><span class="sxs-lookup"><span data-stu-id="b216f-103">VSS Backup State</span></span>

<span data-ttu-id="b216f-104">在備份作業期間，要求者會使用 [**>ivssbackupcomponents：： SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) 來定義進行中的作業類型。</span><span class="sxs-lookup"><span data-stu-id="b216f-104">During a backup operation, the requester uses [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) to define the type of operation in progress.</span></span>

<span data-ttu-id="b216f-105">這項資訊不包含在備份元件檔中可輕易取出的表單中，因此，要求者開發人員應該在任何備份媒體上獨立儲存此資訊。</span><span class="sxs-lookup"><span data-stu-id="b216f-105">This information is not included in an easily retrievable form in the Backup Components Document, so requester developers should store this information independently on any backup media.</span></span>

<span data-ttu-id="b216f-106">備份狀態包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="b216f-106">The backup state contains the following:</span></span>

<dl> <dt>

<span data-ttu-id="b216f-107"><span id="Backup_Type"></span><span id="backup_type"></span><span id="BACKUP_TYPE"></span>備份類型</span><span class="sxs-lookup"><span data-stu-id="b216f-107"><span id="Backup_Type"></span><span id="backup_type"></span><span id="BACKUP_TYPE"></span>Backup Type</span></span>
</dt> <dd>

<span data-ttu-id="b216f-108">備份類型會指定用來識別要備份之檔案的準則。</span><span class="sxs-lookup"><span data-stu-id="b216f-108">The backup type specifies criteria for identifying files to be backed up.</span></span> <span data-ttu-id="b216f-109">這些準則的評估必須使用 VSS API 來進行。</span><span class="sxs-lookup"><span data-stu-id="b216f-109">The evaluation of these criteria must be made using the VSS API.</span></span>

<span data-ttu-id="b216f-110">當您決定要採用的備份類型，以及要使用哪個寫入器時，要求者應該檢查 (或架構的種類，請參閱 [寫入器備份架構支援](writer-backup-schema-support.md)) 每個系統寫入器支援的備份作業。</span><span class="sxs-lookup"><span data-stu-id="b216f-110">When deciding on the type of backup to pursue and which writers to work with, requesters should examine the kinds (or schemas—see [Writer Backup Schema Support](writer-backup-schema-support.md)) of backup operations that each of the system's writers supports.</span></span> <span data-ttu-id="b216f-111">VSS 下的備份可以是下列類型：</span><span class="sxs-lookup"><span data-stu-id="b216f-111">Backups under VSS can be the following types:</span></span>

-   <span data-ttu-id="b216f-112">Full (VSS \_ BT \_ full) —無論上次備份日期為何，都會備份檔案。</span><span class="sxs-lookup"><span data-stu-id="b216f-112">Full (VSS\_BT\_FULL)—files will be backed up regardless of their last backup date.</span></span> <span data-ttu-id="b216f-113">將會更新每個檔案的備份歷程記錄，而這種類型的備份可作為增量或差異備份的基礎使用。</span><span class="sxs-lookup"><span data-stu-id="b216f-113">The backup history of each file will be updated, and this type of backup can be used as the basis of an incremental or differential backup.</span></span> <span data-ttu-id="b216f-114">還原完整備份只需要單一備份映射。</span><span class="sxs-lookup"><span data-stu-id="b216f-114">Restoring a full backup requires only a single backup image.</span></span>
-   <span data-ttu-id="b216f-115">複本備份 (VSS \_ bt \_ 複製) （例如 vss \_ bt \_ 完整備份類型），不論其上次備份日期為何，都會備份檔案。</span><span class="sxs-lookup"><span data-stu-id="b216f-115">Copy Backup (VSS\_BT\_COPY)—like the VSS\_BT\_FULL backup type, files will be backed up regardless of their last backup date.</span></span> <span data-ttu-id="b216f-116">不過，每個檔案的備份歷程記錄將不會更新，而且這類備份無法當做增量或差異備份的基礎。</span><span class="sxs-lookup"><span data-stu-id="b216f-116">However, the backup history of each file will not be updated, and this sort of backup cannot be used as the basis of an incremental or differential backup.</span></span>
-   <span data-ttu-id="b216f-117">增量 (VSS \_ BT \_ 增量) -vss API 是用來確保只有在上一次完整或增量備份之後已變更或新增的檔案才會複製到儲存媒體。</span><span class="sxs-lookup"><span data-stu-id="b216f-117">Incremental (VSS\_BT\_INCREMENTAL)—the VSS API is used to ensure that only files that have been changed or added since the last full or incremental backup are to be copied to a storage medium.</span></span> <span data-ttu-id="b216f-118">還原增量備份需要原始備份映射，以及自初始備份之後所做的所有增量備份映射。</span><span class="sxs-lookup"><span data-stu-id="b216f-118">Restoring an incremental backup requires the original backup image and all incremental backup images made since the initial backup.</span></span>
-   <span data-ttu-id="b216f-119">差異 (VSS \_ BT \_ 差異) -vss API 是用來確保只有在上一次完整備份之後變更或新增的檔案會複製到儲存媒體; 所有的中繼備份資訊都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="b216f-119">Differential (VSS\_BT\_DIFFERENTIAL)—the VSS API is used to ensure that only files that have been changed or added since the last full backup are to be copied to a storage media; all intermediate backup information is ignored.</span></span> <span data-ttu-id="b216f-120">還原差異備份需要原始備份映射，以及自上次完整備份之後所做的最新差異備份映射。</span><span class="sxs-lookup"><span data-stu-id="b216f-120">Restoring a differential backup requires the original backup image and the most recent differential backup image made since the last full backup.</span></span>
-   <span data-ttu-id="b216f-121">記錄檔 (VSS \_ BT \_ 記錄檔) -只有寫入器的記錄檔 (以 [**IVssCreateWriterMetadata：： AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) 方法新增至元件的記錄檔，並藉由呼叫 [**IVssWMComponent：： GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)) 進行取出。</span><span class="sxs-lookup"><span data-stu-id="b216f-121">Log File (VSS\_BT\_LOG)—only a writer's log files (files added to a component with the [**IVssCreateWriterMetadata::AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) method, and retrieved by a call to [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)) will be backed up.</span></span> <span data-ttu-id="b216f-122">這是 VSS 專用的備份類型。</span><span class="sxs-lookup"><span data-stu-id="b216f-122">This backup type is specific to VSS.</span></span>

<span data-ttu-id="b216f-123">要求者可以使用 VSS 以外的資訊和方法來執行這些備份。</span><span class="sxs-lookup"><span data-stu-id="b216f-123">It is possible for requesters to implement these backups using information and methods outside of VSS.</span></span> <span data-ttu-id="b216f-124">只有當要求者使用 VSS API 來執行備份時，才應該將其視為具有其中一個列出的備份類型。</span><span class="sxs-lookup"><span data-stu-id="b216f-124">Only when a requester implements a backup using the VSS API should it be said to have one of the listed backup types.</span></span> <span data-ttu-id="b216f-125">比方說， \_ \_ 只有當要求者使用 [**IVssWMComponent：： GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) 所傳回的資訊來識別記錄檔時，才會參與 VSS BT 記錄類型的備份。</span><span class="sxs-lookup"><span data-stu-id="b216f-125">For instance, a requester participates in a VSS\_BT\_LOG type of backup only if it used the information returned by [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) to identify log files.</span></span> <span data-ttu-id="b216f-126">同樣地，VSS \_ bt \_ 增量和 vss \_ bt \_ 差異類型只適用于增量或差異作業，如 [增量和差異備份](incremental-and-differential-backups.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="b216f-126">Similarly, the VSS\_BT\_INCREMENTAL and VSS\_BT\_DIFFERENTIAL types apply only to incremental or differential operations, as described in [Incremental and Differential Backups](incremental-and-differential-backups.md).</span></span>

</dd> <dt>

<span data-ttu-id="b216f-127"><span id="Specification_about_Selectability"></span><span id="specification_about_selectability"></span><span id="SPECIFICATION_ABOUT_SELECTABILITY"></span>Selectability 的規格</span><span class="sxs-lookup"><span data-stu-id="b216f-127"><span id="Specification_about_Selectability"></span><span id="specification_about_selectability"></span><span id="SPECIFICATION_ABOUT_SELECTABILITY"></span>Specification about Selectability</span></span>
</dt> <dd>

<span data-ttu-id="b216f-128">VSS 備份可能會選擇使用元件 selectability 的 VSS 概念（這稱為「 [*元件模式*](vssgloss-c.md)」），或忽略它們。</span><span class="sxs-lookup"><span data-stu-id="b216f-128">A VSS backup may choose to respect VSS notions of component selectability—this is referred to as running in [*component mode*](vssgloss-c.md)—or to ignore them.</span></span>

<span data-ttu-id="b216f-129">未在元件模式中執行的範例將會執行系統映射備份，其中備份應用程式需要寫入合作以確保資料穩定性，但在這種情況下，不會有相關的元件選取。</span><span class="sxs-lookup"><span data-stu-id="b216f-129">An example of not running in component mode would be performing a system image backup, where the backup application would need writer cooperation to ensure data stability but where selection of components would be irrelevant.</span></span>

</dd> <dt>

<span data-ttu-id="b216f-130"><span id="Saving_Bootable_State"></span><span id="saving_bootable_state"></span><span id="SAVING_BOOTABLE_STATE"></span>正在儲存可開機狀態</span><span class="sxs-lookup"><span data-stu-id="b216f-130"><span id="Saving_Bootable_State"></span><span id="saving_bootable_state"></span><span id="SAVING_BOOTABLE_STATE"></span>Saving Bootable State</span></span>
</dt> <dd>

<span data-ttu-id="b216f-131">VSS 支援在完全可開機的設定中儲存正在執行的系統狀態。</span><span class="sxs-lookup"><span data-stu-id="b216f-131">VSS supports saving the running system state in a fully bootable configuration.</span></span> <span data-ttu-id="b216f-132">不過，這不一定是必要的，而寫入器準備儲存可開機狀態有時可能會降低執行中系統的即時效能。</span><span class="sxs-lookup"><span data-stu-id="b216f-132">However, this is not always necessary, and writer preparation to save a bootable state can sometimes degrade real-time performance of a running system.</span></span>

<span data-ttu-id="b216f-133">因此，要求者會指出備份是否包含可開機的系統狀態，作為 [**>ivssbackupcomponents：： SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)的引數。</span><span class="sxs-lookup"><span data-stu-id="b216f-133">Therefore, requesters indicate whether a backup will include a bootable system state as an argument to [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).</span></span> <span data-ttu-id="b216f-134">寫入器會藉由呼叫 [**CVssWriter：： IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)來判斷是否必須支援儲存可開機的系統狀態。</span><span class="sxs-lookup"><span data-stu-id="b216f-134">Writers determine whether they have to support saving the bootable system state by calling [**CVssWriter::IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup).</span></span>

<span data-ttu-id="b216f-135">即使未選取 [可開機的系統狀態]，也會建立系統檔案的陰影複製，而且可能會備份檔案案。</span><span class="sxs-lookup"><span data-stu-id="b216f-135">Even if bootable system state is not selected, shadow copies of the system files will be made and the files may be backed up.</span></span>

<span data-ttu-id="b216f-136">但是，如果備份未儲存可開機的系統狀態，請務必小心還原系統檔案 (請參閱 [備份及還原 Windows server 2003 R2 和 Windows server 2003 SP1 中的系統狀態](backing-up-and-restoring-system-state-under-vss.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b216f-136">However, great care should be exercised in restoring system files if the backup did not save the bootable system state (see [Backing Up and Restoring System State in Windows Server 2003 R2 and Windows Server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)).</span></span>

<span data-ttu-id="b216f-137">您無法從已抓取的備份元件檔中復原這項資訊，因此要求者作者應儲存系統是否以可開機的系統狀態備份。</span><span class="sxs-lookup"><span data-stu-id="b216f-137">It is not possible to recover this information from a retrieved Backup Components Document, so requester authors should store whether the system was backed up with a bootable system state or not.</span></span>

</dd> <dt>

<span data-ttu-id="b216f-138"><span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>部分檔案支援</span><span class="sxs-lookup"><span data-stu-id="b216f-138"><span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Partial File Support</span></span>
</dt> <dd>

<span data-ttu-id="b216f-139">有些寫入器支援透過覆寫所管理之檔案的部分來還原檔。</span><span class="sxs-lookup"><span data-stu-id="b216f-139">Some writers support file restoration through the overwriting of parts of the files they manage.</span></span> <span data-ttu-id="b216f-140">要求者可以設計來利用這種方式，如果是，則會藉由設定 [**>ivssbackupcomponents：： SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)中的資訊來指出這一點。</span><span class="sxs-lookup"><span data-stu-id="b216f-140">A requester may be designed to take advantage of this, and if so it indicates this by setting the information in [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).</span></span>

</dd> </dl>

 

 



