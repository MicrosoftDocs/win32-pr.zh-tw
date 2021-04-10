---
description: 變更物件路徑中指定之邏輯分頁檔的安全性許可權。
ms.assetid: 3abdfa1d-49d8-4676-b7a5-3be528938ec4
ms.tgt_platform: multiple
title: Win32_PageFile 類別的 ChangeSecurityPermissions 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc30d8780f7c0573b9a63ff83f16ad46b9d2a70f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936348"
---
# <a name="changesecuritypermissions-method-of-the-win32_pagefile-class"></a><span data-ttu-id="74e7e-103">Win32 \_ 分頁檔類別的 ChangeSecurityPermissions 方法</span><span class="sxs-lookup"><span data-stu-id="74e7e-103">ChangeSecurityPermissions method of the Win32\_PageFile class</span></span>

<span data-ttu-id="74e7e-104">**ChangeSecurityPermissions** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會變更物件路徑中所指定之邏輯分頁檔的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="74e7e-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical paging file specified in the object path.</span></span> <span data-ttu-id="74e7e-105">如果邏輯檔案是目錄，則 **ChangeSecurityPermissions** 是遞迴的，並且會變更目錄包含的所有檔案和子目錄的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="74e7e-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="74e7e-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="74e7e-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="74e7e-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="74e7e-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="74e7e-108">語法</span><span class="sxs-lookup"><span data-stu-id="74e7e-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="74e7e-109">參數</span><span class="sxs-lookup"><span data-stu-id="74e7e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74e7e-110">*SecurityDescriptor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74e7e-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74e7e-111">解析為 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例的運算式。</span><span class="sxs-lookup"><span data-stu-id="74e7e-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="74e7e-112">此描述元包含 [**Win32 \_ 分頁檔**](win32-pagefile.md)實例的新安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="74e7e-112">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="74e7e-113">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74e7e-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74e7e-114">要修改的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="74e7e-114">Security privilege to be modified.</span></span> <span data-ttu-id="74e7e-115">例如，若要變更擁有者和任意存取控制清單 (DACL) 安全性，請使用：</span><span class="sxs-lookup"><span data-stu-id="74e7e-115">For example, to change the owner and discretionary access control list (DACL) security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="74e7e-116">-或-</span><span class="sxs-lookup"><span data-stu-id="74e7e-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="74e7e-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**變更 \_擁有者 \_ 安全性 \_ 資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="74e7e-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="74e7e-118">變更邏輯檔案的擁有者。</span><span class="sxs-lookup"><span data-stu-id="74e7e-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="74e7e-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**變更 \_將 \_ 安全性 \_ 資訊群組** (2) </span><span class="sxs-lookup"><span data-stu-id="74e7e-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="74e7e-120">變更邏輯檔案的群組。</span><span class="sxs-lookup"><span data-stu-id="74e7e-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="74e7e-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**變更 \_DACL \_ 安全性 \_ 資訊** (4) </span><span class="sxs-lookup"><span data-stu-id="74e7e-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="74e7e-122">變更邏輯檔案的 DACL。</span><span class="sxs-lookup"><span data-stu-id="74e7e-122">Change the DACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="74e7e-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**變更 \_SACL \_ 安全性 \_ 資訊** (8) </span><span class="sxs-lookup"><span data-stu-id="74e7e-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="74e7e-124">變更邏輯檔案 (SACL) 的系統存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="74e7e-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74e7e-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="74e7e-125">Return value</span></span>

<span data-ttu-id="74e7e-126">傳回值 0 (零) 如果許可權變更，則傳回不同的數位來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="74e7e-126">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="74e7e-127">「成功」</span><span class="sxs-lookup"><span data-stu-id="74e7e-127">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="74e7e-128">0</span><span class="sxs-lookup"><span data-stu-id="74e7e-128">0</span></span>

<span data-ttu-id="74e7e-129">要求成功。</span><span class="sxs-lookup"><span data-stu-id="74e7e-129">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="74e7e-130">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="74e7e-130">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="74e7e-131">2</span><span class="sxs-lookup"><span data-stu-id="74e7e-131">2</span></span>

