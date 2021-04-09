---
description: 使用許可權參數中所設定的值，來判斷使用者是否在代表該編解碼器檔案的 Win32 CodecFile 物件的 AccessMask 屬性中設定指定的許可權 \_ 。
ms.assetid: 068dfcaf-037b-4516-b85a-8ba6558ba561
ms.tgt_platform: multiple
title: 'Win32_CodecFile 類別的 GetEffectivePermission 方法 (Aclui) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc2f24071d5ab864e06686f094707d9111ea07ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847206"
---
# <a name="geteffectivepermission-method-of-the-win32_codecfile-class"></a><span data-ttu-id="11b88-103">Win32 CodecFile 類別的 GetEffectivePermission 方法 \_</span><span class="sxs-lookup"><span data-stu-id="11b88-103">GetEffectivePermission method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="11b88-104">[**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會使用 *許可權* 參數中所設定的值，來判斷使用者是否已在代表該編解碼器檔案的 [**Win32 \_ CodecFile**](win32-codecfile.md)物件的 **AccessMask** 屬性中設定指定的許可權。</span><span class="sxs-lookup"><span data-stu-id="11b88-104">The [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uses the values set in the *Permissions* parameter to determine whether the user has the specified permissions set in the **AccessMask** property of the [**Win32\_CodecFile**](win32-codecfile.md) object that represents the codec file.</span></span> <span data-ttu-id="11b88-105">許可權適用于檔案、檔案所在的目錄，以及共用（如果目錄或檔案位於共用中）。</span><span class="sxs-lookup"><span data-stu-id="11b88-105">The permissions apply to the file, the directory in which the file resides, and the share, if either the directory or the file are in a share.</span></span>

