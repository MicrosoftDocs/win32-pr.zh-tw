---
description: Windows Server 2008 R2 和 Windows 7 對磁碟區陰影複製服務引進了下列變更。
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 新功能： Windows Server 2008 R2 中的 VSS & Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3677f89517a770a4519369ae11f2eed7e7985414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991822"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a><span data-ttu-id="60fef-103">新功能： Windows Server 2008 R2 中的 VSS & Windows 7</span><span class="sxs-lookup"><span data-stu-id="60fef-103">What's New: VSS in Windows Server 2008 R2 & Windows 7</span></span>

<span data-ttu-id="60fef-104">Windows Server 2008 R2 和 Windows 7 對磁碟區陰影複製服務引進了下列變更。</span><span class="sxs-lookup"><span data-stu-id="60fef-104">Windows Server 2008 R2 and Windows 7 introduce the following changes to the Volume Shadow Copy Service.</span></span>

## <a name="new-vss-interfaces"></a><span data-ttu-id="60fef-105">新的 VSS 介面</span><span class="sxs-lookup"><span data-stu-id="60fef-105">New VSS Interfaces</span></span>

<dl>

[<span data-ttu-id="60fef-106">**IVssBackupComponentsEx3**</span><span class="sxs-lookup"><span data-stu-id="60fef-106">**IVssBackupComponentsEx3**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)  
[<span data-ttu-id="60fef-107">**IVssComponentEx2**</span><span class="sxs-lookup"><span data-stu-id="60fef-107">**IVssComponentEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)  
[<span data-ttu-id="60fef-108">**IVssCreateExpressWriterMetadata**</span><span class="sxs-lookup"><span data-stu-id="60fef-108">**IVssCreateExpressWriterMetadata**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)  
[<span data-ttu-id="60fef-109">**IVssExpressWriter**</span><span class="sxs-lookup"><span data-stu-id="60fef-109">**IVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)  
</dl>

## <a name="new-vss-classes"></a><span data-ttu-id="60fef-110">新的 VSS 類別</span><span class="sxs-lookup"><span data-stu-id="60fef-110">New VSS Classes</span></span>

<dl>

[<span data-ttu-id="60fef-111">**CVssWriterEx2**</span><span class="sxs-lookup"><span data-stu-id="60fef-111">**CVssWriterEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex2)  
</dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="60fef-112">新的 VSS 列舉</span><span class="sxs-lookup"><span data-stu-id="60fef-112">New VSS Enumerations</span></span>

<dl>

