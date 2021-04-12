---
description: 使用 VDS
ms.assetid: aa4be499-625d-4dbd-828c-4a55ff2dba2c
title: 使用 VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c648c5cc2507c4819f98367c367099248a0e723f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194918"
---
# <a name="using-vds"></a><span data-ttu-id="2ec53-103">使用 VDS</span><span class="sxs-lookup"><span data-stu-id="2ec53-103">Using VDS</span></span>

<span data-ttu-id="2ec53-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="2ec53-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="2ec53-105">VDS 為腳本和 GUI 開發提供了一個介面，可以簡化管理一組異類儲存系統的 Windows server 系統管理員所執行的活動，並在一段時間內跨不同的硬體設定遷移資料。</span><span class="sxs-lookup"><span data-stu-id="2ec53-105">VDS supplies an interface for scripting and GUI development that can simplify the activities that are performed by a Windows server administrator who manages a heterogeneous set of storage systems, migrating data across different hardware configurations over time.</span></span> <span data-ttu-id="2ec53-106">如果您不熟悉在 VDS 開發中使用的物件，請參閱 [Vds 物件模型](vds-object-model.md)。</span><span class="sxs-lookup"><span data-stu-id="2ec53-106">If you are unfamiliar with the objects that are used in VDS development, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="2ec53-107">開始之前的幾個要點：</span><span class="sxs-lookup"><span data-stu-id="2ec53-107">A few points before you begin:</span></span>

-   <span data-ttu-id="2ec53-108">雖然 VDS 包含軟體提供者，但您必須個別購買硬體提供者和相關聯的硬體，才能利用硬體提供者作業。</span><span class="sxs-lookup"><span data-stu-id="2ec53-108">While VDS includes a software provider, you must purchase a hardware provider and the associated hardware separately to take advantage of the hardware provider operations.</span></span> <span data-ttu-id="2ec53-109">如需安裝指示，請參閱硬體製造商所提供的檔。</span><span class="sxs-lookup"><span data-stu-id="2ec53-109">For installation instructions, see the documentation that is provided by the hardware manufacturer.</span></span>
-   <span data-ttu-id="2ec53-110">某些作業需要 NTFS 格式的磁片區。</span><span class="sxs-lookup"><span data-stu-id="2ec53-110">Some operations require NTFS-formatted volumes.</span></span> <span data-ttu-id="2ec53-111">例如，當您在現有的目錄上掛接磁片區時，包含該目錄的磁片區必須格式化為 NTFS。</span><span class="sxs-lookup"><span data-stu-id="2ec53-111">For example, when you mount a volume on an existing directory, the volume that contains the directory must be formatted with NTFS.</span></span> <span data-ttu-id="2ec53-112">其他檔案系統不支援此操作。</span><span class="sxs-lookup"><span data-stu-id="2ec53-112">Other file systems do not support this operation.</span></span> <span data-ttu-id="2ec53-113">如需有關需要 NTFS 之作業的詳細資訊，請參閱 [VDS 參考](vds-reference.md)中的每個方法頁面。</span><span class="sxs-lookup"><span data-stu-id="2ec53-113">For information about operations that require NTFS, see each method page in [VDS Reference](vds-reference.md).</span></span>

## <a name="programming-languages"></a><span data-ttu-id="2ec53-114">程式語言：</span><span class="sxs-lookup"><span data-stu-id="2ec53-114">Programming Languages</span></span>

<span data-ttu-id="2ec53-115">使用適用于使用 COM 進行開發的任何程式設計語言，例如 C 語言或 c + +。</span><span class="sxs-lookup"><span data-stu-id="2ec53-115">Use any programming language that is suitable for development with COM, such as the C language or C++.</span></span>

## <a name="security"></a><span data-ttu-id="2ec53-116">安全性</span><span class="sxs-lookup"><span data-stu-id="2ec53-116">Security</span></span>

