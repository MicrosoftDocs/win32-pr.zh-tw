---
title: 'IVMVirtualMachine TurnOff 方法 (VPCCOMInterfaces .h) '
description: 關閉虛擬機器。
ms.assetid: 4ea00314-8f1e-47d9-bbb8-b5791af1fb86
keywords:
- TurnOff 方法 Virtual PC
- TurnOff 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，TurnOff 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.TurnOff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27a5b14955fcc8a060c49932e3fa4f238497a567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025354"
---
# <a name="ivmvirtualmachineturnoff-method"></a><span data-ttu-id="184d0-106">IVMVirtualMachine：： TurnOff 方法</span><span class="sxs-lookup"><span data-stu-id="184d0-106">IVMVirtualMachine::TurnOff method</span></span>

<span data-ttu-id="184d0-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="184d0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="184d0-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="184d0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="184d0-109">關閉虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="184d0-109">Turns off the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="184d0-110">語法</span><span class="sxs-lookup"><span data-stu-id="184d0-110">Syntax</span></span>


```C++
HRESULT TurnOff(
  [out, retval] IVMTask **turnOffTask
);
```



## <a name="parameters"></a><span data-ttu-id="184d0-111">參數</span><span class="sxs-lookup"><span data-stu-id="184d0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="184d0-112">*turnOffTask* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="184d0-112">*turnOffTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="184d0-113">[**IVMTask**](ivmtask.md)物件，用來追蹤虛擬機器 turnoff 序列的完成進度。</span><span class="sxs-lookup"><span data-stu-id="184d0-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the virtual machine's turnoff sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="184d0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="184d0-114">Return value</span></span>

<span data-ttu-id="184d0-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="184d0-115">This method can return one of these values.</span></span>



| <span data-ttu-id="184d0-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="184d0-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="184d0-117">Description</span><span class="sxs-lookup"><span data-stu-id="184d0-117">Description</span></span>                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="184d0-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="184d0-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="184d0-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="184d0-119">The operation was successful.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="184d0-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="184d0-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="184d0-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="184d0-121">The parameter is **NULL**.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="184d0-122"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="184d0-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="184d0-123">呼叫端必須具有執行存取權限，才能關閉此虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="184d0-123">The caller must have execute access permissions to turn off this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="184d0-124"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="184d0-124"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="184d0-125">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="184d0-125">The virtual machine is not running.</span></span><br/>                                               |
| <dl> <span data-ttu-id="184d0-126"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="184d0-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="184d0-127">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="184d0-127">The configuration is unknown.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="184d0-128"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="184d0-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="184d0-129">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="184d0-129">An unexpected error has occurred.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="184d0-130">備註</span><span class="sxs-lookup"><span data-stu-id="184d0-130">Remarks</span></span>

<span data-ttu-id="184d0-131">這個方法會關閉虛擬機器的方式，就像在實體機器上關閉電源一樣。</span><span class="sxs-lookup"><span data-stu-id="184d0-131">This method turns off the virtual machine in the same manner as turning the power off on a physical machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="184d0-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="184d0-132">Requirements</span></span>



| <span data-ttu-id="184d0-133">需求</span><span class="sxs-lookup"><span data-stu-id="184d0-133">Requirement</span></span> | <span data-ttu-id="184d0-134">值</span><span class="sxs-lookup"><span data-stu-id="184d0-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="184d0-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="184d0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="184d0-136">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="184d0-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="184d0-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="184d0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="184d0-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="184d0-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="184d0-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="184d0-139">End of client support</span></span><br/>    | <span data-ttu-id="184d0-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="184d0-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="184d0-141">產品</span><span class="sxs-lookup"><span data-stu-id="184d0-141">Product</span></span><br/>                  | <span data-ttu-id="184d0-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="184d0-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="184d0-143">標頭</span><span class="sxs-lookup"><span data-stu-id="184d0-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="184d0-144"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="184d0-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="184d0-145">IID</span><span class="sxs-lookup"><span data-stu-id="184d0-145">IID</span></span><br/>                      | <span data-ttu-id="184d0-146">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="184d0-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="184d0-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="184d0-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="184d0-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="184d0-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

