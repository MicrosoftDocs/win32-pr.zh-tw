---
title: 'IVMVirtualNetwork Name 屬性 (VPCCOMInterfaces .h) '
description: 虛擬網路實例的唯一名稱。
ms.assetid: dd4807dc-abae-4bdb-ba27-597cf1337834
keywords:
- Name 屬性 Virtual PC
- Name 屬性 Virtual PC，IVMVirtualNetwork 介面
- IVMVirtualNetwork 介面 Virtual PC，Name 屬性
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.Name
- IVMVirtualNetwork.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c962d7b65bfddaf5293bd391ae84f04bae512ba9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934927"
---
# <a name="ivmvirtualnetworkname-property"></a><span data-ttu-id="88201-106">IVMVirtualNetwork：： Name 屬性</span><span class="sxs-lookup"><span data-stu-id="88201-106">IVMVirtualNetwork::Name property</span></span>

<span data-ttu-id="88201-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="88201-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="88201-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="88201-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="88201-109">抓取虛擬網路實例的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="88201-109">Retrieves the unique name of the virtual network instance.</span></span>

<span data-ttu-id="88201-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="88201-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="88201-111">語法</span><span class="sxs-lookup"><span data-stu-id="88201-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *virtualNetworkName
);
```



## <a name="property-value"></a><span data-ttu-id="88201-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="88201-112">Property value</span></span>

<span data-ttu-id="88201-113">虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="88201-113">The name of the virtual network.</span></span>

## <a name="error-codes"></a><span data-ttu-id="88201-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="88201-114">Error codes</span></span>



| <span data-ttu-id="88201-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="88201-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="88201-116">意義</span><span class="sxs-lookup"><span data-stu-id="88201-116">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="88201-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="88201-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="88201-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="88201-118">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="88201-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="88201-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="88201-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="88201-120">The parameter is **NULL**.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="88201-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="88201-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="88201-122">發生未預期的錯誤，或虛擬網路實例未知。</span><span class="sxs-lookup"><span data-stu-id="88201-122">An unexpected error has occurred or the virtual network instance is unknown.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="88201-123">備註</span><span class="sxs-lookup"><span data-stu-id="88201-123">Remarks</span></span>

<span data-ttu-id="88201-124">虛擬網路名稱不區分大小寫，例如 "MyNetwork" 和 "MyNetwork" 指的是相同的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="88201-124">Virtual network names are case-insensitive, for example, "MyNetwork" and "mynetwork" refer to the same virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="88201-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="88201-125">Requirements</span></span>



| <span data-ttu-id="88201-126">需求</span><span class="sxs-lookup"><span data-stu-id="88201-126">Requirement</span></span> | <span data-ttu-id="88201-127">值</span><span class="sxs-lookup"><span data-stu-id="88201-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="88201-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88201-128">Minimum supported client</span></span><br/> | <span data-ttu-id="88201-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88201-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="88201-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88201-130">Minimum supported server</span></span><br/> | <span data-ttu-id="88201-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="88201-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="88201-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="88201-132">End of client support</span></span><br/>    | <span data-ttu-id="88201-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="88201-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="88201-134">產品</span><span class="sxs-lookup"><span data-stu-id="88201-134">Product</span></span><br/>                  | <span data-ttu-id="88201-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="88201-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="88201-136">標頭</span><span class="sxs-lookup"><span data-stu-id="88201-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="88201-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="88201-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="88201-138">IID</span><span class="sxs-lookup"><span data-stu-id="88201-138">IID</span></span><br/>                      | <span data-ttu-id="88201-139">IID \_ IVMVirtualNetwork 定義為431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="88201-139">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="88201-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88201-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88201-141">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="88201-141">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

