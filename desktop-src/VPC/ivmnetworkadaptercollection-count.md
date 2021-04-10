---
title: 'IVMNetworkAdapterCollection Count 屬性 (VPCCOMInterfaces .h) '
description: 捕獲此集合中的網路介面數目。
ms.assetid: 0b6391fa-62fe-4db1-b0a2-565ab17157ab
keywords:
- Count 屬性 Virtual PC
- Count 屬性 Virtual PC，IVMNetworkAdapterCollection 介面
- IVMNetworkAdapterCollection 介面 Virtual PC、Count 屬性
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Count
- IVMNetworkAdapterCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a287122d9829cd98f355d44e6bd408f6ca0d67a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093755"
---
# <a name="ivmnetworkadaptercollectioncount-property"></a><span data-ttu-id="27a7f-106">IVMNetworkAdapterCollection：： Count 屬性</span><span class="sxs-lookup"><span data-stu-id="27a7f-106">IVMNetworkAdapterCollection::Count property</span></span>

<span data-ttu-id="27a7f-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="27a7f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="27a7f-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="27a7f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="27a7f-109">捕獲此集合中的網路介面數目。</span><span class="sxs-lookup"><span data-stu-id="27a7f-109">Retrieves the number of network interfaces in this collection.</span></span>

<span data-ttu-id="27a7f-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="27a7f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="27a7f-111">語法</span><span class="sxs-lookup"><span data-stu-id="27a7f-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="27a7f-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="27a7f-112">Property value</span></span>

<span data-ttu-id="27a7f-113">網路介面的數目。</span><span class="sxs-lookup"><span data-stu-id="27a7f-113">The number of network interfaces.</span></span>

## <a name="error-codes"></a><span data-ttu-id="27a7f-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="27a7f-114">Error codes</span></span>



| <span data-ttu-id="27a7f-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="27a7f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="27a7f-116">意義</span><span class="sxs-lookup"><span data-stu-id="27a7f-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="27a7f-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="27a7f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="27a7f-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="27a7f-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="27a7f-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="27a7f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="27a7f-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="27a7f-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="27a7f-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="27a7f-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="27a7f-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="27a7f-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="27a7f-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="27a7f-123">Requirements</span></span>



| <span data-ttu-id="27a7f-124">需求</span><span class="sxs-lookup"><span data-stu-id="27a7f-124">Requirement</span></span> | <span data-ttu-id="27a7f-125">值</span><span class="sxs-lookup"><span data-stu-id="27a7f-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27a7f-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27a7f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="27a7f-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27a7f-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="27a7f-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27a7f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="27a7f-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="27a7f-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="27a7f-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="27a7f-130">End of client support</span></span><br/>    | <span data-ttu-id="27a7f-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="27a7f-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="27a7f-132">產品</span><span class="sxs-lookup"><span data-stu-id="27a7f-132">Product</span></span><br/>                  | <span data-ttu-id="27a7f-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="27a7f-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="27a7f-134">標頭</span><span class="sxs-lookup"><span data-stu-id="27a7f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="27a7f-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="27a7f-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="27a7f-136">IID</span><span class="sxs-lookup"><span data-stu-id="27a7f-136">IID</span></span><br/>                      | <span data-ttu-id="27a7f-137">IID \_ IVMNetworkAdapterCollection 定義為 ebaeafe9-ebcd-47cf-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="27a7f-137">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27a7f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27a7f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27a7f-139">**IVMNetworkAdapterCollection**</span><span class="sxs-lookup"><span data-stu-id="27a7f-139">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