<span data-ttu-id="2ec53-117">預設會啟用 Windows 防火牆。</span><span class="sxs-lookup"><span data-stu-id="2ec53-117">Windows Firewall is enabled by default.</span></span> <span data-ttu-id="2ec53-118">這可能會導致可遠端執行的回呼介面（例如 [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)）的驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="2ec53-118">This can cause authentication to fail for callback interfaces, such as [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink), that can be executed remotely.</span></span> <span data-ttu-id="2ec53-119">如果在用戶端或伺服器上啟用了 Windows 防火牆，您必須將遠端磁片區管理新增至 Windows 防火牆的 [ **例外** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2ec53-119">If Windows Firewall is enabled on either the client or the server, you must add Remote Volume Management to the **Exceptions** tab in Windows Firewall.</span></span>

<span data-ttu-id="2ec53-120">**Windows Server 2003：** 在 Windows Server 2003 （含 Service Pack 2） (SP2) 和 Windows Server 2003 Service Pack 1 (SP1) 中，如果用戶端或伺服器上已啟用 Windows 防火牆，且伺服器設定為使用 NTLM 驗證，則您必須將下列設定新增至適用電腦的 Windows 防火牆的 [ **例外** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2ec53-120">**Windows Server 2003:** In Windows Server 2003 with Service Pack 2 (SP2) and Windows Server 2003 with Service Pack 1 (SP1), if Windows Firewall is enabled on either the client or the server and if the server is configured to use NTLM authentication, you must add the following settings to the **Exceptions** tab in Windows Firewall for the appropriate computer.</span></span>

| <span data-ttu-id="2ec53-121">電腦</span><span class="sxs-lookup"><span data-stu-id="2ec53-121">Computer</span></span>                 | <span data-ttu-id="2ec53-122">例外狀況設定</span><span class="sxs-lookup"><span data-stu-id="2ec53-122">Exceptions settings</span></span>                                                                 |
|--------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2ec53-123"> (本機) 的用戶端電腦</span><span class="sxs-lookup"><span data-stu-id="2ec53-123">Client computer (local)</span></span>  | <span data-ttu-id="2ec53-124">Dmremote.exe</span><span class="sxs-lookup"><span data-stu-id="2ec53-124">Dmremote.exe</span></span><br/> <span data-ttu-id="2ec53-125">Mmc.exe</span><span class="sxs-lookup"><span data-stu-id="2ec53-125">Mmc.exe</span></span><br/> <span data-ttu-id="2ec53-126">Vdsldr.exe</span><span class="sxs-lookup"><span data-stu-id="2ec53-126">Vdsldr.exe</span></span><br/> <span data-ttu-id="2ec53-127">TCP 135</span><span class="sxs-lookup"><span data-stu-id="2ec53-127">TCP 135</span></span><br/> |
| <span data-ttu-id="2ec53-128"> (遠端) 的伺服器電腦</span><span class="sxs-lookup"><span data-stu-id="2ec53-128">Server computer (remote)</span></span> | <span data-ttu-id="2ec53-129">Dmadmin.exe</span><span class="sxs-lookup"><span data-stu-id="2ec53-129">Dmadmin.exe</span></span><br/> <span data-ttu-id="2ec53-130">Vds.exe</span><span class="sxs-lookup"><span data-stu-id="2ec53-130">Vds.exe</span></span><br/> <span data-ttu-id="2ec53-131">TCP 135</span><span class="sxs-lookup"><span data-stu-id="2ec53-131">TCP 135</span></span><br/>                        |



 

<span data-ttu-id="2ec53-132">請注意，在 Windows Server 2003 SP1 之前，預設不會啟用 Windows 防火牆。</span><span class="sxs-lookup"><span data-stu-id="2ec53-132">Note that Windows Firewall is not enabled by default until Windows Server 2003 with SP1.</span></span>

<span data-ttu-id="2ec53-133">使用 VDS 的應用程式必須在 Backup 操作員或 Administrators 群組帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="2ec53-133">An application that is using VDS must run under the Backup Operator or Administrators group account.</span></span> <span data-ttu-id="2ec53-134">如果沒有適當的許可權，應用程式可以建立服務載入器物件，但物件不會載入 VDS。</span><span class="sxs-lookup"><span data-stu-id="2ec53-134">Without the appropriate privilege, an application can create a service loader object, but the object will not load VDS.</span></span> <span data-ttu-id="2ec53-135">相反地，它會傳回錯誤，指出拒絕存取 VDS。</span><span class="sxs-lookup"><span data-stu-id="2ec53-135">Instead, it returns an error indicating that access to VDS is denied.</span></span>

<span data-ttu-id="2ec53-136">如果網路使用 NTLM 驗證，用戶端電腦應該允許匿名存取。</span><span class="sxs-lookup"><span data-stu-id="2ec53-136">If the network uses NTLM authentication, the client computer should allow anonymous access.</span></span> <span data-ttu-id="2ec53-137">在此情況下，如果用戶端電腦正在執行 Windows Server 作業系統，則預設會啟用匿名存取。</span><span class="sxs-lookup"><span data-stu-id="2ec53-137">In this case, if the client computer is running a Windows Server operating system, anonymous access is enabled by default.</span></span> <span data-ttu-id="2ec53-138">如果正在執行 Windows 用戶端作業系統，則必須使用 Dcomcnfg.exe 啟用匿名存取。</span><span class="sxs-lookup"><span data-stu-id="2ec53-138">If it is running a Windows Client operating system, anonymous access must be enabled using Dcomcnfg.exe.</span></span>

## <a name="configuration-and-query-operations"></a><span data-ttu-id="2ec53-139">設定和查詢作業</span><span class="sxs-lookup"><span data-stu-id="2ec53-139">Configuration and Query Operations</span></span>

<span data-ttu-id="2ec53-140">設定和查詢作業的範圍是最相關的電腦、提供者、子系統或套件。</span><span class="sxs-lookup"><span data-stu-id="2ec53-140">Configuration and query operations are scoped by the most relevant computer, provider, subsystem, or pack.</span></span> <span data-ttu-id="2ec53-141">查詢只會跨越一個提供者或一個層級的系結階層。</span><span class="sxs-lookup"><span data-stu-id="2ec53-141">Queries traverse only one provider or one level of the binding hierarchy.</span></span> <span data-ttu-id="2ec53-142">若要建立完整的視圖，呼叫端必須在每個層級之間進行查詢。</span><span class="sxs-lookup"><span data-stu-id="2ec53-142">To build a full view, the caller must query across and down each level.</span></span> <span data-ttu-id="2ec53-143">下列清單包含範例：</span><span class="sxs-lookup"><span data-stu-id="2ec53-143">The following list includes examples:</span></span>

-   <span data-ttu-id="2ec53-144">若要查看電腦上的所有磁片，呼叫者必須針對那些提供者所宣告的磁片，在所有軟體提供者上進行查詢。</span><span class="sxs-lookup"><span data-stu-id="2ec53-144">To view all disks on a computer, callers must query across all software providers for the disks that are claimed by those providers.</span></span>
-   <span data-ttu-id="2ec53-145">為了判斷哪些磁片有助於軟體堆疊磁片區，呼叫端會先判斷參與的 plex，然後查詢每個叢的磁片區。</span><span class="sxs-lookup"><span data-stu-id="2ec53-145">To determine which disks contribute to a software-stacked volume, callers first determine the contributing plexes and then query for the disk extents for each plex.</span></span>
-   <span data-ttu-id="2ec53-146">若要查看所有連接到指定子系統的磁片磁碟機，呼叫端必須查詢子系統。</span><span class="sxs-lookup"><span data-stu-id="2ec53-146">To view all the drives that are attached to a given subsystem, callers must query the subsystem.</span></span>
-   <span data-ttu-id="2ec53-147">若要查看由指定子系統公開的所有 Lun，呼叫端必須查詢子系統。</span><span class="sxs-lookup"><span data-stu-id="2ec53-147">To view all the LUNs that are exposed by a given subsystem, callers must query the subsystem.</span></span>
-   <span data-ttu-id="2ec53-148">若要查看 SAN 或叢集上的所有存放裝置，呼叫端必須查詢每部電腦的所有硬體提供者、查詢所有子系統的每個提供者，然後查詢每個子系統。</span><span class="sxs-lookup"><span data-stu-id="2ec53-148">To view all storage on a SAN or a cluster, callers must query each computer for all hardware providers, query each provider for all subsystems, and then query each subsystem.</span></span>

<span data-ttu-id="2ec53-149">雖然每個個別查詢都不會傳回重複專案，但是跨電腦或跨提供者的重複查詢可能會累積重複專案。</span><span class="sxs-lookup"><span data-stu-id="2ec53-149">While each individual query will not return duplicates, repeated queries across computers or across providers can accumulate duplicates.</span></span> <span data-ttu-id="2ec53-150">呼叫端必須執行任何篩選。</span><span class="sxs-lookup"><span data-stu-id="2ec53-150">Callers must implement any filtering.</span></span> <span data-ttu-id="2ec53-151">另外也請注意，SAN 管理應用程式可以使用 Active Directory 或存放庫來保存設定資訊;可能不需要查詢每部電腦。</span><span class="sxs-lookup"><span data-stu-id="2ec53-151">Note also that SAN management applications can use the Active Directory or a repository to persist configuration information; it might not be necessary to query each computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ec53-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="2ec53-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ec53-153">虛擬磁碟服務</span><span class="sxs-lookup"><span data-stu-id="2ec53-153">Virtual Disk Service</span></span>](virtual-disk-service-portal.md)
</dt> <dt>

[<span data-ttu-id="2ec53-154">VDS 物件模型</span><span class="sxs-lookup"><span data-stu-id="2ec53-154">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="2ec53-155">VDS 參考</span><span class="sxs-lookup"><span data-stu-id="2ec53-155">VDS Reference</span></span>](vds-reference.md)
</dt> </dl>

 

