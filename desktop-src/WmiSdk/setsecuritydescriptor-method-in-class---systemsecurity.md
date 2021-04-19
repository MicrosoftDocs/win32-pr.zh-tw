---
description: 寫入安全描述項的更新版本，以控制您所連接之 WMI 命名空間的存取權。 安全描述項會以 SecurityDescriptor 的實例來表示 \_ \_ 。
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: __SystemSecurity 類別的 SetSecurityDescriptor 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: fcdc192801b839451cee256f57090780818d2046
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987673"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a><span data-ttu-id="e5d2e-104">\_ \_ SystemSecurity 類別的 SetSecurityDescriptor 方法</span><span class="sxs-lookup"><span data-stu-id="e5d2e-104">SetSecurityDescriptor method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="e5d2e-105">[**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer)方法會寫入安全描述項的更新版本，以控制您所連接之 WMI 命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-105">The [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) method writes an updated version of the security descriptor that controls access to the WMI namespace to which you are connected.</span></span> <span data-ttu-id="e5d2e-106">安全描述項會以 [**\_ \_ SecurityDescriptor**](--securitydescriptor.md)的實例來表示。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-106">The security descriptor is represented by an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span> <span data-ttu-id="e5d2e-107">如需詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-107">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e5d2e-108">語法</span><span class="sxs-lookup"><span data-stu-id="e5d2e-108">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="e5d2e-109">參數</span><span class="sxs-lookup"><span data-stu-id="e5d2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5d2e-110">*描述* \[ 項在\]</span><span class="sxs-lookup"><span data-stu-id="e5d2e-110">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d2e-111">與 WMI 命名空間相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-111">The security descriptor associated with the WMI Namespace.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5d2e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5d2e-112">Return value</span></span>

<span data-ttu-id="e5d2e-113">傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="e5d2e-114">如需詳細資訊，請參閱 [WMI 傳回碼](wmi-return-codes.md) 或 [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-114">For more information, see [WMI Return Codes](wmi-return-codes.md) or [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="e5d2e-115">**0**</span><span class="sxs-lookup"><span data-stu-id="e5d2e-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e5d2e-116">順利完成。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="e5d2e-117">**2**</span><span class="sxs-lookup"><span data-stu-id="e5d2e-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e5d2e-118">使用者無法存取所要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-118">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="e5d2e-119">**8**</span><span class="sxs-lookup"><span data-stu-id="e5d2e-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e5d2e-120">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-120">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="e5d2e-121">**9**</span><span class="sxs-lookup"><span data-stu-id="e5d2e-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e5d2e-122">使用者沒有足夠的許可權來執行方法。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-122">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="e5d2e-123">**21**</span><span class="sxs-lookup"><span data-stu-id="e5d2e-123">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e5d2e-124">在方法呼叫中指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-124">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5d2e-125">備註</span><span class="sxs-lookup"><span data-stu-id="e5d2e-125">Remarks</span></span>

<span data-ttu-id="e5d2e-126">[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例代表 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control)資料類型，並包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)，以及 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/a-gly)。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-126">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*System Access Control List*](/windows/desktop/SecGloss/a-gly) (SACL).</span></span> <span data-ttu-id="e5d2e-127">如需詳細資訊，請參閱 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-127">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="e5d2e-128">如果未在取得安全描述項時授與或啟用 **SeSecurityPrivilege** ，則只會傳回傳回的安全描述項中的 DACL。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-128">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="e5d2e-129">如需詳細資訊，請參閱 [**許可權常數**](privilege-constants.md) 和 [執行特殊許可權作業](executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-129">For more information, see [**Privilege Constants**](privilege-constants.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

<span data-ttu-id="e5d2e-130">呼叫這個方法時，您可以同時更新 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 實例中的 dacl 和 SACL，但是您也可以只更新 dacl 或只更新 sacl。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-130">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="e5d2e-131">下列 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control) 中的值會決定是否要更新 DACL 或 SACL 或兩者。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-131">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL or the SACL or both are updated.</span></span>

-   <span data-ttu-id="e5d2e-132">**\_有 SE DACL \_**</span><span class="sxs-lookup"><span data-stu-id="e5d2e-132">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="e5d2e-133">表示 DACL 應該更新。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-133">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="e5d2e-134">如果未設定此值，WMI 就會保留 DACL 的原始值。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-134">If this is not set then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="e5d2e-135">**\_出現 SE SACL \_**</span><span class="sxs-lookup"><span data-stu-id="e5d2e-135">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="e5d2e-136">指出 SACL 應該更新。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-136">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="e5d2e-137">如果未設定此值，WMI 就會保留 SACL 的原始值。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-137">If this is not set then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="e5d2e-138">若要更新 SACL，帳戶必須啟用 **SeSecurityPrivilege** 許可權。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-138">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="e5d2e-139">針對腳本，許可權名稱為 **SeSecurityPrivilege**。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-139">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="e5d2e-140">如需詳細資訊，請參閱 [**許可權常數**](privilege-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-140">For more information, see [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="e5d2e-141">如果群組信任者和擁有者信任的屬性不是 **Null**，則會更新這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-141">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="e5d2e-142">否則，WMI 會保留原始值。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-142">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="e5d2e-143">如需詳細資訊，請參閱 [WMI 安全描述項物件](wmi-security-descriptor-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-143">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md).</span></span>

<span data-ttu-id="e5d2e-144">當中的新 SACL 是 **Null** 時，在呼叫這個方法時，目標安全物件上的安全描述項 SACL 會保持不變。</span><span class="sxs-lookup"><span data-stu-id="e5d2e-144">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5d2e-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5d2e-145">Requirements</span></span>



| <span data-ttu-id="e5d2e-146">需求</span><span class="sxs-lookup"><span data-stu-id="e5d2e-146">Requirement</span></span> | <span data-ttu-id="e5d2e-147">值</span><span class="sxs-lookup"><span data-stu-id="e5d2e-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e5d2e-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5d2e-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e5d2e-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5d2e-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e5d2e-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5d2e-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e5d2e-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5d2e-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e5d2e-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="e5d2e-152">Namespace</span></span><br/>                | <span data-ttu-id="e5d2e-153">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="e5d2e-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="e5d2e-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5d2e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5d2e-155">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="e5d2e-155">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="e5d2e-156">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="e5d2e-156">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

