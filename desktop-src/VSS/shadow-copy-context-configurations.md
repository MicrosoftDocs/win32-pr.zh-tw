---
description: 要求者藉由設定其內容來控制陰影複製的功能。 此內容會指出陰影複製是否會存留在目前的作業中，以及寫入器/提供者協調的程度。
ms.assetid: adf79bc8-e893-444a-b750-d7ffd09de7c9
title: 陰影複製內容設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb41d0e2604dcf92d27f490175cdcbafd49822c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513125"
---
# <a name="shadow-copy-context-configurations"></a><span data-ttu-id="bfd53-104">陰影複製內容設定</span><span class="sxs-lookup"><span data-stu-id="bfd53-104">Shadow Copy Context Configurations</span></span>

<span data-ttu-id="bfd53-105">要求者藉由設定其內容來控制陰影複製的功能。</span><span class="sxs-lookup"><span data-stu-id="bfd53-105">Requesters control a shadow copy's features by setting its context.</span></span> <span data-ttu-id="bfd53-106">此內容會指出陰影複製是否會存留在目前的作業中，以及寫入器/提供者協調的程度。</span><span class="sxs-lookup"><span data-stu-id="bfd53-106">This context indicates whether the shadow copy will survive the current operation, and the degree of writer/provider coordination.</span></span>

## <a name="persistence-and-shadow-copy-context"></a><span data-ttu-id="bfd53-107">持續性和陰影複製內容</span><span class="sxs-lookup"><span data-stu-id="bfd53-107">Persistence and Shadow Copy Context</span></span>

<span data-ttu-id="bfd53-108">陰影複製可能是 [*持續*](vssgloss-p.md)性的，也就是在終止備份作業或釋放 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 物件後，不會刪除陰影複製。</span><span class="sxs-lookup"><span data-stu-id="bfd53-108">A shadow copy may be [*persistent*](vssgloss-p.md)—that is, the shadow copy is not deleted following the termination of a backup operation or the release of an [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) object.</span></span>

<span data-ttu-id="bfd53-109">持續性陰影複製需要 **vss \_ CTX \_ 用戶端 \_ 可存取** 的 vss [**\_ \_ 快照 \_ 內容內容**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)、 **vss \_ CTX \_ 應用程式 \_ 復原** 或 **vss \_ CTX \_ NAS \_ 復原**。</span><span class="sxs-lookup"><span data-stu-id="bfd53-109">Persistent shadow copies require [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) contexts of **VSS\_CTX\_CLIENT\_ACCESSIBLE**, **VSS\_CTX\_APP\_ROLLBACK**, or **VSS\_CTX\_NAS\_ROLLBACK**.</span></span> <span data-ttu-id="bfd53-110">只有 NTFS 磁片區才能進行永久性陰影複製。</span><span class="sxs-lookup"><span data-stu-id="bfd53-110">Persistent shadow copies can be made only for NTFS volumes.</span></span>

<span data-ttu-id="bfd53-111">非持續性陰影複製是使用 **vss \_ CTX \_ 備份** 或 **vss CTX 檔案 \_ \_ \_ 共用 \_ 備份** 的內容所建立。</span><span class="sxs-lookup"><span data-stu-id="bfd53-111">Nonpersistent shadow copies are created with contexts of **VSS\_CTX\_BACKUP** or **VSS\_CTX\_FILE\_SHARE\_BACKUP**.</span></span> <span data-ttu-id="bfd53-112">非持續性陰影複製可針對 NTFS 和非 NTFS 磁片區進行。</span><span class="sxs-lookup"><span data-stu-id="bfd53-112">Nonpersistent shadow copies can be made for NTFS and non-NTFS volumes.</span></span>

## <a name="writer-participation-and-shadow-copies"></a><span data-ttu-id="bfd53-113">作者參與和陰影複製</span><span class="sxs-lookup"><span data-stu-id="bfd53-113">Writer Participation and Shadow Copies</span></span>

<span data-ttu-id="bfd53-114">陰影複製內容可以分類為涉及寫入器或不涉及寫入器。</span><span class="sxs-lookup"><span data-stu-id="bfd53-114">A shadow copy context can be classified as either involving writers or not involving writers.</span></span>

<span data-ttu-id="bfd53-115">在建立時涉及寫入器的陰影複製內容包括：</span><span class="sxs-lookup"><span data-stu-id="bfd53-115">Shadow copy contexts that involve writers in their creation include:</span></span>

