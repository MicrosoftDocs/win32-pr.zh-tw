---
description: 深入瞭解： <span id=vhd.vhd_functions></span> 虛擬磁片功能
MS-HAID: vhd.vhd\_functions
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 虛擬磁片功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f31af2b24a55baa3c64bfe5bd9e09e0b9e2f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973469"
---
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span data-ttu-id="d1f8c-103"><span id="vhd.vhd_functions"></span>虛擬磁片功能</span><span class="sxs-lookup"><span data-stu-id="d1f8c-103"><span id="vhd.vhd_functions"></span>Virtual Disk Functions</span></span>

<span data-ttu-id="d1f8c-104">虛擬磁片中使用下列函式：</span><span class="sxs-lookup"><span data-stu-id="d1f8c-104">The following functions are used in Virtual Disks:</span></span>

## <a name="span-idin_this_sectionspanin-this-section"></a><span data-ttu-id="d1f8c-105"><span id="in_this_section"></span>本節內容</span><span class="sxs-lookup"><span data-stu-id="d1f8c-105"><span id="in_this_section"></span>In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d1f8c-106">主題</span><span class="sxs-lookup"><span data-stu-id="d1f8c-106">Topic</span></span></th>
<th><span data-ttu-id="d1f8c-107">描述</span><span class="sxs-lookup"><span data-stu-id="d1f8c-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1f8c-108"><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-108"><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-109">針對 VHD 設定檔案套用目前虛擬磁片的快照集。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-109">Applies a snapshot of the current virtual disk for VHD Set files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1f8c-110"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-110"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-111">將父系附加至以 <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> 旗標開啟的虛擬磁片。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-111">Attaches a parent to a virtual disk opened with the <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1f8c-112"><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-112"><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-113">藉由尋找適當的 VHD 提供者來完成附件，將虛擬硬碟 (VHD) 或 CD 或 DVD 影像檔案 (ISO) 。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-113">Attaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate VHD provider to accomplish the attachment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1f8c-114"><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-114"><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-115">中斷先前初始化的鏡像作業，並將鏡像設定為使用中的虛擬磁片。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-115">Breaks a previously initiated mirror operation and sets the mirror to be the active virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1f8c-116"><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-116"><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-117">減少虛擬硬碟 (VHD) 備份存放區檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-117">Reduces the size of a virtual hard disk (VHD) backing store file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1f8c-118"><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-118"><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-119">使用預設參數或使用現有的虛擬磁片或實體磁片，建立虛擬硬碟 (VHD) 影像檔案。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-119">Creates a virtual hard disk (VHD) image file, either using default parameters or using an existing virtual disk or physical disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1f8c-120"><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-120"><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-121">從 VHD 設定檔案刪除快照集。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-121">Deletes a snapshot from a VHD Set file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1f8c-122"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-122"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-123">從虛擬磁片刪除中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-123">Deletes metadata from a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1f8c-124"><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-124"><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-125">藉由尋找適當的虛擬磁片提供者來完成作業，將虛擬硬碟 (VHD) 或 CD 或 DVD 影像檔案 (ISO) 。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-125">Detaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate virtual disk provider to accomplish the operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1f8c-126"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-126"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-127">列舉與虛擬磁片相關聯的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-127">Enumerates the metadata associated with a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1f8c-128"><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-128"><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-129">增加固定或可動態擴充的虛擬硬碟 (VHD) 的大小。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-129">Increases the size of a fixed or dynamically expandable virtual hard disk (VHD).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1f8c-130"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-130"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-131">傳回虛擬硬碟 (Vhd) 或 CD 或 DVD 映射檔案之間的關聯 (ISO) 或這些磁片中包含的磁片區及其父磁片或磁片區。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-131">Returns the relationships between virtual hard disks (VHDs) or CD or DVD image file (ISO) or the volumes contained within those disks and their parent disk or volume.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1f8c-132"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-132"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-133">捕獲 VHD 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-133">Retrieves information about a VHD.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1f8c-134"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-134"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-135">從虛擬磁片抓取指定的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-135">Retrieves the specified metadata from the virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1f8c-136"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-136"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-137">檢查非同步虛擬硬碟 (VHD) 操作的進度。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-137">Checks the progress of an asynchronous virtual hard disk (VHD) operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1f8c-138"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-138"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-139">抓取實體裝置物件的路徑，其中包含虛擬硬碟 (VHD) 或 CD 或 DVD 影像檔 (ISO) 。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-139">Retrieves the path to the physical device object that contains a virtual hard disk (VHD) or CD or DVD image file (ISO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1f8c-140"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-140"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-141">使用鏈中的一或多個父虛擬磁片，合併差異鏈中的子虛擬硬碟 (VHD) 。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-141">Merges a child virtual hard disk (VHD) in a differencing chain with one or more parent virtual disks in the chain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1f8c-142"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-142"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-143">起始虛擬磁片的鏡像作業。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-143">Initiates a mirror operation for a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1f8c-144"><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-144"><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-145">修改虛擬磁片檔案的內部內容。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-145">Modifies the internal contents of a virtual disk file.</span></span> <span data-ttu-id="d1f8c-146">可以用來設定使用中分葉或修正快照集專案。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-146">Can be used to set the active leaf, or to fix up snapshot entries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1f8c-147"><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-147"><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-148">開啟虛擬硬碟 (VHD) 或 CD 或 DVD 影像檔 (ISO) 以供使用。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-148">Opens a virtual hard disk (VHD) or CD or DVD image file (ISO) for use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1f8c-149"><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-149"><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-150">抓取復原變更追蹤 (.RCT) 所追蹤之虛擬硬碟的指定區域變更的相關資訊 (VHD) 。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-150">Retrieves information about changes to the specified areas of a virtual hard disk (VHD) that are tracked by resilient change tracking (RCT).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1f8c-151"><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-151"><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-152">直接向虛擬硬碟發出內嵌的 SCSI 要求。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-152">Issues an embedded SCSI request directly to a virtual hard disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1f8c-153"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-153"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-154">調整虛擬磁片的大小。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-154">Resizes a virtual disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1f8c-155"><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-155"><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-156">設定虛擬硬碟 (VHD) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-156">Sets information about a virtual hard disk (VHD).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1f8c-157"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-157"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-158">設定虛擬磁片的中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-158">Sets a metadata item for a virtual disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1f8c-159"><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1f8c-159"><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="d1f8c-160">為 VHD 設定檔案的目前虛擬磁片建立快照集。</span><span class="sxs-lookup"><span data-stu-id="d1f8c-160">Creates a snapshot of the current virtual disk for VHD Set files.</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 
