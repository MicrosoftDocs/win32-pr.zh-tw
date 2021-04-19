---
description: Windows Vista。
ms.assetid: 3b16744d-b9c2-4462-a409-de94d9103c39
title: Windows Vista 中 VSS 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 122caa350ede984d5b05eb7eedd6039d82a76f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972226"
---
# <a name="whats-new-in-vss-in-windows-vista"></a><span data-ttu-id="22354-103">Windows Vista 中 VSS 的新功能</span><span class="sxs-lookup"><span data-stu-id="22354-103">What's New in VSS in Windows Vista</span></span>

<span data-ttu-id="22354-104">Windows Vista 對磁碟區陰影複製服務引進了下列變更。</span><span class="sxs-lookup"><span data-stu-id="22354-104">Windows Vista introduces the following changes to the Volume Shadow Copy Service.</span></span>

<span data-ttu-id="22354-105">請注意，Windows Vista 的所有變更也適用于 Windows Server 2008 和 Windows Vista Service Pack 1 (SP1) 。</span><span class="sxs-lookup"><span data-stu-id="22354-105">Note that all changes for Windows Vista also apply to Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

## <a name="new-vss-interfaces"></a><span data-ttu-id="22354-106">新的 VSS 介面</span><span class="sxs-lookup"><span data-stu-id="22354-106">New VSS Interfaces</span></span>

