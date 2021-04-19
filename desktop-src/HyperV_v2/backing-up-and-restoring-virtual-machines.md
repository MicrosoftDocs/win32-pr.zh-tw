---
description: Hyper-v 使用磁碟區陰影複製服務 (VSS) 來備份和還原虛擬機器。
ms.assetid: 94C67F22-658D-49DD-9588-6BB4FCF7ADA9
title: 備份和還原虛擬機器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9cf6d5b80a4c7392fb38e893a4fafad3f90435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985454"
---
# <a name="backing-up-and-restoring-virtual-machines"></a><span data-ttu-id="bd4df-103">備份和還原虛擬機器</span><span class="sxs-lookup"><span data-stu-id="bd4df-103">Backing up and restoring virtual machines</span></span>

<span data-ttu-id="bd4df-104">Hyper-v 使用磁碟區陰影複製服務 (VSS) 來備份和還原虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bd4df-104">Hyper-V uses the Volume Shadow Copy Service (VSS) to backup and restore virtual machines.</span></span> <span data-ttu-id="bd4df-105">如果在客體作業系統中安裝備份 (磁片區快照集) 整合服務，則會安裝 VSS 要求者，讓客體作業系統中的 VSS 寫入器參與虛擬機器的備份。</span><span class="sxs-lookup"><span data-stu-id="bd4df-105">If the backup (volume snapshot) integration services are installed in the guest operating system, a VSS requester is installed that will allow VSS writers in the guest operating system to participate in the backup of the virtual machine.</span></span> <span data-ttu-id="bd4df-106">如需詳細資訊，請參閱下列各節：</span><span class="sxs-lookup"><span data-stu-id="bd4df-106">For details, see the following sections:</span></span>

