---
title: 'IVMNetworkAdapterCollection 專案屬性 (VPCCOMInterfaces .h) '
description: 對應至指定之索引的 IVMNetworkAdapter 物件。
ms.assetid: 3de76e24-3315-473f-870b-074be8bcfe70
keywords:
- 專案屬性 Virtual PC
- 專案屬性 Virtual PC，IVMNetworkAdapterCollection 介面
- IVMNetworkAdapterCollection 介面 Virtual PC，Item 屬性
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Item
- IVMNetworkAdapterCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63d2f7ee389938a44c6608241fb3fb2d48ec1bca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935025"
---
# <a name="ivmnetworkadaptercollectionitem-property"></a><span data-ttu-id="787ce-106">IVMNetworkAdapterCollection：： Item 屬性</span><span class="sxs-lookup"><span data-stu-id="787ce-106">IVMNetworkAdapterCollection::Item property</span></span>

<span data-ttu-id="787ce-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="787ce-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="787ce-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="787ce-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="787ce-109">抓取對應至指定之索引的 [**IVMNetworkAdapter**](ivmnetworkadapter.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="787ce-109">Retrieves the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that corresponds to the specified index.</span></span>

<span data-ttu-id="787ce-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="787ce-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="787ce-111">語法</span><span class="sxs-lookup"><span data-stu-id="787ce-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMNetworkAdapter **networkInterface
);
```



## <a name="property-value"></a><span data-ttu-id="787ce-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="787ce-112">Property value</span></span>

<span data-ttu-id="787ce-113">[**IVMNetworkAdapter**](ivmnetworkadapter.md)物件。</span><span class="sxs-lookup"><span data-stu-id="787ce-113">The [**IVMNetworkAdapter**](ivmnetworkadapter.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="787ce-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="787ce-114">Error codes</span></span>



| <span data-ttu-id="787ce-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="787ce-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="787ce-116">意義</span><span class="sxs-lookup"><span data-stu-id="787ce-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="787ce-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="787ce-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="787ce-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="787ce-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="787ce-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="787ce-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="787ce-120">*NetworkInterface* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="787ce-120">The *networkInterface* parameter is **NULL**.</span></span> <br/>                                      |
| <dl> <span data-ttu-id="787ce-121"><dt>會 \_E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="787ce-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="787ce-122">要求專案的索引未對應到此集合中的專案。</span><span class="sxs-lookup"><span data-stu-id="787ce-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="787ce-123"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="787ce-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="787ce-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="787ce-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="787ce-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="787ce-125">Requirements</span></span>



| <span data-ttu-id="787ce-126">需求</span><span class="sxs-lookup"><span data-stu-id="787ce-126">Requirement</span></span> | <span data-ttu-id="787ce-127">值</span><span class="sxs-lookup"><span data-stu-id="787ce-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="787ce-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="787ce-128">Minimum supported client</span></span><br/> | <span data-ttu-id="787ce-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="787ce-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="787ce-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="787ce-130">Minimum supported server</span></span><br/> | <span data-ttu-id="787ce-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="787ce-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="787ce-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="787ce-132">End of client support</span></span><br/>    | <span data-ttu-id="787ce-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="787ce-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="787ce-134">產品</span><span class="sxs-lookup"><span data-stu-id="787ce-134">Product</span></span><br/>                  | <span data-ttu-id="787ce-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="787ce-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="787ce-136">標頭</span><span class="sxs-lookup"><span data-stu-id="787ce-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="787ce-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="787ce-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="787ce-138">IID</span><span class="sxs-lookup"><span data-stu-id="787ce-138">IID</span></span><br/>                      | <span data-ttu-id="787ce-139">IID \_ IVMNetworkAdapterCollection 定義為 ebaeafe9-ebcd-47cf-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="787ce-139">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="787ce-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="787ce-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="787ce-141">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="787ce-141">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> <dt>

[<span data-ttu-id="787ce-142">**IVMNetworkAdapterCollection**</span><span class="sxs-lookup"><span data-stu-id="787ce-142">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

