---
description: 要求者可以使用 >ivssbackupcomponents：： BreakSnapshotSet 或 IVssBackupComponentsEx2：： BreakSnapshotSetEx 方法來中斷陰影複製集。
ms.assetid: fb796b2f-b6fb-48ee-8d42-36f88cb165aa
title: 中斷陰影複製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dac84c9f45d16d8a88f9d61ad6e4c277dfad3ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985127"
---
# <a name="breaking-shadow-copies"></a><span data-ttu-id="d3135-103">中斷陰影複製</span><span class="sxs-lookup"><span data-stu-id="d3135-103">Breaking Shadow Copies</span></span>

<span data-ttu-id="d3135-104">要求者可以使用 [**>ivssbackupcomponents：： BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) 或 [**IVssBackupComponentsEx2：： BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) 方法來中斷陰影複製集。</span><span class="sxs-lookup"><span data-stu-id="d3135-104">A requester can break a shadow copy set by using the [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) or [**IVssBackupComponentsEx2::BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) method.</span></span>

<span data-ttu-id="d3135-105">中斷陰影複製是包含不會再由 VSS 管理之陰影複製的磁片區。</span><span class="sxs-lookup"><span data-stu-id="d3135-105">A broken shadow copy is a volume that contains a shadow copy that is no longer managed by VSS.</span></span> <span data-ttu-id="d3135-106">只有陰影複製的 [*提供者*](vssgloss-p.md) 是 [*硬體提供者*](vssgloss-h.md)時，中斷陰影複製才有意義。</span><span class="sxs-lookup"><span data-stu-id="d3135-106">Breaking a shadow copy has meaning only if the shadow copy's [*provider*](vssgloss-p.md) is a [*hardware provider*](vssgloss-h.md).</span></span> <span data-ttu-id="d3135-107">這是因為只有硬體提供者可以使用獨立于 VSS 的生命週期，將陰影複製實作為實際的磁片區。</span><span class="sxs-lookup"><span data-stu-id="d3135-107">This is because only hardware providers can implement a shadow copy as an actual volume with a life cycle independent of VSS.</span></span> <span data-ttu-id="d3135-108">如果 VSS 無法管理這類磁片區，仍可使用。</span><span class="sxs-lookup"><span data-stu-id="d3135-108">If VSS does not manage such a volume, it still is available.</span></span>

<span data-ttu-id="d3135-109">軟體提供者只有在與 VSS 作業相關時，才會維護陰影複製。</span><span class="sxs-lookup"><span data-stu-id="d3135-109">Software providers maintain shadow copies only while involved in VSS operations.</span></span> <span data-ttu-id="d3135-110">基於這個理由，中斷陰影複製對軟體提供者沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="d3135-110">For that reason, breaking a shadow copy has no meaning for software providers.</span></span>

<span data-ttu-id="d3135-111">如果陰影複製是由硬體提供者所管理，要求者必須先匯入陰影複製，然後再呼叫 [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) 或 [**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)。</span><span class="sxs-lookup"><span data-stu-id="d3135-111">If the shadow copy was managed by a hardware provider, the requester must import the shadow copy before calling [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) or [**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex).</span></span> <span data-ttu-id="d3135-112">如果是硬體提供者所建立的無法轉移 () 陰影複製，則會隱含地匯入 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 呼叫的一部分。</span><span class="sxs-lookup"><span data-stu-id="d3135-112">In case of non-transportable (created by a hardware provider) shadow copies, they are imported implicitly as part of the [**IVssBackupComponents::DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) call.</span></span>

<span data-ttu-id="d3135-113">要求者呼叫 [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) 或 [**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)之後，仍然可以透過其裝置物件或其他存取路徑存取陰影複製集，但不再是陰影複製集。</span><span class="sxs-lookup"><span data-stu-id="d3135-113">After the requester has called [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) or [**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex), the shadow copy set is still accessible via its device objects or other access paths, but it is no longer a shadow copy set.</span></span> <span data-ttu-id="d3135-114">您可以使用虛擬磁碟服務 (VDS) COM 介面，以一或多個 Lun 的形式來管理。</span><span class="sxs-lookup"><span data-stu-id="d3135-114">It can be managed as one or more LUNs by using the Virtual Disk Service (VDS) COM interfaces.</span></span> <span data-ttu-id="d3135-115">使用 VDS，要求者可以將 Lun 轉換成讀取/寫入、使用磁碟機號掛接，或遮罩/取消遮罩至其他電腦。</span><span class="sxs-lookup"><span data-stu-id="d3135-115">Using VDS, a requester can convert the LUNs to read/write, mount them with drive letters, or mask/unmask them to other computers.</span></span> <span data-ttu-id="d3135-116">如需詳細資訊，請參閱 [VDS API 檔](../vds/virtual-disk-service-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="d3135-116">See the [VDS API documentation](../vds/virtual-disk-service-portal.md) for more information.</span></span>

 

 
