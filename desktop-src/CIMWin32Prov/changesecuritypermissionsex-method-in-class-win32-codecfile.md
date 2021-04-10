---
description: 變更物件路徑中所指定之編解碼器檔案的安全性許可權 (這個方法是) 的擴充版 ChangeSecurityPermissions 方法。
ms.assetid: 3eac4ae1-3c0e-4e81-8b23-9ad8698f723c
ms.tgt_platform: multiple
title: Win32_CodecFile 類別的 ChangeSecurityPermissionsEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 549c55a5066bdaba4699ec76ed3b7be23eb28b96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847251"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="5fa6c-103">Win32 CodecFile 類別的 ChangeSecurityPermissionsEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5fa6c-103">ChangeSecurityPermissionsEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="5fa6c-104">**ChangeSecurityPermissionsEx** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會變更物件路徑中所指定之編解碼器檔案的安全性許可權， (這個方法是 [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md)方法的擴充版本) 。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the codec file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="5fa6c-105">如果邏輯檔案是目錄，則這個方法是遞迴的，並且會變更目錄包含的所有檔案和子目錄的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="5fa6c-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5fa6c-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5fa6c-108">語法</span><span class="sxs-lookup"><span data-stu-id="5fa6c-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="5fa6c-109">參數</span><span class="sxs-lookup"><span data-stu-id="5fa6c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fa6c-110">*SecurityDescriptor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5fa6c-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-111">解析為 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例的運算式。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="5fa6c-112">此描述元包含 [**Win32 \_ CodecFile**](win32-codecfile.md)實例的新安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-112">This descriptor contains new security permissions for the instance of [**Win32\_CodecFile**](win32-codecfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fa6c-113">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5fa6c-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-114">要修改的實際安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-114">Actual security privilege to be modified.</span></span> <span data-ttu-id="5fa6c-115">例如，若要變更擁有者和任意存取控制清單 (DACL) 安全性，請使用下列程式：</span><span class="sxs-lookup"><span data-stu-id="5fa6c-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="5fa6c-116">-或-</span><span class="sxs-lookup"><span data-stu-id="5fa6c-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="5fa6c-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**變更 \_擁有者 \_ 安全性 \_ 資訊** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="5fa6c-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="5fa6c-118">變更邏輯檔案的擁有者。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="5fa6c-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**變更 \_群組 \_ 安全性 \_ 資訊** (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="5fa6c-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="5fa6c-120">變更邏輯檔案的群組。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="5fa6c-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**變更 \_DACL \_ 安全性 \_ 資訊** (4 (0x4) ) </span><span class="sxs-lookup"><span data-stu-id="5fa6c-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="5fa6c-122">變更邏輯檔案 (DACL) 的任意存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-122">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="5fa6c-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**變更 \_SACL \_ 安全性 \_ 資訊** (8 (0x8) ) </span><span class="sxs-lookup"><span data-stu-id="5fa6c-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="5fa6c-124">變更邏輯檔案 (SACL) 的系統存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5fa6c-125">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5fa6c-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-126">**ChangeSecurityPermissionsEx** 方法失敗之檔案或目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="5fa6c-127">當方法成功時，此參數為 null。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-127">This parameter is null when the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="5fa6c-128">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="5fa6c-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-129">將子檔案或目錄命名為 **ChangeSecurityPermissionsEx** 的起點。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="5fa6c-130">一般而言， *StartFileName* 參數是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-130">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="5fa6c-131">如果這個參數是 null，則會在 [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-131">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="5fa6c-132">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="5fa6c-132">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-133">若 **為 true**，則會將擁有權的變更以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-133">If **true**, the changes of ownership are applied recursively to files and directories in the directory that the [**CIM\_LogicalFile**](cim-logicalfile.md) instance specifies.</span></span> <span data-ttu-id="5fa6c-134">若為檔案實例，則會忽略 *遞迴* 輸入參數。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-134">For file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fa6c-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="5fa6c-135">Return value</span></span>

<span data-ttu-id="5fa6c-136">傳回值 0 (零) 如果許可權變更，則傳回不同的數位來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-136">Returns an value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5fa6c-137">「成功」</span><span class="sxs-lookup"><span data-stu-id="5fa6c-137">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-138">0</span><span class="sxs-lookup"><span data-stu-id="5fa6c-138">0</span></span>

