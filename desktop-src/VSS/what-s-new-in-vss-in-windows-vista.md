---
description: Windows Vista。
ms.assetid: 3b16744d-b9c2-4462-a409-de94d9103c39
title: Windows Vista 中 VSS 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9e0780b092b2bed0235ba62377da9a4f7f0b53bded9e3f7feb5d412f5ab982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751140"
---
# <a name="whats-new-in-vss-in-windows-vista"></a>Windows Vista 中 VSS 的新功能

WindowsVista 對磁碟區陰影複製服務引進了下列變更。

請注意，Windows Vista 的所有變更也適用于 Windows Server 2008 和 Windows Vista Service Pack 1 (SP1) 。

## <a name="new-vss-interfaces"></a>新的 VSS 介面

[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[**IVssComponentEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[**IVssCreateWriterMetadataEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[**IVssDifferentialSoftwareSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[**IVssExamineWriterMetadataEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a>新的 VSS 類別

[**CVssWriterEx**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a>新的 VSS 列舉

[**VSS \_ 向前復原 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a>現有的 VSS 列舉修改

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_備份 \_ 架構**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) 列舉
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>已新增值：
</dt> <dd>

VSS \_ BS \_ 授權 \_ 還原

VSS \_ BS \_ 獨立 \_ 系統 \_ 狀態

VSS \_ BS \_ 還原 \_ 重新命名

VSS \_ BS \_ 向前復原 \_ 還原

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS \_元件 \_ 旗標**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags) 列舉
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>已新增值：
</dt> <dd>

VSS \_ CF \_ 非 \_ 系統 \_ 狀態

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_ VSS \_ 磁片區 \_ 快照集 \_ 屬性**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)列舉
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>已新增值：
</dt> <dd>

VSS \_ VOLSNAP \_ ATTR \_ 沒有自動 \_ 恢復

VSS \_ VOLSNAP \_ ATTR \_ 未 \_ 交易

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>VSS 事件追蹤和記錄

-   VSS 追蹤檔現在可以位於任何本機磁片區上。 在 Windows Vista 之前的 Windows 版本上，VSS 追蹤檔案無法位於陰影複製集中的磁片區上。
-   已改寫許多事件記錄檔專案，使其更清楚。
-   所有 VSS 事件記錄檔專案現在都包含內容資訊。

## <a name="vss-error-reporting"></a>VSS 錯誤報表

-   您現在可以藉由呼叫 [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) 函式，並在 \_ \_ \_ *dwFlags* 參數中指定 HMODULE 旗標的格式訊息，來取出所有 VSS 錯誤碼的描述。
-   VSS 錯誤碼訊息包含在 vsstrace.dll 中。 必須在 *lpSource* 參數中指定此模組的控制碼。

## <a name="excluding-files-from-shadow-copies"></a>排除陰影複製中的檔案

應用程式或服務可使用 FilesNotToSnapshot 登錄機碼來指定要從新建立的陰影複製中刪除的檔案。 如需詳細資訊，請參閱 [從陰影複製中排除](excluding-files-from-shadow-copies.md)檔案。

## <a name="backup-and-restore-application-compatibility"></a>備份與還原應用程式相容性

備份與還原應用程式的開發人員必須留意 Windows Vista 和 Windows Server 2008 中的某些新功能。 如需應用程式相容性檢查清單，請參閱 [備份和還原的應用程式相容性](application-compatibility-for-backup-and-restore.md)。

 

 
