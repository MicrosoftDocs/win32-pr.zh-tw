---
description: 判斷呼叫端是否具有 CIM DeviceFile 物件的匯總許可權 \_ ，以及檔案或目錄所在的共用（如同許可權引數所指定）。
ms.assetid: e566f1f6-773e-4ecb-8145-369afaad0f99
ms.tgt_platform: multiple
title: 'CIM_DeviceFile 類別的 GetEffectivePermission 方法 (Aclui) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4b74c489c41b3da83f0e009526af225fd7de889
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110504"
---
# <a name="geteffectivepermission-method-of-the-cim_devicefile-class"></a><span data-ttu-id="61989-103">CIM DeviceFile 類別的 GetEffectivePermission 方法 \_</span><span class="sxs-lookup"><span data-stu-id="61989-103">GetEffectivePermission method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="61989-104">**GetEffectivePermission** 方法會判斷呼叫端是否具有 [**CIM \_ DeviceFile**](cim-devicefile.md)物件的匯總許可權，以及檔案或目錄所在的共用（如同 **許可權** 引數所指定）。</span><span class="sxs-lookup"><span data-stu-id="61989-104">The **GetEffectivePermission** method determines whether the caller has the aggregated permissions on the [**CIM\_DeviceFile**](cim-devicefile.md) object, and the share on which the file or directory resides, as specified by the **Permission** argument.</span></span> <span data-ttu-id="61989-105">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="61989-105">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61989-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="61989-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="61989-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="61989-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="61989-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="61989-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="61989-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="61989-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="61989-110">語法</span><span class="sxs-lookup"><span data-stu-id="61989-110">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="61989-111">參數</span><span class="sxs-lookup"><span data-stu-id="61989-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61989-112">*許可權* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61989-112">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61989-113">呼叫端可以查詢的許可權清單。</span><span class="sxs-lookup"><span data-stu-id="61989-113">List of permissions that the caller can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="61989-114"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**檔案 \_讀取 \_ 資料 (檔) 檔案 \_ 清單 \_ 目錄 (目錄)** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="61989-114"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="61989-115">授與從檔案讀取資料的許可權。</span><span class="sxs-lookup"><span data-stu-id="61989-115">Grants the right to read data from the file.</span></span> <span data-ttu-id="61989-116">若為目錄，此值會授與許可權來列出目錄的內容。</span><span class="sxs-lookup"><span data-stu-id="61989-116">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="61989-117"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**檔案 \_寫入 \_ 資料 (檔案) 檔案 \_ 新增檔案 \_ (目錄)** (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="61989-117"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="61989-118">授與將資料寫入檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="61989-118">Grants the right to write data to the file.</span></span> <span data-ttu-id="61989-119">若為目錄，此值會授與在目錄中建立檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="61989-119">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="61989-120"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**檔案 \_附加 \_ 資料 (檔) 檔案 \_ 新增 \_ 子目錄 (目錄)** (4 (0x4) ) </span><span class="sxs-lookup"><span data-stu-id="61989-120"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="61989-121">授與將資料附加至檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="61989-121">Grants the right to append data to the file.</span></span> <span data-ttu-id="61989-122">若為目錄，此值會授與建立子目錄的許可權。</span><span class="sxs-lookup"><span data-stu-id="61989-122">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="61989-123"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**檔案 \_讀取 \_ EA** (8 (0x8) ) </span><span class="sxs-lookup"><span data-stu-id="61989-123"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="61989-124">授與讀取擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="61989-124">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="61989-125"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**檔案 \_寫入 \_ EA** (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="61989-125"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="61989-126">授予寫入擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="61989-126">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>

