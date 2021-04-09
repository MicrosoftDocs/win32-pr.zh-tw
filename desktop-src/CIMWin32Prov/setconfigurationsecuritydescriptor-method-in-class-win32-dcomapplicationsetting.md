---
description: 使用 Win32 SecurityDescriptor 類別的實例所定義的新安全描述項，更新 DCOM 應用程式的設定安全描述項 \_ 。
ms.assetid: e0fe3d2f-7641-4cae-972d-888e800548de
ms.tgt_platform: multiple
title: Win32_DCOMApplicationSetting 類別的 SetConfigurationSecurityDescriptor 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.SetConfigurationSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8556e49d2e87e12763e3f0699bcff1f786ac1e72
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847084"
---
# <a name="setconfigurationsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="fad3a-103">Win32 DCOMApplicationSetting 類別的 SetConfigurationSecurityDescriptor 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fad3a-103">SetConfigurationSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="fad3a-104">**SetConfigurationSecurityDescriptor** 方法會使用 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)類別的實例所定義的新安全描述項，來更新 DCOM 應用程式的設定安全描述項。</span><span class="sxs-lookup"><span data-stu-id="fad3a-104">The **SetConfigurationSecurityDescriptor** method updates the configuration security descriptor of the DCOM application with a new security descriptor that is defined by an instance of a [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="fad3a-105">此安全描述項會控制哪些人可以設定應用程式。</span><span class="sxs-lookup"><span data-stu-id="fad3a-105">This security descriptor controls who is allowed to configure the application.</span></span> <span data-ttu-id="fad3a-106">執行腳本或應用程式（呼叫這個方法）的帳戶必須具有 **SeSecurityPrivilege** 和 **SeRestorePrivilege** 許可權。</span><span class="sxs-lookup"><span data-stu-id="fad3a-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privileges.</span></span> <span data-ttu-id="fad3a-107">如需詳細資訊，請參閱 [變更安全物件的存取安全性](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)。</span><span class="sxs-lookup"><span data-stu-id="fad3a-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="fad3a-108">語法</span><span class="sxs-lookup"><span data-stu-id="fad3a-108">Syntax</span></span>


