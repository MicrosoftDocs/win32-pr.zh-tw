---
title: 'IVMVirtualMachine DiscardUndoDisks 方法 (VPCCOMInterfaces .h) '
description: 捨棄虛擬復原磁片。
ms.assetid: 5c3a4b3f-ea58-498c-b7cf-54f028fa061c
keywords:
- DiscardUndoDisks 方法 Virtual PC
- DiscardUndoDisks 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，DiscardUndoDisks 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d548b69a6cfebc383a0233f01ef19ad14d051474
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465525"
---
# <a name="ivmvirtualmachinediscardundodisks-method"></a><span data-ttu-id="3cae1-106">IVMVirtualMachine：:D iscardUndoDisks 方法</span><span class="sxs-lookup"><span data-stu-id="3cae1-106">IVMVirtualMachine::DiscardUndoDisks method</span></span>

<span data-ttu-id="3cae1-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="3cae1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3cae1-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="3cae1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3cae1-109">捨棄虛擬復原磁片。</span><span class="sxs-lookup"><span data-stu-id="3cae1-109">Discards the virtual undo disks.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cae1-110">語法</span><span class="sxs-lookup"><span data-stu-id="3cae1-110">Syntax</span></span>


```C++
HRESULT DiscardUndoDisks();
```



## <a name="parameters"></a><span data-ttu-id="3cae1-111">參數</span><span class="sxs-lookup"><span data-stu-id="3cae1-111">Parameters</span></span>

<span data-ttu-id="3cae1-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3cae1-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3cae1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3cae1-113">Return value</span></span>

<span data-ttu-id="3cae1-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3cae1-114">This method can return one of these values.</span></span>



| <span data-ttu-id="3cae1-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="3cae1-115">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="3cae1-116">Description</span><span class="sxs-lookup"><span data-stu-id="3cae1-116">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3cae1-117"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3cae1-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="3cae1-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="3cae1-118">The operation was successful.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="3cae1-119"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="3cae1-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="3cae1-120">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="3cae1-120">The configuration is unknown.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="3cae1-121"><dt>**VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="3cae1-121"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="3cae1-122">當虛擬機器正在執行或處於儲存狀態時，無法捨棄虛擬復原磁片。</span><span class="sxs-lookup"><span data-stu-id="3cae1-122">The virtual undo disks cannot be discarded while the virtual machine is running or in a saved state.</span></span><br/> |
| <dl> <span data-ttu-id="3cae1-123"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3cae1-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="3cae1-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3cae1-124">An unexpected error has occurred.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="3cae1-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cae1-125">Requirements</span></span>



| <span data-ttu-id="3cae1-126">需求</span><span class="sxs-lookup"><span data-stu-id="3cae1-126">Requirement</span></span> | <span data-ttu-id="3cae1-127">值</span><span class="sxs-lookup"><span data-stu-id="3cae1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cae1-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3cae1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3cae1-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cae1-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3cae1-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3cae1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3cae1-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="3cae1-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3cae1-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="3cae1-132">End of client support</span></span><br/>    | <span data-ttu-id="3cae1-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3cae1-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3cae1-134">產品</span><span class="sxs-lookup"><span data-stu-id="3cae1-134">Product</span></span><br/>                  | <span data-ttu-id="3cae1-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3cae1-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3cae1-136">標頭</span><span class="sxs-lookup"><span data-stu-id="3cae1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cae1-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="3cae1-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3cae1-138">IID</span><span class="sxs-lookup"><span data-stu-id="3cae1-138">IID</span></span><br/>                      | <span data-ttu-id="3cae1-139">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="3cae1-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="3cae1-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cae1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cae1-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="3cae1-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

