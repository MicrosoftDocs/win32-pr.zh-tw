---
title: 'IVMVirtualMachine Pause 方法 (VPCCOMInterfaces. h) '
description: 暫停虛擬機器。
ms.assetid: 29ac40c4-7713-4782-8a31-42f2c32b8f7d
keywords:
- 暫停方法虛擬電腦
- 暫停方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine interface Virtual PC，Pause 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Pause
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c953da05d34c999066a6bc87cb1f51983defbd5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843944"
---
# <a name="ivmvirtualmachinepause-method"></a><span data-ttu-id="d1460-106">IVMVirtualMachine：:P ause 方法</span><span class="sxs-lookup"><span data-stu-id="d1460-106">IVMVirtualMachine::Pause method</span></span>

<span data-ttu-id="d1460-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="d1460-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d1460-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="d1460-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d1460-109">暫停虛擬機器 (VM) 。</span><span class="sxs-lookup"><span data-stu-id="d1460-109">Pauses the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1460-110">語法</span><span class="sxs-lookup"><span data-stu-id="d1460-110">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="d1460-111">參數</span><span class="sxs-lookup"><span data-stu-id="d1460-111">Parameters</span></span>

<span data-ttu-id="d1460-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d1460-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1460-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1460-113">Return value</span></span>

<span data-ttu-id="d1460-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d1460-114">This method can return one of these values.</span></span>



| <span data-ttu-id="d1460-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="d1460-115">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="d1460-116">Description</span><span class="sxs-lookup"><span data-stu-id="d1460-116">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1460-117"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d1460-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="d1460-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="d1460-118">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d1460-119"><dt>**E \_FAIL**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="d1460-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="d1460-120">VM 已暫停。</span><span class="sxs-lookup"><span data-stu-id="d1460-120">The VM is already paused.</span></span><br/>                                         |
| <dl> <span data-ttu-id="d1460-121"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="d1460-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="d1460-122">呼叫端必須具有執行存取權限，才能暫停此 VM。</span><span class="sxs-lookup"><span data-stu-id="d1460-122">The caller must have execute access permissions to pause this VM.</span></span><br/> |
| <dl> <span data-ttu-id="d1460-123"><dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d1460-123"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="d1460-124">作業未及時完成。</span><span class="sxs-lookup"><span data-stu-id="d1460-124">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="d1460-125"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="d1460-125"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="d1460-126">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="d1460-126">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="d1460-127"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="d1460-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="d1460-128">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="d1460-128">The configuration is unknown.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d1460-129"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d1460-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="d1460-130">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d1460-130">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="d1460-131">備註</span><span class="sxs-lookup"><span data-stu-id="d1460-131">Remarks</span></span>

<span data-ttu-id="d1460-132">**暫停** 不會儲存 VM 的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d1460-132">**Pause** does not save the current state of the VM.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1460-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1460-133">Requirements</span></span>



| <span data-ttu-id="d1460-134">需求</span><span class="sxs-lookup"><span data-stu-id="d1460-134">Requirement</span></span> | <span data-ttu-id="d1460-135">值</span><span class="sxs-lookup"><span data-stu-id="d1460-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1460-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1460-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d1460-137">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1460-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1460-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1460-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d1460-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="d1460-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d1460-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d1460-140">End of client support</span></span><br/>    | <span data-ttu-id="d1460-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d1460-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d1460-142">產品</span><span class="sxs-lookup"><span data-stu-id="d1460-142">Product</span></span><br/>                  | <span data-ttu-id="d1460-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d1460-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d1460-144">標頭</span><span class="sxs-lookup"><span data-stu-id="d1460-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1460-145"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="d1460-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d1460-146">IID</span><span class="sxs-lookup"><span data-stu-id="d1460-146">IID</span></span><br/>                      | <span data-ttu-id="d1460-147">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="d1460-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d1460-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1460-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1460-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="d1460-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