<span data-ttu-id="74e7e-132">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="74e7e-132">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="74e7e-133">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="74e7e-133">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="74e7e-134">8</span><span class="sxs-lookup"><span data-stu-id="74e7e-134">8</span></span>

<span data-ttu-id="74e7e-135">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="74e7e-135">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="74e7e-136">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="74e7e-136">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="74e7e-137">9</span><span class="sxs-lookup"><span data-stu-id="74e7e-137">9</span></span>

<span data-ttu-id="74e7e-138">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="74e7e-138">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="74e7e-139">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="74e7e-139">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="74e7e-140">10</span><span class="sxs-lookup"><span data-stu-id="74e7e-140">10</span></span>

<span data-ttu-id="74e7e-141">指定的物件已存在。</span><span class="sxs-lookup"><span data-stu-id="74e7e-141">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="74e7e-142">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="74e7e-142">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="74e7e-143">11</span><span class="sxs-lookup"><span data-stu-id="74e7e-143">11</span></span>

<span data-ttu-id="74e7e-144">檔案系統不是 NTFS 檔案系統。</span><span class="sxs-lookup"><span data-stu-id="74e7e-144">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="74e7e-145">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="74e7e-145">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="74e7e-146">12</span><span class="sxs-lookup"><span data-stu-id="74e7e-146">12</span></span>

<span data-ttu-id="74e7e-147">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="74e7e-147">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="74e7e-148">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="74e7e-148">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="74e7e-149">13</span><span class="sxs-lookup"><span data-stu-id="74e7e-149">13</span></span>

<span data-ttu-id="74e7e-150">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="74e7e-150">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="74e7e-151">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="74e7e-151">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="74e7e-152">14</span><span class="sxs-lookup"><span data-stu-id="74e7e-152">14</span></span>

<span data-ttu-id="74e7e-153">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="74e7e-153">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="74e7e-154">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="74e7e-154">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="74e7e-155">15</span><span class="sxs-lookup"><span data-stu-id="74e7e-155">15</span></span>

<span data-ttu-id="74e7e-156">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="74e7e-156">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="74e7e-157">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="74e7e-157">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="74e7e-158">16</span><span class="sxs-lookup"><span data-stu-id="74e7e-158">16</span></span>

<span data-ttu-id="74e7e-159">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="74e7e-159">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="74e7e-160">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="74e7e-160">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="74e7e-161">17</span><span class="sxs-lookup"><span data-stu-id="74e7e-161">17</span></span>

<span data-ttu-id="74e7e-162">遺漏操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="74e7e-162">A privilege required for the operation is missing.</span></span>

</dd> <dt>

<span data-ttu-id="74e7e-163">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="74e7e-163">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="74e7e-164">21</span><span class="sxs-lookup"><span data-stu-id="74e7e-164">21</span></span>

<span data-ttu-id="74e7e-165">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="74e7e-165">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74e7e-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="74e7e-166">Requirements</span></span>



| <span data-ttu-id="74e7e-167">需求</span><span class="sxs-lookup"><span data-stu-id="74e7e-167">Requirement</span></span> | <span data-ttu-id="74e7e-168">值</span><span class="sxs-lookup"><span data-stu-id="74e7e-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74e7e-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74e7e-169">Minimum supported client</span></span><br/> | <span data-ttu-id="74e7e-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74e7e-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="74e7e-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74e7e-171">Minimum supported server</span></span><br/> | <span data-ttu-id="74e7e-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74e7e-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="74e7e-173">命名空間</span><span class="sxs-lookup"><span data-stu-id="74e7e-173">Namespace</span></span><br/>                | <span data-ttu-id="74e7e-174">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="74e7e-174">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="74e7e-175">MOF</span><span class="sxs-lookup"><span data-stu-id="74e7e-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74e7e-176"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="74e7e-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="74e7e-177">DLL</span><span class="sxs-lookup"><span data-stu-id="74e7e-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74e7e-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74e7e-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74e7e-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74e7e-179">See also</span></span>

<dl> <dt>

<span data-ttu-id="74e7e-180">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="74e7e-180">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="74e7e-181">**Win32 \_ 分頁檔**</span><span class="sxs-lookup"><span data-stu-id="74e7e-181">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

