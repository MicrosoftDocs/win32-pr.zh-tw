---
description: 取得安全描述項，控制誰可以存取 DCOM 應用程式。
ms.assetid: 5ddd563b-f731-47ac-8a13-20940adfa86d
ms.tgt_platform: multiple
title: Win32_DCOMApplicationSetting 類別的 GetAccessSecurityDescriptor 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.GetAccessSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e8d87150582a425d23988f70f88ea36bc356476a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970718"
---
# <a name="getaccesssecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="9db33-103">Win32 DCOMApplicationSetting 類別的 GetAccessSecurityDescriptor 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9db33-103">GetAccessSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="9db33-104">**GetAccessSecurityDescriptor** WMI 方法會取得安全描述項，以控制誰可以存取 DCOM 應用程式。</span><span class="sxs-lookup"><span data-stu-id="9db33-104">The **GetAccessSecurityDescriptor** WMI method gets the security descriptor that controls who can access a DCOM application.</span></span> <span data-ttu-id="9db33-105">安全描述項是 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="9db33-105">The security descriptor is an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="9db33-106">執行腳本或應用程式（呼叫這個方法）的帳戶必須具有 **SeSecurityPrivilege** 和 **SeRestorePrivilege** 許可權。</span><span class="sxs-lookup"><span data-stu-id="9db33-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privilege.</span></span> <span data-ttu-id="9db33-107">如需詳細資訊，請參閱 [變更安全物件的存取安全性](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)。</span><span class="sxs-lookup"><span data-stu-id="9db33-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="9db33-108">語法</span><span class="sxs-lookup"><span data-stu-id="9db33-108">Syntax</span></span>


```mof
uint32 GetAccessSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="9db33-109">參數</span><span class="sxs-lookup"><span data-stu-id="9db33-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db33-110">*描述* \[ 項擴展\]</span><span class="sxs-lookup"><span data-stu-id="9db33-110">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9db33-111">要針對 DCOM 應用程式設定的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="9db33-111">The security descriptor to set for the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db33-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9db33-112">Return value</span></span>

<span data-ttu-id="9db33-113">傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="9db33-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="9db33-114">如需詳細資訊，請參閱 [WMI 傳回碼](/windows/desktop/WmiSdk/wmi-return-codes) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="9db33-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="9db33-115">「成功」</span><span class="sxs-lookup"><span data-stu-id="9db33-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="9db33-116">0</span><span class="sxs-lookup"><span data-stu-id="9db33-116">0</span></span>

<span data-ttu-id="9db33-117">成功完成</span><span class="sxs-lookup"><span data-stu-id="9db33-117">Successful completion</span></span>

</dd> <dt>

<span data-ttu-id="9db33-118">**2**</span><span class="sxs-lookup"><span data-stu-id="9db33-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="9db33-119">使用者無法存取所要求的資訊</span><span class="sxs-lookup"><span data-stu-id="9db33-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="9db33-120">**8**</span><span class="sxs-lookup"><span data-stu-id="9db33-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="9db33-121">未知的失敗</span><span class="sxs-lookup"><span data-stu-id="9db33-121">Unknown failure</span></span>

</dd> <dt>

<span data-ttu-id="9db33-122">**9**</span><span class="sxs-lookup"><span data-stu-id="9db33-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="9db33-123">使用者沒有足夠的許可權來執行方法</span><span class="sxs-lookup"><span data-stu-id="9db33-123">The user does not have adequate privileges to execute the method</span></span>

</dd> <dt>

<span data-ttu-id="9db33-124">**21**</span><span class="sxs-lookup"><span data-stu-id="9db33-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="9db33-125">在方法呼叫中指定的參數無效</span><span class="sxs-lookup"><span data-stu-id="9db33-125">A parameter specified in the method call is invalid</span></span>

</dd> <dt>

<span data-ttu-id="9db33-126">**其他**</span><span class="sxs-lookup"><span data-stu-id="9db33-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="9db33-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="9db33-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9db33-128">備註</span><span class="sxs-lookup"><span data-stu-id="9db33-128">Remarks</span></span>

<span data-ttu-id="9db33-129">[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例代表 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control)資料類型，並包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)，以及 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="9db33-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="9db33-130">如需詳細資訊，請參閱 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。</span><span class="sxs-lookup"><span data-stu-id="9db33-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="9db33-131">如果未在取得安全描述項時授與或啟用 **SeSecurityPrivilege** ，則只會傳回傳回的安全描述項中的 DACL。</span><span class="sxs-lookup"><span data-stu-id="9db33-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="9db33-132">如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants) 和 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。</span><span class="sxs-lookup"><span data-stu-id="9db33-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="9db33-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="9db33-133">Requirements</span></span>



| <span data-ttu-id="9db33-134">需求</span><span class="sxs-lookup"><span data-stu-id="9db33-134">Requirement</span></span> | <span data-ttu-id="9db33-135">值</span><span class="sxs-lookup"><span data-stu-id="9db33-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9db33-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9db33-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9db33-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9db33-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9db33-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9db33-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9db33-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9db33-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9db33-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="9db33-140">Namespace</span></span><br/>                | <span data-ttu-id="9db33-141">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9db33-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9db33-142">MOF</span><span class="sxs-lookup"><span data-stu-id="9db33-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9db33-143"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9db33-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9db33-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9db33-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9db33-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9db33-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9db33-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9db33-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db33-147">**Win32 \_ DCOMApplicationSetting**</span><span class="sxs-lookup"><span data-stu-id="9db33-147">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="9db33-148">**許可權常數**</span><span class="sxs-lookup"><span data-stu-id="9db33-148">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="9db33-149">WMI 安全描述項物件</span><span class="sxs-lookup"><span data-stu-id="9db33-149">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="9db33-150">變更安全物件的存取安全性</span><span class="sxs-lookup"><span data-stu-id="9db33-150">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

