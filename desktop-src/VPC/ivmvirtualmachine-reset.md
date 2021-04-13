---
title: 'IVMVirtualMachine Reset 方法 (VPCCOMInterfaces .h) '
description: 重設虛擬機器。
ms.assetid: 44daf6be-66ce-4291-a535-c30369eed60f
keywords:
- 重設方法虛擬電腦
- Reset 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，Reset 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Reset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45314eef6d837ac00647d477f3652b63221d977c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466393"
---
# <a name="ivmvirtualmachinereset-method"></a><span data-ttu-id="258e3-106">IVMVirtualMachine：： Reset 方法</span><span class="sxs-lookup"><span data-stu-id="258e3-106">IVMVirtualMachine::Reset method</span></span>

<span data-ttu-id="258e3-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="258e3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="258e3-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="258e3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="258e3-109">重設 (VM) 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="258e3-109">Resets the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="258e3-110">語法</span><span class="sxs-lookup"><span data-stu-id="258e3-110">Syntax</span></span>


```C++
HRESULT Reset(
  [out, retval] IVMTask **resetTask
);
```



## <a name="parameters"></a><span data-ttu-id="258e3-111">參數</span><span class="sxs-lookup"><span data-stu-id="258e3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="258e3-112">*resetTask* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="258e3-112">*resetTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="258e3-113">[**IVMTask**](ivmtask.md)物件，可用來追蹤 VM 重設順序的完成進度。</span><span class="sxs-lookup"><span data-stu-id="258e3-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the VM's reset sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="258e3-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="258e3-114">Return value</span></span>

<span data-ttu-id="258e3-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="258e3-115">This method can return one of these values.</span></span>



| <span data-ttu-id="258e3-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="258e3-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="258e3-117">Description</span><span class="sxs-lookup"><span data-stu-id="258e3-117">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="258e3-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="258e3-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="258e3-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="258e3-119">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="258e3-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="258e3-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="258e3-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="258e3-121">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="258e3-122"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="258e3-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="258e3-123">呼叫端必須具有執行存取權限，才能重設此 VM。</span><span class="sxs-lookup"><span data-stu-id="258e3-123">The caller must have execute access permissions to reset this VM.</span></span><br/> |
| <dl> <span data-ttu-id="258e3-124"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="258e3-124"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="258e3-125">VM 未執行。</span><span class="sxs-lookup"><span data-stu-id="258e3-125">The VM is not running.</span></span><br/>                                            |
| <dl> <span data-ttu-id="258e3-126"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="258e3-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="258e3-127">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="258e3-127">The configuration is unknown.</span></span><br/>                                     |
| <dl> <span data-ttu-id="258e3-128"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="258e3-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="258e3-129">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="258e3-129">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="258e3-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="258e3-130">Requirements</span></span>



| <span data-ttu-id="258e3-131">需求</span><span class="sxs-lookup"><span data-stu-id="258e3-131">Requirement</span></span> | <span data-ttu-id="258e3-132">值</span><span class="sxs-lookup"><span data-stu-id="258e3-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="258e3-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="258e3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="258e3-134">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="258e3-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="258e3-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="258e3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="258e3-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="258e3-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="258e3-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="258e3-137">End of client support</span></span><br/>    | <span data-ttu-id="258e3-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="258e3-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="258e3-139">產品</span><span class="sxs-lookup"><span data-stu-id="258e3-139">Product</span></span><br/>                  | <span data-ttu-id="258e3-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="258e3-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="258e3-141">標頭</span><span class="sxs-lookup"><span data-stu-id="258e3-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="258e3-142"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="258e3-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="258e3-143">IID</span><span class="sxs-lookup"><span data-stu-id="258e3-143">IID</span></span><br/>                      | <span data-ttu-id="258e3-144">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="258e3-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="258e3-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="258e3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="258e3-146">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="258e3-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