[<span data-ttu-id="60fef-113">**VSS \_ 修復 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="60fef-113">**VSS\_RECOVERY\_OPTIONS**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a><span data-ttu-id="60fef-114">新的 VSS 函式</span><span class="sxs-lookup"><span data-stu-id="60fef-114">New VSS Functions</span></span>

<dl>

[<span data-ttu-id="60fef-115">**CreateVssExpressWriter**</span><span class="sxs-lookup"><span data-stu-id="60fef-115">**CreateVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="60fef-116">現有的 VSS 介面修改</span><span class="sxs-lookup"><span data-stu-id="60fef-116">Existing VSS Interface Modifications</span></span>

<dl>

<span data-ttu-id="60fef-117">[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex) 介面</span><span class="sxs-lookup"><span data-stu-id="60fef-117">[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex) interface</span></span><dl> <span data-ttu-id="60fef-118">新增的方法： [ **ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)</span><span class="sxs-lookup"><span data-stu-id="60fef-118">Added method: [**ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)</span></span>  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a><span data-ttu-id="60fef-119">VSS 事件追蹤和記錄</span><span class="sxs-lookup"><span data-stu-id="60fef-119">VSS Event Tracing and Logging</span></span>

<span data-ttu-id="60fef-120">從 Windows Server 2008 R2 和 Windows 7 開始，您可以使用 VssTrace 工具、Logman 工具或 Tracelog.exe 工具來收集 VSS 基礎結構的追蹤資訊。</span><span class="sxs-lookup"><span data-stu-id="60fef-120">Beginning with Windows Server 2008 R2 and Windows 7, you can use the VssTrace tool, the Logman tool, or the Tracelog tool to collect tracing information for the VSS infrastructure.</span></span> <span data-ttu-id="60fef-121">如需詳細資訊，請參閱搭配 [使用追蹤工具和 VSS](using-tracing-tools-with-vss.md)。</span><span class="sxs-lookup"><span data-stu-id="60fef-121">For more information, see [Using Tracing Tools with VSS](using-tracing-tools-with-vss.md).</span></span>

## <a name="lun-resynchronization"></a><span data-ttu-id="60fef-122">LUN 重新同步處理</span><span class="sxs-lookup"><span data-stu-id="60fef-122">LUN Resynchronization</span></span>

<span data-ttu-id="60fef-123">在 Windows Server 2008 R2 和 Windows 7 中，VSS 要求者可以使用名為 LUN 重新同步 (LUN resynchronization 或 LUN resync) 的硬體陰影複製提供者功能。</span><span class="sxs-lookup"><span data-stu-id="60fef-123">In Windows Server 2008 R2 and Windows 7, VSS requesters can use a hardware shadow copy provider feature called LUN resynchronization (or "LUN resync").</span></span> <span data-ttu-id="60fef-124">這是一種快速復原配置，可讓應用程式系統管理員將資料從陰影複製還原到原始的邏輯單元編號 (LUN) 或新的 LUN。</span><span class="sxs-lookup"><span data-stu-id="60fef-124">This is a fast-recovery scheme that allows an application administrator to restore data from a shadow copy to the original logical unit number (LUN) or to a new LUN.</span></span> <span data-ttu-id="60fef-125">陰影複製可以是完整再製或差異陰影複製。</span><span class="sxs-lookup"><span data-stu-id="60fef-125">The shadow copy can be a full clone or a differential shadow copy.</span></span> <span data-ttu-id="60fef-126">不論是哪一種情況，在重新同步作業結束時，目的地 LUN 的內容都會與陰影複製 LUN 相同。</span><span class="sxs-lookup"><span data-stu-id="60fef-126">In either case, at the end of the resync operation, the destination LUN will have the same contents as the shadow copy LUN.</span></span> <span data-ttu-id="60fef-127">在重新同步作業期間，陣列會執行從陰影複製到目的地 LUN 的區塊層級複製。</span><span class="sxs-lookup"><span data-stu-id="60fef-127">During the resync operation, the array performs a block-level copy from the shadow copy to the destination LUN.</span></span> <span data-ttu-id="60fef-128">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="60fef-128">For more information, see the following:</span></span>

-   [<span data-ttu-id="60fef-129">LUN 重新同步-Server 2008 R2 中的快速復原案例</span><span class="sxs-lookup"><span data-stu-id="60fef-129">LUN Resync - A fast recovery scenario in Server 2008 R2</span></span>](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   <span data-ttu-id="60fef-130">[磁碟區陰影複製服務](/windows-server/storage/file-server/volume-shadow-copy-service)中的「如何使用陰影複製」</span><span class="sxs-lookup"><span data-stu-id="60fef-130">"How Shadow Copies Are Used" in [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service)</span></span>
-   [<span data-ttu-id="60fef-131">常見的 LUN 重新同步問題</span><span class="sxs-lookup"><span data-stu-id="60fef-131">Common LUN Resync gotchas</span></span>](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a><span data-ttu-id="60fef-132">快速寫入器</span><span class="sxs-lookup"><span data-stu-id="60fef-132">Express Writers</span></span>

<span data-ttu-id="60fef-133">在 Windows Server 2008 R2 和 Windows 7 中，VSS express 介面可讓應用程式註冊其資料檔案的位置，而不需要執行 VSS 寫入器。</span><span class="sxs-lookup"><span data-stu-id="60fef-133">In Windows Server 2008 R2 and Windows 7, the VSS express interface allows an application to register the location of its data files without implementing a VSS writer.</span></span> <span data-ttu-id="60fef-134">如需詳細資訊，請參閱 [磁碟區陰影複製服務 (VSS) Express 寫入](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx)器。</span><span class="sxs-lookup"><span data-stu-id="60fef-134">For more information, see [Volume Shadow Copy Service (VSS) Express Writers](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).</span></span>

## <a name="new-vss-writers"></a><span data-ttu-id="60fef-135">新的 VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="60fef-135">New VSS Writers</span></span>

<span data-ttu-id="60fef-136">Windows Server 2008 R2 和 Windows 7 引進下列 VSS 寫入器：</span><span class="sxs-lookup"><span data-stu-id="60fef-136">Windows Server 2008 R2 and Windows 7 introduce the following VSS writers:</span></span>

-   <span data-ttu-id="60fef-137">效能計數器寫入器</span><span class="sxs-lookup"><span data-stu-id="60fef-137">Performance Counters Writer</span></span>
-   <span data-ttu-id="60fef-138">工作排程器寫入器</span><span class="sxs-lookup"><span data-stu-id="60fef-138">Task Scheduler Writer</span></span>
-   <span data-ttu-id="60fef-139">VSS 中繼資料存放區寫入器</span><span class="sxs-lookup"><span data-stu-id="60fef-139">VSS Metadata Store Writer</span></span>

<span data-ttu-id="60fef-140">這些新的寫入器記載于 [內建的 VSS 寫入](in-box-vss-writers.md)器中。</span><span class="sxs-lookup"><span data-stu-id="60fef-140">These new writers are documented in [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 
