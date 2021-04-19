---
description: 針對執行過時 Windows 的電腦上的個別使用者清單設定遠端存取許可權，無法使用透過 Windows 安全描述項的存取控制。
ms.assetid: f6da65d3-86dd-4fc8-b4c0-f7ddc8536d4e
ms.tgt_platform: multiple
title: __SystemSecurity：： Set9XUserList 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Set9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: dd377da3adf55aef6a78576e1c978196f349f619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990408"
---
# <a name="__systemsecurityset9xuserlist-method"></a><span data-ttu-id="31e64-103">\_\_SystemSecurity：： Set9XUserList 方法</span><span class="sxs-lookup"><span data-stu-id="31e64-103">\_\_SystemSecurity::Set9XUserList method</span></span>

<span data-ttu-id="31e64-104">**\_ \_ SystemSecurity：： Set9XUserList** 方法會針對執行過時 windows 的電腦上的個別使用者清單設定遠端存取許可權，而無法使用透過 windows 安全描述項的存取控制。</span><span class="sxs-lookup"><span data-stu-id="31e64-104">The **\_\_SystemSecurity::Set9XUserList** method sets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

<span data-ttu-id="31e64-105">此清單會指定為内嵌物件的陣列，其中每個物件都是 [**\_ \_ NTLMUser9X**](--ntlmuser9x.md)類別的實例。</span><span class="sxs-lookup"><span data-stu-id="31e64-105">The list is specified as an array of embedded objects where each object is an instance of the [**\_\_NTLMUser9X**](--ntlmuser9x.md) class.</span></span> <span data-ttu-id="31e64-106">這項功能類似于安全描述項，但更受限制。</span><span class="sxs-lookup"><span data-stu-id="31e64-106">This functions similar to the security descriptor, but it is more limited.</span></span> <span data-ttu-id="31e64-107">群組不受支援，而且無法控制本機存取，因為本機使用者一律具有完整存取權。</span><span class="sxs-lookup"><span data-stu-id="31e64-107">Groups are not supported and there is no control over local access, because the local user always has full access.</span></span> <span data-ttu-id="31e64-108">拒絕和允許存取控制專案 (ACE) ，因此 ACE 順序在 (DACL) 的任意存取控制清單中很重要。</span><span class="sxs-lookup"><span data-stu-id="31e64-108">Both deny and allow access control entries (ACE) are permitted, and because of this, the ACE order is important in the discretionary access control list (DACL).</span></span> <span data-ttu-id="31e64-109">如需詳細資訊，請參閱 [DACL 中的 Ace 順序](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)。</span><span class="sxs-lookup"><span data-stu-id="31e64-109">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

## <a name="syntax"></a><span data-ttu-id="31e64-110">語法</span><span class="sxs-lookup"><span data-stu-id="31e64-110">Syntax</span></span>


```C++
HRESULT Set9XUserList(
  [in] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a><span data-ttu-id="31e64-111">參數</span><span class="sxs-lookup"><span data-stu-id="31e64-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31e64-112">*ul* \[在\]</span><span class="sxs-lookup"><span data-stu-id="31e64-112">*ul* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31e64-113">使用者的陣列。</span><span class="sxs-lookup"><span data-stu-id="31e64-113">Array of users.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31e64-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="31e64-114">Return value</span></span>

<span data-ttu-id="31e64-115">這個方法會傳回 **HRESULT** ，指出方法呼叫的狀態。</span><span class="sxs-lookup"><span data-stu-id="31e64-115">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="31e64-116">下列清單列出對 **Set9XUserList** 而言很重要的傳回值。</span><span class="sxs-lookup"><span data-stu-id="31e64-116">The following list lists the return values that are of significance to **Set9XUserList**.</span></span> <span data-ttu-id="31e64-117">針對編寫腳本和 Visual Basic 應用程式，可以從 OutParameters 取得結果 [ReturnValue](parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="31e64-117">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="31e64-118">如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="31e64-118">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="31e64-119">**\_ \_ \_ 已停用 WBEM E 方法**</span><span class="sxs-lookup"><span data-stu-id="31e64-119">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="31e64-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="31e64-120">This method is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31e64-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="31e64-121">Requirements</span></span>



| <span data-ttu-id="31e64-122">需求</span><span class="sxs-lookup"><span data-stu-id="31e64-122">Requirement</span></span> | <span data-ttu-id="31e64-123">值</span><span class="sxs-lookup"><span data-stu-id="31e64-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="31e64-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31e64-124">Minimum supported client</span></span><br/> | <span data-ttu-id="31e64-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31e64-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="31e64-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31e64-126">Minimum supported server</span></span><br/> | <span data-ttu-id="31e64-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31e64-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="31e64-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="31e64-128">Namespace</span></span><br/>                | <span data-ttu-id="31e64-129">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="31e64-129">all WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="31e64-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31e64-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e64-131">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="31e64-131">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="31e64-132">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="31e64-132">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="31e64-133">**\_\_SystemSecurity::GetSD**</span><span class="sxs-lookup"><span data-stu-id="31e64-133">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="31e64-134">**\_\_SystemSecurity::SetSD**</span><span class="sxs-lookup"><span data-stu-id="31e64-134">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="31e64-135">**Win32 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="31e64-135">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="31e64-136">**Win32 \_ SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="31e64-136">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="31e64-137">保護 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="31e64-137">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="31e64-138">WMI 安全性常數</span><span class="sxs-lookup"><span data-stu-id="31e64-138">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> </dl>

 