<span data-ttu-id="5fa6c-139">要求成功。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-139">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="5fa6c-140">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="5fa6c-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-141">2</span><span class="sxs-lookup"><span data-stu-id="5fa6c-141">2</span></span>

<span data-ttu-id="5fa6c-142">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-142">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="5fa6c-143">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="5fa6c-143">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-144">8</span><span class="sxs-lookup"><span data-stu-id="5fa6c-144">8</span></span>

<span data-ttu-id="5fa6c-145">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-145">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5fa6c-146">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="5fa6c-146">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-147">9</span><span class="sxs-lookup"><span data-stu-id="5fa6c-147">9</span></span>

<span data-ttu-id="5fa6c-148">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-148">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5fa6c-149">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="5fa6c-149">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-150">10</span><span class="sxs-lookup"><span data-stu-id="5fa6c-150">10</span></span>

<span data-ttu-id="5fa6c-151">指定的物件已存在。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-151">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5fa6c-152">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="5fa6c-152">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-153">11</span><span class="sxs-lookup"><span data-stu-id="5fa6c-153">11</span></span>

<span data-ttu-id="5fa6c-154">檔案系統不是 NTFS 檔案系統。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-154">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="5fa6c-155">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="5fa6c-155">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-156">12</span><span class="sxs-lookup"><span data-stu-id="5fa6c-156">12</span></span>

<span data-ttu-id="5fa6c-157">平臺不 Windows NT 或 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-157">The platform is not Windows NT or Windows 2000.</span></span>

</dd> <dt>

<span data-ttu-id="5fa6c-158">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="5fa6c-158">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-159">13</span><span class="sxs-lookup"><span data-stu-id="5fa6c-159">13</span></span>

<span data-ttu-id="5fa6c-160">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-160">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="5fa6c-161">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="5fa6c-161">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-162">14</span><span class="sxs-lookup"><span data-stu-id="5fa6c-162">14</span></span>

<span data-ttu-id="5fa6c-163">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-163">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="5fa6c-164">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="5fa6c-164">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-165">15</span><span class="sxs-lookup"><span data-stu-id="5fa6c-165">15</span></span>

<span data-ttu-id="5fa6c-166">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-166">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="5fa6c-167">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="5fa6c-167">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-168">16</span><span class="sxs-lookup"><span data-stu-id="5fa6c-168">16</span></span>

<span data-ttu-id="5fa6c-169">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-169">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5fa6c-170">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="5fa6c-170">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-171">17</span><span class="sxs-lookup"><span data-stu-id="5fa6c-171">17</span></span>

<span data-ttu-id="5fa6c-172">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-172">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="5fa6c-173">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="5fa6c-173">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5fa6c-174">21</span><span class="sxs-lookup"><span data-stu-id="5fa6c-174">21</span></span>

<span data-ttu-id="5fa6c-175">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="5fa6c-175">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fa6c-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="5fa6c-176">Requirements</span></span>



| <span data-ttu-id="5fa6c-177">需求</span><span class="sxs-lookup"><span data-stu-id="5fa6c-177">Requirement</span></span> | <span data-ttu-id="5fa6c-178">值</span><span class="sxs-lookup"><span data-stu-id="5fa6c-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa6c-179">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5fa6c-179">Minimum supported client</span></span><br/> | <span data-ttu-id="5fa6c-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5fa6c-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5fa6c-181">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5fa6c-181">Minimum supported server</span></span><br/> | <span data-ttu-id="5fa6c-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5fa6c-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5fa6c-183">命名空間</span><span class="sxs-lookup"><span data-stu-id="5fa6c-183">Namespace</span></span><br/>                | <span data-ttu-id="5fa6c-184">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5fa6c-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5fa6c-185">MOF</span><span class="sxs-lookup"><span data-stu-id="5fa6c-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fa6c-186"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5fa6c-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fa6c-187">DLL</span><span class="sxs-lookup"><span data-stu-id="5fa6c-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fa6c-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fa6c-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fa6c-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5fa6c-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="5fa6c-190">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5fa6c-190">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5fa6c-191">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="5fa6c-191">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

