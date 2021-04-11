---
description: Windows Server 2008。
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: Windows Server 2008 和 Windows Vista SP1 中 VSS 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f053e327a7a54a9597bc06836b37c00effc62f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113161"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="2e55a-103">Windows Server 2008 和 Windows Vista SP1 中 VSS 的新功能</span><span class="sxs-lookup"><span data-stu-id="2e55a-103">What's New in VSS in Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="2e55a-104">Windows Server 2008 和 Windows Vista （含 Service Pack 1） (SP1) 引進磁碟區陰影複製服務的下列變更。</span><span class="sxs-lookup"><span data-stu-id="2e55a-104">Windows Server 2008 and Windows Vista with Service Pack 1 (SP1) introduce the following changes to the Volume Shadow Copy Service.</span></span>

> [!Note]  
> <span data-ttu-id="2e55a-105">Windows Vista 的所有變更適用于 Windows Server 2008 和 Windows Vista SP1。</span><span class="sxs-lookup"><span data-stu-id="2e55a-105">All changes for Windows Vista apply to Windows Server 2008 and Windows Vista with SP1.</span></span> <span data-ttu-id="2e55a-106">如需這些變更的詳細資訊，請參閱 [Windows Vista 中 VSS 的新功能](what-s-new-in-vss-in-windows-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="2e55a-106">For details on those changes, see [What's New in VSS in Windows Vista](what-s-new-in-vss-in-windows-vista.md).</span></span>

 

-   [<span data-ttu-id="2e55a-107">新的 VSS 介面</span><span class="sxs-lookup"><span data-stu-id="2e55a-107">New VSS Interfaces</span></span>](#new-vss-interfaces)
-   [<span data-ttu-id="2e55a-108">新的 VSS 列舉</span><span class="sxs-lookup"><span data-stu-id="2e55a-108">New VSS Enumerations</span></span>](#new-vss-enumerations)
-   [<span data-ttu-id="2e55a-109">新的 VSS 結構</span><span class="sxs-lookup"><span data-stu-id="2e55a-109">New VSS Structures</span></span>](#new-vss-structures)
-   [<span data-ttu-id="2e55a-110">現有的 VSS 列舉修改</span><span class="sxs-lookup"><span data-stu-id="2e55a-110">Existing VSS Enumeration Modifications</span></span>](#existing-vss-enumeration-modifications)
-   [<span data-ttu-id="2e55a-111">現有的 VSS 介面修改</span><span class="sxs-lookup"><span data-stu-id="2e55a-111">Existing VSS Interface Modifications</span></span>](#existing-vss-interface-modifications)
-   [<span data-ttu-id="2e55a-112">新的 VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2e55a-112">New VSS Writers</span></span>](#new-vss-writers)

## <a name="new-vss-interfaces"></a><span data-ttu-id="2e55a-113">新的 VSS 介面</span><span class="sxs-lookup"><span data-stu-id="2e55a-113">New VSS Interfaces</span></span>

<dl>

[<span data-ttu-id="2e55a-114">**IVssDifferentialSoftwareSnapshotMgmt3**</span><span class="sxs-lookup"><span data-stu-id="2e55a-114">**IVssDifferentialSoftwareSnapshotMgmt3**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[<span data-ttu-id="2e55a-115">**IVssHardwareSnapshotProviderEx**</span><span class="sxs-lookup"><span data-stu-id="2e55a-115">**IVssHardwareSnapshotProviderEx**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="2e55a-116">新的 VSS 列舉</span><span class="sxs-lookup"><span data-stu-id="2e55a-116">New VSS Enumerations</span></span>

<dl>

[<span data-ttu-id="2e55a-117">**\_VSS \_ 硬體 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="2e55a-117">**\_VSS\_HARDWARE\_OPTIONS**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[<span data-ttu-id="2e55a-118">**VSS \_ 保護 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="2e55a-118">**VSS\_PROTECTION\_FAULT**</span></span>](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[<span data-ttu-id="2e55a-119">**VSS \_ 保護 \_ 層級**</span><span class="sxs-lookup"><span data-stu-id="2e55a-119">**VSS\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a><span data-ttu-id="2e55a-120">新的 VSS 結構</span><span class="sxs-lookup"><span data-stu-id="2e55a-120">New VSS Structures</span></span>

<dl>

[<span data-ttu-id="2e55a-121">**VSS \_ 磁片區 \_ 保護 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="2e55a-121">**VSS\_VOLUME\_PROTECTION\_INFO**</span></span>](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="2e55a-122">現有的 VSS 列舉修改</span><span class="sxs-lookup"><span data-stu-id="2e55a-122">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="2e55a-123"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_備份 \_ 架構**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) 列舉</span><span class="sxs-lookup"><span data-stu-id="2e55a-123"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="2e55a-124"><span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>已新增值：</span><span class="sxs-lookup"><span data-stu-id="2e55a-124"><span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Added value:</span></span>
</dt> <dd>

<span data-ttu-id="2e55a-125">VSS \_ BS \_ 寫入器 \_ 支援 \_ 平行 \_ 還原</span><span class="sxs-lookup"><span data-stu-id="2e55a-125">VSS\_BS\_WRITER\_SUPPORTS\_PARALLEL\_RESTORES</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="2e55a-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_ VSS \_ 磁片區 \_ 快照集 \_ 屬性**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)列舉</span><span class="sxs-lookup"><span data-stu-id="2e55a-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="2e55a-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>已新增值：</span><span class="sxs-lookup"><span data-stu-id="2e55a-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="2e55a-128">VSS \_ VOLSNAP \_ ATTR \_ 延遲 \_ POSTSNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="2e55a-128">VSS\_VOLSNAP\_ATTR\_DELAYED\_POSTSNAPSHOT</span></span>

<span data-ttu-id="2e55a-129">VSS \_ VOLSNAP \_ ATTR \_ TXF \_ 復原</span><span class="sxs-lookup"><span data-stu-id="2e55a-129">VSS\_VOLSNAP\_ATTR\_TXF\_RECOVERY</span></span>

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="2e55a-130">現有的 VSS 介面修改</span><span class="sxs-lookup"><span data-stu-id="2e55a-130">Existing VSS Interface Modifications</span></span>

<dl> <dt>

<span data-ttu-id="2e55a-131"><span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2) 介面</span><span class="sxs-lookup"><span data-stu-id="2e55a-131"><span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="2e55a-132"><span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>新增的方法：</span><span class="sxs-lookup"><span data-stu-id="2e55a-132"><span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Added method:</span></span>
</dt> <dd>

[<span data-ttu-id="2e55a-133">**BreakSnapshotSetEx**</span><span class="sxs-lookup"><span data-stu-id="2e55a-133">**BreakSnapshotSetEx**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a><span data-ttu-id="2e55a-134">新的 VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2e55a-134">New VSS Writers</span></span>

<span data-ttu-id="2e55a-135">Windows Server 2008 和 Windows Vista SP1 引進下列 VSS 寫入器：</span><span class="sxs-lookup"><span data-stu-id="2e55a-135">Windows Server 2008 and Windows Vista with SP1 introduce the following VSS writers:</span></span>

-   <span data-ttu-id="2e55a-136">IIS 設定寫入器</span><span class="sxs-lookup"><span data-stu-id="2e55a-136">IIS Configuration Writer</span></span>
-   <span data-ttu-id="2e55a-137">IIS 元資料庫寫入器</span><span class="sxs-lookup"><span data-stu-id="2e55a-137">IIS Metabase Writer</span></span>
-   <span data-ttu-id="2e55a-138">NPS VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2e55a-138">NPS VSS Writer</span></span>
-   <span data-ttu-id="2e55a-139">遠端桌面服務 (終端機服務) 閘道 VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2e55a-139">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>
-   <span data-ttu-id="2e55a-140">遠端桌面服務 (終端機服務) 授權 VSS 寫入器</span><span class="sxs-lookup"><span data-stu-id="2e55a-140">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>

<span data-ttu-id="2e55a-141">這些寫入器記載于 [內建的 VSS 寫入](in-box-vss-writers.md)器中。</span><span class="sxs-lookup"><span data-stu-id="2e55a-141">These writers are documented in [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 