<span data-ttu-id="11b88-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="11b88-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="11b88-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="11b88-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="11b88-108">語法</span><span class="sxs-lookup"><span data-stu-id="11b88-108">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="11b88-109">參數</span><span class="sxs-lookup"><span data-stu-id="11b88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11b88-110">*許可權* \[在\]</span><span class="sxs-lookup"><span data-stu-id="11b88-110">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11b88-111">在 [**Win32 \_ CodecFile**](win32-codecfile.md)物件的 **AccessMask** 屬性中設定的許可權點陣圖。</span><span class="sxs-lookup"><span data-stu-id="11b88-111">Bitmap of permissions that are set in the **AccessMask** property of the [**Win32\_CodecFile**](win32-codecfile.md) object.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="11b88-112"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**檔案 \_讀取 \_ 資料 (檔) 檔案 \_ 清單 \_ 目錄 (目錄)** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="11b88-112"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="11b88-113">授與從檔案讀取資料的許可權。</span><span class="sxs-lookup"><span data-stu-id="11b88-113">Grants the right to read data from the file.</span></span> <span data-ttu-id="11b88-114">若為目錄，此值會授與許可權來列出目錄的內容。</span><span class="sxs-lookup"><span data-stu-id="11b88-114">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="11b88-115"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**檔案 \_寫入 \_ 資料 (檔案) 檔案 \_ 新增檔案 \_ (目錄)** (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="11b88-115"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="11b88-116">授與將資料寫入檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="11b88-116">Grants the right to write data to the file.</span></span> <span data-ttu-id="11b88-117">若為目錄，此值會授與在目錄中建立檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="11b88-117">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="11b88-118"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**檔案 \_附加 \_ 資料 (檔) 檔案 \_ 新增 \_ 子目錄 (目錄)** (4 (0x4) ) </span><span class="sxs-lookup"><span data-stu-id="11b88-118"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="11b88-119">授與將資料附加至檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="11b88-119">Grants the right to append data to the file.</span></span> <span data-ttu-id="11b88-120">若為目錄，此值會授與建立子目錄的許可權。</span><span class="sxs-lookup"><span data-stu-id="11b88-120">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="11b88-121"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**檔案 \_讀取 \_ EA** (8 (0x8) ) </span><span class="sxs-lookup"><span data-stu-id="11b88-121"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="11b88-122">授與讀取擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="11b88-122">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="11b88-123"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**檔案 \_寫入 \_ EA** (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="11b88-123"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="11b88-124">授予寫入擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="11b88-124">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="11b88-125"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**檔案 \_執行 (檔) 檔案 \_ (目錄)** (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="11b88-125"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="11b88-126">授與許可權來執行檔案。</span><span class="sxs-lookup"><span data-stu-id="11b88-126">Grants the right to execute a file.</span></span> <span data-ttu-id="11b88-127">若為目錄，可以進行目錄的往返。</span><span class="sxs-lookup"><span data-stu-id="11b88-127">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="11b88-128"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**檔案 \_刪除 \_ 子 (目錄)** (64 (0x40) ) </span><span class="sxs-lookup"><span data-stu-id="11b88-128"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="11b88-129">授與刪除目錄的許可權，以及其包含的所有檔案（即使檔案是唯讀的）。</span><span class="sxs-lookup"><span data-stu-id="11b88-129">Grants the right to delete a directory and all of the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="11b88-130"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**檔案 \_讀取 \_ 屬性** (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="11b88-130"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="11b88-131">授與讀取檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="11b88-131">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="11b88-132"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**檔案 \_將 \_ 屬性寫入** (256 (0x100) ) </span><span class="sxs-lookup"><span data-stu-id="11b88-132"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="11b88-133">授與變更檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="11b88-133">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="11b88-134"><span id="DELETE"></span><span id="delete"></span>**刪除** (65536 (0x10000) ) </span><span class="sxs-lookup"><span data-stu-id="11b88-134"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="11b88-135">授與刪除存取權。</span><span class="sxs-lookup"><span data-stu-id="11b88-135">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="11b88-136"><span id="READ_CONTROL"></span><span id="read_control"></span>**讀取 \_控制** (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="11b88-136"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="11b88-137">授與安全描述項和擁有者的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="11b88-137">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="11b88-138"><span id="WRITE_DAC"></span><span id="write_dac"></span>**寫入 \_DAC** (262144 (0x40000) ) </span><span class="sxs-lookup"><span data-stu-id="11b88-138"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="11b88-139">授與任意存取控制清單 (ACL) 的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="11b88-139">Grants write access to the discretionary access control list (ACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="11b88-140"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**寫入 \_擁有** 者 (524288 (0x80000) ) </span><span class="sxs-lookup"><span data-stu-id="11b88-140"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="11b88-141">指派寫入擁有者。</span><span class="sxs-lookup"><span data-stu-id="11b88-141">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="11b88-142"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**同步處理** (1048576 (0x100000) ) </span><span class="sxs-lookup"><span data-stu-id="11b88-142"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="11b88-143">同步存取，並允許進程等候物件進入已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="11b88-143">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11b88-144">傳回值</span><span class="sxs-lookup"><span data-stu-id="11b88-144">Return value</span></span>

<span data-ttu-id="11b88-145">當呼叫端具有指定的許可權時傳回 **True** ，當呼叫端沒有指定的許可權時傳回 **false** 。</span><span class="sxs-lookup"><span data-stu-id="11b88-145">Returns **True** when the caller has the specified permissions, and **false** when the caller does not have the specified permissions.</span></span>

## <a name="requirements"></a><span data-ttu-id="11b88-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="11b88-146">Requirements</span></span>



| <span data-ttu-id="11b88-147">需求</span><span class="sxs-lookup"><span data-stu-id="11b88-147">Requirement</span></span> | <span data-ttu-id="11b88-148">值</span><span class="sxs-lookup"><span data-stu-id="11b88-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11b88-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11b88-149">Minimum supported client</span></span><br/> | <span data-ttu-id="11b88-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11b88-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="11b88-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11b88-151">Minimum supported server</span></span><br/> | <span data-ttu-id="11b88-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11b88-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="11b88-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="11b88-153">Namespace</span></span><br/>                | <span data-ttu-id="11b88-154">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="11b88-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="11b88-155">標頭</span><span class="sxs-lookup"><span data-stu-id="11b88-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="11b88-156"><dt>Aclui。h</dt></span><span class="sxs-lookup"><span data-stu-id="11b88-156"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="11b88-157">MOF</span><span class="sxs-lookup"><span data-stu-id="11b88-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11b88-158"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="11b88-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="11b88-159">DLL</span><span class="sxs-lookup"><span data-stu-id="11b88-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11b88-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11b88-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11b88-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11b88-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="11b88-162">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="11b88-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="11b88-163">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="11b88-163">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

