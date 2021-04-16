---
description: 變更物件路徑中指定之邏輯快速鍵檔的安全性許可權。
ms.assetid: abd5aec8-4684-4b8d-8fdf-d3a7a5eec103
ms.tgt_platform: multiple
title: Win32_ShortcutFile 類別的 ChangeSecurityPermissions 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad2d482e0be93a1abec80fc710a1a43d7873dd99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468337"
---
# <a name="changesecuritypermissions-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="5d26c-103">Win32 ShortcutFile 類別的 ChangeSecurityPermissions 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5d26c-103">ChangeSecurityPermissions method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="5d26c-104">**ChangeSecurityPermissions** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會變更物件路徑中指定之邏輯快速鍵檔的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="5d26c-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical shortcut file specified in the object path.</span></span> <span data-ttu-id="5d26c-105">如果邏輯檔案是目錄，則 **ChangeSecurityPermissions** 是遞迴的，並且會變更目錄包含的所有檔案和子目錄的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="5d26c-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span> <span data-ttu-id="5d26c-106">**ChangeSecurityPermissions** 會傳回整數值 0 (零) 如果許可權變更，則傳回不同的數位來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="5d26c-106">**ChangeSecurityPermissions** returns an integer value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<span data-ttu-id="5d26c-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="5d26c-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5d26c-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="5d26c-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d26c-109">語法</span><span class="sxs-lookup"><span data-stu-id="5d26c-109">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="5d26c-110">參數</span><span class="sxs-lookup"><span data-stu-id="5d26c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d26c-111">*SecurityDescriptor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5d26c-111">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d26c-112">解析為 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例的運算式。</span><span class="sxs-lookup"><span data-stu-id="5d26c-112">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="5d26c-113">此描述元包含 [**Win32 \_ 分頁檔**](win32-pagefile.md)實例的新安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="5d26c-113">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d26c-114">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5d26c-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d26c-115">要修改的實際安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="5d26c-115">Actual security privilege to be modified.</span></span> <span data-ttu-id="5d26c-116">例如，若要變更擁有者和 DACL 安全性，請使用：</span><span class="sxs-lookup"><span data-stu-id="5d26c-116">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="5d26c-117">或</span><span class="sxs-lookup"><span data-stu-id="5d26c-117">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="5d26c-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**變更 \_擁有者 \_ 安全性 \_ 資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="5d26c-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5d26c-119">變更邏輯檔案的擁有者。</span><span class="sxs-lookup"><span data-stu-id="5d26c-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="5d26c-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**變更 \_將 \_ 安全性 \_ 資訊群組** (2) </span><span class="sxs-lookup"><span data-stu-id="5d26c-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5d26c-121">變更邏輯檔案的群組。</span><span class="sxs-lookup"><span data-stu-id="5d26c-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="5d26c-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**變更 \_DACL \_ 安全性 \_ 資訊** (4) </span><span class="sxs-lookup"><span data-stu-id="5d26c-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5d26c-123">變更邏輯檔案 (DACL) 的任意存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="5d26c-123">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="5d26c-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**變更 \_SACL \_ 安全性 \_ 資訊** (8) </span><span class="sxs-lookup"><span data-stu-id="5d26c-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="5d26c-125">變更邏輯檔案 (SACL) 的系統存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="5d26c-125">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d26c-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d26c-126">Return value</span></span>

<span data-ttu-id="5d26c-127">傳回值 0 (零) 如果許可權變更，則傳回不同的數位來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="5d26c-127">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5d26c-128">「成功」</span><span class="sxs-lookup"><span data-stu-id="5d26c-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="5d26c-129">0</span><span class="sxs-lookup"><span data-stu-id="5d26c-129">0</span></span>

<span data-ttu-id="5d26c-130">要求成功。</span><span class="sxs-lookup"><span data-stu-id="5d26c-130">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="5d26c-131">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="5d26c-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="5d26c-132">2</span><span class="sxs-lookup"><span data-stu-id="5d26c-132">2</span></span>

