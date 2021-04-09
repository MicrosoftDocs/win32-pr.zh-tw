---
title: 'IVMNetworkAdapter VirtualNetwork 屬性 (VPCCOMInterfaces .h) '
description: 抓取網路介面所連接的虛擬網路。
ms.assetid: 7f52fd86-5f83-41d8-ba48-7db65e9c357c
keywords:
- VirtualNetwork 屬性 Virtual PC
- VirtualNetwork 屬性 Virtual PC，IVMNetworkAdapter 介面
- IVMNetworkAdapter 介面 Virtual PC，VirtualNetwork 屬性
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualNetwork
- IVMNetworkAdapter.get_VirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b932ef553d3952fbc69edba3416ac20049984810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024534"
---
# <a name="ivmnetworkadaptervirtualnetwork-property"></a><span data-ttu-id="0dd76-106">IVMNetworkAdapter：： VirtualNetwork 屬性</span><span class="sxs-lookup"><span data-stu-id="0dd76-106">IVMNetworkAdapter::VirtualNetwork property</span></span>

<span data-ttu-id="0dd76-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="0dd76-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0dd76-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="0dd76-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0dd76-109">抓取網路介面所連接的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="0dd76-109">Retrieves the virtual network to which the network interface is attached.</span></span>

<span data-ttu-id="0dd76-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="0dd76-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dd76-111">語法</span><span class="sxs-lookup"><span data-stu-id="0dd76-111">Syntax</span></span>


```C++
HRESULT get_VirtualNetwork(
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a><span data-ttu-id="0dd76-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="0dd76-112">Property value</span></span>

<span data-ttu-id="0dd76-113">代表此虛擬網路介面所連接之虛擬網路的 [**IVMVirtualNetwork**](ivmvirtualnetwork.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="0dd76-113">An [**IVMVirtualNetwork**](ivmvirtualnetwork.md) interface that represents the virtual network to which this virtual network interface is attached.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0dd76-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0dd76-114">Error codes</span></span>



| <span data-ttu-id="0dd76-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="0dd76-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="0dd76-116">意義</span><span class="sxs-lookup"><span data-stu-id="0dd76-116">Meaning</span></span>                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0dd76-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0dd76-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="0dd76-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="0dd76-118">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="0dd76-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0dd76-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="0dd76-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0dd76-120">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="0dd76-121"><dt>S \_FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0dd76-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="0dd76-122">此網路介面已被插即用，且未連線至虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="0dd76-122">This network interface is unplugged and is not connected to a virtual network.</span></span><br/> |
| <dl> <span data-ttu-id="0dd76-123"><dt>VM \_電子 \_ 不正確 \_ 虛擬 \_ 網路 \_ 識別碼</dt> <dt>0xA00400702</dt></span><span class="sxs-lookup"><span data-stu-id="0dd76-123"><dt>VM\_E\_INVALID\_VIRTUAL\_NETWORK\_ID</dt> <dt>0xA00400702</dt></span></span> </dl> | <span data-ttu-id="0dd76-124">此介面已連線到具有無效識別碼的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="0dd76-124">This interface is connected to a virtual network with an invalid ID.</span></span><br/>           |
| <dl> <span data-ttu-id="0dd76-125"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0dd76-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="0dd76-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0dd76-126">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="0dd76-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="0dd76-127">Requirements</span></span>



| <span data-ttu-id="0dd76-128">需求</span><span class="sxs-lookup"><span data-stu-id="0dd76-128">Requirement</span></span> | <span data-ttu-id="0dd76-129">值</span><span class="sxs-lookup"><span data-stu-id="0dd76-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dd76-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0dd76-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0dd76-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0dd76-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0dd76-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0dd76-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0dd76-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="0dd76-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0dd76-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0dd76-134">End of client support</span></span><br/>    | <span data-ttu-id="0dd76-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0dd76-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0dd76-136">產品</span><span class="sxs-lookup"><span data-stu-id="0dd76-136">Product</span></span><br/>                  | <span data-ttu-id="0dd76-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0dd76-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0dd76-138">標頭</span><span class="sxs-lookup"><span data-stu-id="0dd76-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dd76-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="0dd76-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0dd76-140">IID</span><span class="sxs-lookup"><span data-stu-id="0dd76-140">IID</span></span><br/>                      | <span data-ttu-id="0dd76-141">IID \_ IVMNetworkAdapter 定義為 e32e4165-22b8-4dc0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="0dd76-141">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="0dd76-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0dd76-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dd76-143">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="0dd76-143">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

