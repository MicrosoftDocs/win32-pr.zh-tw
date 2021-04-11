---
title: 'IVMVirtualMachine Resume 方法 (VPCCOMInterfaces .h) '
description: 繼續 VM。
ms.assetid: 4a2d6b64-8dcf-484e-940d-b0180aba9f01
keywords:
- Resume 方法 Virtual PC
- Resume 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC、Resume 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Resume
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c24af1e1a00aa0fa29acc077faf48287c0307414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844056"
---
# <a name="ivmvirtualmachineresume-method"></a><span data-ttu-id="fe3ee-106">IVMVirtualMachine：： Resume 方法</span><span class="sxs-lookup"><span data-stu-id="fe3ee-106">IVMVirtualMachine::Resume method</span></span>

<span data-ttu-id="fe3ee-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="fe3ee-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fe3ee-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="fe3ee-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fe3ee-109">繼續 (VM) 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="fe3ee-109">Resumes the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe3ee-110">語法</span><span class="sxs-lookup"><span data-stu-id="fe3ee-110">Syntax</span></span>


```C++
HRESULT Resume();
```



## <a name="parameters"></a><span data-ttu-id="fe3ee-111">參數</span><span class="sxs-lookup"><span data-stu-id="fe3ee-111">Parameters</span></span>

<span data-ttu-id="fe3ee-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fe3ee-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe3ee-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe3ee-113">Return value</span></span>

<span data-ttu-id="fe3ee-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fe3ee-114">This method can return one of these values.</span></span>



| <span data-ttu-id="fe3ee-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="fe3ee-115">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="fe3ee-116">Description</span><span class="sxs-lookup"><span data-stu-id="fe3ee-116">Description</span></span>                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe3ee-117"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fe3ee-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="fe3ee-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="fe3ee-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="fe3ee-119"><dt>**E \_FAIL**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="fe3ee-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="fe3ee-120">VM 未暫停。</span><span class="sxs-lookup"><span data-stu-id="fe3ee-120">The VM is not paused.</span></span><br/>                                              |
| <dl> <span data-ttu-id="fe3ee-121"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="fe3ee-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="fe3ee-122">呼叫端必須具有執行存取權限才能繼續此 VM。</span><span class="sxs-lookup"><span data-stu-id="fe3ee-122">The caller must have execute access permissions to resume this VM.</span></span><br/> |
| <dl> <span data-ttu-id="fe3ee-123"><dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fe3ee-123"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="fe3ee-124">作業未及時完成。</span><span class="sxs-lookup"><span data-stu-id="fe3ee-124">The operation did not complete in a timely manner.</span></span><br/>                 |
| <dl> <span data-ttu-id="fe3ee-125"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="fe3ee-125"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="fe3ee-126">VM 未執行。</span><span class="sxs-lookup"><span data-stu-id="fe3ee-126">The VM is not running.</span></span><br/>                                             |
| <dl> <span data-ttu-id="fe3ee-127"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="fe3ee-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="fe3ee-128">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="fe3ee-128">The configuration is unknown.</span></span><br/>                                      |
| <dl> <span data-ttu-id="fe3ee-129"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fe3ee-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="fe3ee-130">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="fe3ee-130">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="fe3ee-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe3ee-131">Requirements</span></span>



| <span data-ttu-id="fe3ee-132">需求</span><span class="sxs-lookup"><span data-stu-id="fe3ee-132">Requirement</span></span> | <span data-ttu-id="fe3ee-133">值</span><span class="sxs-lookup"><span data-stu-id="fe3ee-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3ee-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe3ee-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fe3ee-135">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe3ee-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fe3ee-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe3ee-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fe3ee-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="fe3ee-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fe3ee-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="fe3ee-138">End of client support</span></span><br/>    | <span data-ttu-id="fe3ee-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fe3ee-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fe3ee-140">產品</span><span class="sxs-lookup"><span data-stu-id="fe3ee-140">Product</span></span><br/>                  | <span data-ttu-id="fe3ee-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fe3ee-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fe3ee-142">標頭</span><span class="sxs-lookup"><span data-stu-id="fe3ee-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe3ee-143"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe3ee-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fe3ee-144">IID</span><span class="sxs-lookup"><span data-stu-id="fe3ee-144">IID</span></span><br/>                      | <span data-ttu-id="fe3ee-145">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="fe3ee-145">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="fe3ee-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe3ee-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe3ee-147">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="fe3ee-147">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

