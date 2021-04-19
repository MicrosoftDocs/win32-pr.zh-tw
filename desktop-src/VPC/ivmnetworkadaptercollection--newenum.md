---
title: 'IVMNetworkAdapterCollection _NewEnum 屬性 (VPCCOMInterfaces) '
description: '擷取集合的列舉值。 |IVMNetworkAdapterCollection _NewEnum 屬性 (VPCCOMInterfaces) '
ms.assetid: 9b970fc6-f8a3-4a16-9d59-789a59a99b68
keywords:
- _NewEnum 屬性 Virtual PC
- _NewEnum 屬性 Virtual PC，IVMNetworkAdapterCollection 介面
- IVMNetworkAdapterCollection 介面 Virtual PC，_NewEnum 屬性
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection._NewEnum
- IVMNetworkAdapterCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caf118700a81865ff93ee581cbb2efd07d237805
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106998977"
---
# <a name="ivmnetworkadaptercollection_newenum-property"></a><span data-ttu-id="4f151-107">IVMNetworkAdapterCollection：： \_ NewEnum 屬性</span><span class="sxs-lookup"><span data-stu-id="4f151-107">IVMNetworkAdapterCollection::\_NewEnum property</span></span>

<span data-ttu-id="4f151-108">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="4f151-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4f151-109">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="4f151-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4f151-110">擷取集合的列舉值。</span><span class="sxs-lookup"><span data-stu-id="4f151-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="4f151-111">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="4f151-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f151-112">語法</span><span class="sxs-lookup"><span data-stu-id="4f151-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="4f151-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="4f151-113">Property value</span></span>

<span data-ttu-id="4f151-114">[IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)列舉值。</span><span class="sxs-lookup"><span data-stu-id="4f151-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4f151-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="4f151-115">Error codes</span></span>



| <span data-ttu-id="4f151-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="4f151-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4f151-117">意義</span><span class="sxs-lookup"><span data-stu-id="4f151-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="4f151-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4f151-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4f151-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="4f151-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="4f151-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4f151-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4f151-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4f151-121">The parameter is **NULL**.</span></span><br/>    |
| <dl> <span data-ttu-id="4f151-122"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4f151-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4f151-123">發生意外錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f151-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4f151-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f151-124">Requirements</span></span>



| <span data-ttu-id="4f151-125">需求</span><span class="sxs-lookup"><span data-stu-id="4f151-125">Requirement</span></span> | <span data-ttu-id="4f151-126">值</span><span class="sxs-lookup"><span data-stu-id="4f151-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f151-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f151-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4f151-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f151-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4f151-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f151-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4f151-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="4f151-130">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4f151-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4f151-131">End of client support</span></span><br/>    | <span data-ttu-id="4f151-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4f151-132">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="4f151-133">產品</span><span class="sxs-lookup"><span data-stu-id="4f151-133">Product</span></span><br/>                  | <span data-ttu-id="4f151-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4f151-134">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="4f151-135">標頭</span><span class="sxs-lookup"><span data-stu-id="4f151-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f151-136"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="4f151-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="4f151-137">IID</span><span class="sxs-lookup"><span data-stu-id="4f151-137">IID</span></span><br/>                      | <span data-ttu-id="4f151-138">IID \_ IVMNetworkAdapterCollection 定義為 ebaeafe9-ebcd-47cf-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="4f151-138">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f151-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f151-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f151-140">**IVMNetworkAdapterCollection**</span><span class="sxs-lookup"><span data-stu-id="4f151-140">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