-   [<span data-ttu-id="bd4df-107">備份虛擬機器</span><span class="sxs-lookup"><span data-stu-id="bd4df-107">Backing up the virtual machines</span></span>](#backing-up-the-virtual-machines)
-   [<span data-ttu-id="bd4df-108">還原虛擬機器</span><span class="sxs-lookup"><span data-stu-id="bd4df-108">Restoring the virtual machines</span></span>](#restoring-the-virtual-machines)
-   [<span data-ttu-id="bd4df-109">容錯移轉叢集與 Hyper-v VSS</span><span class="sxs-lookup"><span data-stu-id="bd4df-109">Failover clustering and Hyper-V VSS</span></span>](#failover-clustering-and-hyper-v-vss)
-   [<span data-ttu-id="bd4df-110">Hyper-v VSS 寫入器的詳細資料</span><span class="sxs-lookup"><span data-stu-id="bd4df-110">Details on the Hyper-V VSS Writer</span></span>](#details-on-the-hyper-v-vss-writer)
-   [<span data-ttu-id="bd4df-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd4df-111">Related topics</span></span>](#related-topics)

## <a name="backing-up-the-virtual-machines"></a><span data-ttu-id="bd4df-112">備份虛擬機器</span><span class="sxs-lookup"><span data-stu-id="bd4df-112">Backing up the virtual machines</span></span>

<span data-ttu-id="bd4df-113">Hyper-v 使用兩種機制的其中一種來備份每部虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bd4df-113">Hyper-V uses one of two mechanisms to back up each virtual machine.</span></span> <span data-ttu-id="bd4df-114">預設的備份機制稱為「儲存狀態」方法，在此方法中，虛擬機器在處理 PrepareForSnapshot 事件期間會處於儲存狀態，快照集會採用適當的磁片區，而虛擬機器則會在處理 PostSnapshot 事件期間回到先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="bd4df-114">The default backup mechanism is called the "Saved State" method, where the virtual machine is put into a saved state during the processing of the PrepareForSnapshot event, snapshots are taken of the appropriate volumes, and the virtual machine is returned to the previous state during the processing of the PostSnapshot event.</span></span>

<span data-ttu-id="bd4df-115">另一項備份機制稱為「子 VM 快照」方法，它會使用子虛擬機器內的 VSS 來參與備份。</span><span class="sxs-lookup"><span data-stu-id="bd4df-115">The other backup mechanism is called the "Child VM Snapshot" method, which uses VSS inside the child virtual machine to participate in the backup.</span></span> <span data-ttu-id="bd4df-116">若要支援「子 VM 快照集」方法，必須符合下列所有條件：</span><span class="sxs-lookup"><span data-stu-id="bd4df-116">For the "Child VM Snapshot" method to be supported, all of the following conditions must be met:</span></span>

-   <span data-ttu-id="bd4df-117">備份 (磁片區快照集) 整合服務已安裝且正在子虛擬機器中執行。</span><span class="sxs-lookup"><span data-stu-id="bd4df-117">Backup (volume snapshot) Integration Service is installed and running in the child virtual machine.</span></span> <span data-ttu-id="bd4df-118">服務名稱是「Hyper-v 磁片區陰影複製要求者」。</span><span class="sxs-lookup"><span data-stu-id="bd4df-118">The service name is "Hyper-V Volume Shadow Copy Requestor".</span></span>
-   <span data-ttu-id="bd4df-119">子虛擬機器必須處於執行中狀態。</span><span class="sxs-lookup"><span data-stu-id="bd4df-119">The child virtual machine must be in the running state.</span></span>
-   <span data-ttu-id="bd4df-120">虛擬機器的快照集檔案位置會設定為主機作業系統中的相同磁片區，作為虛擬機器的 VHD 檔案。</span><span class="sxs-lookup"><span data-stu-id="bd4df-120">The Snapshot File Location for the virtual machine is set to be the same volume in the host operating system as the VHD files for the virtual machine.</span></span>
-   <span data-ttu-id="bd4df-121">子虛擬機器上的所有磁片區都是基本磁碟，而且沒有動態磁碟。</span><span class="sxs-lookup"><span data-stu-id="bd4df-121">All volumes on the child virtual machine are basic disks and there are no dynamic disks.</span></span>
-   <span data-ttu-id="bd4df-122">子虛擬機器上的所有磁片都必須使用支援快照集的檔案系統 (例如，NTFS) 。</span><span class="sxs-lookup"><span data-stu-id="bd4df-122">All disks on the child virtual machine must use a file system that supports snapshots (for example, NTFS).</span></span>

<span data-ttu-id="bd4df-123">一般而言，備份虛擬機器的程式與在 [VSS 下處理備份的總覽](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)中所述的步驟相同。</span><span class="sxs-lookup"><span data-stu-id="bd4df-123">In general, the process for backing up virtual machines is the same as described in [Overview of Processing a Backup Under VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss).</span></span> <span data-ttu-id="bd4df-124">當 Hyper-v VSS 寫入器 (「Hyper-v 虛擬機器管理」服務的一部分) 處理 PrepareForSnapshot 事件時，就會發生獨特的行為。</span><span class="sxs-lookup"><span data-stu-id="bd4df-124">The unique behavior happens when the Hyper-V VSS writer (part of the "Hyper-V Virtual Machine Management" service) processes the PrepareForSnapshot event.</span></span> <span data-ttu-id="bd4df-125">如果備份是使用「子 VM 快照集」方法完成的，則會進行額外的處理，但是子虛擬機器看不到它。</span><span class="sxs-lookup"><span data-stu-id="bd4df-125">If the backup was done using the "Child VM Snapshot" method, there is additional processing done but it is not visible to the child virtual machine.</span></span>

<span data-ttu-id="bd4df-126">下列程式說明如何備份虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bd4df-126">The following procedure describes how to back up virtual machines.</span></span>

<span data-ttu-id="bd4df-127">**備份虛擬機器**</span><span class="sxs-lookup"><span data-stu-id="bd4df-127">**To back up virtual machines**</span></span>

1.  <span data-ttu-id="bd4df-128">針對寫入器中繼資料中的每個虛擬機器，如果使用「儲存狀態」方法，虛擬機器會進入儲存狀態。</span><span class="sxs-lookup"><span data-stu-id="bd4df-128">For each virtual machine in the writer metadata, if the "Saved State" method is used, the virtual machine is put into a saved state.</span></span> <span data-ttu-id="bd4df-129">針對使用「子 VM 快照」方法的虛擬機器，子虛擬機器中的 Hyper-v 磁片區陰影複製要求者服務會依照在 [VSS 下處理備份](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)的詳細說明，來處理備份。</span><span class="sxs-lookup"><span data-stu-id="bd4df-129">For virtual machines using the "Child VM Snapshot" method, the Hyper-V Volume Shadow Copy Requestor Service in the child virtual machine processes the backup as detailed in [Overview of Processing a Backup Under VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss).</span></span> <span data-ttu-id="bd4df-130">子虛擬機器上的所有 VSS 事件都是在 PrepareForSnapshot 事件的主機作業系統處理期間發生。</span><span class="sxs-lookup"><span data-stu-id="bd4df-130">All VSS events on the child virtual machine occur during the host operating system processing of the PrepareForSnapshot event.</span></span>
2.  <span data-ttu-id="bd4df-131">當所有虛擬機器都處於已儲存狀態或建立快照集之後，Hyper-v VSS 寫入器會從 PrepareForSnapshot 事件中返回。</span><span class="sxs-lookup"><span data-stu-id="bd4df-131">After all virtual machines have either been put in the saved state or had snapshots taken, the Hyper-V VSS writer returns from the PrepareForSnapshot event.</span></span> <span data-ttu-id="bd4df-132">在凍結和解除凍結事件期間，Hyper-v VSS 寫入器不會進行任何處理。</span><span class="sxs-lookup"><span data-stu-id="bd4df-132">No processing is done by the Hyper-V VSS writer during the Freeze and Thaw events.</span></span>
3.  <span data-ttu-id="bd4df-133">當 Hyper-v VSS 寫入器處理 PostSnapshot 事件時，使用「儲存狀態」方法備份並由 Hyper-v VSS 寫入器進入儲存狀態的虛擬機器，將會回到備份開始之前的狀態。</span><span class="sxs-lookup"><span data-stu-id="bd4df-133">When the Hyper-V VSS writer processes the PostSnapshot event, virtual machines that were backed up using the "Saved State" method and were put into a saved state by the Hyper-V VSS writer are returned to the state they were in before the backup started.</span></span> <span data-ttu-id="bd4df-134">針對使用「子 VM 快照集」方法進行備份的虛擬機器，會將拍攝快照集的 VHD 檔案的主機映射回復至處理 PrepareForSnapshot 事件期間所建立的快照集。</span><span class="sxs-lookup"><span data-stu-id="bd4df-134">For the virtual machines that were backed up using the "Child VM Snapshot" method, the host image of the VHD files that had the snapshots taken are rolled back to the snapshot taken during the processing of the PrepareForSnapshot event.</span></span> <span data-ttu-id="bd4df-135">這項處理會獨立于子虛擬機器上的 VSS 寫入器完成，因此所建立的快照集必須是可自動復原的。</span><span class="sxs-lookup"><span data-stu-id="bd4df-135">This processing is done independently of the VSS writers on the child virtual machines so the snapshots taken must be auto-recoverable.</span></span> <span data-ttu-id="bd4df-136"> (**VSS \_ VOLSNAP \_ ATTR \_ \_** 未在內容中設定自動復原。 ) </span><span class="sxs-lookup"><span data-stu-id="bd4df-136">(**VSS\_VOLSNAP\_ATTR\_NO\_AUTORECOVERY** is not set in the context.)</span></span>

<span data-ttu-id="bd4df-137">不支援部份備份。</span><span class="sxs-lookup"><span data-stu-id="bd4df-137">Partial backups are not supported.</span></span> <span data-ttu-id="bd4df-138">如果有任何虛擬機器無法建立快照集，將不會備份任何虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bd4df-138">If any virtual machine fails to create a snapshot, no virtual machines will be backed up.</span></span>

> [!Note]  
> <span data-ttu-id="bd4df-139">主機作業系統看不到傳遞和 iSCSI 磁片，因此 Hyper-v VSS 寫入器不會加以備份。</span><span class="sxs-lookup"><span data-stu-id="bd4df-139">Pass-through and iSCSI disks are not visible to the host operating system and therefore not backed up by the Hyper-V VSS writer.</span></span> <span data-ttu-id="bd4df-140">您必須在虛擬機器上完全完成這些磁片區的備份。</span><span class="sxs-lookup"><span data-stu-id="bd4df-140">Backups of these volumes must be done entirely on the virtual machine.</span></span>

 

## <a name="restoring-the-virtual-machines"></a><span data-ttu-id="bd4df-141">還原虛擬機器</span><span class="sxs-lookup"><span data-stu-id="bd4df-141">Restoring the virtual machines</span></span>

<span data-ttu-id="bd4df-142">還原虛擬機器是由主機作業系統完全完成;子虛擬機器上的 VSS 寫入器不包含在其中。</span><span class="sxs-lookup"><span data-stu-id="bd4df-142">Restoring the virtual machines is done entirely by the host operating system; the VSS writers on the child virtual machines are not involved.</span></span>

<span data-ttu-id="bd4df-143">下列程式說明如何還原虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bd4df-143">The following procedure describes how to restore virtual machines.</span></span>

<span data-ttu-id="bd4df-144">**還原虛擬機器**</span><span class="sxs-lookup"><span data-stu-id="bd4df-144">**To restore virtual machines**</span></span>

1.  <span data-ttu-id="bd4df-145">在處理 PreRestore 事件期間，Hyper-v VSS 寫入器會關閉，並刪除即將還原的任何虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bd4df-145">During the processing of the PreRestore event, the Hyper-V VSS writer turns off and deletes any virtual machines that are about to be restored.</span></span>
2.  <span data-ttu-id="bd4df-146">在所有 VSS 寫入器都處理 PreRestore 事件之後，就會還原檔案。</span><span class="sxs-lookup"><span data-stu-id="bd4df-146">After all VSS writers have processed the PreRestore event, the files are restored.</span></span>
3.  <span data-ttu-id="bd4df-147">在處理 PostRestore 事件期間，Hyper-v VSS 寫入器會呼叫 [**>ivsscomponent：： GetFileRestoreStatus**](/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getfilerestorestatus) 方法。</span><span class="sxs-lookup"><span data-stu-id="bd4df-147">During the processing of the PostRestore event, the Hyper-V VSS writer calls the [**IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getfilerestorestatus) method.</span></span> <span data-ttu-id="bd4df-148">如果傳回不是 **VSS \_ RS \_ ALL**，則 hyper-v VSS 寫入器會呼叫 [**SetWriterFailure**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure)方法，並從 [**OnPostRestore**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore)方法傳回 **False** 。</span><span class="sxs-lookup"><span data-stu-id="bd4df-148">If the return is not **VSS\_RS\_ALL**, then the Hyper-V VSS writer calls the [**SetWriterFailure**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure) method and returns **False** from the [**OnPostRestore**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore) method.</span></span>
4.  <span data-ttu-id="bd4df-149">針對每個已還原的虛擬機器，Hyper-v VSS 寫入器會向 Hyper-v 管理服務註冊虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bd4df-149">For each virtual machine that was restored, the Hyper-V VSS writer registers the virtual machine with the Hyper-V management service.</span></span> <span data-ttu-id="bd4df-150">如果虛擬機器還原至非預設位置，則會在連結至該位置的預設位置中建立符號連結。</span><span class="sxs-lookup"><span data-stu-id="bd4df-150">If the virtual machine is restored to a nondefault location, a symbolic link is created in the default location linking to that location.</span></span>
5.  <span data-ttu-id="bd4df-151">針對每個已還原的 VHD，此位置會與針對該虛擬機器指定的位置進行比較。</span><span class="sxs-lookup"><span data-stu-id="bd4df-151">For each VHD that was restored, the location is compared with the one specified for that virtual machine.</span></span> <span data-ttu-id="bd4df-152">如果位置不同，則會使用適當的位置來更新設定。</span><span class="sxs-lookup"><span data-stu-id="bd4df-152">If the location is different, then the configuration is updated with the proper location.</span></span>
6.  <span data-ttu-id="bd4df-153">網路設定已更新。</span><span class="sxs-lookup"><span data-stu-id="bd4df-153">The network configuration is updated.</span></span> <span data-ttu-id="bd4df-154">如果虛擬機器在備份時連接的虛擬交換器仍結束，則會建立新的埠並連接至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bd4df-154">If the virtual switches that the virtual machine was connected to when it was backed up still exit, new ports are created and connected to the virtual machine.</span></span>

## <a name="failover-clustering-and-hyper-v-vss"></a><span data-ttu-id="bd4df-155">容錯移轉叢集與 Hyper-v VSS</span><span class="sxs-lookup"><span data-stu-id="bd4df-155">Failover clustering and Hyper-V VSS</span></span>

<span data-ttu-id="bd4df-156">Hyper-v VSS 寫入器不會針對屬於容錯移轉叢集一部分的虛擬機器提供任何考慮。</span><span class="sxs-lookup"><span data-stu-id="bd4df-156">The Hyper-V VSS writer does not give any consideration to virtual machines that are part of a failover cluster.</span></span> <span data-ttu-id="bd4df-157">在「儲存狀態」方法備份和所有還原期間，虛擬機器會進入儲存狀態或完全刪除。</span><span class="sxs-lookup"><span data-stu-id="bd4df-157">During both the "Saved State" method backups and all restores, the virtual machine would be put into the saved state or deleted entirely.</span></span> <span data-ttu-id="bd4df-158">叢集服務會看到此錯誤，並導致這些節點上的應用程式容錯移轉至其他節點。</span><span class="sxs-lookup"><span data-stu-id="bd4df-158">This would be seen as a failure by the clustering service and cause the applications on those nodes to be failed over to other nodes.</span></span> <span data-ttu-id="bd4df-159">若要在「儲存狀態」備份期間避免此情況，必須使用叢集服務來儲存虛擬機器狀態。</span><span class="sxs-lookup"><span data-stu-id="bd4df-159">To avoid this during "Saved State" backups, the virtual machine state must be saved using the clustering service.</span></span> <span data-ttu-id="bd4df-160">為了避免在還原期間發生此情況，虛擬機器上的資源必須離線。</span><span class="sxs-lookup"><span data-stu-id="bd4df-160">To avoid this during a restore, the resources on the virtual machine would need to be taken offline.</span></span>

## <a name="details-on-the-hyper-v-vss-writer"></a><span data-ttu-id="bd4df-161">Hyper-v VSS 寫入器的詳細資料</span><span class="sxs-lookup"><span data-stu-id="bd4df-161">Details on the Hyper-V VSS Writer</span></span>

<span data-ttu-id="bd4df-162">寫入器名稱： Microsoft Hyper-V VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="bd4df-162">Writer Name: Microsoft Hyper-V VSS Writer</span></span>

<span data-ttu-id="bd4df-163">寫入器識別碼：66841cd4-6ded-4f4b-8f17-fd23f8ddc3de</span><span class="sxs-lookup"><span data-stu-id="bd4df-163">Writer ID: 66841cd4-6ded-4f4b-8f17-fd23f8ddc3de</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd4df-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd4df-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd4df-165">在 VSS 下處理備份的總覽</span><span class="sxs-lookup"><span data-stu-id="bd4df-165">Overview of Processing a Backup Under VSS</span></span>](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)
</dt> <dt>

[<span data-ttu-id="bd4df-166">在 VSS 下處理還原的總覽</span><span class="sxs-lookup"><span data-stu-id="bd4df-166">Overview of Processing a Restore Under VSS</span></span>](/windows/desktop/VSS/overview-of-processing-a-restore-under-vss)
</dt> </dl>

 

 
