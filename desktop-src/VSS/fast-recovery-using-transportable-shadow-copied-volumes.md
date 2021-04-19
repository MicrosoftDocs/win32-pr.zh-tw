---
description: 可轉移的陰影複製可用於加速快速復原。
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: 使用可轉移陰影複製的磁片區快速復原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a588395de36b0e6773eacf7f46a45452a69c13c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984741"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a><span data-ttu-id="bce50-103">使用可轉移陰影複製的磁片區快速復原</span><span class="sxs-lookup"><span data-stu-id="bce50-103">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>

<span data-ttu-id="bce50-104">可 [*轉移的陰影複製*](vssgloss-t.md)可用於加速 *快速* 復原。</span><span class="sxs-lookup"><span data-stu-id="bce50-104">[*Transportable shadow copies*](vssgloss-t.md) can be used to facilitate a *fast recovery*.</span></span>

<span data-ttu-id="bce50-105">快速復原可以用來快速還原為較早的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="bce50-105">Fast recovery can be used to quickly revert to an earlier shadow copy.</span></span> <span data-ttu-id="bce50-106">涉及的步驟如下：</span><span class="sxs-lookup"><span data-stu-id="bce50-106">The steps involved are:</span></span>

1.  <span data-ttu-id="bce50-107">建立適當 Lun 的可轉移陰影複製。</span><span class="sxs-lookup"><span data-stu-id="bce50-107">Create the transportable shadow copy of the appropriate LUNs.</span></span> <span data-ttu-id="bce50-108">陰影複製可以是持續性或非 [*持續*](vssgloss-p.md) 性的。</span><span class="sxs-lookup"><span data-stu-id="bce50-108">The shadow copy can be either [*persistent*](vssgloss-p.md) or nonpersistent.</span></span>
2.  <span data-ttu-id="bce50-109">移除原始 Lun</span><span class="sxs-lookup"><span data-stu-id="bce50-109">Remove the original LUNs</span></span>
    1.  <span data-ttu-id="bce50-110">如果電腦位於叢集中，請將受影響的磁片資源標示為離線，或啟用這些磁片資源的 [維護模式](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) 。</span><span class="sxs-lookup"><span data-stu-id="bce50-110">If the computer is inside a cluster, mark the affected disk resources as offline, or enable the [maintenance mode](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) for these disk resources.</span></span>
    2.  <span data-ttu-id="bce50-111">從這部電腦遮罩受影響的 Lun (以及如果電腦位於叢集中的所有其他節點) 。</span><span class="sxs-lookup"><span data-stu-id="bce50-111">Mask the affected LUNs from this computer (and all other nodes if the computer is in a cluster).</span></span>
3.  <span data-ttu-id="bce50-112">使用 [**>ivssbackupcomponents：： ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) 方法匯入陰影複製。</span><span class="sxs-lookup"><span data-stu-id="bce50-112">Import the shadow copy using the [**IVssBackupComponents::ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) method.</span></span>
4.  <span data-ttu-id="bce50-113">使用 [**>ivssbackupcomponents：： BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) 方法來中斷陰影複製。</span><span class="sxs-lookup"><span data-stu-id="bce50-113">Break the shadow copy using the [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) method.</span></span>
5.  <span data-ttu-id="bce50-114">將新的陰影複製磁片區標示為讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="bce50-114">Mark the new shadow copy volumes as read/write.</span></span>
6.  <span data-ttu-id="bce50-115">如果電腦位於叢集中，則會將新的陰影複製 Lun 公開為原始 Lun。</span><span class="sxs-lookup"><span data-stu-id="bce50-115">If the computer is in a cluster, expose the new shadow copy LUNs as the original LUNs.</span></span>
    1.  <span data-ttu-id="bce50-116">將陰影複製 Lun 取消遮罩至叢集中的其他節點。</span><span class="sxs-lookup"><span data-stu-id="bce50-116">Unmask the shadow copy LUNs to the other nodes in the cluster.</span></span>
    2.  <span data-ttu-id="bce50-117">將先前標示為離線的資源標記為線上，或停用這些磁片資源的維護模式。</span><span class="sxs-lookup"><span data-stu-id="bce50-117">Mark the resources that were previously marked as offline as online, or disable the maintenance mode for those disk resources.</span></span>

> [!Note]  
> <span data-ttu-id="bce50-118">在 Windows Server 2003 Service Pack 1 (SP1) 之前，不支援叢集中的可轉移陰影複製。</span><span class="sxs-lookup"><span data-stu-id="bce50-118">Transportable shadow copies in a cluster are not supported before Windows Server 2003 with Service Pack 1 (SP1).</span></span> <span data-ttu-id="bce50-119">只有符合規範的 Lun 才支援這項功能，其中至少有一個 SCSI 重要產品資料 (VPD) 0x83 \_ 類型1、2或8的儲存體識別碼，以及關聯0，而且 lun 必須維持具有 MBR 磁碟分區的基本磁碟。</span><span class="sxs-lookup"><span data-stu-id="bce50-119">This is only supported with compliant LUNs, which have at least one SCSI Vital Product Data (VPD) page 0x83 STORAGE\_IDENTIFIER of type 1,2, or 8, and association 0, and the LUNs must maintain a basic disk with MBR partitioning.</span></span>

 

 

 
