---
description: 判斷呼叫端是否具有 CIM 目錄物件的匯總許可權 \_ ，以及檔案或目錄所在的共用（如同許可權引數所指定）。 這個方法繼承自 CIM \_ LogicalFile。
ms.assetid: b3dc1e3c-5c99-46ba-93c4-15fbf18e98e8
ms.tgt_platform: multiple
title: 'CIM_Directory 類別的 GetEffectivePermission 方法 (Aclui) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 436a30517b7f3306ef8be2426385fe385947296e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847207"
---
# <a name="geteffectivepermission-method-of-the-cim_directory-class"></a><span data-ttu-id="102a7-104">CIM 目錄類別的 GetEffectivePermission 方法 \_</span><span class="sxs-lookup"><span data-stu-id="102a7-104">GetEffectivePermission method of the CIM\_Directory class</span></span>

<span data-ttu-id="102a7-105">**GetEffectivePermission** 方法會判斷呼叫端是否具有 [**CIM \_ 目錄**](cim-directory.md)物件的匯總許可權，以及檔案或目錄所在的共用（如同 **許可權** 引數所指定）。</span><span class="sxs-lookup"><span data-stu-id="102a7-105">The **GetEffectivePermission** method determines whether the caller has the aggregated permissions on the [**CIM\_Directory**](cim-directory.md) object, and the share on which the file or directory resides, as specified by the **Permission** argument.</span></span> <span data-ttu-id="102a7-106">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="102a7-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="102a7-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="102a7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="102a7-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="102a7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="102a7-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="102a7-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="102a7-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="102a7-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="102a7-111">語法</span><span class="sxs-lookup"><span data-stu-id="102a7-111">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="102a7-112">參數</span><span class="sxs-lookup"><span data-stu-id="102a7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="102a7-113">*許可權* \[在\]</span><span class="sxs-lookup"><span data-stu-id="102a7-113">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="102a7-114">使用者可以查詢的許可權清單。</span><span class="sxs-lookup"><span data-stu-id="102a7-114">List of permissions that the user can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="102a7-115"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**檔案 \_讀取 \_ 資料 (檔) 檔案 \_ 清單 \_ 目錄 (目錄)** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="102a7-115"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="102a7-116">授與從檔案讀取資料的許可權。</span><span class="sxs-lookup"><span data-stu-id="102a7-116">Grants the right to read data from the file.</span></span> <span data-ttu-id="102a7-117">若為目錄，此值會授與許可權來列出目錄的內容。</span><span class="sxs-lookup"><span data-stu-id="102a7-117">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="102a7-118"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**檔案 \_寫入 \_ 資料 (檔案) 檔案 \_ 新增檔案 \_ (目錄)** (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="102a7-118"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="102a7-119">授與將資料寫入檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="102a7-119">Grants the right to write data to the file.</span></span> <span data-ttu-id="102a7-120">若為目錄，此值會授與在目錄中建立檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="102a7-120">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="102a7-121"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**檔案 \_附加 \_ 資料 (檔) 檔案 \_ 新增 \_ 子目錄 (目錄)** (4 (0x4) ) </span><span class="sxs-lookup"><span data-stu-id="102a7-121"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="102a7-122">授與將資料附加至檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="102a7-122">Grants the right to append data to the file.</span></span> <span data-ttu-id="102a7-123">若為目錄，此值會授與建立子目錄的許可權。</span><span class="sxs-lookup"><span data-stu-id="102a7-123">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="102a7-124"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**檔案 \_讀取 \_ EA** (8 (0x8) ) </span><span class="sxs-lookup"><span data-stu-id="102a7-124"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="102a7-125">授與讀取擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="102a7-125">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="102a7-126"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**檔案 \_寫入 \_ EA** (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="102a7-126"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="102a7-127">授予寫入擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="102a7-127">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="102a7-128"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**檔案 \_執行 (檔) 檔案 \_ (目錄)** (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="102a7-128"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="102a7-129">授與許可權來執行檔案。</span><span class="sxs-lookup"><span data-stu-id="102a7-129">Grants the right to execute a file.</span></span> <span data-ttu-id="102a7-130">若為目錄，可以進行目錄的往返。</span><span class="sxs-lookup"><span data-stu-id="102a7-130">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="102a7-131"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**檔案 \_刪除 \_ 子 (目錄)** (64 (0x40) ) </span><span class="sxs-lookup"><span data-stu-id="102a7-131"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="102a7-132">授與刪除目錄的許可權，以及其包含的所有檔案（即使檔案是唯讀的）。</span><span class="sxs-lookup"><span data-stu-id="102a7-132">Grants the right to delete a directory and all the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="102a7-133"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**檔案 \_讀取 \_ 屬性** (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="102a7-133"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="102a7-134">授與讀取檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="102a7-134">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="102a7-135"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**檔案 \_將 \_ 屬性寫入** (256 (0x100) ) </span><span class="sxs-lookup"><span data-stu-id="102a7-135"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="102a7-136">授與變更檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="102a7-136">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="102a7-137"><span id="DELETE"></span><span id="delete"></span>**刪除** (65536 (0x10000) ) </span><span class="sxs-lookup"><span data-stu-id="102a7-137"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="102a7-138">授與刪除存取權。</span><span class="sxs-lookup"><span data-stu-id="102a7-138">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="102a7-139"><span id="READ_CONTROL"></span><span id="read_control"></span>**讀取 \_控制** (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="102a7-139"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="102a7-140">授與安全描述項和擁有者的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="102a7-140">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="102a7-141"><span id="WRITE_DAC"></span><span id="write_dac"></span>**寫入 \_DAC** (262144 (0x40000) ) </span><span class="sxs-lookup"><span data-stu-id="102a7-141"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="102a7-142">授與任意 ACL 的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="102a7-142">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="102a7-143"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**寫入 \_擁有** 者 (524288 (0x80000) ) </span><span class="sxs-lookup"><span data-stu-id="102a7-143"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="102a7-144">指派寫入擁有者。</span><span class="sxs-lookup"><span data-stu-id="102a7-144">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="102a7-145"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**同步處理** (1048576 (0x100000) ) </span><span class="sxs-lookup"><span data-stu-id="102a7-145"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="102a7-146">同步存取，並允許進程等候物件進入已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="102a7-146">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="102a7-147">傳回值</span><span class="sxs-lookup"><span data-stu-id="102a7-147">Return value</span></span>

<span data-ttu-id="102a7-148">如果呼叫具有必要的許可權，則傳回 **True** ;否則，它會傳回 **false**。</span><span class="sxs-lookup"><span data-stu-id="102a7-148">Returns **True** if the call has the necessary permission; otherwise, it returns **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="102a7-149">備註</span><span class="sxs-lookup"><span data-stu-id="102a7-149">Remarks</span></span>

<span data-ttu-id="102a7-150">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="102a7-150">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="102a7-151">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="102a7-151">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="102a7-152">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="102a7-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="102a7-153">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="102a7-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="102a7-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="102a7-154">Requirements</span></span>



| <span data-ttu-id="102a7-155">需求</span><span class="sxs-lookup"><span data-stu-id="102a7-155">Requirement</span></span> | <span data-ttu-id="102a7-156">值</span><span class="sxs-lookup"><span data-stu-id="102a7-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="102a7-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="102a7-157">Minimum supported client</span></span><br/> | <span data-ttu-id="102a7-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="102a7-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="102a7-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="102a7-159">Minimum supported server</span></span><br/> | <span data-ttu-id="102a7-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="102a7-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="102a7-161">命名空間</span><span class="sxs-lookup"><span data-stu-id="102a7-161">Namespace</span></span><br/>                | <span data-ttu-id="102a7-162">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="102a7-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="102a7-163">標頭</span><span class="sxs-lookup"><span data-stu-id="102a7-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="102a7-164"><dt>Aclui。h</dt></span><span class="sxs-lookup"><span data-stu-id="102a7-164"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="102a7-165">MOF</span><span class="sxs-lookup"><span data-stu-id="102a7-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="102a7-166"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="102a7-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="102a7-167">DLL</span><span class="sxs-lookup"><span data-stu-id="102a7-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="102a7-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="102a7-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="102a7-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="102a7-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="102a7-170">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="102a7-170">**CIM\_Directory**</span></span>](geteffectivepermission-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="102a7-171">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="102a7-171">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