<span data-ttu-id="5d26c-133">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="5d26c-133">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="5d26c-134">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="5d26c-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="5d26c-135">8</span><span class="sxs-lookup"><span data-stu-id="5d26c-135">8</span></span>

<span data-ttu-id="5d26c-136">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="5d26c-136">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5d26c-137">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="5d26c-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="5d26c-138">9</span><span class="sxs-lookup"><span data-stu-id="5d26c-138">9</span></span>

<span data-ttu-id="5d26c-139">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="5d26c-139">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5d26c-140">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="5d26c-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="5d26c-141">10</span><span class="sxs-lookup"><span data-stu-id="5d26c-141">10</span></span>

<span data-ttu-id="5d26c-142">指定的物件已存在。</span><span class="sxs-lookup"><span data-stu-id="5d26c-142">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5d26c-143">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="5d26c-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="5d26c-144">11</span><span class="sxs-lookup"><span data-stu-id="5d26c-144">11</span></span>

<span data-ttu-id="5d26c-145">檔案系統不是 NTFS 檔案系統。</span><span class="sxs-lookup"><span data-stu-id="5d26c-145">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="5d26c-146">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="5d26c-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="5d26c-147">12</span><span class="sxs-lookup"><span data-stu-id="5d26c-147">12</span></span>

<span data-ttu-id="5d26c-148">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="5d26c-148">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="5d26c-149">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="5d26c-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="5d26c-150">13</span><span class="sxs-lookup"><span data-stu-id="5d26c-150">13</span></span>

<span data-ttu-id="5d26c-151">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="5d26c-151">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="5d26c-152">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="5d26c-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="5d26c-153">14</span><span class="sxs-lookup"><span data-stu-id="5d26c-153">14</span></span>

<span data-ttu-id="5d26c-154">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="5d26c-154">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="5d26c-155">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="5d26c-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="5d26c-156">15</span><span class="sxs-lookup"><span data-stu-id="5d26c-156">15</span></span>

<span data-ttu-id="5d26c-157">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="5d26c-157">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="5d26c-158">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="5d26c-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="5d26c-159">16</span><span class="sxs-lookup"><span data-stu-id="5d26c-159">16</span></span>

<span data-ttu-id="5d26c-160">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="5d26c-160">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5d26c-161">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="5d26c-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="5d26c-162">17</span><span class="sxs-lookup"><span data-stu-id="5d26c-162">17</span></span>

<span data-ttu-id="5d26c-163">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="5d26c-163">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="5d26c-164">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="5d26c-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5d26c-165">21</span><span class="sxs-lookup"><span data-stu-id="5d26c-165">21</span></span>

<span data-ttu-id="5d26c-166">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="5d26c-166">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d26c-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d26c-167">Requirements</span></span>



| <span data-ttu-id="5d26c-168">需求</span><span class="sxs-lookup"><span data-stu-id="5d26c-168">Requirement</span></span> | <span data-ttu-id="5d26c-169">值</span><span class="sxs-lookup"><span data-stu-id="5d26c-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d26c-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d26c-170">Minimum supported client</span></span><br/> | <span data-ttu-id="5d26c-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d26c-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d26c-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d26c-172">Minimum supported server</span></span><br/> | <span data-ttu-id="5d26c-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d26c-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d26c-174">命名空間</span><span class="sxs-lookup"><span data-stu-id="5d26c-174">Namespace</span></span><br/>                | <span data-ttu-id="5d26c-175">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5d26c-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5d26c-176">MOF</span><span class="sxs-lookup"><span data-stu-id="5d26c-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d26c-177"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d26c-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d26c-178">DLL</span><span class="sxs-lookup"><span data-stu-id="5d26c-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d26c-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d26c-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d26c-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d26c-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="5d26c-181">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5d26c-181">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5d26c-182">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="5d26c-182">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

