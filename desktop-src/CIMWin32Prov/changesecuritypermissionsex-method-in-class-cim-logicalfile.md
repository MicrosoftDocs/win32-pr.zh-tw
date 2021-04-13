---
description: 變更物件路徑中指定之邏輯檔案的安全性許可權 (這個方法是) 的擴充版本 ChangeSecurityPermissions 方法。
ms.assetid: 29155533-0898-4f8f-af08-f3ea46c8c1d3
ms.tgt_platform: multiple
title: CIM_LogicalFile 類別的 ChangeSecurityPermissionsEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af2dc82ef54b6f32eee20f17cd61c0769cc64b1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510539"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="fd6ab-103">CIM LogicalFile 類別的 ChangeSecurityPermissionsEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fd6ab-103">ChangeSecurityPermissionsEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="fd6ab-104">**ChangeSecurityPermissionsEx** 方法會變更物件路徑中所指定之邏輯檔案的安全性許可權 (這個方法是 [**) 的擴充**](changesecuritypermissions-method-in-class-cim-logicalfile.md)版本。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md) method).</span></span> <span data-ttu-id="fd6ab-105">如果邏輯檔案是目錄，則此方法會以遞迴方式運作，以變更目錄所包含的所有檔案和子目錄的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd6ab-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fd6ab-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fd6ab-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fd6ab-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd6ab-110">語法</span><span class="sxs-lookup"><span data-stu-id="fd6ab-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="fd6ab-111">參數</span><span class="sxs-lookup"><span data-stu-id="fd6ab-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd6ab-112">*SecurityDescriptor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd6ab-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-113">指定安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-113">Specifies the security information.</span></span>

</dd> <dt>

<span data-ttu-id="fd6ab-114">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd6ab-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-115">要修改的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-115">Security privilege to modify.</span></span> <span data-ttu-id="fd6ab-116">例如，若要變更擁有者和 DACL 安全性，請使用</span><span class="sxs-lookup"><span data-stu-id="fd6ab-116">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="fd6ab-117">或</span><span class="sxs-lookup"><span data-stu-id="fd6ab-117">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span data-ttu-id="fd6ab-118"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**變更 \_擁有者 \_ 安全性 \_ 資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="fd6ab-118"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Change\_Owner\_Security\_Information** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fd6ab-119">變更邏輯檔案的擁有者。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span data-ttu-id="fd6ab-120"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**變更 \_將 \_ 安全性 \_ 資訊群組** (2) </span><span class="sxs-lookup"><span data-stu-id="fd6ab-120"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Change\_Group\_Security\_Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fd6ab-121">變更邏輯檔案的群組。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="fd6ab-122"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**變更 \_Dacl \_ 安全性 \_ 資訊** (4) </span><span class="sxs-lookup"><span data-stu-id="fd6ab-122"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Change\_Dacl\_Security\_Information** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fd6ab-123">變更邏輯檔案的 ACL。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-123">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="fd6ab-124"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**變更 \_Sacl \_ 安全性 \_ 資訊** (8) </span><span class="sxs-lookup"><span data-stu-id="fd6ab-124"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Change\_Sacl\_Security\_Information** (8)</span></span>


</dt> <dd>

<span data-ttu-id="fd6ab-125">變更邏輯檔案的系統 ACL。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-125">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fd6ab-126">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fd6ab-126">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-127">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-127">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="fd6ab-128">如果方法成功，這個參數的值會是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-128">This parameter has a value of **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="fd6ab-129">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="fd6ab-129">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-130">字串，表示要作為此方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-130">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="fd6ab-131">一般而言， *StartFileName* 參數是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-131">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="fd6ab-132">如果參數值為 **null**，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-132">If the parameter value is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="fd6ab-133">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="fd6ab-133">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-134">若 **為 TRUE**，則會以遞迴方式將安全性許可權套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-134">If **TRUE**, the security permissions are applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="fd6ab-135">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-135">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd6ab-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd6ab-136">Return value</span></span>

<span data-ttu-id="fd6ab-137">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-137">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="fd6ab-138">「成功」</span><span class="sxs-lookup"><span data-stu-id="fd6ab-138">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-139">0</span><span class="sxs-lookup"><span data-stu-id="fd6ab-139">0</span></span>

