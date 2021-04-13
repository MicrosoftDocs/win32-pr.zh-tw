---
title: 'IVMVirtualMachineCollection _NewEnum 屬性 (VPCCOMInterfaces) '
description: '擷取集合的列舉值。 |IVMVirtualMachineCollection _NewEnum 屬性 (VPCCOMInterfaces) '
ms.assetid: 86b51542-139c-4e2b-baec-2c90956d99b3
keywords:
- _NewEnum 屬性 Virtual PC
- _NewEnum 屬性 Virtual PC，IVMVirtualMachineCollection 介面
- IVMVirtualMachineCollection 介面 Virtual PC，_NewEnum 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection._NewEnum
- IVMVirtualMachineCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea610b005ea9482d59de65311256f77446e442cd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322260"
---
# <a name="ivmvirtualmachinecollection_newenum-property"></a><span data-ttu-id="f85f3-107">IVMVirtualMachineCollection：： \_ NewEnum 屬性</span><span class="sxs-lookup"><span data-stu-id="f85f3-107">IVMVirtualMachineCollection::\_NewEnum property</span></span>

<span data-ttu-id="f85f3-108">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="f85f3-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f85f3-109">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="f85f3-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f85f3-110">擷取集合的列舉值。</span><span class="sxs-lookup"><span data-stu-id="f85f3-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="f85f3-111">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="f85f3-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f85f3-112">語法</span><span class="sxs-lookup"><span data-stu-id="f85f3-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="f85f3-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="f85f3-113">Property value</span></span>

<span data-ttu-id="f85f3-114">[IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)列舉值。</span><span class="sxs-lookup"><span data-stu-id="f85f3-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f85f3-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f85f3-115">Error codes</span></span>



| <span data-ttu-id="f85f3-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="f85f3-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f85f3-117">意義</span><span class="sxs-lookup"><span data-stu-id="f85f3-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="f85f3-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f85f3-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f85f3-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="f85f3-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="f85f3-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f85f3-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f85f3-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f85f3-121">The parameter is **NULL**.</span></span><br/>    |
| <dl> <span data-ttu-id="f85f3-122"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f85f3-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f85f3-123">發生意外錯誤。</span><span class="sxs-lookup"><span data-stu-id="f85f3-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f85f3-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f85f3-124">Requirements</span></span>



| <span data-ttu-id="f85f3-125">需求</span><span class="sxs-lookup"><span data-stu-id="f85f3-125">Requirement</span></span> | <span data-ttu-id="f85f3-126">值</span><span class="sxs-lookup"><span data-stu-id="f85f3-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f85f3-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f85f3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f85f3-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f85f3-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f85f3-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f85f3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f85f3-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="f85f3-130">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f85f3-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f85f3-131">End of client support</span></span><br/>    | <span data-ttu-id="f85f3-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f85f3-132">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="f85f3-133">產品</span><span class="sxs-lookup"><span data-stu-id="f85f3-133">Product</span></span><br/>                  | <span data-ttu-id="f85f3-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f85f3-134">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="f85f3-135">標頭</span><span class="sxs-lookup"><span data-stu-id="f85f3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f85f3-136"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="f85f3-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="f85f3-137">IID</span><span class="sxs-lookup"><span data-stu-id="f85f3-137">IID</span></span><br/>                      | <span data-ttu-id="f85f3-138">IID \_ IVMVirtualMachineCollection 定義為 59f31786-2a3d-4fbf-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="f85f3-138">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f85f3-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f85f3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f85f3-140">**IVMVirtualMachineCollection**</span><span class="sxs-lookup"><span data-stu-id="f85f3-140">**IVMVirtualMachineCollection**</span></span>](ivmvirtualmachinecollection.md)
</dt> </dl>

 

