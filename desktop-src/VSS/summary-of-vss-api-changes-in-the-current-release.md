---
description: Windows Server 2003 中的 VSS API 變更摘要
ms.assetid: 35572fc6-9147-4726-ae7a-d78292683ba0
title: Windows Server 2003 中的 VSS API 變更摘要
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9154da0ac67dd7a599064ed3b5cf1dc7285b0fb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971743"
---
# <a name="summary-of-vss-api-changes-in-windows-server-2003"></a><span data-ttu-id="0bcf7-103">Windows Server 2003 中的 VSS API 變更摘要</span><span class="sxs-lookup"><span data-stu-id="0bcf7-103">Summary of VSS API Changes in Windows Server 2003</span></span>

## <a name="changes-in-the-vss-service"></a><span data-ttu-id="0bcf7-104">VSS 服務中的變更</span><span class="sxs-lookup"><span data-stu-id="0bcf7-104">Changes in the VSS Service</span></span>

<dl> <dt>

<span data-ttu-id="0bcf7-105"><span id="Events_added_"></span><span id="events_added_"></span><span id="EVENTS_ADDED_"></span>新增的事件：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-105"><span id="Events_added_"></span><span id="events_added_"></span><span id="EVENTS_ADDED_"></span>Events added:</span></span>
</dt> <dd>

[<span data-ttu-id="0bcf7-106">*BackupShutdown*</span><span class="sxs-lookup"><span data-stu-id="0bcf7-106">*BackupShutdown*</span></span>](vssgloss-b.md)

</dd> </dl>

## <a name="changes-in-vss-functionality"></a><span data-ttu-id="0bcf7-107">VSS 功能的變更</span><span class="sxs-lookup"><span data-stu-id="0bcf7-107">Changes in VSS Functionality</span></span>

<dl> <dt>

<span data-ttu-id="0bcf7-108"><span id="Additional_functionality_"></span><span id="additional_functionality_"></span><span id="ADDITIONAL_FUNCTIONALITY_"></span>其他功能：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-108"><span id="Additional_functionality_"></span><span id="additional_functionality_"></span><span id="ADDITIONAL_FUNCTIONALITY_"></span>Additional functionality:</span></span>
</dt> <dd>

[<span data-ttu-id="0bcf7-109">*部分檔案支援*</span><span class="sxs-lookup"><span data-stu-id="0bcf7-109">*partial file support*</span></span>](vssgloss-p.md)

[<span data-ttu-id="0bcf7-110">*導向目標*</span><span class="sxs-lookup"><span data-stu-id="0bcf7-110">*directed targeting*</span></span>](vssgloss-d.md)

</dd> </dl>

## <a name="new-vss-interfaces"></a><span data-ttu-id="0bcf7-111">新的 VSS 介面</span><span class="sxs-lookup"><span data-stu-id="0bcf7-111">New VSS Interfaces</span></span>

