---
description: 取得安全描述項，可控制您所連接之 WMI 命名空間的存取權。 安全描述項會以 SecurityDescriptor 的實例傳回 \_ \_ 。
ms.assetid: b031af45-9237-434d-91db-69222306c615
ms.tgt_platform: multiple
title: __SystemSecurity 類別的 GetSecurityDescriptor 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 7aece0a50678689141de9b9a38a014414578de3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980560"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a><span data-ttu-id="b0fc7-104">\_ \_ SystemSecurity 類別的 GetSecurityDescriptor 方法</span><span class="sxs-lookup"><span data-stu-id="b0fc7-104">GetSecurityDescriptor method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="b0fc7-105">**GetSecurityDescriptor** 方法會取得安全描述項，以控制您所連接之 WMI 命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="b0fc7-105">The **GetSecurityDescriptor** method gets the security descriptor that controls access to the WMI namespace to which you are connected.</span></span> <span data-ttu-id="b0fc7-106">安全描述項會以 [**\_ \_ SecurityDescriptor**](--securitydescriptor.md)的實例傳回。</span><span class="sxs-lookup"><span data-stu-id="b0fc7-106">The security descriptor is returned as an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span> <span data-ttu-id="b0fc7-107">如需詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="b0fc7-107">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0fc7-108">語法</span><span class="sxs-lookup"><span data-stu-id="b0fc7-108">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="b0fc7-109">參數</span><span class="sxs-lookup"><span data-stu-id="b0fc7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0fc7-110">*描述* \[ 項擴展\]</span><span class="sxs-lookup"><span data-stu-id="b0fc7-110">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0fc7-111">與 WMI 命名空間相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b0fc7-111">The security descriptor associated with the WMI namespace.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0fc7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b0fc7-112">Return value</span></span>

<span data-ttu-id="b0fc7-113">傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="b0fc7-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="b0fc7-114">如需詳細資訊，請參閱 [WMI 傳回碼](wmi-return-codes.md) 或 [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="b0fc7-114">For more information, see [WMI Return Codes](wmi-return-codes.md) or [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="b0fc7-115">**0**</span><span class="sxs-lookup"><span data-stu-id="b0fc7-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b0fc7-116">順利完成。</span><span class="sxs-lookup"><span data-stu-id="b0fc7-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="b0fc7-117">**2**</span><span class="sxs-lookup"><span data-stu-id="b0fc7-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b0fc7-118">使用者無法存取所要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="b0fc7-118">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="b0fc7-119">**8**</span><span class="sxs-lookup"><span data-stu-id="b0fc7-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b0fc7-120">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="b0fc7-120">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="b0fc7-121">**9**</span><span class="sxs-lookup"><span data-stu-id="b0fc7-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b0fc7-122">使用者沒有足夠的許可權來執行方法。</span><span class="sxs-lookup"><span data-stu-id="b0fc7-122">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="b0fc7-123">**21**</span><span class="sxs-lookup"><span data-stu-id="b0fc7-123">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b0fc7-124">在方法呼叫中指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="b0fc7-124">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0fc7-125">備註</span><span class="sxs-lookup"><span data-stu-id="b0fc7-125">Remarks</span></span>

<span data-ttu-id="b0fc7-126">[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例代表 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control)資料類型，並包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)，以及 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="b0fc7-126">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="b0fc7-127">如需詳細資訊，請參閱 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。</span><span class="sxs-lookup"><span data-stu-id="b0fc7-127">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="b0fc7-128">如果未在取得安全描述項時授與或啟用 **SeSecurityPrivilege** ，則只會傳回傳回的安全描述項中的 DACL。</span><span class="sxs-lookup"><span data-stu-id="b0fc7-128">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="b0fc7-129">如需詳細資訊，請參閱 [**許可權常數**](privilege-constants.md) 和 [執行特殊許可權作業](executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="b0fc7-129">For more information, see [**Privilege Constants**](privilege-constants.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0fc7-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0fc7-130">Requirements</span></span>



| <span data-ttu-id="b0fc7-131">需求</span><span class="sxs-lookup"><span data-stu-id="b0fc7-131">Requirement</span></span> | <span data-ttu-id="b0fc7-132">值</span><span class="sxs-lookup"><span data-stu-id="b0fc7-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b0fc7-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0fc7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b0fc7-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0fc7-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b0fc7-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0fc7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b0fc7-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0fc7-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b0fc7-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="b0fc7-137">Namespace</span></span><br/>                | <span data-ttu-id="b0fc7-138">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="b0fc7-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b0fc7-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0fc7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0fc7-140">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="b0fc7-140">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="b0fc7-141">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="b0fc7-141">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