<span data-ttu-id="61989-127"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**檔案 \_執行 (檔) 檔案 \_ (目錄)** (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="61989-127"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="61989-128">授與許可權來執行檔案。</span><span class="sxs-lookup"><span data-stu-id="61989-128">Grants the right to execute a file.</span></span> <span data-ttu-id="61989-129">若為目錄，可以進行目錄的往返。</span><span class="sxs-lookup"><span data-stu-id="61989-129">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="61989-130"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**檔案 \_刪除 \_ 子 (目錄)** (64 (0x40) ) </span><span class="sxs-lookup"><span data-stu-id="61989-130"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="61989-131">授與刪除目錄的許可權，以及其包含的所有檔案（即使檔案是唯讀的）。</span><span class="sxs-lookup"><span data-stu-id="61989-131">Grants the right to delete a directory and all the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="61989-132"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**檔案 \_讀取 \_ 屬性** (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="61989-132"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="61989-133">授與讀取檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="61989-133">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="61989-134"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**檔案 \_將 \_ 屬性寫入** (256 (0x100) ) </span><span class="sxs-lookup"><span data-stu-id="61989-134"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="61989-135">授與變更檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="61989-135">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="61989-136"><span id="DELETE"></span><span id="delete"></span>**刪除** (65536 (0x10000) ) </span><span class="sxs-lookup"><span data-stu-id="61989-136"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="61989-137">授與刪除存取權。</span><span class="sxs-lookup"><span data-stu-id="61989-137">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="61989-138"><span id="READ_CONTROL"></span><span id="read_control"></span>**讀取 \_控制** (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="61989-138"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="61989-139">授與安全描述項和擁有者的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="61989-139">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="61989-140"><span id="WRITE_DAC"></span><span id="write_dac"></span>**寫入 \_DAC** (262144 (0x40000) ) </span><span class="sxs-lookup"><span data-stu-id="61989-140"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="61989-141">授與任意 ACL 的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="61989-141">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="61989-142"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**寫入 \_擁有** 者 (524288 (0x80000) ) </span><span class="sxs-lookup"><span data-stu-id="61989-142"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="61989-143">指派寫入擁有者。</span><span class="sxs-lookup"><span data-stu-id="61989-143">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="61989-144"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**同步處理** (1048576 (0x100000) ) </span><span class="sxs-lookup"><span data-stu-id="61989-144"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="61989-145">同步存取，並允許進程等候物件進入已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="61989-145">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61989-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="61989-146">Return value</span></span>

<span data-ttu-id="61989-147">如果呼叫具有必要的許可權，則傳回 **True** ;否則，它會傳回 **True**。</span><span class="sxs-lookup"><span data-stu-id="61989-147">Returns **True** if the call has the necessary permission; otherwise, it returns **True**.</span></span>

## <a name="remarks"></a><span data-ttu-id="61989-148">備註</span><span class="sxs-lookup"><span data-stu-id="61989-148">Remarks</span></span>

<span data-ttu-id="61989-149">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="61989-149">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="61989-150">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="61989-150">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="61989-151">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="61989-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="61989-152">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="61989-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="61989-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="61989-153">Requirements</span></span>



| <span data-ttu-id="61989-154">需求</span><span class="sxs-lookup"><span data-stu-id="61989-154">Requirement</span></span> | <span data-ttu-id="61989-155">值</span><span class="sxs-lookup"><span data-stu-id="61989-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61989-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61989-156">Minimum supported client</span></span><br/> | <span data-ttu-id="61989-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61989-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="61989-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61989-158">Minimum supported server</span></span><br/> | <span data-ttu-id="61989-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61989-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="61989-160">命名空間</span><span class="sxs-lookup"><span data-stu-id="61989-160">Namespace</span></span><br/>                | <span data-ttu-id="61989-161">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="61989-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="61989-162">標頭</span><span class="sxs-lookup"><span data-stu-id="61989-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="61989-163"><dt>Aclui。h</dt></span><span class="sxs-lookup"><span data-stu-id="61989-163"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="61989-164">MOF</span><span class="sxs-lookup"><span data-stu-id="61989-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61989-165"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="61989-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="61989-166">DLL</span><span class="sxs-lookup"><span data-stu-id="61989-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61989-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61989-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61989-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61989-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61989-169">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="61989-169">**CIM\_DeviceFile**</span></span>](geteffectivepermission-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="61989-170">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="61989-170">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