[<span data-ttu-id="0bcf7-112">**IVssWMDependency**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-112">**IVssWMDependency**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="0bcf7-113">現有的 VSS 介面修改</span><span class="sxs-lookup"><span data-stu-id="0bcf7-113">Existing VSS Interface Modifications</span></span>

<dl> <dt>

<span data-ttu-id="0bcf7-114"><span id="IVssAsync_interface"></span><span id="ivssasync_interface"></span><span id="IVSSASYNC_INTERFACE"></span>[**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync) 介面</span><span class="sxs-lookup"><span data-stu-id="0bcf7-114"><span id="IVssAsync_interface"></span><span id="ivssasync_interface"></span><span id="IVSSASYNC_INTERFACE"></span>[**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="0bcf7-115"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>修改的方法：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-115"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Methods modified:</span></span>
</dt> <dd>

[<span data-ttu-id="0bcf7-116">**IVssAsync：： Wait**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-116">**IVssAsync::Wait**</span></span>](/windows/desktop/api/Vss/nf-vss-ivssasync-wait)

</dd> </dl> </dd> <dt>

<span data-ttu-id="0bcf7-117"><span id="IVssBackupComponents_interface"></span><span id="ivssbackupcomponents_interface"></span><span id="IVSSBACKUPCOMPONENTS_INTERFACE"></span>[**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面</span><span class="sxs-lookup"><span data-stu-id="0bcf7-117"><span id="IVssBackupComponents_interface"></span><span id="ivssbackupcomponents_interface"></span><span id="IVSSBACKUPCOMPONENTS_INTERFACE"></span>[**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="0bcf7-118"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>新增的方法：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-118"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="0bcf7-119">**>ivssbackupcomponents：： AddNewTarget**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-119">**IVssBackupComponents::AddNewTarget**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)

[<span data-ttu-id="0bcf7-120">**>ivssbackupcomponents：： QueryRevertStatus**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-120">**IVssBackupComponents::QueryRevertStatus**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-queryrevertstatus)

[<span data-ttu-id="0bcf7-121">**>ivssbackupcomponents：： RevertToSnapshot**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-121">**IVssBackupComponents::RevertToSnapshot**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-reverttosnapshot)

[<span data-ttu-id="0bcf7-122">**>ivssbackupcomponents：： SetRangesFilePath**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-122">**IVssBackupComponents::SetRangesFilePath**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)

[<span data-ttu-id="0bcf7-123">**>ivssbackupcomponents：： SetRestoreState**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-123">**IVssBackupComponents::SetRestoreState**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)

</dd> </dl> </dd> <dt>

<span data-ttu-id="0bcf7-124"><span id="IVssCreateWriterMetadata_interface"></span><span id="ivsscreatewritermetadata_interface"></span><span id="IVSSCREATEWRITERMETADATA_INTERFACE"></span>[**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) 介面</span><span class="sxs-lookup"><span data-stu-id="0bcf7-124"><span id="IVssCreateWriterMetadata_interface"></span><span id="ivsscreatewritermetadata_interface"></span><span id="IVSSCREATEWRITERMETADATA_INTERFACE"></span>[**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="0bcf7-125"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>新增的方法：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-125"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="0bcf7-126">**IVssCreateWriterMetadata：： AddComponentDependency**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-126">**IVssCreateWriterMetadata::AddComponentDependency**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency)

[<span data-ttu-id="0bcf7-127">**IVssCreateWriterMetadata：： SetBackupSchema**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-127">**IVssCreateWriterMetadata::SetBackupSchema**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)

</dd> <dt>

<span data-ttu-id="0bcf7-128"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>修改的方法：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-128"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Methods modified:</span></span>
</dt> <dd>

[<span data-ttu-id="0bcf7-129">**IVssCreateWriterMetadata：： AddComponent**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-129">**IVssCreateWriterMetadata::AddComponent**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)

[<span data-ttu-id="0bcf7-130">**IVssCreateWriterMetadata：： AddDatabaseFiles**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-130">**IVssCreateWriterMetadata::AddDatabaseFiles**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)

[<span data-ttu-id="0bcf7-131">**IVssCreateWriterMetadata：： AddDatabaseLogFiles**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-131">**IVssCreateWriterMetadata::AddDatabaseLogFiles**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)

[<span data-ttu-id="0bcf7-132">**IVssCreateWriterMetadata：： AddFilesToFileGroup**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-132">**IVssCreateWriterMetadata::AddFilesToFileGroup**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)

</dd> </dl> </dd> <dt>

<span data-ttu-id="0bcf7-133"><span id="IVssExamineWriterMetadata_interface"></span><span id="ivssexaminewritermetadata_interface"></span><span id="IVSSEXAMINEWRITERMETADATA_INTERFACE"></span>[**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) 介面</span><span class="sxs-lookup"><span data-stu-id="0bcf7-133"><span id="IVssExamineWriterMetadata_interface"></span><span id="ivssexaminewritermetadata_interface"></span><span id="IVSSEXAMINEWRITERMETADATA_INTERFACE"></span>[**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="0bcf7-134"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>新增的方法：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-134"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="0bcf7-135">**IVssExamineWriterMetadata::GetBackupSchema**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-135">**IVssExamineWriterMetadata::GetBackupSchema**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)

</dd> </dl> </dd> <dt>

<span data-ttu-id="0bcf7-136"><span id="IVssComponent_interface"></span><span id="ivsscomponent_interface"></span><span id="IVSSCOMPONENT_INTERFACE"></span>[**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面</span><span class="sxs-lookup"><span data-stu-id="0bcf7-136"><span id="IVssComponent_interface"></span><span id="ivsscomponent_interface"></span><span id="IVSSCOMPONENT_INTERFACE"></span>[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="0bcf7-137"><span id="Methods_removed_"></span><span id="methods_removed_"></span><span id="METHODS_REMOVED_"></span>移除的方法：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-137"><span id="Methods_removed_"></span><span id="methods_removed_"></span><span id="METHODS_REMOVED_"></span>Methods removed:</span></span>
</dt> <dd>

<span data-ttu-id="0bcf7-138">**>ivsscomponent：： AddNewTarget**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-138">**IVssComponent::AddNewTarget**</span></span>

</dd> <dt>

<span data-ttu-id="0bcf7-139"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>新增的方法：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-139"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="0bcf7-140">**>ivsscomponent：： AddDifferencedFilesByLastModifyTime**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-140">**IVssComponent::AddDifferencedFilesByLastModifyTime**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)

[<span data-ttu-id="0bcf7-141">**>ivsscomponent：： GetDifferencedFile**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-141">**IVssComponent::GetDifferencedFile**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)

[<span data-ttu-id="0bcf7-142">**>ivsscomponent：： GetDifferencedFilesCount**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-142">**IVssComponent::GetDifferencedFilesCount**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)

</dd> <dt>

<span data-ttu-id="0bcf7-143"><span id="Methods_no_longer_reserved_"></span><span id="methods_no_longer_reserved_"></span><span id="METHODS_NO_LONGER_RESERVED_"></span>不再保留的方法：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-143"><span id="Methods_no_longer_reserved_"></span><span id="methods_no_longer_reserved_"></span><span id="METHODS_NO_LONGER_RESERVED_"></span>Methods no longer reserved:</span></span>
</dt> <dd>

[<span data-ttu-id="0bcf7-144">**>ivsscomponent：： AddDirectedTarget**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-144">**IVssComponent::AddDirectedTarget**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)

[<span data-ttu-id="0bcf7-145">**>ivsscomponent：： GetDirectedTarget**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-145">**IVssComponent::GetDirectedTarget**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)

</dd> </dl> </dd> <dt>

<span data-ttu-id="0bcf7-146"><span id="IVssWMComponent_interface"></span><span id="ivsswmcomponent_interface"></span><span id="IVSSWMCOMPONENT_INTERFACE"></span>[**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) 介面</span><span class="sxs-lookup"><span data-stu-id="0bcf7-146"><span id="IVssWMComponent_interface"></span><span id="ivsswmcomponent_interface"></span><span id="IVSSWMCOMPONENT_INTERFACE"></span>[**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="0bcf7-147"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>新增的方法：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-147"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="0bcf7-148">**IVssWMComponent::GetDependency**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-148">**IVssWMComponent::GetDependency**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency)

</dd> </dl> </dd> <dt>

<span data-ttu-id="0bcf7-149"><span id="IVssWMFiledesc_interface"></span><span id="ivsswmfiledesc_interface"></span><span id="IVSSWMFILEDESC_INTERFACE"></span>[**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) 介面</span><span class="sxs-lookup"><span data-stu-id="0bcf7-149"><span id="IVssWMFiledesc_interface"></span><span id="ivsswmfiledesc_interface"></span><span id="IVSSWMFILEDESC_INTERFACE"></span>[**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="0bcf7-150"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>新增的方法：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-150"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="0bcf7-151">**IVssWMFiledesc::GetBackupTypeMask**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-151">**IVssWMFiledesc::GetBackupTypeMask**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)

</dd> </dl> </dd> </dl>

## <a name="existing-vss-class-modifications"></a><span data-ttu-id="0bcf7-152">現有的 VSS 類別修改</span><span class="sxs-lookup"><span data-stu-id="0bcf7-152">Existing VSS Class Modifications</span></span>

<dl> <dt>

<span data-ttu-id="0bcf7-153"><span id="CVssWriter_class"></span><span id="cvsswriter_class"></span><span id="CVSSWRITER_CLASS"></span>[**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) 類別</span><span class="sxs-lookup"><span data-stu-id="0bcf7-153"><span id="CVssWriter_class"></span><span id="cvsswriter_class"></span><span id="CVSSWRITER_CLASS"></span>[**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) class</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="0bcf7-154"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>修改的方法：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-154"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Methods modified:</span></span>
</dt> <dd>

[<span data-ttu-id="0bcf7-155">**CVssWriter：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-155">**CVssWriter::Initialize**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)

</dd> <dt>

<span data-ttu-id="0bcf7-156"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>新增的方法：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-156"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="0bcf7-157">**CVssWriter：： GetCoNtext**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-157">**CVssWriter::GetContext**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext)

[<span data-ttu-id="0bcf7-158">**CVssWriter::GetRestoreType**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-158">**CVssWriter::GetRestoreType**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)

[<span data-ttu-id="0bcf7-159">**CVssWriter::GetSnapshotDeviceName**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-159">**CVssWriter::GetSnapshotDeviceName**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)

[<span data-ttu-id="0bcf7-160">**CVssWriter::OnBackupShutdown**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-160">**CVssWriter::OnBackupShutdown**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)

</dd> </dl> </dd> </dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="0bcf7-161">新的 VSS 列舉</span><span class="sxs-lookup"><span data-stu-id="0bcf7-161">New VSS Enumerations</span></span>

<dl> <dt>

<span data-ttu-id="0bcf7-162"><span id="VSS_BACKUP_SCHEMA"></span><span id="vss_backup_schema"></span>[**VSS \_ 備份 \_ 架構**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)</span><span class="sxs-lookup"><span data-stu-id="0bcf7-162"><span id="VSS_BACKUP_SCHEMA"></span><span id="vss_backup_schema"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0bcf7-163"><span id="VSS_COMPONENT_FLAGS"></span><span id="vss_component_flags"></span>[**VSS \_ 元件 \_ 旗標**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)</span><span class="sxs-lookup"><span data-stu-id="0bcf7-163"><span id="VSS_COMPONENT_FLAGS"></span><span id="vss_component_flags"></span>[**VSS\_COMPONENT\_FLAGS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0bcf7-164"><span id="VSS_FILE_SPEC_BACKUP_TYPE"></span><span id="vss_file_spec_backup_type"></span>[**VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)</span><span class="sxs-lookup"><span data-stu-id="0bcf7-164"><span id="VSS_FILE_SPEC_BACKUP_TYPE"></span><span id="vss_file_spec_backup_type"></span>[**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0bcf7-165"><span id="VSS_RESTORE_TYPE"></span><span id="vss_restore_type"></span>[**VSS \_ 還原 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)</span><span class="sxs-lookup"><span data-stu-id="0bcf7-165"><span id="VSS_RESTORE_TYPE"></span><span id="vss_restore_type"></span>[**VSS\_RESTORE\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)</span></span>
<span data-ttu-id="0bcf7-166"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0bcf7-166"></dt> <dd></dd> </dl></span></span>

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="0bcf7-167">現有的 VSS 列舉修改</span><span class="sxs-lookup"><span data-stu-id="0bcf7-167">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="0bcf7-168"><span id="VSS_BACKUP_TYPE_enumeration"></span><span id="vss_backup_type_enumeration"></span><span id="VSS_BACKUP_TYPE_ENUMERATION"></span>[**VSS \_備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) 列舉</span><span class="sxs-lookup"><span data-stu-id="0bcf7-168"><span id="VSS_BACKUP_TYPE_enumeration"></span><span id="vss_backup_type_enumeration"></span><span id="VSS_BACKUP_TYPE_ENUMERATION"></span>[**VSS\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="0bcf7-169"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>已新增值：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-169"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="0bcf7-170">VSS \_ BT \_ 複製</span><span class="sxs-lookup"><span data-stu-id="0bcf7-170">VSS\_BT\_COPY</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0bcf7-171"><span id="VSS_RESTORE_TARGET_enumeration"></span><span id="vss_restore_target_enumeration"></span><span id="VSS_RESTORE_TARGET_ENUMERATION"></span>[**VSS \_還原 \_ 目標**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target) 列舉</span><span class="sxs-lookup"><span data-stu-id="0bcf7-171"><span id="VSS_RESTORE_TARGET_enumeration"></span><span id="vss_restore_target_enumeration"></span><span id="VSS_RESTORE_TARGET_ENUMERATION"></span>[**VSS\_RESTORE\_TARGET**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="0bcf7-172"><span id="Removed_values_"></span><span id="removed_values_"></span><span id="REMOVED_VALUES_"></span>已移除值：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-172"><span id="Removed_values_"></span><span id="removed_values_"></span><span id="REMOVED_VALUES_"></span>Removed values:</span></span>
</dt> <dd>

<span data-ttu-id="0bcf7-173">VSS \_ RT \_ 新增</span><span class="sxs-lookup"><span data-stu-id="0bcf7-173">VSS\_RT\_NEW</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0bcf7-174"><span id="VSS_RESTOREMETHOD_ENUM_enumeration"></span><span id="vss_restoremethod_enum_enumeration"></span><span id="VSS_RESTOREMETHOD_ENUM_ENUMERATION"></span>[**VSS \_RESTOREMETHOD \_ 列舉**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) 列舉</span><span class="sxs-lookup"><span data-stu-id="0bcf7-174"><span id="VSS_RESTOREMETHOD_ENUM_enumeration"></span><span id="vss_restoremethod_enum_enumeration"></span><span id="VSS_RESTOREMETHOD_ENUM_ENUMERATION"></span>[**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="0bcf7-175"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>已新增值：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-175"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="0bcf7-176">\_ \_ \_ \_ \_ 如果 \_ 無法 \_ 取代，則在重新開機時還原 VSS RME</span><span class="sxs-lookup"><span data-stu-id="0bcf7-176">VSS\_RME\_RESTORE\_AT\_REBOOT\_IF\_CANNOT\_REPLACE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0bcf7-177"><span id="VSS_SNAPSHOT_STATE_enumeration"></span><span id="vss_snapshot_state_enumeration"></span><span id="VSS_SNAPSHOT_STATE_ENUMERATION"></span>[**VSS \_快照集 \_ 狀態**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state) 列舉</span><span class="sxs-lookup"><span data-stu-id="0bcf7-177"><span id="VSS_SNAPSHOT_STATE_enumeration"></span><span id="vss_snapshot_state_enumeration"></span><span id="VSS_SNAPSHOT_STATE_ENUMERATION"></span>[**VSS\_SNAPSHOT\_STATE**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="0bcf7-178"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>已新增值：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-178"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="0bcf7-179">VSS \_ SS \_ 處理 \_ POSTCOMMIT</span><span class="sxs-lookup"><span data-stu-id="0bcf7-179">VSS\_SS\_PROCESSING\_POSTCOMMIT</span></span>

<span data-ttu-id="0bcf7-180">VSS \_ SS \_ 處理 \_ PREFINALCOMMIT</span><span class="sxs-lookup"><span data-stu-id="0bcf7-180">VSS\_SS\_PROCESSING\_PREFINALCOMMIT</span></span>

<span data-ttu-id="0bcf7-181">VSS \_ SS \_ PREFINALCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="0bcf7-181">VSS\_SS\_PREFINALCOMMITTED</span></span>

<span data-ttu-id="0bcf7-182">VSS \_ SS \_ 處理 \_ POSTFINALCOMMIT</span><span class="sxs-lookup"><span data-stu-id="0bcf7-182">VSS\_SS\_PROCESSING\_POSTFINALCOMMIT</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0bcf7-183"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_ VSS \_ 磁片區 \_ 快照集 \_ 屬性**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)列舉</span><span class="sxs-lookup"><span data-stu-id="0bcf7-183"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="0bcf7-184"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>已新增值：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-184"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="0bcf7-185">VSS \_ VOLSNAP \_ ATTR \_ 自動回復</span><span class="sxs-lookup"><span data-stu-id="0bcf7-185">VSS\_VOLSNAP\_ATTR\_AUTORECOVER</span></span>

</dd> <dt>

<span data-ttu-id="0bcf7-186"><span id="Reserved_values_now_support_"></span><span id="reserved_values_now_support_"></span><span id="RESERVED_VALUES_NOW_SUPPORT_"></span>保留值現在支援：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-186"><span id="Reserved_values_now_support_"></span><span id="reserved_values_now_support_"></span><span id="RESERVED_VALUES_NOW_SUPPORT_"></span>Reserved values now support:</span></span>
</dt> <dd>

<span data-ttu-id="0bcf7-187">VSS \_ VOLSNAP \_ ATTR \_ 硬體 \_ 輔助</span><span class="sxs-lookup"><span data-stu-id="0bcf7-187">VSS\_VOLSNAP\_ATTR\_HARDWARE\_ASSISTED</span></span>

<span data-ttu-id="0bcf7-188">已匯 \_ 入 VSS VOLSNAP \_ ATTR \_</span><span class="sxs-lookup"><span data-stu-id="0bcf7-188">VSS\_VOLSNAP\_ATTR\_IMPORTED</span></span>

<span data-ttu-id="0bcf7-189">在 \_ \_ \_ 本機公開的 VSS VOLSNAP ATTR \_</span><span class="sxs-lookup"><span data-stu-id="0bcf7-189">VSS\_VOLSNAP\_ATTR\_EXPOSED\_LOCALLY</span></span>

<span data-ttu-id="0bcf7-190">遠端公開的 VSS \_ VOLSNAP \_ ATTR \_ \_</span><span class="sxs-lookup"><span data-stu-id="0bcf7-190">VSS\_VOLSNAP\_ATTR\_EXPOSED\_REMOTELY</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0bcf7-191"><span id="VSS_WRITER_STATE_enumeration"></span><span id="vss_writer_state_enumeration"></span><span id="VSS_WRITER_STATE_ENUMERATION"></span>[**VSS \_寫入器 \_ 狀態**](/windows/desktop/api/Vss/ne-vss-vss_writer_state) 列舉</span><span class="sxs-lookup"><span data-stu-id="0bcf7-191"><span id="VSS_WRITER_STATE_enumeration"></span><span id="vss_writer_state_enumeration"></span><span id="VSS_WRITER_STATE_ENUMERATION"></span>[**VSS\_WRITER\_STATE**](/windows/desktop/api/Vss/ne-vss-vss_writer_state) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="0bcf7-192"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>已新增值：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-192"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="0bcf7-193">VSS \_ WS-MANAGEMENT \_ \_ 在 \_ BACKUPSHUTDOWN 失敗</span><span class="sxs-lookup"><span data-stu-id="0bcf7-193">VSS\_WS\_FAILED\_AT\_BACKUPSHUTDOWN</span></span>

</dd> </dl> </dd> </dl>

## <a name="changes-to-vss-structures"></a><span data-ttu-id="0bcf7-194">VSS 結構的變更</span><span class="sxs-lookup"><span data-stu-id="0bcf7-194">Changes to VSS Structures</span></span>

<dl> <dt>

<span data-ttu-id="0bcf7-195"><span id="VSS_COMPONENTINFO_structure"></span><span id="vss_componentinfo_structure"></span><span id="VSS_COMPONENTINFO_STRUCTURE"></span>[**VSS \_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) 結構</span><span class="sxs-lookup"><span data-stu-id="0bcf7-195"><span id="VSS_COMPONENTINFO_structure"></span><span id="vss_componentinfo_structure"></span><span id="VSS_COMPONENTINFO_STRUCTURE"></span>[**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="0bcf7-196"><span id="Added_members_"></span><span id="added_members_"></span><span id="ADDED_MEMBERS_"></span>新增的成員：</span><span class="sxs-lookup"><span data-stu-id="0bcf7-196"><span id="Added_members_"></span><span id="added_members_"></span><span id="ADDED_MEMBERS_"></span>Added members:</span></span>
</dt> <dd>

<span data-ttu-id="0bcf7-197">**bSelectableForRestore**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-197">**bSelectableForRestore**</span></span>

<span data-ttu-id="0bcf7-198">**dwComponentFlags**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-198">**dwComponentFlags**</span></span>

<span data-ttu-id="0bcf7-199">**cDependencies**</span><span class="sxs-lookup"><span data-stu-id="0bcf7-199">**cDependencies**</span></span>

</dd> </dl> </dd> </dl>

 

 



