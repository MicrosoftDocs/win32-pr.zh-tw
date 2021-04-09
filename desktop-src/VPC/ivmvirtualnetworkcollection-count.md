---
title: 'IVMVirtualNetworkCollection Count 屬性 (VPCCOMInterfaces .h) '
description: 捕獲此集合中的虛擬網路數目。
ms.assetid: a9a3ab48-74a0-498e-936e-a99c7b027a85
keywords:
- Count 屬性 Virtual PC
- Count 屬性 Virtual PC，IVMVirtualNetworkCollection 介面
- IVMVirtualNetworkCollection 介面 Virtual PC、Count 屬性
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Count
- IVMVirtualNetworkCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82e3244327d5840c8f7cce8ed498f90cd406d573
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686216"
---
# <a name="ivmvirtualnetworkcollectioncount-property"></a><span data-ttu-id="49ba7-106">IVMVirtualNetworkCollection：： Count 屬性</span><span class="sxs-lookup"><span data-stu-id="49ba7-106">IVMVirtualNetworkCollection::Count property</span></span>

<span data-ttu-id="49ba7-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="49ba7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="49ba7-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="49ba7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="49ba7-109">捕獲此集合中的虛擬網路數目。</span><span class="sxs-lookup"><span data-stu-id="49ba7-109">Retrieves the number of virtual networks in this collection.</span></span>

<span data-ttu-id="49ba7-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="49ba7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="49ba7-111">語法</span><span class="sxs-lookup"><span data-stu-id="49ba7-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="49ba7-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="49ba7-112">Property value</span></span>

<span data-ttu-id="49ba7-113">虛擬網路的數目。</span><span class="sxs-lookup"><span data-stu-id="49ba7-113">The number of virtual networks.</span></span>

## <a name="error-codes"></a><span data-ttu-id="49ba7-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="49ba7-114">Error codes</span></span>



| <span data-ttu-id="49ba7-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="49ba7-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="49ba7-116">意義</span><span class="sxs-lookup"><span data-stu-id="49ba7-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="49ba7-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="49ba7-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="49ba7-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="49ba7-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="49ba7-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="49ba7-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="49ba7-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="49ba7-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="49ba7-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="49ba7-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="49ba7-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="49ba7-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="49ba7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="49ba7-123">Requirements</span></span>



| <span data-ttu-id="49ba7-124">需求</span><span class="sxs-lookup"><span data-stu-id="49ba7-124">Requirement</span></span> | <span data-ttu-id="49ba7-125">值</span><span class="sxs-lookup"><span data-stu-id="49ba7-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49ba7-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49ba7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="49ba7-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49ba7-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="49ba7-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49ba7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="49ba7-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="49ba7-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="49ba7-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="49ba7-130">End of client support</span></span><br/>    | <span data-ttu-id="49ba7-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="49ba7-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="49ba7-132">產品</span><span class="sxs-lookup"><span data-stu-id="49ba7-132">Product</span></span><br/>                  | <span data-ttu-id="49ba7-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="49ba7-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="49ba7-134">標頭</span><span class="sxs-lookup"><span data-stu-id="49ba7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="49ba7-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="49ba7-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="49ba7-136">IID</span><span class="sxs-lookup"><span data-stu-id="49ba7-136">IID</span></span><br/>                      | <span data-ttu-id="49ba7-137">IID \_ IVMVirtualNetworkCollection 定義為8ed680be-4242-4b2a-a21c-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="49ba7-137">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49ba7-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49ba7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ba7-139">**IVMVirtualNetworkCollection**</span><span class="sxs-lookup"><span data-stu-id="49ba7-139">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

