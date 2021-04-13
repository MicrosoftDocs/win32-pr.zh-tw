---
description: 下列清單指出 Windows Server 2003 Service Pack 1 (SP1) 中磁碟區陰影複製服務介面的新增和變更：
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: Windows Server 2003 SP1 中 VSS 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559b51d5b019d9d57aa154c4728ef5c8f4bb19d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469096"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a><span data-ttu-id="518bc-103">Windows Server 2003 SP1 中 VSS 的新功能</span><span class="sxs-lookup"><span data-stu-id="518bc-103">What's New in VSS in Windows Server 2003 SP1</span></span>

<span data-ttu-id="518bc-104">下列清單指出 Windows Server 2003 Service Pack 1 (SP1) 中磁碟區陰影複製服務介面的新增和變更：</span><span class="sxs-lookup"><span data-stu-id="518bc-104">The following list indicates additions and changes to the Volume Shadow Copy Service interface in Windows Server 2003 with Service Pack 1 (SP1):</span></span>

## <a name="auto-recovery"></a><span data-ttu-id="518bc-105">自動復原</span><span class="sxs-lookup"><span data-stu-id="518bc-105">Auto-recovery</span></span>

<span data-ttu-id="518bc-106">[*自動*](vssgloss-a.md) 復原讓寫入器有時間更新陰影複製中的元件，再將陰影複製永久變更為唯讀。</span><span class="sxs-lookup"><span data-stu-id="518bc-106">[*Auto-recovery*](vssgloss-a.md) allows writers a time to update components in a shadow copy before the shadow copy is permanently changed to read-only.</span></span> <span data-ttu-id="518bc-107">例如，資料庫可能需要復原所有陰影複製的任何未完成交易 (資料庫寫入器會為資料庫元件) 設定 **VSS \_ CF \_ 備份 \_** 復原旗標。</span><span class="sxs-lookup"><span data-stu-id="518bc-107">For example, a database may need to rollback any incomplete transactions for all shadow copies (the database writer would set the **VSS\_CF\_BACKUP\_RECOVERY** flag for the database components).</span></span> <span data-ttu-id="518bc-108">由要求者起始的自動復原允許精細的還原 (例如，還原資料庫中的一個資料表或郵件伺服器上的一個資料夾) 或復原以支援資料採礦，以執行對生產伺服器而言太慢的分析 (要求者會將 **VSS \_ VOLSNAP \_ ATTR \_ 復原復原 \_** 新增至陰影複製內容。 ) 自動復原與可傳送的陰影複製不相容，但使用以可 [轉移陰影複製磁片](fast-recovery-using-transportable-shadow-copied-volumes.md)區的快速復原來支援相同的功能。</span><span class="sxs-lookup"><span data-stu-id="518bc-108">Auto-recovery initiated by the requester allows both fine-grained restore (for example restoring one table in a database or one folder on a mail server), or the rollback to support data mining to perform analysis that would be too slow for a production server (the requester would add **VSS\_VOLSNAP\_ATTR\_ROLLBACK\_RECOVERY** to the shadow copy context.) Auto-recovery is not compatible with transportable shadow copies, but the same functionality is supported by using [Fast Recovery Using Transportable Shadow Copied Volumes](fast-recovery-using-transportable-shadow-copied-volumes.md).</span></span>

<span data-ttu-id="518bc-109">下列程式設計項目有變更可支援自動復原：</span><span class="sxs-lookup"><span data-stu-id="518bc-109">The following programming elements have changes to support auto-recovery:</span></span>

<span data-ttu-id="518bc-110">類別方法</span><span class="sxs-lookup"><span data-stu-id="518bc-110">Class methods</span></span>

-   [<span data-ttu-id="518bc-111">**CVssWriter::GetSnapshotDeviceName**</span><span class="sxs-lookup"><span data-stu-id="518bc-111">**CVssWriter::GetSnapshotDeviceName**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [<span data-ttu-id="518bc-112">**CVssWriter::OnPostSnapshot**</span><span class="sxs-lookup"><span data-stu-id="518bc-112">**CVssWriter::OnPostSnapshot**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

<span data-ttu-id="518bc-113">列舉</span><span class="sxs-lookup"><span data-stu-id="518bc-113">Enumerations</span></span>

-   [<span data-ttu-id="518bc-114">**VSS \_ 元件 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="518bc-114">**VSS\_COMPONENT\_FLAGS**</span></span>](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [<span data-ttu-id="518bc-115">**\_VSS \_ 磁片區 \_ 快照集 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="518bc-115">**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

<span data-ttu-id="518bc-116">介面方法</span><span class="sxs-lookup"><span data-stu-id="518bc-116">Interface methods</span></span>

-   [<span data-ttu-id="518bc-117">**IVssProviderCreateSnapshotSet：:P reFinalCommitSnapshots**</span><span class="sxs-lookup"><span data-stu-id="518bc-117">**IVssProviderCreateSnapshotSet::PreFinalCommitSnapshots**</span></span>](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [<span data-ttu-id="518bc-118">**IVssProviderCreateSnapshotSet：:P ostFinalCommitSnapshots**</span><span class="sxs-lookup"><span data-stu-id="518bc-118">**IVssProviderCreateSnapshotSet::PostFinalCommitSnapshots**</span></span>](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a><span data-ttu-id="518bc-119">完整支援可轉移的陰影複製</span><span class="sxs-lookup"><span data-stu-id="518bc-119">Full Support for Transportable Shadow Copies</span></span>

<span data-ttu-id="518bc-120">所有版本的 Windows Server 2003 SP1 都支援可轉移的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="518bc-120">Transportable shadow copies are supported in all editions of Windows Server 2003 with SP1.</span></span> <span data-ttu-id="518bc-121">如需詳細資訊，請參閱匯 [入可傳送的陰影複製磁片](importing-transportable-shadow-copied-volumes.md)區。</span><span class="sxs-lookup"><span data-stu-id="518bc-121">For more information, see [Importing Transportable Shadow Copied Volumes](importing-transportable-shadow-copied-volumes.md).</span></span>

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a><span data-ttu-id="518bc-122">使用可轉移陰影複製的磁片區快速復原</span><span class="sxs-lookup"><span data-stu-id="518bc-122">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>

[<span data-ttu-id="518bc-123">使用可轉移陰影複製的磁片區快速復原</span><span class="sxs-lookup"><span data-stu-id="518bc-123">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a><span data-ttu-id="518bc-124">陰影複製存放區域管理</span><span class="sxs-lookup"><span data-stu-id="518bc-124">Shadow copy storage area management</span></span>

[<span data-ttu-id="518bc-125">**IVssSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="518bc-125">**IVssSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



