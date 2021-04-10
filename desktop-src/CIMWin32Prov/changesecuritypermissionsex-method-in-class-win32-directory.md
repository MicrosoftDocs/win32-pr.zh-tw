---
description: 變更物件路徑中指定之目錄專案檔的安全性許可權 (這個方法是) 的 ChangeSecurityPermissions 方法擴充版本。
ms.assetid: 787e48af-7cb4-4d0b-a2f1-ffa696466ef2
ms.tgt_platform: multiple
title: Win32_Directory 類別的 ChangeSecurityPermissionsEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4bcadd4a4ad115a1a367db4f2a2f645eb6a4742c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187698"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_directory-class"></a><span data-ttu-id="1b091-103">Win32 目錄類別的 ChangeSecurityPermissionsEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1b091-103">ChangeSecurityPermissionsEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="1b091-104">**ChangeSecurityPermissionsEx** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會變更物件路徑中指定之目錄專案檔的安全性許可權， (這個方法是 [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md)方法的擴充版本) 。</span><span class="sxs-lookup"><span data-stu-id="1b091-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the directory entry file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="1b091-105">如果邏輯檔案是目錄，則這個方法是遞迴的，並且會變更目錄包含的所有檔案和子目錄的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="1b091-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="1b091-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="1b091-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1b091-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="1b091-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b091-108">語法</span><span class="sxs-lookup"><span data-stu-id="1b091-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="1b091-109">參數</span><span class="sxs-lookup"><span data-stu-id="1b091-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b091-110">*SecurityDescriptor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b091-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b091-111">解析為 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例的運算式。</span><span class="sxs-lookup"><span data-stu-id="1b091-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="1b091-112">此參數包含 [**Win32 \_ 分頁檔**](win32-pagefile.md)實例的新安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="1b091-112">This parameter contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b091-113">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b091-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b091-114">要修改的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="1b091-114">Security privilege to be modified.</span></span> <span data-ttu-id="1b091-115">例如，若要變更擁有者和任意存取控制清單 (DACL) 安全性，請使用下列程式：</span><span class="sxs-lookup"><span data-stu-id="1b091-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="1b091-116">-或-</span><span class="sxs-lookup"><span data-stu-id="1b091-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="1b091-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**變更 \_擁有者 \_ 安全性 \_ 資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="1b091-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1b091-118">變更邏輯檔案的擁有者。</span><span class="sxs-lookup"><span data-stu-id="1b091-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="1b091-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**變更 \_將 \_ 安全性 \_ 資訊群組** (2) </span><span class="sxs-lookup"><span data-stu-id="1b091-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1b091-120">變更邏輯檔案的群組。</span><span class="sxs-lookup"><span data-stu-id="1b091-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="1b091-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**變更 \_DACL \_ 安全性 \_ 資訊** (4) </span><span class="sxs-lookup"><span data-stu-id="1b091-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1b091-122">變更邏輯檔案的 DACL 清單。</span><span class="sxs-lookup"><span data-stu-id="1b091-122">Change the DACL list of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="1b091-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**變更 \_SACL \_ 安全性 \_ 資訊** (8) </span><span class="sxs-lookup"><span data-stu-id="1b091-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="1b091-124">變更邏輯檔案 (SACL) 的系統存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="1b091-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1b091-125">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1b091-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b091-126">**ChangeSecurityPermissionsEx** 方法失敗之檔案或目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b091-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="1b091-127">如果方法成功，則此參數為 null。</span><span class="sxs-lookup"><span data-stu-id="1b091-127">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="1b091-128">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1b091-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1b091-129">將子檔案或目錄命名為 **ChangeSecurityPermissionsEx** 的起點。</span><span class="sxs-lookup"><span data-stu-id="1b091-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="1b091-130">一般而言， *StartFileName* 參數是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="1b091-130">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="1b091-131">如果這個參數是 null，則會在 **ExecMethod** 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="1b091-131">If this parameter is null, the operation is performed on the file or directory that is specified in the **ExecMethod** call.</span></span> <span data-ttu-id="1b091-132">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="1b091-132">This parameter is optional.</span></span>

<span data-ttu-id="1b091-133">如果使用 *StartFileName* ，則 *遞迴* 也必須設定為 true。</span><span class="sxs-lookup"><span data-stu-id="1b091-133">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="1b091-134">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1b091-134">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1b091-135">若 **為 true**，則會將擁有權變更以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="1b091-135">If **true**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="1b091-136">若為檔案實例，則會忽略 *遞迴* 輸入參數。</span><span class="sxs-lookup"><span data-stu-id="1b091-136">For file instances, the *Recursive* input parameter is ignored.</span></span> <span data-ttu-id="1b091-137">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="1b091-137">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b091-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b091-138">Return value</span></span>