```mof
uint32 SetConfigurationSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="fad3a-109">參數</span><span class="sxs-lookup"><span data-stu-id="fad3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fad3a-110">*描述* \[ 項在\]</span><span class="sxs-lookup"><span data-stu-id="fad3a-110">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fad3a-111">要針對 DCOM 應用程式設定的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="fad3a-111">The security descriptor to set for the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fad3a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="fad3a-112">Return value</span></span>

<span data-ttu-id="fad3a-113">傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="fad3a-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="fad3a-114">如需詳細資訊，請參閱 [WMI 傳回碼](/windows/desktop/WmiSdk/wmi-return-codes) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="fad3a-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="fad3a-115">「成功」</span><span class="sxs-lookup"><span data-stu-id="fad3a-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="fad3a-116">0</span><span class="sxs-lookup"><span data-stu-id="fad3a-116">0</span></span>

<span data-ttu-id="fad3a-117">成功完成</span><span class="sxs-lookup"><span data-stu-id="fad3a-117">Successful completion</span></span>

</dd> <dt>

<span data-ttu-id="fad3a-118">**2**</span><span class="sxs-lookup"><span data-stu-id="fad3a-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="fad3a-119">使用者無法存取所要求的資訊</span><span class="sxs-lookup"><span data-stu-id="fad3a-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="fad3a-120">**8**</span><span class="sxs-lookup"><span data-stu-id="fad3a-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="fad3a-121">未知的失敗</span><span class="sxs-lookup"><span data-stu-id="fad3a-121">Unknown failure</span></span>

</dd> <dt>

<span data-ttu-id="fad3a-122">**9**</span><span class="sxs-lookup"><span data-stu-id="fad3a-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="fad3a-123">使用者沒有足夠的許可權來執行方法</span><span class="sxs-lookup"><span data-stu-id="fad3a-123">The user does not have adequate privileges to execute the method</span></span>

</dd> <dt>

<span data-ttu-id="fad3a-124">**21**</span><span class="sxs-lookup"><span data-stu-id="fad3a-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="fad3a-125">在方法呼叫中指定的參數無效</span><span class="sxs-lookup"><span data-stu-id="fad3a-125">A parameter specified in the method call is invalid</span></span>

</dd> <dt>

<span data-ttu-id="fad3a-126">**其他**</span><span class="sxs-lookup"><span data-stu-id="fad3a-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="fad3a-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="fad3a-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fad3a-128">備註</span><span class="sxs-lookup"><span data-stu-id="fad3a-128">Remarks</span></span>

<span data-ttu-id="fad3a-129">[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例代表 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control)資料類型，並包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)，以及 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="fad3a-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="fad3a-130">如需詳細資訊，請參閱 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。</span><span class="sxs-lookup"><span data-stu-id="fad3a-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="fad3a-131">如果未在取得安全描述項時授與或啟用 **SeSecurityPrivilege** ，則只會傳回傳回的安全描述項中的 DACL。</span><span class="sxs-lookup"><span data-stu-id="fad3a-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="fad3a-132">如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants) 和 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。</span><span class="sxs-lookup"><span data-stu-id="fad3a-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="fad3a-133">呼叫這個方法時，您可以同時更新 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 實例中的 dacl 和 SACL，但是您也可以只更新 dacl 或只更新 sacl。</span><span class="sxs-lookup"><span data-stu-id="fad3a-133">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="fad3a-134">[ [**安全 \_ 描述項] \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control) 中的下列值，可決定是否要更新 DACL、SACL 或兩者。</span><span class="sxs-lookup"><span data-stu-id="fad3a-134">The following values in the [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="fad3a-135">**\_有 SE DACL \_**</span><span class="sxs-lookup"><span data-stu-id="fad3a-135">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="fad3a-136">表示 DACL 應該更新。</span><span class="sxs-lookup"><span data-stu-id="fad3a-136">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="fad3a-137">如果未設定此值，WMI 就會保留 DACL 的原始值。</span><span class="sxs-lookup"><span data-stu-id="fad3a-137">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="fad3a-138">**\_出現 SE SACL \_**</span><span class="sxs-lookup"><span data-stu-id="fad3a-138">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="fad3a-139">指出 SACL 應該更新。</span><span class="sxs-lookup"><span data-stu-id="fad3a-139">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="fad3a-140">如果未設定此值，WMI 就會保留 SACL 的原始值。</span><span class="sxs-lookup"><span data-stu-id="fad3a-140">If this is not set then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="fad3a-141">若要更新 SACL，帳戶必須啟用 **SeSecurityPrivilege** 許可權。</span><span class="sxs-lookup"><span data-stu-id="fad3a-141">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="fad3a-142">針對腳本，許可權名稱為 **SeSecurityPrivilege**。</span><span class="sxs-lookup"><span data-stu-id="fad3a-142">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="fad3a-143">如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants)。</span><span class="sxs-lookup"><span data-stu-id="fad3a-143">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="fad3a-144">如果群組信任者和擁有者信任的屬性不是 **Null**，則會更新這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fad3a-144">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="fad3a-145">否則，WMI 會保留原始值。</span><span class="sxs-lookup"><span data-stu-id="fad3a-145">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="fad3a-146">如需詳細資訊，請參閱 [WMI 安全描述項物件](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)。</span><span class="sxs-lookup"><span data-stu-id="fad3a-146">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="fad3a-147">當新的 SACL 在呼叫這個方法時為 **Null** ，則目標安全物件上的安全描述項 SACL 會保持不變。</span><span class="sxs-lookup"><span data-stu-id="fad3a-147">When a new SACL is **NULL** in a call to this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="fad3a-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="fad3a-148">Requirements</span></span>



| <span data-ttu-id="fad3a-149">需求</span><span class="sxs-lookup"><span data-stu-id="fad3a-149">Requirement</span></span> | <span data-ttu-id="fad3a-150">值</span><span class="sxs-lookup"><span data-stu-id="fad3a-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fad3a-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fad3a-151">Minimum supported client</span></span><br/> | <span data-ttu-id="fad3a-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fad3a-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fad3a-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fad3a-153">Minimum supported server</span></span><br/> | <span data-ttu-id="fad3a-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fad3a-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fad3a-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="fad3a-155">Namespace</span></span><br/>                | <span data-ttu-id="fad3a-156">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fad3a-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fad3a-157">MOF</span><span class="sxs-lookup"><span data-stu-id="fad3a-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fad3a-158"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fad3a-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fad3a-159">DLL</span><span class="sxs-lookup"><span data-stu-id="fad3a-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fad3a-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fad3a-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fad3a-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fad3a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad3a-162">**Win32 \_ DCOMApplicationSetting**</span><span class="sxs-lookup"><span data-stu-id="fad3a-162">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="fad3a-163">**許可權常數**</span><span class="sxs-lookup"><span data-stu-id="fad3a-163">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="fad3a-164">WMI 安全描述項物件</span><span class="sxs-lookup"><span data-stu-id="fad3a-164">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="fad3a-165">變更安全物件的存取安全性</span><span class="sxs-lookup"><span data-stu-id="fad3a-165">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