[<span data-ttu-id="22354-107">**IVssBackupComponentsEx2**</span><span class="sxs-lookup"><span data-stu-id="22354-107">**IVssBackupComponentsEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[<span data-ttu-id="22354-108">**IVssComponentEx**</span><span class="sxs-lookup"><span data-stu-id="22354-108">**IVssComponentEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[<span data-ttu-id="22354-109">**IVssCreateWriterMetadataEx**</span><span class="sxs-lookup"><span data-stu-id="22354-109">**IVssCreateWriterMetadataEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[<span data-ttu-id="22354-110">**IVssDifferentialSoftwareSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="22354-110">**IVssDifferentialSoftwareSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[<span data-ttu-id="22354-111">**IVssExamineWriterMetadataEx2**</span><span class="sxs-lookup"><span data-stu-id="22354-111">**IVssExamineWriterMetadataEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a><span data-ttu-id="22354-112">新的 VSS 類別</span><span class="sxs-lookup"><span data-stu-id="22354-112">New VSS Classes</span></span>

[<span data-ttu-id="22354-113">**CVssWriterEx**</span><span class="sxs-lookup"><span data-stu-id="22354-113">**CVssWriterEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a><span data-ttu-id="22354-114">新的 VSS 列舉</span><span class="sxs-lookup"><span data-stu-id="22354-114">New VSS Enumerations</span></span>

[<span data-ttu-id="22354-115">**VSS \_ 向前復原 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="22354-115">**VSS\_ROLLFORWARD\_TYPE**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="22354-116">現有的 VSS 列舉修改</span><span class="sxs-lookup"><span data-stu-id="22354-116">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="22354-117"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_備份 \_ 架構**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) 列舉</span><span class="sxs-lookup"><span data-stu-id="22354-117"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="22354-118"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>已新增值：</span><span class="sxs-lookup"><span data-stu-id="22354-118"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="22354-119">VSS \_ BS \_ 授權 \_ 還原</span><span class="sxs-lookup"><span data-stu-id="22354-119">VSS\_BS\_AUTHORITATIVE\_RESTORE</span></span>

<span data-ttu-id="22354-120">VSS \_ BS \_ 獨立 \_ 系統 \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="22354-120">VSS\_BS\_INDEPENDENT\_SYSTEM\_STATE</span></span>

<span data-ttu-id="22354-121">VSS \_ BS \_ 還原 \_ 重新命名</span><span class="sxs-lookup"><span data-stu-id="22354-121">VSS\_BS\_RESTORE\_RENAME</span></span>

<span data-ttu-id="22354-122">VSS \_ BS \_ 向前復原 \_ 還原</span><span class="sxs-lookup"><span data-stu-id="22354-122">VSS\_BS\_ROLLFORWARD\_RESTORE</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="22354-123"><span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS \_元件 \_ 旗標**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags) 列舉</span><span class="sxs-lookup"><span data-stu-id="22354-123"><span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS\_COMPONENT\_FLAGS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="22354-124"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>已新增值：</span><span class="sxs-lookup"><span data-stu-id="22354-124"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="22354-125">VSS \_ CF \_ 非 \_ 系統 \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="22354-125">VSS\_CF\_NOT\_SYSTEM\_STATE</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="22354-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_ VSS \_ 磁片區 \_ 快照集 \_ 屬性**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)列舉</span><span class="sxs-lookup"><span data-stu-id="22354-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="22354-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>已新增值：</span><span class="sxs-lookup"><span data-stu-id="22354-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="22354-128">VSS \_ VOLSNAP \_ ATTR \_ 沒有自動 \_ 恢復</span><span class="sxs-lookup"><span data-stu-id="22354-128">VSS\_VOLSNAP\_ATTR\_NO\_AUTORECOVERY</span></span>

<span data-ttu-id="22354-129">VSS \_ VOLSNAP \_ ATTR \_ 未 \_ 交易</span><span class="sxs-lookup"><span data-stu-id="22354-129">VSS\_VOLSNAP\_ATTR\_NOT\_TRANSACTED</span></span>

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a><span data-ttu-id="22354-130">VSS 事件追蹤和記錄</span><span class="sxs-lookup"><span data-stu-id="22354-130">VSS Event Tracing and Logging</span></span>

-   <span data-ttu-id="22354-131">VSS 追蹤檔現在可以位於任何本機磁片區上。</span><span class="sxs-lookup"><span data-stu-id="22354-131">The VSS trace file can now be located on any local volume.</span></span> <span data-ttu-id="22354-132">在 Windows Vista 之前的 Windows 版本上，VSS 追蹤檔案無法位於陰影複製集中的磁片區上。</span><span class="sxs-lookup"><span data-stu-id="22354-132">On versions of Windows prior to Windows Vista, the VSS trace file could not be located on a volume that was in the shadow copy set.</span></span>
-   <span data-ttu-id="22354-133">已改寫許多事件記錄檔專案，使其更清楚。</span><span class="sxs-lookup"><span data-stu-id="22354-133">Many event log entries have been reworded to make them clearer.</span></span>
-   <span data-ttu-id="22354-134">所有 VSS 事件記錄檔專案現在都包含內容資訊。</span><span class="sxs-lookup"><span data-stu-id="22354-134">All VSS event log entries now contain context information.</span></span>

## <a name="vss-error-reporting"></a><span data-ttu-id="22354-135">VSS 錯誤報表</span><span class="sxs-lookup"><span data-stu-id="22354-135">VSS Error Reporting</span></span>

-   <span data-ttu-id="22354-136">您現在可以藉由呼叫 [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) 函式，並在 \_ \_ \_ *dwFlags* 參數中指定 HMODULE 旗標的格式訊息，來取出所有 VSS 錯誤碼的描述。</span><span class="sxs-lookup"><span data-stu-id="22354-136">Descriptions of all VSS error codes can now be retrieved by calling the [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_HMODULE flag specified in the *dwFlags* parameter.</span></span>
-   <span data-ttu-id="22354-137">VSS 錯誤碼訊息包含在 vsstrace.dll 中。</span><span class="sxs-lookup"><span data-stu-id="22354-137">The VSS error code messages are contained in vsstrace.dll.</span></span> <span data-ttu-id="22354-138">必須在 *lpSource* 參數中指定此模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="22354-138">A handle to this module must be specified in the *lpSource* parameter.</span></span>

## <a name="excluding-files-from-shadow-copies"></a><span data-ttu-id="22354-139">排除陰影複製中的檔案</span><span class="sxs-lookup"><span data-stu-id="22354-139">Excluding Files from Shadow Copies</span></span>

<span data-ttu-id="22354-140">應用程式或服務可使用 FilesNotToSnapshot 登錄機碼來指定要從新建立的陰影複製中刪除的檔案。</span><span class="sxs-lookup"><span data-stu-id="22354-140">Applications or services can use the FilesNotToSnapshot registry key to specify files to be deleted from newly created shadow copies.</span></span> <span data-ttu-id="22354-141">如需詳細資訊，請參閱 [從陰影複製中排除](excluding-files-from-shadow-copies.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="22354-141">For more information, see [Excluding Files from Shadow Copies](excluding-files-from-shadow-copies.md).</span></span>

## <a name="backup-and-restore-application-compatibility"></a><span data-ttu-id="22354-142">備份與還原應用程式相容性</span><span class="sxs-lookup"><span data-stu-id="22354-142">Backup and Restore Application Compatibility</span></span>

<span data-ttu-id="22354-143">備份與還原應用程式的開發人員必須瞭解 Windows Vista 和 Windows Server 2008 中的某些新功能。</span><span class="sxs-lookup"><span data-stu-id="22354-143">Developers of backup and restore applications need to be aware of certain new features in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="22354-144">如需應用程式相容性檢查清單，請參閱 [備份和還原的應用程式相容性](application-compatibility-for-backup-and-restore.md)。</span><span class="sxs-lookup"><span data-stu-id="22354-144">For an application compatibility checklist, see [Application Compatibility for Backup and Restore](application-compatibility-for-backup-and-restore.md).</span></span>

 

 