-   <span data-ttu-id="bfd53-116">**VSS \_ CTX \_ 應用程式 \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="bfd53-116">**VSS\_CTX\_APP\_ROLLBACK**</span></span>
-   <span data-ttu-id="bfd53-117">**VSS \_ CTX \_ 備份**</span><span class="sxs-lookup"><span data-stu-id="bfd53-117">**VSS\_CTX\_BACKUP**</span></span>
-   <span data-ttu-id="bfd53-118">**VSS \_ CTX \_ 用戶端 \_ 可存取的 \_ 寫入器**</span><span class="sxs-lookup"><span data-stu-id="bfd53-118">**VSS\_CTX\_CLIENT\_ACCESSIBLE\_WRITERS**</span></span>

<span data-ttu-id="bfd53-119">在建立時不牽涉到寫入器的那些套裝程式括：</span><span class="sxs-lookup"><span data-stu-id="bfd53-119">Those that do not involve writers in their creation include:</span></span>

-   <span data-ttu-id="bfd53-120">**\_ \_ 可存取 VSS CTX 用戶端 \_**</span><span class="sxs-lookup"><span data-stu-id="bfd53-120">**VSS\_CTX\_CLIENT\_ACCESSIBLE**</span></span>
-   <span data-ttu-id="bfd53-121">**VSS \_ CTX \_ 檔案 \_ 共用 \_ 備份**</span><span class="sxs-lookup"><span data-stu-id="bfd53-121">**VSS\_CTX\_FILE\_SHARE\_BACKUP**</span></span>
-   <span data-ttu-id="bfd53-122">**VSS \_ CTX \_ NAS \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="bfd53-122">**VSS\_CTX\_NAS\_ROLLBACK**</span></span>

<span data-ttu-id="bfd53-123">其中一個內容可以用於這兩種陰影複製類型，但無法用於建立陰影複製：</span><span class="sxs-lookup"><span data-stu-id="bfd53-123">One context can be used with both types of shadow copies, but cannot be used in creating a shadow copy:</span></span>

-   <span data-ttu-id="bfd53-124">**VSS \_ CTX \_ 全部**</span><span class="sxs-lookup"><span data-stu-id="bfd53-124">**VSS\_CTX\_ALL**</span></span>

<span data-ttu-id="bfd53-125">使用 VSS CTX 建立陰影複製， **\_ \_ 所有** (使用 [**>ivssbackupcomponents：： StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) 和 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) 都不受支援。</span><span class="sxs-lookup"><span data-stu-id="bfd53-125">Creating a shadow copy with a context of **VSS\_CTX\_ALL** (using [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) and [**IVssBackupComponents::DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) is not supported.</span></span>

<span data-ttu-id="bfd53-126">支援 VSS CTX 內容的作業 **\_ \_ 全都** 是管理作業 [**>ivssbackupcomponents：： Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)、 [**>ivssbackupcomponents：:D Eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots)、 [**>ivssbackupcomponents：： BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)和 [**>ivssbackupcomponents：： ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot)。</span><span class="sxs-lookup"><span data-stu-id="bfd53-126">Operations that support a context of **VSS\_CTX\_ALL** are the administrative operations [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::DeleteSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset), and [**IVssBackupComponents::ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).</span></span>

## <a name="obtaining-shadow-copy-information"></a><span data-ttu-id="bfd53-127">取得陰影複製資訊</span><span class="sxs-lookup"><span data-stu-id="bfd53-127">Obtaining Shadow Copy Information</span></span>

<span data-ttu-id="bfd53-128">如果要求者知道陰影複製 (其 **vss \_ 識別碼**) 的識別 GUID，則可以藉由將呼叫 [**>ivssbackupcomponents：： GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties)所傳回的 [**vss \_ 快照 \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)集內容結構解壓縮，來取得其 **vss \_ 識別碼**) 所識別之特定陰影複製 (內容的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bfd53-128">If a requester knows the identifying GUID of a shadow copy (its **VSS\_ID**), it can obtain information about the context of a specific shadow copy (identified by its **VSS\_ID**) by unpacking the [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure returned by a call to [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span></span>

<span data-ttu-id="bfd53-129">為了取得系統上所有陰影複製的相關內容資訊，要求者會檢查 (的 **Obj 成員。** [**vss \_ \_ 物件**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)樣式的 **\_ lSnapshotAttributes** 成員，這是使用 [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject)所取得的 [**vss) \_ 快照 \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)集的結構，可用來反復查看由呼叫 [**>ivssbackupcomponents：： Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)所傳回的物件清單。</span><span class="sxs-lookup"><span data-stu-id="bfd53-129">To obtain context information about all shadow copies on a system, a requester examines the **m\_lSnapshotAttributes** member of the **Obj.Snap** member of the [**VSS\_OBJECT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (which is a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure) structure obtained by using [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) to iterate over the list of objects returned by a call to [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span>

 

 



