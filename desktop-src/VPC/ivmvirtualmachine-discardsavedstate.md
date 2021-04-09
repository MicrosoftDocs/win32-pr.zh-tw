---
title: 'IVMVirtualMachine DiscardSavedState 方法 (VPCCOMInterfaces .h) '
description: 捨棄已儲存之虛擬機器的任何儲存狀態資訊。
ms.assetid: 546d6ea9-bfa3-487d-a333-399986bdf9a1
keywords:
- DiscardSavedState 方法 Virtual PC
- DiscardSavedState 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，DiscardSavedState 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardSavedState
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce5c9cc0b07af2cc8c995d0c368d7747fa1475a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025225"
---
# <a name="ivmvirtualmachinediscardsavedstate-method"></a><span data-ttu-id="5ef9e-106">IVMVirtualMachine：:D iscardSavedState 方法</span><span class="sxs-lookup"><span data-stu-id="5ef9e-106">IVMVirtualMachine::DiscardSavedState method</span></span>

<span data-ttu-id="5ef9e-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="5ef9e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5ef9e-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="5ef9e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5ef9e-109">捨棄已儲存之虛擬機器的任何儲存狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="5ef9e-109">Discards any saved state information for a saved virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ef9e-110">語法</span><span class="sxs-lookup"><span data-stu-id="5ef9e-110">Syntax</span></span>


```C++
HRESULT DiscardSavedState();
```



## <a name="parameters"></a><span data-ttu-id="5ef9e-111">參數</span><span class="sxs-lookup"><span data-stu-id="5ef9e-111">Parameters</span></span>

<span data-ttu-id="5ef9e-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5ef9e-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ef9e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5ef9e-113">Return value</span></span>

<span data-ttu-id="5ef9e-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5ef9e-114">This method can return one of these values.</span></span>



| <span data-ttu-id="5ef9e-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="5ef9e-115">Return code/value</span></span>                                                                                                                                                           | <span data-ttu-id="5ef9e-116">Description</span><span class="sxs-lookup"><span data-stu-id="5ef9e-116">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ef9e-117"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5ef9e-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="5ef9e-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="5ef9e-118">The operation was successful.</span></span><br/>                               |
| <dl> <span data-ttu-id="5ef9e-119"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="5ef9e-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="5ef9e-120">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="5ef9e-120">The configuration is unknown.</span></span><br/>                               |
| <dl> <span data-ttu-id="5ef9e-121"><dt>**VM \_E \_ VM \_ 正在**</dt>執行 <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="5ef9e-121"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>           | <span data-ttu-id="5ef9e-122">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="5ef9e-122">The virtual machine is running.</span></span><br/>                             |
| <dl> <span data-ttu-id="5ef9e-123"><dt>**VM \_E \_ VM \_ 沒有 \_ 儲存的 \_ 狀態**</dt> <dt>0xA00400501</dt></span><span class="sxs-lookup"><span data-stu-id="5ef9e-123"><dt>**VM\_E\_VM\_NO\_SAVED\_STATE**</dt> <dt>0xA00400501</dt></span></span> </dl> | <span data-ttu-id="5ef9e-124">虛擬機器未執行，但沒有儲存的狀態。</span><span class="sxs-lookup"><span data-stu-id="5ef9e-124">The virtual machine is not running, but has no saved state.</span></span><br/> |
| <dl> <span data-ttu-id="5ef9e-125"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5ef9e-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="5ef9e-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5ef9e-126">An unexpected error has occurred.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="5ef9e-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ef9e-127">Requirements</span></span>



| <span data-ttu-id="5ef9e-128">需求</span><span class="sxs-lookup"><span data-stu-id="5ef9e-128">Requirement</span></span> | <span data-ttu-id="5ef9e-129">值</span><span class="sxs-lookup"><span data-stu-id="5ef9e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef9e-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ef9e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5ef9e-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ef9e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5ef9e-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ef9e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5ef9e-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="5ef9e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5ef9e-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5ef9e-134">End of client support</span></span><br/>    | <span data-ttu-id="5ef9e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5ef9e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5ef9e-136">產品</span><span class="sxs-lookup"><span data-stu-id="5ef9e-136">Product</span></span><br/>                  | <span data-ttu-id="5ef9e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5ef9e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5ef9e-138">標頭</span><span class="sxs-lookup"><span data-stu-id="5ef9e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ef9e-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="5ef9e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5ef9e-140">IID</span><span class="sxs-lookup"><span data-stu-id="5ef9e-140">IID</span></span><br/>                      | <span data-ttu-id="5ef9e-141">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="5ef9e-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="5ef9e-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ef9e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef9e-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="5ef9e-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

