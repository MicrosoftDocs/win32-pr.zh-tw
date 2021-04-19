---
description: 代表檔案或目錄（例如 Win32 \_ CodecFile 或 CIM 資料檔案）的 WMI 類別 \_ 包含 AccessMask 屬性。
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: '檔案和目錄存取權限常數 (Winnt. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0ddca31034ffde79fa9d9ff902a364cf07e311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999105"
---
# <a name="file-and-directory-access-rights-constants"></a><span data-ttu-id="b4dfd-103">檔案和目錄存取權限常數</span><span class="sxs-lookup"><span data-stu-id="b4dfd-103">File and Directory Access Rights Constants</span></span>

<span data-ttu-id="b4dfd-104">代表檔案或目錄（例如 [**Win32 \_ CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile) 或 [**CIM \_ 資料**](/windows/desktop/CIMWin32Prov/cim-datafile)檔）的 WMI 類別包含 **AccessMask** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-104">WMI classes that represent files or directories, such as [**Win32\_CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile) or [**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), contain an **AccessMask** property.</span></span> <span data-ttu-id="b4dfd-105">這個屬性包含的位設定會指定使用者或群組對於檔案的特定存取或作業必須擁有的存取權限。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-105">This property contains bit settings that specify the access rights a user or group must have for specific access or operations on the file.</span></span> <span data-ttu-id="b4dfd-106">如需詳細資訊，請參閱檔案 [安全性和存取權限](/windows/desktop/FileIO/file-security-and-access-rights) ，以及 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-106">For more information, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="b4dfd-107">包含 **AccessMask** 屬性的檔案或目錄類別包括：</span><span class="sxs-lookup"><span data-stu-id="b4dfd-107">The file or directory classes which contain an **AccessMask** property include:</span></span>

