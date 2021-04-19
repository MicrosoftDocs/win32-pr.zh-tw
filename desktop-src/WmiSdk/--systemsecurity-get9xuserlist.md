---
description: 針對執行過時 Windows 的電腦上的個別使用者清單取得遠端存取許可權，但無法使用透過 Windows 安全描述項的存取控制。
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: __SystemSecurity：： Get9XUserList 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Get9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: 521f2fe489089d486480c138293ebea39ca6f105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975827"
---
# <a name="__systemsecurityget9xuserlist-method"></a><span data-ttu-id="0061c-103">\_\_SystemSecurity：： Get9XUserList 方法</span><span class="sxs-lookup"><span data-stu-id="0061c-103">\_\_SystemSecurity::Get9XUserList method</span></span>

<span data-ttu-id="0061c-104">[**\_ \_ SystemSecurity：： Set9XUserList**](--systemsecurity-set9xuserlist.md)方法會針對執行過時 windows 的電腦上的個別使用者清單取得遠端存取許可權，但無法使用透過 windows 安全描述項的存取控制。</span><span class="sxs-lookup"><span data-stu-id="0061c-104">The [**\_\_SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) method gets the remote access rights for a list of individual users on computers running obsolete versions of Windows , where access control through Windows security descriptors is not available.</span></span>

<span data-ttu-id="0061c-105">這項功能類似于安全描述項，但更受限制。</span><span class="sxs-lookup"><span data-stu-id="0061c-105">This functions similar to the security descriptor, but it is more limited.</span></span> <span data-ttu-id="0061c-106">群組不受支援，而且無法控制本機存取，因為本機使用者一律具有完整存取權。</span><span class="sxs-lookup"><span data-stu-id="0061c-106">Groups are not supported and there is no control over local access, because the local user always has full access.</span></span> <span data-ttu-id="0061c-107">拒絕和允許存取控制專案 (ACE) ，因此 ACE 順序在 (DACL) 的任意存取控制清單中很重要。</span><span class="sxs-lookup"><span data-stu-id="0061c-107">Both deny and allow access control entries (ACE) are permitted, and because of this, the ACE order is important in the discretionary access control list (DACL).</span></span> <span data-ttu-id="0061c-108">如需詳細資訊，請參閱 [DACL 中的 Ace 順序](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)。</span><span class="sxs-lookup"><span data-stu-id="0061c-108">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

## <a name="syntax"></a><span data-ttu-id="0061c-109">語法</span><span class="sxs-lookup"><span data-stu-id="0061c-109">Syntax</span></span>


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a><span data-ttu-id="0061c-110">參數</span><span class="sxs-lookup"><span data-stu-id="0061c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0061c-111">*ul* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0061c-111">*ul* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0061c-112">使用者的陣列。</span><span class="sxs-lookup"><span data-stu-id="0061c-112">Array of users.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0061c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0061c-113">Return value</span></span>

<span data-ttu-id="0061c-114">這個方法會傳回 **HRESULT** ，指出方法呼叫的狀態。</span><span class="sxs-lookup"><span data-stu-id="0061c-114">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="0061c-115">下列清單列出對 **Get9XUserList** 而言很重要的傳回值。</span><span class="sxs-lookup"><span data-stu-id="0061c-115">The following list lists the return values that are of significance to **Get9XUserList**.</span></span> <span data-ttu-id="0061c-116">針對腳本和 Visual Basic 的應用程式，結果可以是 [OutParameters. ReturnValue](parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="0061c-116">For scripting and Visual Basic applications, the result can be [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="0061c-117">如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="0061c-117">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="0061c-118">**\_ \_ \_ 已停用 WBEM E 方法**</span><span class="sxs-lookup"><span data-stu-id="0061c-118">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="0061c-119">支援的 Windows 版本不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0061c-119">This method is not supported on supported versions of Windows.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0061c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0061c-120">Requirements</span></span>



| <span data-ttu-id="0061c-121">需求</span><span class="sxs-lookup"><span data-stu-id="0061c-121">Requirement</span></span> | <span data-ttu-id="0061c-122">值</span><span class="sxs-lookup"><span data-stu-id="0061c-122">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0061c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0061c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0061c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0061c-124">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0061c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0061c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0061c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0061c-126">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="0061c-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="0061c-127">Namespace</span></span><br/>                | <span data-ttu-id="0061c-128">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="0061c-128">all WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="0061c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0061c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0061c-130">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="0061c-130">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="0061c-131">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="0061c-131">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="0061c-132">**\_\_SystemSecurity::GetSD**</span><span class="sxs-lookup"><span data-stu-id="0061c-132">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="0061c-133">**\_\_SystemSecurity::SetSD**</span><span class="sxs-lookup"><span data-stu-id="0061c-133">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="0061c-134">**Win32 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="0061c-134">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="0061c-135">**Win32 \_ SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0061c-135">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="0061c-136">保護 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="0061c-136">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="0061c-137">WMI 安全性常數</span><span class="sxs-lookup"><span data-stu-id="0061c-137">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> </dl>

 

