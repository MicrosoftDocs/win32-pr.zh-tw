---
description: Windows Server 2008。
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: Windows Server 2008 和 Windows Vista SP1 中 VSS 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ee109eec31c084dc43fb9e0cc6341f443a16e6aa06ac989a7f328d9bb3011f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006118"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a>Windows Server 2008 和 Windows Vista SP1 中 VSS 的新功能

WindowsServer 2008 和 Windows Vista （含 Service Pack 1） (SP1) 對磁碟區陰影複製服務引進下列變更。

> [!Note]  
> Windows Vista 的所有變更適用于 Windows Server 2008 和 Windows Vista SP1。 如需這些變更的詳細資訊，請參閱[Windows Vista 中 VSS 的新功能](what-s-new-in-vss-in-windows-vista.md)。

 

-   [新的 VSS 介面](#new-vss-interfaces)
-   [新的 VSS 列舉](#new-vss-enumerations)
-   [新的 VSS 結構](#new-vss-structures)
-   [現有的 VSS 列舉修改](#existing-vss-enumeration-modifications)
-   [現有的 VSS 介面修改](#existing-vss-interface-modifications)
-   [新的 VSS 寫入器](#new-vss-writers)

## <a name="new-vss-interfaces"></a>新的 VSS 介面

<dl>

[**IVssDifferentialSoftwareSnapshotMgmt3**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a>新的 VSS 列舉

<dl>

[**\_VSS \_ 硬體 \_ 選項**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[**VSS \_ 保護 \_ 錯誤**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[**VSS \_ 保護 \_ 層級**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a>新的 VSS 結構

<dl>

[**VSS \_ 磁片區 \_ 保護 \_ 資訊**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a>現有的 VSS 列舉修改

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_備份 \_ 架構**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) 列舉
</dt> <dd>

<dl> <dt>

<span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>已新增值：
</dt> <dd>

VSS \_ BS \_ 寫入器 \_ 支援 \_ 平行 \_ 還原

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_ VSS \_ 磁片區 \_ 快照集 \_ 屬性**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)列舉
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>已新增值：
</dt> <dd>

VSS \_ VOLSNAP \_ ATTR \_ 延遲 \_ POSTSNAPSHOT

VSS \_ VOLSNAP \_ ATTR \_ TXF \_ 復原

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a>現有的 VSS 介面修改

<dl> <dt>

<span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2) 介面
</dt> <dd>

<dl> <dt>

<span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>新增的方法：
</dt> <dd>

[**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a>新的 VSS 寫入器

WindowsServer 2008 和 Windows Vista SP1 引進下列 VSS 寫入器：

-   IIS 設定寫入器
-   IIS 元資料庫寫入器
-   NPS VSS 寫入器
-   遠端桌面服務 (終端機服務) 閘道 VSS 寫入器
-   遠端桌面服務 (終端機服務) 授權 VSS 寫入器

這些寫入器記載于 [內建的 VSS 寫入](in-box-vss-writers.md)器中。

 

 