-   [<span data-ttu-id="b4dfd-108">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-108">**CIM\_DataFile**</span></span>](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [<span data-ttu-id="b4dfd-109">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-109">**CIM\_Directory**</span></span>](/windows/desktop/CIMWin32Prov/cim-directory)
-   [<span data-ttu-id="b4dfd-110">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-110">**CIM\_LogicalFile**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [<span data-ttu-id="b4dfd-111">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-111">**Win32\_CodecFile**</span></span>](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [<span data-ttu-id="b4dfd-112">**Win32 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-112">**Win32\_Directory**</span></span>](/windows/desktop/CIMWin32Prov/win32-directory)
-   <span data-ttu-id="b4dfd-113">[**Win32 \_ NTEventLogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b4dfd-113">[**Win32\_NTEventLogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))</span></span>
-   [<span data-ttu-id="b4dfd-114">**Win32 \_ 共用**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-114">**Win32\_Share**</span></span>](/windows/desktop/CIMWin32Prov/win32-share)
-   [<span data-ttu-id="b4dfd-115">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-115">**Win32\_ShortcutFile**</span></span>](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

<span data-ttu-id="b4dfd-116">下列清單列出 **AccessMask** 屬性中的檔案和目錄存取權限的值。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-116">The following list lists the values for file and directory access rights in the **AccessMask** property.</span></span> <span data-ttu-id="b4dfd-117">這個屬性是點陣圖。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-117">This property is a bitmap.</span></span>

<dl> <dt>

<span data-ttu-id="b4dfd-118"><span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**檔案 \_ 讀取 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-118"><span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**FILE\_READ\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-119">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-119">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-120">授與從檔案讀取資料的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-120">Grants the right to read data from the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-121"><span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**檔案 \_ 清單 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-121"><span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-122">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-122">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-123">授與從檔案讀取資料的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-123">Grants the right to read data from the file.</span></span> <span data-ttu-id="b4dfd-124">若為目錄，此值會授與許可權來列出目錄的內容。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-124">For a directory, this value grants the right to list the contents of the directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-125"><span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**檔案 \_ 寫入 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-125"><span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**FILE\_WRITE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-126">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-126">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-127">授與將資料寫入檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-127">Grants the right to write data to the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-128"><span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**檔案 \_ 新增 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-128"><span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**FILE\_ADD\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-129">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-129">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-130">授與將資料寫入檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-130">Grants the right to write data to the file.</span></span> <span data-ttu-id="b4dfd-131">若為目錄，此值會授與在目錄中建立檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-131">For a directory, this value grants the right to create a file in the directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-132"><span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**檔案 \_ 附加 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-132"><span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**FILE\_APPEND\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-133">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-133">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-134">授與將資料附加至檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-134">Grants the right to append data to the file.</span></span> <span data-ttu-id="b4dfd-135">若為目錄，此值會授與建立子目錄的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-135">For a directory, this value grants the right to create a subdirectory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-136"><span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**檔案 \_ 新增 \_ 子目錄**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-136"><span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-137">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-137">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-138">授與將資料附加至檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-138">Grants the right to append data to the file.</span></span> <span data-ttu-id="b4dfd-139">若為目錄，此值會授與建立子目錄的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-139">For a directory, this value grants the right to create a subdirectory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-140"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**檔案 \_ 讀取 \_ EA**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-140"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-141">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-141">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-142">授與讀取擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-142">Grants the right to read extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-143"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**檔案 \_ 寫入 \_ EA**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-143"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-144">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-144">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-145">授予寫入擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-145">Grants the right to write extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-146"><span id="FILE_EXECUTE"></span><span id="file_execute"></span>**檔案 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-146"><span id="FILE_EXECUTE"></span><span id="file_execute"></span>**FILE\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-147">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-147">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-148">授與許可權來執行檔案。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-148">Grants the right to execute a file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-149"><span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**檔案 \_ 遍歷**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-149"><span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**FILE\_TRAVERSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-150">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-150">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-151">授與許可權來執行檔案。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-151">Grants the right to execute a file.</span></span> <span data-ttu-id="b4dfd-152">若為目錄，可以進行目錄的往返。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-152">For a directory, the directory can be traversed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-153"><span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**檔案 \_ 刪除 \_ 子系**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-153"><span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-154">64 (0x40) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-154">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-155">授與刪除目錄的許可權，以及它所包含的所有檔案 (其子) ，即使檔案是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-155">Grants the right to delete a directory and all the files it contains (its children), even if the files are read-only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-156"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**檔案 \_ 讀取 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-156"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-157">128 (0x80) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-157">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-158">授與讀取檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-158">Grants the right to read file attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-159"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**檔案 \_ 寫入 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-159"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-160">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="b4dfd-160">256 (0x100)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-161">授與變更檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-161">Grants the right to change file attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-162"><span id="DELETE"></span><span id="delete"></span>**刪除**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-162"><span id="DELETE"></span><span id="delete"></span>**DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-163">65536 (0x10000) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-163">65536 (0x10000)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-164">授與刪除物件的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-164">Grants the right to delete the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-165"><span id="READ_CONTROL"></span><span id="read_control"></span>**讀取 \_ 控制**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-165"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-166">131072 (0x20000) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-166">131072 (0x20000)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-167">授與許可權，以讀取物件安全描述項中的資訊，而不包含 SACL 中的資訊。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-167">Grants the right to read the information in the security descriptor for the object, not including the information in the SACL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-168"><span id="WRITE_DAC"></span><span id="write_dac"></span>**寫入 \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-168"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-169">262144 (0x40000) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-169">262144 (0x40000)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-170">授與許可權來修改物件之物件安全描述項中的 DACL。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-170">Grants the right to modify the DACL in the object security descriptor for the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-171"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**寫入 \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-171"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-172">524288 (0x80000) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-172">524288 (0x80000)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-173">授與許可權來變更物件之安全描述項中的擁有者。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-173">Grants the right to change the owner in the security descriptor for the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4dfd-174"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**同步**</span><span class="sxs-lookup"><span data-stu-id="b4dfd-174"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4dfd-175">1048576 (0x100000) </span><span class="sxs-lookup"><span data-stu-id="b4dfd-175">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="b4dfd-176">授與使用物件進行同步處理的許可權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-176">Grants the right to use the object for synchronization.</span></span> <span data-ttu-id="b4dfd-177">這可讓進程等候，直到物件處於已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-177">This enables a process to wait until the object is in signaled state.</span></span> <span data-ttu-id="b4dfd-178">某些物件類型不支援此存取權。</span><span class="sxs-lookup"><span data-stu-id="b4dfd-178">Some object types do not support this access right.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4dfd-179">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4dfd-179">Requirements</span></span>



| <span data-ttu-id="b4dfd-180">需求</span><span class="sxs-lookup"><span data-stu-id="b4dfd-180">Requirement</span></span> | <span data-ttu-id="b4dfd-181">值</span><span class="sxs-lookup"><span data-stu-id="b4dfd-181">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4dfd-182">標頭</span><span class="sxs-lookup"><span data-stu-id="b4dfd-182">Header</span></span><br/> | <dl> <span data-ttu-id="b4dfd-183"><dt>Winnt。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4dfd-183"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4dfd-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4dfd-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4dfd-185">WMI 安全性常數</span><span class="sxs-lookup"><span data-stu-id="b4dfd-185">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="b4dfd-186">維護 WMI 安全性</span><span class="sxs-lookup"><span data-stu-id="b4dfd-186">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

