---
title: 'IVMVirtualNetworkCollection 專案屬性 (VPCCOMInterfaces .h) '
description: 對應至指定之索引的 IVMVirtualNetwork 物件。
ms.assetid: 1c6a3449-f76a-4216-8840-0fb9fb133e67
keywords:
- 專案屬性 Virtual PC
- 專案屬性 Virtual PC，IVMVirtualNetworkCollection 介面
- IVMVirtualNetworkCollection 介面 Virtual PC，Item 屬性
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Item
- IVMVirtualNetworkCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac5a7648db4708fbc1b445029419ee794809abcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025188"
---
# <a name="ivmvirtualnetworkcollectionitem-property"></a><span data-ttu-id="6b204-106">IVMVirtualNetworkCollection：： Item 屬性</span><span class="sxs-lookup"><span data-stu-id="6b204-106">IVMVirtualNetworkCollection::Item property</span></span>

<span data-ttu-id="6b204-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="6b204-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6b204-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="6b204-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6b204-109">抓取對應至指定之索引的 [**IVMVirtualNetwork**](ivmvirtualnetwork.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="6b204-109">Retrieves the [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that corresponds to the specified index.</span></span>

<span data-ttu-id="6b204-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6b204-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b204-111">語法</span><span class="sxs-lookup"><span data-stu-id="6b204-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a><span data-ttu-id="6b204-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="6b204-112">Property value</span></span>

<span data-ttu-id="6b204-113">[**IVMVirtualNetwork**](ivmvirtualnetwork.md)物件。</span><span class="sxs-lookup"><span data-stu-id="6b204-113">The [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6b204-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="6b204-114">Error codes</span></span>



| <span data-ttu-id="6b204-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="6b204-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6b204-116">意義</span><span class="sxs-lookup"><span data-stu-id="6b204-116">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b204-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6b204-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6b204-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="6b204-118">The operation was successful.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="6b204-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6b204-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6b204-120">*VirtualNetwork* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6b204-120">The *virtualNetwork* parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="6b204-121"><dt>會 \_E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="6b204-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="6b204-122">要求專案的索引未對應到此集合中的專案。</span><span class="sxs-lookup"><span data-stu-id="6b204-122">The index of the requested item does not correspond to an item in this collection.</span></span><br/> |
| <dl> <span data-ttu-id="6b204-123"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6b204-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6b204-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6b204-124">An unexpected error has occurred.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="6b204-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b204-125">Requirements</span></span>



| <span data-ttu-id="6b204-126">需求</span><span class="sxs-lookup"><span data-stu-id="6b204-126">Requirement</span></span> | <span data-ttu-id="6b204-127">值</span><span class="sxs-lookup"><span data-stu-id="6b204-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b204-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b204-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6b204-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b204-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6b204-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b204-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6b204-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="6b204-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6b204-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6b204-132">End of client support</span></span><br/>    | <span data-ttu-id="6b204-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6b204-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="6b204-134">產品</span><span class="sxs-lookup"><span data-stu-id="6b204-134">Product</span></span><br/>                  | <span data-ttu-id="6b204-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6b204-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="6b204-136">標頭</span><span class="sxs-lookup"><span data-stu-id="6b204-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b204-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="6b204-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="6b204-138">IID</span><span class="sxs-lookup"><span data-stu-id="6b204-138">IID</span></span><br/>                      | <span data-ttu-id="6b204-139">IID \_ IVMVirtualNetworkCollection 定義為8ed680be-4242-4b2a-a21c-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="6b204-139">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6b204-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b204-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b204-141">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="6b204-141">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> <dt>

[<span data-ttu-id="6b204-142">**IVMVirtualNetworkCollection**</span><span class="sxs-lookup"><span data-stu-id="6b204-142">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

