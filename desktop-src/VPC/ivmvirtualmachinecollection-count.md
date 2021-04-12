---
title: 'IVMVirtualMachineCollection Count 屬性 (VPCCOMInterfaces .h) '
description: 捕獲此集合中的虛擬機器數目。
ms.assetid: c1f38528-fd9b-4b86-aac6-de944379b92e
keywords:
- Count 屬性 Virtual PC
- Count 屬性 Virtual PC，IVMVirtualMachineCollection 介面
- IVMVirtualMachineCollection 介面 Virtual PC、Count 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Count
- IVMVirtualMachineCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f641fad504c6dd593737cf35014813f49609a4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105648"
---
# <a name="ivmvirtualmachinecollectioncount-property"></a><span data-ttu-id="e4d6a-106">IVMVirtualMachineCollection：： Count 屬性</span><span class="sxs-lookup"><span data-stu-id="e4d6a-106">IVMVirtualMachineCollection::Count property</span></span>

<span data-ttu-id="e4d6a-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="e4d6a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e4d6a-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="e4d6a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e4d6a-109">捕獲此集合中的虛擬機器數目。</span><span class="sxs-lookup"><span data-stu-id="e4d6a-109">Retrieves the number of virtual machines in this collection.</span></span>

<span data-ttu-id="e4d6a-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e4d6a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4d6a-111">語法</span><span class="sxs-lookup"><span data-stu-id="e4d6a-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="e4d6a-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="e4d6a-112">Property value</span></span>

<span data-ttu-id="e4d6a-113">虛擬機器的數目。</span><span class="sxs-lookup"><span data-stu-id="e4d6a-113">The number of virtual machines.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e4d6a-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e4d6a-114">Error codes</span></span>



| <span data-ttu-id="e4d6a-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="e4d6a-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="e4d6a-116">意義</span><span class="sxs-lookup"><span data-stu-id="e4d6a-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e4d6a-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e4d6a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e4d6a-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="e4d6a-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="e4d6a-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e4d6a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="e4d6a-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e4d6a-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="e4d6a-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e4d6a-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e4d6a-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e4d6a-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e4d6a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4d6a-123">Requirements</span></span>



| <span data-ttu-id="e4d6a-124">需求</span><span class="sxs-lookup"><span data-stu-id="e4d6a-124">Requirement</span></span> | <span data-ttu-id="e4d6a-125">值</span><span class="sxs-lookup"><span data-stu-id="e4d6a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d6a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4d6a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e4d6a-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4d6a-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e4d6a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4d6a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e4d6a-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="e4d6a-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e4d6a-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e4d6a-130">End of client support</span></span><br/>    | <span data-ttu-id="e4d6a-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d6a-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="e4d6a-132">產品</span><span class="sxs-lookup"><span data-stu-id="e4d6a-132">Product</span></span><br/>                  | <span data-ttu-id="e4d6a-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e4d6a-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="e4d6a-134">標頭</span><span class="sxs-lookup"><span data-stu-id="e4d6a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4d6a-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="e4d6a-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="e4d6a-136">IID</span><span class="sxs-lookup"><span data-stu-id="e4d6a-136">IID</span></span><br/>                      | <span data-ttu-id="e4d6a-137">IID \_ IVMVirtualMachineCollection 定義為 59f31786-2a3d-4fbf-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="e4d6a-137">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e4d6a-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4d6a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4d6a-139">**IVMVirtualMachineCollection**</span><span class="sxs-lookup"><span data-stu-id="e4d6a-139">**IVMVirtualMachineCollection**</span></span>](ivmvirtualmachinecollection.md)
</dt> </dl>

 