<span data-ttu-id="fd6ab-140">成功。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-140">Success.</span></span>

</dd> <dt>

<span data-ttu-id="fd6ab-141">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="fd6ab-141">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-142">2</span><span class="sxs-lookup"><span data-stu-id="fd6ab-142">2</span></span>

<span data-ttu-id="fd6ab-143">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-143">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="fd6ab-144">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="fd6ab-144">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-145">8</span><span class="sxs-lookup"><span data-stu-id="fd6ab-145">8</span></span>

<span data-ttu-id="fd6ab-146">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-146">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="fd6ab-147">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="fd6ab-147">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-148">9</span><span class="sxs-lookup"><span data-stu-id="fd6ab-148">9</span></span>

<span data-ttu-id="fd6ab-149">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-149">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="fd6ab-150">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="fd6ab-150">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-151">10</span><span class="sxs-lookup"><span data-stu-id="fd6ab-151">10</span></span>

<span data-ttu-id="fd6ab-152">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-152">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="fd6ab-153">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="fd6ab-153">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-154">11</span><span class="sxs-lookup"><span data-stu-id="fd6ab-154">11</span></span>

<span data-ttu-id="fd6ab-155">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-155">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="fd6ab-156">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="fd6ab-156">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-157">12</span><span class="sxs-lookup"><span data-stu-id="fd6ab-157">12</span></span>

<span data-ttu-id="fd6ab-158">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-158">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="fd6ab-159">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="fd6ab-159">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-160">13</span><span class="sxs-lookup"><span data-stu-id="fd6ab-160">13</span></span>

<span data-ttu-id="fd6ab-161">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-161">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="fd6ab-162">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="fd6ab-162">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-163">14</span><span class="sxs-lookup"><span data-stu-id="fd6ab-163">14</span></span>

<span data-ttu-id="fd6ab-164">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-164">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="fd6ab-165">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="fd6ab-165">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-166">15</span><span class="sxs-lookup"><span data-stu-id="fd6ab-166">15</span></span>

<span data-ttu-id="fd6ab-167">共用違規。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-167">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="fd6ab-168">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="fd6ab-168">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-169">16</span><span class="sxs-lookup"><span data-stu-id="fd6ab-169">16</span></span>

<span data-ttu-id="fd6ab-170">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-170">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="fd6ab-171">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="fd6ab-171">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-172">17</span><span class="sxs-lookup"><span data-stu-id="fd6ab-172">17</span></span>

<span data-ttu-id="fd6ab-173">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-173">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="fd6ab-174">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="fd6ab-174">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="fd6ab-175">21</span><span class="sxs-lookup"><span data-stu-id="fd6ab-175">21</span></span>

<span data-ttu-id="fd6ab-176">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-176">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd6ab-177">備註</span><span class="sxs-lookup"><span data-stu-id="fd6ab-177">Remarks</span></span>

<span data-ttu-id="fd6ab-178">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-178">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="fd6ab-179">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="fd6ab-179">To use this method, you must implement it in your own provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd6ab-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd6ab-180">Requirements</span></span>



| <span data-ttu-id="fd6ab-181">需求</span><span class="sxs-lookup"><span data-stu-id="fd6ab-181">Requirement</span></span> | <span data-ttu-id="fd6ab-182">值</span><span class="sxs-lookup"><span data-stu-id="fd6ab-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6ab-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd6ab-183">Minimum supported client</span></span><br/> | <span data-ttu-id="fd6ab-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd6ab-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd6ab-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd6ab-185">Minimum supported server</span></span><br/> | <span data-ttu-id="fd6ab-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd6ab-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd6ab-187">命名空間</span><span class="sxs-lookup"><span data-stu-id="fd6ab-187">Namespace</span></span><br/>                | <span data-ttu-id="fd6ab-188">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fd6ab-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fd6ab-189">MOF</span><span class="sxs-lookup"><span data-stu-id="fd6ab-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd6ab-190"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd6ab-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd6ab-191">DLL</span><span class="sxs-lookup"><span data-stu-id="fd6ab-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd6ab-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd6ab-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd6ab-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd6ab-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6ab-194">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="fd6ab-194">**CIM\_LogicalFile**</span></span>](changesecuritypermissionsex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="fd6ab-195">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="fd6ab-195">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