<span data-ttu-id="1b091-139">傳回值 0 (零) 如果許可權變更，則傳回不同的數位來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="1b091-139">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1b091-140">「成功」</span><span class="sxs-lookup"><span data-stu-id="1b091-140">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="1b091-141">0</span><span class="sxs-lookup"><span data-stu-id="1b091-141">0</span></span>

<span data-ttu-id="1b091-142">要求成功。</span><span class="sxs-lookup"><span data-stu-id="1b091-142">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="1b091-143">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="1b091-143">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="1b091-144">2</span><span class="sxs-lookup"><span data-stu-id="1b091-144">2</span></span>

<span data-ttu-id="1b091-145">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="1b091-145">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="1b091-146">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="1b091-146">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="1b091-147">8</span><span class="sxs-lookup"><span data-stu-id="1b091-147">8</span></span>

<span data-ttu-id="1b091-148">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="1b091-148">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="1b091-149">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="1b091-149">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="1b091-150">9</span><span class="sxs-lookup"><span data-stu-id="1b091-150">9</span></span>

<span data-ttu-id="1b091-151">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="1b091-151">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1b091-152">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="1b091-152">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="1b091-153">10</span><span class="sxs-lookup"><span data-stu-id="1b091-153">10</span></span>

<span data-ttu-id="1b091-154">指定的物件已存在。</span><span class="sxs-lookup"><span data-stu-id="1b091-154">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1b091-155">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="1b091-155">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="1b091-156">11</span><span class="sxs-lookup"><span data-stu-id="1b091-156">11</span></span>

<span data-ttu-id="1b091-157">檔案系統不是 NTFS 檔案系統。</span><span class="sxs-lookup"><span data-stu-id="1b091-157">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="1b091-158">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="1b091-158">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="1b091-159">12</span><span class="sxs-lookup"><span data-stu-id="1b091-159">12</span></span>

<span data-ttu-id="1b091-160">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="1b091-160">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1b091-161">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="1b091-161">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="1b091-162">13</span><span class="sxs-lookup"><span data-stu-id="1b091-162">13</span></span>

<span data-ttu-id="1b091-163">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="1b091-163">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="1b091-164">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="1b091-164">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="1b091-165">14</span><span class="sxs-lookup"><span data-stu-id="1b091-165">14</span></span>

<span data-ttu-id="1b091-166">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="1b091-166">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="1b091-167">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="1b091-167">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="1b091-168">15</span><span class="sxs-lookup"><span data-stu-id="1b091-168">15</span></span>

<span data-ttu-id="1b091-169">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="1b091-169">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="1b091-170">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="1b091-170">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="1b091-171">16</span><span class="sxs-lookup"><span data-stu-id="1b091-171">16</span></span>

<span data-ttu-id="1b091-172">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="1b091-172">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1b091-173">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="1b091-173">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="1b091-174">17</span><span class="sxs-lookup"><span data-stu-id="1b091-174">17</span></span>

<span data-ttu-id="1b091-175">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="1b091-175">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="1b091-176">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="1b091-176">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1b091-177">21</span><span class="sxs-lookup"><span data-stu-id="1b091-177">21</span></span>

<span data-ttu-id="1b091-178">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="1b091-178">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b091-179">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b091-179">Requirements</span></span>



| <span data-ttu-id="1b091-180">需求</span><span class="sxs-lookup"><span data-stu-id="1b091-180">Requirement</span></span> | <span data-ttu-id="1b091-181">值</span><span class="sxs-lookup"><span data-stu-id="1b091-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b091-182">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b091-182">Minimum supported client</span></span><br/> | <span data-ttu-id="1b091-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b091-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b091-184">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b091-184">Minimum supported server</span></span><br/> | <span data-ttu-id="1b091-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b091-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b091-186">命名空間</span><span class="sxs-lookup"><span data-stu-id="1b091-186">Namespace</span></span><br/>                | <span data-ttu-id="1b091-187">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1b091-187">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1b091-188">MOF</span><span class="sxs-lookup"><span data-stu-id="1b091-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b091-189"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b091-189"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b091-190">DLL</span><span class="sxs-lookup"><span data-stu-id="1b091-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b091-191"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b091-191"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b091-192">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b091-192">See also</span></span>

<dl> <dt>

<span data-ttu-id="1b091-193">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1b091-193">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1b091-194">**Win32 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="1b091-194">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

