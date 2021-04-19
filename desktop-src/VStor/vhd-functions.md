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
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span id="vhd.vhd_functions"></span>虛擬磁片功能

虛擬磁片中使用下列函式：

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>本節內容

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></p></td>
<td><p>針對 VHD 設定檔案套用目前虛擬磁片的快照集。</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></p></td>
<td><p>將父系附加至以 <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> 旗標開啟的虛擬磁片。</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></p></td>
<td><p>藉由尋找適當的 VHD 提供者來完成附件，將虛擬硬碟 (VHD) 或 CD 或 DVD 影像檔案 (ISO) 。</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></p></td>
<td><p>中斷先前初始化的鏡像作業，並將鏡像設定為使用中的虛擬磁片。</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></p></td>
<td><p>減少虛擬硬碟 (VHD) 備份存放區檔案的大小。</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></p></td>
<td><p>使用預設參數或使用現有的虛擬磁片或實體磁片，建立虛擬硬碟 (VHD) 影像檔案。</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></p></td>
<td><p>從 VHD 設定檔案刪除快照集。</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></p></td>
<td><p>從虛擬磁片刪除中繼資料。</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></p></td>
<td><p>藉由尋找適當的虛擬磁片提供者來完成作業，將虛擬硬碟 (VHD) 或 CD 或 DVD 影像檔案 (ISO) 。</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></p></td>
<td><p>列舉與虛擬磁片相關聯的中繼資料。</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></p></td>
<td><p>增加固定或可動態擴充的虛擬硬碟 (VHD) 的大小。</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></p></td>
<td><p>傳回虛擬硬碟 (Vhd) 或 CD 或 DVD 映射檔案之間的關聯 (ISO) 或這些磁片中包含的磁片區及其父磁片或磁片區。</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></p></td>
<td><p>捕獲 VHD 的相關資訊。</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></p></td>
<td><p>從虛擬磁片抓取指定的中繼資料。</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></p></td>
<td><p>檢查非同步虛擬硬碟 (VHD) 操作的進度。</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></p></td>
<td><p>抓取實體裝置物件的路徑，其中包含虛擬硬碟 (VHD) 或 CD 或 DVD 影像檔 (ISO) 。</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></p></td>
<td><p>使用鏈中的一或多個父虛擬磁片，合併差異鏈中的子虛擬硬碟 (VHD) 。</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></p></td>
<td><p>起始虛擬磁片的鏡像作業。</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></p></td>
<td><p>修改虛擬磁片檔案的內部內容。 可以用來設定使用中分葉或修正快照集專案。</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></p></td>
<td><p>開啟虛擬硬碟 (VHD) 或 CD 或 DVD 影像檔 (ISO) 以供使用。</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></p></td>
<td><p>抓取復原變更追蹤 (.RCT) 所追蹤之虛擬硬碟的指定區域變更的相關資訊 (VHD) 。</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></p></td>
<td><p>直接向虛擬硬碟發出內嵌的 SCSI 要求。</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></p></td>
<td><p>調整虛擬磁片的大小。</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></p></td>
<td><p>設定虛擬硬碟 (VHD) 的相關資訊。</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></p></td>
<td><p>設定虛擬磁片的中繼資料專案。</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></p></td>
<td><p>為 VHD 設定檔案的目前虛擬磁片建立快照集。</p></td>
</tr>
</tbody>
</table>

 

 

 
