---
description: 寫入控制印表機存取權之安全描述項的更新版本。
ms.assetid: 6a709043-473e-4b24-8b52-6c68b670ebcf
ms.tgt_platform: multiple
title: Win32_Printer 類別的 SetSecurityDescriptor 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1572919d0ac0b5c18a6fc5084636c52b9b3ea1c6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191042"
---
# <a name="setsecuritydescriptor-method-of-the-win32_printer-class"></a><span data-ttu-id="e6ccf-103">Win32 Printer 類別的 SetSecurityDescriptor 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e6ccf-103">SetSecurityDescriptor method of the Win32\_Printer class</span></span>

<span data-ttu-id="e6ccf-104">**SetSecurityDescriptor** 方法會寫入控制印表機存取權之安全描述項的更新版本。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-104">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="e6ccf-105">安全描述項是 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-105">The security descriptor is an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="e6ccf-106">如需詳細資訊，請參閱 [變更安全物件的存取安全性](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-106">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

<span data-ttu-id="e6ccf-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e6ccf-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e6ccf-109">語法</span><span class="sxs-lookup"><span data-stu-id="e6ccf-109">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="e6ccf-110">參數</span><span class="sxs-lookup"><span data-stu-id="e6ccf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6ccf-111">*描述* \[ 項在\]</span><span class="sxs-lookup"><span data-stu-id="e6ccf-111">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ccf-112">與印表機相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-112">The security descriptor that is associated with the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6ccf-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6ccf-113">Return value</span></span>

<span data-ttu-id="e6ccf-114">傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-114">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="e6ccf-115">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e6ccf-116">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e6ccf-117">**0**</span><span class="sxs-lookup"><span data-stu-id="e6ccf-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e6ccf-118">順利完成。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-118">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="e6ccf-119">**2**</span><span class="sxs-lookup"><span data-stu-id="e6ccf-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e6ccf-120">使用者無法存取所要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-120">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="e6ccf-121">**8**</span><span class="sxs-lookup"><span data-stu-id="e6ccf-121">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e6ccf-122">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-122">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="e6ccf-123">**9**</span><span class="sxs-lookup"><span data-stu-id="e6ccf-123">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e6ccf-124">使用者沒有足夠的許可權來執行方法。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-124">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="e6ccf-125">**21**</span><span class="sxs-lookup"><span data-stu-id="e6ccf-125">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e6ccf-126">在方法呼叫中指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-126">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6ccf-127">備註</span><span class="sxs-lookup"><span data-stu-id="e6ccf-127">Remarks</span></span>

<span data-ttu-id="e6ccf-128">[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例代表 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control)資料類型，並包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)，以及 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-128">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="e6ccf-129">如需詳細資訊，請參閱 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-129">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="e6ccf-130">如果未在取得安全描述項時授與或啟用 **SeSecurityPrivilege** ，則只會傳回傳回的安全描述項中的 DACL。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-130">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="e6ccf-131">如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants) 和 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-131">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="e6ccf-132">呼叫這個方法時，您可以同時更新 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 實例中的 dacl 和 SACL，但是您也可以只更新 dacl 或只更新 sacl。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-132">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you can also update only the DACL or only the SACL.</span></span>

