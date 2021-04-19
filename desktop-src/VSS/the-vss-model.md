---
description: VSS 的設計目的是要解決一般磁片區備份問題中所述的問題。
ms.assetid: f9a3efea-d6e8-40df-92ac-f6faaa4fca60
title: VSS 模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e65061b9496fe04769a9b2429f7e05a2064de63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970431"
---
# <a name="the-vss-model"></a><span data-ttu-id="12323-103">VSS 模型</span><span class="sxs-lookup"><span data-stu-id="12323-103">The VSS Model</span></span>

<span data-ttu-id="12323-104">VSS 的設計目的是要解決 [一般磁片區備份問題](common-volume-backup-issues.md)中所述的問題。</span><span class="sxs-lookup"><span data-stu-id="12323-104">VSS is designed to address the problems described in [Common Volume Backup Issues](common-volume-backup-issues.md).</span></span>

<span data-ttu-id="12323-105">VSS 模型包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="12323-105">The VSS model includes the following:</span></span>

-   <span data-ttu-id="12323-106">陰影複製機制。</span><span class="sxs-lookup"><span data-stu-id="12323-106">The shadow copy mechanism.</span></span> <span data-ttu-id="12323-107">VSS 提供磁片的快速磁片區狀態快速捕獲，也就是磁片區的 [*陰影複製*](vssgloss-s.md) 。</span><span class="sxs-lookup"><span data-stu-id="12323-107">VSS provides fast volume capture of the state of a disk at one instant in time—a [*shadow copy*](vssgloss-s.md) of the volume.</span></span> <span data-ttu-id="12323-108">此磁片區複本與即時磁片區並存存在，而且會包含磁片上所有檔案的複本，這些檔案會以個別裝置的形式有效儲存和提供。</span><span class="sxs-lookup"><span data-stu-id="12323-108">This volume copy exists side by side with the live volume, and contains copies of all files on disk effectively saved and available as a separate device.</span></span>
-   <span data-ttu-id="12323-109">透過應用程式協調進行一致的檔案狀態。</span><span class="sxs-lookup"><span data-stu-id="12323-109">Consistent file state via application coordination.</span></span> <span data-ttu-id="12323-110">VSS 提供以 COM 為基礎的事件驅動處理序間通訊機制，參與的進程可以用來判斷有關備份、還原和陰影複製 (磁片區捕獲) 作業的系統狀態。</span><span class="sxs-lookup"><span data-stu-id="12323-110">VSS provides a COM-based, event-driven interprocess communication mechanism that participating processes can use to determine system state with respect to backup, restore, and shadow copy (volume capture) operations.</span></span> <span data-ttu-id="12323-111">這些事件會定義應用程式用來修改磁片 ([*寫入*](vssgloss-w.md) 器上資料的階段，) 可以在建立陰影複製之前，將所有的檔案帶入一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="12323-111">These events define stages by which applications modifying data on disk ([*writers*](vssgloss-w.md)) can bring all their files into a consistent state prior to the creation of the shadow copy.</span></span>
-   <span data-ttu-id="12323-112">將應用程式停機時間降到最低。</span><span class="sxs-lookup"><span data-stu-id="12323-112">Minimizing application downtime.</span></span> <span data-ttu-id="12323-113">VSS 陰影複製會與要備份之磁片區的即時複本並行存在，因此除了陰影複製準備和建立的短暫期間，應用程式可以繼續其工作。</span><span class="sxs-lookup"><span data-stu-id="12323-113">The VSS shadow copy exists in parallel with a live copy of the volume to be backed up, so except for the brief period of the shadow copy's preparation and creation, an application can continue its work.</span></span> <span data-ttu-id="12323-114">實際建立陰影複製所需的時間（在 [*凍結*](vssgloss-f.md) 和 [*解除凍結*](vssgloss-t.md) 事件之間發生）通常需要大約一分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="12323-114">The time needed to actually create a shadow copy, which occurs between [*Freeze*](vssgloss-f.md) and [*Thaw*](vssgloss-t.md) events, typically takes about one minute.</span></span>

    <span data-ttu-id="12323-115">當寫入器準備進行陰影複製時，包括排清 i/o 和儲存狀態 (請參閱) [的備份前工作總覽](overview-of-pre-backup-tasks.md) 重要，它比實際備份磁片區所需的時間短一點，因為大型磁片區可能需要數小時的時間。</span><span class="sxs-lookup"><span data-stu-id="12323-115">While a writer's preparation for a shadow copy, including flushing I/O and saving state (see [Overview of Pre-Backup Tasks](overview-of-pre-backup-tasks.md)), may be nontrivial, it is significantly shorter than the time required to actually back up a volume—which for large volumes may take hours.</span></span>

-   <span data-ttu-id="12323-116">VSS 的整合介面。</span><span class="sxs-lookup"><span data-stu-id="12323-116">Unified interface to VSS.</span></span> <span data-ttu-id="12323-117">VSS 會將陰影複製機制抽象化在通用介面內，同時讓硬體廠商新增及管理其專屬提供者的獨特功能。</span><span class="sxs-lookup"><span data-stu-id="12323-117">VSS abstracts the shadow copy mechanisms within a common interface while enabling a hardware vendor to add and manage the unique features of its own providers.</span></span> <span data-ttu-id="12323-118">任何備份應用程式 [*(要求*](vssgloss-r.md) 者) 和任何寫入器都應該能夠在支援 VSS 介面的任何磁片儲存系統上執行。</span><span class="sxs-lookup"><span data-stu-id="12323-118">Any backup application ([*requester*](vssgloss-r.md)) and any writer should be able to run on any disk storage system that supports the VSS interface.</span></span>
-   <span data-ttu-id="12323-119">Multivolume 備份。</span><span class="sxs-lookup"><span data-stu-id="12323-119">Multivolume backup.</span></span> <span data-ttu-id="12323-120">VSS 支援 [*陰影複製集*](vssgloss-s.md)（這是陰影複製的集合），跨多個廠商的多個磁片區類型。</span><span class="sxs-lookup"><span data-stu-id="12323-120">VSS supports [*shadow copy sets*](vssgloss-s.md), which are collections of shadow copies, across multiple types of disk volumes from multiple vendors.</span></span> <span data-ttu-id="12323-121">陰影複製集中的所有陰影複製都將使用相同的時間戳記來建立，並且會呈現 multivolume 磁片狀態的相同磁片狀態。</span><span class="sxs-lookup"><span data-stu-id="12323-121">All shadow copies in a shadow copy set will be created with the same time stamp and will present the same disk state for a multivolume disk state.</span></span>
-   <span data-ttu-id="12323-122">原生陰影複製支援。</span><span class="sxs-lookup"><span data-stu-id="12323-122">Native shadow copy support.</span></span> <span data-ttu-id="12323-123">從 Windows XP 開始，陰影複製支援可透過 VSS 提供，做為 Windows 作業系統的原生部分。</span><span class="sxs-lookup"><span data-stu-id="12323-123">Beginning with Windows XP, shadow copy support is available through VSS as a native part of the Windows operating system.</span></span> <span data-ttu-id="12323-124">只要系統上至少有一個 NTFS 磁片，就可以將這些系統設定為支援所有掛接之磁片系統的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="12323-124">As long as at least one NTFS disk is present on a system, these systems can be configured to support shadow copies of all disk systems mounted on them.</span></span>

 

 



