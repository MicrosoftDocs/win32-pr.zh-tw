---
description: 傳回控制印表機存取的安全描述項。
ms.assetid: c12ca35c-07b3-41ad-98c4-48ee584059d1
ms.tgt_platform: multiple
title: Win32_Printer 類別的 GetSecurityDescriptor 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c74d79430d15fa136c6edeb2a6e77e79e76b02ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971128"
---
# <a name="getsecuritydescriptor-method-of-the-win32_printer-class"></a><span data-ttu-id="4e21c-103">Win32 Printer 類別的 GetSecurityDescriptor 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4e21c-103">GetSecurityDescriptor method of the Win32\_Printer class</span></span>

<span data-ttu-id="4e21c-104">**GetSecurityDescriptor** 方法會傳回控制印表機存取的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="4e21c-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="4e21c-105">描述項會以 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)的實例傳回。</span><span class="sxs-lookup"><span data-stu-id="4e21c-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="4e21c-106">如需詳細資訊，請參閱 [變更安全物件的存取安全性](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)。</span><span class="sxs-lookup"><span data-stu-id="4e21c-106">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

<span data-ttu-id="4e21c-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="4e21c-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4e21c-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="4e21c-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4e21c-109">語法</span><span class="sxs-lookup"><span data-stu-id="4e21c-109">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="4e21c-110">參數</span><span class="sxs-lookup"><span data-stu-id="4e21c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e21c-111">*描述* \[ 項擴展\]</span><span class="sxs-lookup"><span data-stu-id="4e21c-111">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e21c-112">與印表機相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="4e21c-112">The security descriptor associated with the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e21c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e21c-113">Return value</span></span>

<span data-ttu-id="4e21c-114">傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="4e21c-114">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="4e21c-115">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="4e21c-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4e21c-116">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="4e21c-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4e21c-117">**0**</span><span class="sxs-lookup"><span data-stu-id="4e21c-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4e21c-118">順利完成。</span><span class="sxs-lookup"><span data-stu-id="4e21c-118">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="4e21c-119">**2**</span><span class="sxs-lookup"><span data-stu-id="4e21c-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="4e21c-120">使用者無法存取所要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="4e21c-120">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="4e21c-121">**8**</span><span class="sxs-lookup"><span data-stu-id="4e21c-121">**8**</span></span>
</dt> <dd>

<span data-ttu-id="4e21c-122">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="4e21c-122">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="4e21c-123">**9**</span><span class="sxs-lookup"><span data-stu-id="4e21c-123">**9**</span></span>
</dt> <dd>

<span data-ttu-id="4e21c-124">使用者沒有足夠的許可權來執行方法。</span><span class="sxs-lookup"><span data-stu-id="4e21c-124">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="4e21c-125">**21**</span><span class="sxs-lookup"><span data-stu-id="4e21c-125">**21**</span></span>
</dt> <dd>

<span data-ttu-id="4e21c-126">在方法呼叫中指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="4e21c-126">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e21c-127">備註</span><span class="sxs-lookup"><span data-stu-id="4e21c-127">Remarks</span></span>

<span data-ttu-id="4e21c-128">[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例代表 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control)資料類型，並包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)，以及 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="4e21c-128">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="4e21c-129">如需詳細資訊，請參閱 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。</span><span class="sxs-lookup"><span data-stu-id="4e21c-129">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="4e21c-130">如果未在取得安全描述項時授與或啟用 **SeSecurityPrivilege** ，則只會傳回傳回的安全描述項中的 DACL。</span><span class="sxs-lookup"><span data-stu-id="4e21c-130">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="4e21c-131">如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants) 和 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。</span><span class="sxs-lookup"><span data-stu-id="4e21c-131">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="4e21c-132">範例</span><span class="sxs-lookup"><span data-stu-id="4e21c-132">Examples</span></span>

<span data-ttu-id="4e21c-133">下列 VBScript 程式碼範例會列出連接到本機電腦的印表機，並取得每部印表機的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="4e21c-133">The following VBScript code example lists the printers attached to the local computer and gets the security descriptor for each printer.</span></span> <span data-ttu-id="4e21c-134">然後， (ACE) 在 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)中的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)， (DACL) 會進行解壓縮，以判斷哪些使用者可以存取印表機。</span><span class="sxs-lookup"><span data-stu-id="4e21c-134">Then the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACE) in the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) are extracted to determine which users have access to the printer.</span></span>


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set objWMIService = GetObject("winmgmts:")
Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        arrACEs = objSD.DACL
    For Each objACE in arrACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="requirements"></a><span data-ttu-id="4e21c-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e21c-135">Requirements</span></span>



| <span data-ttu-id="4e21c-136">需求</span><span class="sxs-lookup"><span data-stu-id="4e21c-136">Requirement</span></span> | <span data-ttu-id="4e21c-137">值</span><span class="sxs-lookup"><span data-stu-id="4e21c-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e21c-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e21c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4e21c-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e21c-139">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="4e21c-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e21c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4e21c-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e21c-141">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="4e21c-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="4e21c-142">Namespace</span></span><br/>                | <span data-ttu-id="4e21c-143">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4e21c-143">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="4e21c-144">MOF</span><span class="sxs-lookup"><span data-stu-id="4e21c-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e21c-145"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e21c-145"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e21c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4e21c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e21c-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e21c-147"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="4e21c-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e21c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e21c-149">**Win32 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="4e21c-149">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="4e21c-150">**許可權常數**</span><span class="sxs-lookup"><span data-stu-id="4e21c-150">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="4e21c-151">WMI 安全描述項物件</span><span class="sxs-lookup"><span data-stu-id="4e21c-151">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="4e21c-152">變更安全物件的存取安全性</span><span class="sxs-lookup"><span data-stu-id="4e21c-152">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

