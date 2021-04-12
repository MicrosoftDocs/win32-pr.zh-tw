---
title: 'IVMVirtualMachine NetworkAdapters 屬性 (VPCCOMInterfaces .h) '
description: 抓取連接至虛擬機器之 Nic 的可列舉集合。
ms.assetid: 3877edf7-92b8-43c9-8229-a198a07079a4
keywords:
- NetworkAdapters 屬性 Virtual PC
- NetworkAdapters 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，NetworkAdapters 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.NetworkAdapters
- IVMVirtualMachine.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ce6e1fa22eca40c037eebb48803fe182810c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384797"
---
# <a name="ivmvirtualmachinenetworkadapters-property"></a><span data-ttu-id="7049d-106">IVMVirtualMachine：： NetworkAdapters 屬性</span><span class="sxs-lookup"><span data-stu-id="7049d-106">IVMVirtualMachine::NetworkAdapters property</span></span>

<span data-ttu-id="7049d-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="7049d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7049d-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="7049d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7049d-109">抓取連接至虛擬機器之 Nic 的可列舉集合。</span><span class="sxs-lookup"><span data-stu-id="7049d-109">Retrieves an enumerable collection of NICs attached to the virtual machine.</span></span>

<span data-ttu-id="7049d-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="7049d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7049d-111">語法</span><span class="sxs-lookup"><span data-stu-id="7049d-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **networkAdapterCollection
);
```



## <a name="property-value"></a><span data-ttu-id="7049d-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="7049d-112">Property value</span></span>

<span data-ttu-id="7049d-113">[**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)物件。</span><span class="sxs-lookup"><span data-stu-id="7049d-113">An [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7049d-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="7049d-114">Error codes</span></span>



| <span data-ttu-id="7049d-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="7049d-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7049d-116">意義</span><span class="sxs-lookup"><span data-stu-id="7049d-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7049d-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7049d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7049d-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="7049d-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="7049d-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7049d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7049d-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7049d-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="7049d-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="7049d-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="7049d-122">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="7049d-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="7049d-123"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7049d-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7049d-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7049d-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7049d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="7049d-125">Requirements</span></span>



| <span data-ttu-id="7049d-126">需求</span><span class="sxs-lookup"><span data-stu-id="7049d-126">Requirement</span></span> | <span data-ttu-id="7049d-127">值</span><span class="sxs-lookup"><span data-stu-id="7049d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7049d-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7049d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7049d-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7049d-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7049d-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7049d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7049d-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="7049d-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7049d-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7049d-132">End of client support</span></span><br/>    | <span data-ttu-id="7049d-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7049d-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7049d-134">產品</span><span class="sxs-lookup"><span data-stu-id="7049d-134">Product</span></span><br/>                  | <span data-ttu-id="7049d-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7049d-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7049d-136">標頭</span><span class="sxs-lookup"><span data-stu-id="7049d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7049d-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="7049d-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7049d-138">IID</span><span class="sxs-lookup"><span data-stu-id="7049d-138">IID</span></span><br/>                      | <span data-ttu-id="7049d-139">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="7049d-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="7049d-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7049d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7049d-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="7049d-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