<span data-ttu-id="e6ccf-133">下列 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control) 中的值會決定是否要更新 DACL、SACL 或兩者。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-133">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="e6ccf-134">**\_有 SE DACL \_**</span><span class="sxs-lookup"><span data-stu-id="e6ccf-134">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="e6ccf-135">表示 DACL 應該更新。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-135">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="e6ccf-136">如果未設定此值，WMI 就會保留 DACL 的原始值。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-136">If this is not set then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="e6ccf-137">**\_出現 SE SACL \_**</span><span class="sxs-lookup"><span data-stu-id="e6ccf-137">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="e6ccf-138">指出 SACL 應該更新。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-138">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="e6ccf-139">如果未設定此值，WMI 就會保留 SACL 的原始值。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-139">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="e6ccf-140">若要更新 SACL，帳戶必須啟用 **SeSecurityPrivilege** 許可權。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-140">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="e6ccf-141">針對腳本，許可權名稱為 **SeSecurityPrivilege**。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-141">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="e6ccf-142">如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants)。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-142">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="e6ccf-143">如果群組信任者和擁有者信任的屬性不是 **Null**，則會更新這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-143">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="e6ccf-144">否則，WMI 會保留原始值。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-144">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="e6ccf-145">如需詳細資訊，請參閱 [WMI 安全描述項物件](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-145">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="e6ccf-146">當新的 SACL 在呼叫這個方法時為 **Null** ，則目標安全物件上的安全描述項 SACL 會保持不變。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-146">When a new SACL is **NULL** in a call to this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="examples"></a><span data-ttu-id="e6ccf-147">範例</span><span class="sxs-lookup"><span data-stu-id="e6ccf-147">Examples</span></span>

<span data-ttu-id="e6ccf-148">[ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) PowerShell 範例會將許可權 (ACL) 從某個印表機取代為另一個印表機。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-148">The [Copy-ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) PowerShell sample Replace the permissions (ACL) from one printer to another.</span></span>

<span data-ttu-id="e6ccf-149">下列 PowerShell 程式碼範例說明如何設定印表機的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="e6ccf-149">The following PowerShell code sample describes how to set the security descriptor for a printer.</span></span>


```PowerShell
# Specify the user or group
$user = "everyone"

# create instances of necessary classes
$SD = ([WMIClass] "Win32_SecurityDescriptor").CreateInstance()
$ace = ([WMIClass] "Win32_Ace").CreateInstance()
$Trustee = ([WMIClass] "Win32_Trustee").CreateInstance()

# Translate a name of user or group to SID
$SID = (new-object security.principal.ntaccount $user).translate([security.principal.securityidentifier])

# Get binary form from SID and byte Array
[byte[]] $SIDArray = ,0 * $SID.BinaryLength
$SID.GetBinaryForm($SIDArray,0)

# Fill Trustee object parameters
$Trustee.Name = $user
$Trustee.SID = $SIDArray

# Set AccessMask which can contain following values:
# Takeownership - 524288
# ReadPermissions - 131072
# ChangePermissions - 262144
# ManageDocuments - 983088
# ManagePrinters - 983052
# Print + ReadPermissions - 131080
$ace.AccessMask = 983052

# Set AceType. Can be 0 (Allow), or 1 (Deny), or 2 (System Audit)
$ace.AceType = 0
$ace.AceFlags = 0  

# Write Win32_Trustee object to Win32_Ace Trustee property
$ace.Trustee = $Trustee

# Write Win32_Ace and Win32_Trustee objects to SecurityDescriptor object
$SD.DACL = $ace

# Set SE_DACL_PRESENT control flag
$SD.ControlFlags = 0x0004

# Get printer object. For example 'CutePDF Writer' printer object
$Printer = gwmi win32_printer -filter "name = 'CutePDF Writer'"

# Enable SeSecurityPrivilege privilegies
$Printer.psbase.Scope.Options.EnablePrivileges = $true

# Invoke SetSecurityDescriptor method and write new ACE to specified
# printer ACL.
$Printer.SetSecurityDescriptor($SD)
```



## <a name="requirements"></a><span data-ttu-id="e6ccf-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6ccf-150">Requirements</span></span>



| <span data-ttu-id="e6ccf-151">需求</span><span class="sxs-lookup"><span data-stu-id="e6ccf-151">Requirement</span></span> | <span data-ttu-id="e6ccf-152">值</span><span class="sxs-lookup"><span data-stu-id="e6ccf-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ccf-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6ccf-153">Minimum supported client</span></span><br/> | <span data-ttu-id="e6ccf-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6ccf-154">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="e6ccf-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6ccf-155">Minimum supported server</span></span><br/> | <span data-ttu-id="e6ccf-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6ccf-156">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="e6ccf-157">命名空間</span><span class="sxs-lookup"><span data-stu-id="e6ccf-157">Namespace</span></span><br/>                | <span data-ttu-id="e6ccf-158">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e6ccf-158">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="e6ccf-159">MOF</span><span class="sxs-lookup"><span data-stu-id="e6ccf-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6ccf-160"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6ccf-160"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6ccf-161">DLL</span><span class="sxs-lookup"><span data-stu-id="e6ccf-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6ccf-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6ccf-162"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="e6ccf-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6ccf-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6ccf-164">**Win32 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="e6ccf-164">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="e6ccf-165">**許可權常數**</span><span class="sxs-lookup"><span data-stu-id="e6ccf-165">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="e6ccf-166">WMI 安全描述項物件</span><span class="sxs-lookup"><span data-stu-id="e6ccf-166">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="e6ccf-167">變更安全物件的存取安全性</span><span class="sxs-lookup"><span data-stu-id="e6ccf-167">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

