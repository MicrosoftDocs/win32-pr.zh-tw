---
description: 判斷使用者是否具有在分頁檔案所在的 Win32 分頁檔物件、目錄和共用的許可權參數中所指定的所有必要許可權 \_ ，如果檔案或目錄位於共用上。
ms.assetid: 1c417ac2-6968-4faf-b596-8df9308f8647
ms.tgt_platform: multiple
title: 'Win32_PageFile 類別的 GetEffectivePermission 方法 (Aclui) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3b9985d18e93f3a3dbcc8f65484bf3fd72284fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936216"
---
# <a name="geteffectivepermission-method-of-the-win32_pagefile-class"></a><span data-ttu-id="fdf67-103">Win32 \_ 分頁檔類別的 GetEffectivePermission 方法</span><span class="sxs-lookup"><span data-stu-id="fdf67-103">GetEffectivePermission method of the Win32\_PageFile class</span></span>

<span data-ttu-id="fdf67-104">[**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會判斷使用者是否具有在分頁檔案所在的 [**Win32 \_ 頁面**](win32-pagefile.md)檔物件、目錄和共用的 *許可權* 參數中所指定的所有必要許可權，如果檔案或目錄位於共用上。</span><span class="sxs-lookup"><span data-stu-id="fdf67-104">The [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method determines whether the user has all of the required permissions specified in the *Permissions* parameter identified for the [**Win32\_PageFile**](win32-pagefile.md) object, directory, and share where the paging file is located, if the file or directory are on a share.</span></span>

<span data-ttu-id="fdf67-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="fdf67-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fdf67-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="fdf67-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fdf67-107">語法</span><span class="sxs-lookup"><span data-stu-id="fdf67-107">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="fdf67-108">參數</span><span class="sxs-lookup"><span data-stu-id="fdf67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdf67-109">*許可權* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fdf67-109">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdf67-110">呼叫端可以查詢的許可權點陣圖。</span><span class="sxs-lookup"><span data-stu-id="fdf67-110">Bitmap of permissions that the caller can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="fdf67-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**檔案 \_讀取 \_ 資料 (檔) 檔案 \_ 清單 \_ 目錄 (目錄)** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="fdf67-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="fdf67-112">授與從檔案讀取資料的許可權。</span><span class="sxs-lookup"><span data-stu-id="fdf67-112">Grants the right to read data from the file.</span></span> <span data-ttu-id="fdf67-113">若為目錄，此值會授與許可權來列出目錄的內容。</span><span class="sxs-lookup"><span data-stu-id="fdf67-113">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="fdf67-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**檔案 \_寫入 \_ 資料 (檔案) 檔案 \_ 新增檔案 \_ (目錄)** (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="fdf67-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="fdf67-115">授與將資料寫入檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="fdf67-115">Grants the right to write data to the file.</span></span> <span data-ttu-id="fdf67-116">若為目錄，此值會授與在目錄中建立檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="fdf67-116">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="fdf67-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**檔案 \_附加 \_ 資料 (檔) 檔案 \_ 新增 \_ 子目錄 (目錄)** (4 (0x4) ) </span><span class="sxs-lookup"><span data-stu-id="fdf67-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="fdf67-118">授與將資料附加至檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="fdf67-118">Grants the right to append data to the file.</span></span> <span data-ttu-id="fdf67-119">若為目錄，此值會授與建立子目錄的許可權。</span><span class="sxs-lookup"><span data-stu-id="fdf67-119">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="fdf67-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**檔案 \_讀取 \_ EA** (8 (0x8) ) </span><span class="sxs-lookup"><span data-stu-id="fdf67-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="fdf67-121">授與讀取擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="fdf67-121">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="fdf67-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**檔案 \_寫入 \_ EA** (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="fdf67-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="fdf67-123">授予寫入擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="fdf67-123">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>

<span data-ttu-id="fdf67-124"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**檔案 \_執行 (檔) 檔案 \_ (目錄)** (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="fdf67-124"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="fdf67-125">授與許可權來執行檔案。</span><span class="sxs-lookup"><span data-stu-id="fdf67-125">Grants the right to execute a file.</span></span> <span data-ttu-id="fdf67-126">若為目錄，可以進行目錄的往返。</span><span class="sxs-lookup"><span data-stu-id="fdf67-126">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="fdf67-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**檔案 \_刪除 \_ 子 (目錄)** (64 (0x40) ) </span><span class="sxs-lookup"><span data-stu-id="fdf67-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="fdf67-128">授與刪除目錄的許可權，以及其包含的所有檔案（即使檔案是唯讀的）。</span><span class="sxs-lookup"><span data-stu-id="fdf67-128">Grants the right to delete a directory and all of the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="fdf67-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**檔案 \_讀取 \_ 屬性** (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="fdf67-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="fdf67-130">授與讀取檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="fdf67-130">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="fdf67-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**檔案 \_將 \_ 屬性寫入** (256 (0x100) ) </span><span class="sxs-lookup"><span data-stu-id="fdf67-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="fdf67-132">授與變更檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="fdf67-132">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="fdf67-133"><span id="DELETE"></span><span id="delete"></span>**刪除** (65536 (0x10000) ) </span><span class="sxs-lookup"><span data-stu-id="fdf67-133"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="fdf67-134">授與刪除存取權。</span><span class="sxs-lookup"><span data-stu-id="fdf67-134">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="fdf67-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**讀取 \_控制** (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="fdf67-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="fdf67-136">授與安全描述項和擁有者的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="fdf67-136">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="fdf67-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**寫入 \_DAC** (262144 (0x40000) ) </span><span class="sxs-lookup"><span data-stu-id="fdf67-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="fdf67-138">授與任意存取控制清單 (DACL) 的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="fdf67-138">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="fdf67-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**寫入 \_擁有** 者 (524288 (0x80000) ) </span><span class="sxs-lookup"><span data-stu-id="fdf67-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="fdf67-140">指派寫入擁有者。</span><span class="sxs-lookup"><span data-stu-id="fdf67-140">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="fdf67-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**同步處理** (1048576 (0x100000) ) </span><span class="sxs-lookup"><span data-stu-id="fdf67-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="fdf67-142">同步存取，並允許進程等候物件進入已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="fdf67-142">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdf67-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="fdf67-143">Return value</span></span>

<span data-ttu-id="fdf67-144">如果呼叫端具有指定的許可權，則傳回 **True** ，如果呼叫端沒有指定的許可權，則傳回 **false** 。</span><span class="sxs-lookup"><span data-stu-id="fdf67-144">Returns **True** if the caller has the specified permissions, and **false** if the caller does not have the specified permissions.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdf67-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdf67-145">Requirements</span></span>



| <span data-ttu-id="fdf67-146">需求</span><span class="sxs-lookup"><span data-stu-id="fdf67-146">Requirement</span></span> | <span data-ttu-id="fdf67-147">值</span><span class="sxs-lookup"><span data-stu-id="fdf67-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdf67-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fdf67-148">Minimum supported client</span></span><br/> | <span data-ttu-id="fdf67-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fdf67-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fdf67-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fdf67-150">Minimum supported server</span></span><br/> | <span data-ttu-id="fdf67-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdf67-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fdf67-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="fdf67-152">Namespace</span></span><br/>                | <span data-ttu-id="fdf67-153">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fdf67-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fdf67-154">標頭</span><span class="sxs-lookup"><span data-stu-id="fdf67-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdf67-155"><dt>Aclui。h</dt></span><span class="sxs-lookup"><span data-stu-id="fdf67-155"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="fdf67-156">MOF</span><span class="sxs-lookup"><span data-stu-id="fdf67-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdf67-157"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fdf67-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fdf67-158">DLL</span><span class="sxs-lookup"><span data-stu-id="fdf67-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdf67-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdf67-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdf67-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdf67-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="fdf67-161">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fdf67-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fdf67-162">**Win32 \_ 分頁檔**</span><span class="sxs-lookup"><span data-stu-id="fdf67-162">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

