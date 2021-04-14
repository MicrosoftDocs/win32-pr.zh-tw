---
title: 'IVMNetworkAdapter DetachFromVirtualNetwork 方法 (VPCCOMInterfaces .h) '
description: 從虛擬網路卸離網路介面。
ms.assetid: f1a00ea2-2b79-4b5c-a4bd-3cab66deb0d0
keywords:
- DetachFromVirtualNetwork 方法 Virtual PC
- DetachFromVirtualNetwork 方法 Virtual PC，IVMNetworkAdapter 介面
- IVMNetworkAdapter 介面 Virtual PC，DetachFromVirtualNetwork 方法
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.DetachFromVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d5046844764fe9e9eb6552fe1a04b6140201b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384805"
---
# <a name="ivmnetworkadapterdetachfromvirtualnetwork-method"></a><span data-ttu-id="cef4d-106">IVMNetworkAdapter：:D etachFromVirtualNetwork 方法</span><span class="sxs-lookup"><span data-stu-id="cef4d-106">IVMNetworkAdapter::DetachFromVirtualNetwork method</span></span>

<span data-ttu-id="cef4d-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="cef4d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cef4d-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="cef4d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cef4d-109">從虛擬網路卸離網路介面。</span><span class="sxs-lookup"><span data-stu-id="cef4d-109">Detaches the network interface from its virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="cef4d-110">語法</span><span class="sxs-lookup"><span data-stu-id="cef4d-110">Syntax</span></span>


```C++
HRESULT DetachFromVirtualNetwork();
```



## <a name="parameters"></a><span data-ttu-id="cef4d-111">參數</span><span class="sxs-lookup"><span data-stu-id="cef4d-111">Parameters</span></span>

<span data-ttu-id="cef4d-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="cef4d-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cef4d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="cef4d-113">Return value</span></span>

<span data-ttu-id="cef4d-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cef4d-114">This method can return one of these values.</span></span>



| <span data-ttu-id="cef4d-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="cef4d-115">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="cef4d-116">Description</span><span class="sxs-lookup"><span data-stu-id="cef4d-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="cef4d-117"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cef4d-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="cef4d-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="cef4d-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="cef4d-119"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cef4d-119"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="cef4d-120">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cef4d-120">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cef4d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="cef4d-121">Requirements</span></span>



| <span data-ttu-id="cef4d-122">需求</span><span class="sxs-lookup"><span data-stu-id="cef4d-122">Requirement</span></span> | <span data-ttu-id="cef4d-123">值</span><span class="sxs-lookup"><span data-stu-id="cef4d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cef4d-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cef4d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cef4d-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cef4d-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cef4d-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cef4d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cef4d-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="cef4d-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cef4d-128">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="cef4d-128">End of client support</span></span><br/>    | <span data-ttu-id="cef4d-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cef4d-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cef4d-130">產品</span><span class="sxs-lookup"><span data-stu-id="cef4d-130">Product</span></span><br/>                  | <span data-ttu-id="cef4d-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cef4d-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cef4d-132">標頭</span><span class="sxs-lookup"><span data-stu-id="cef4d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cef4d-133"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="cef4d-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cef4d-134">IID</span><span class="sxs-lookup"><span data-stu-id="cef4d-134">IID</span></span><br/>                      | <span data-ttu-id="cef4d-135">IID \_ IVMNetworkAdapter 定義為 e32e4165-22b8-4dc0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="cef4d-135">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="cef4d-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cef4d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cef4d-137">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="cef4d-137">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

