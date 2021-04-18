---
title: 'IVMVirtualMachine DetachUSBDevice 方法 (VPCCOMInterfaces .h) '
description: 從虛擬機器釋放 USB 裝置。
ms.assetid: ae2b70b1-7bf3-4a84-9f05-4e91de93fa73
keywords:
- DetachUSBDevice 方法 Virtual PC
- DetachUSBDevice 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，DetachUSBDevice 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DetachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f5a858c25822e9e9ba1a11686003b326133a59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966131"
---
# <a name="ivmvirtualmachinedetachusbdevice-method"></a><span data-ttu-id="856db-106">IVMVirtualMachine：:D etachUSBDevice 方法</span><span class="sxs-lookup"><span data-stu-id="856db-106">IVMVirtualMachine::DetachUSBDevice method</span></span>

<span data-ttu-id="856db-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="856db-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="856db-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="856db-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="856db-109">從虛擬機器釋放 USB 裝置。</span><span class="sxs-lookup"><span data-stu-id="856db-109">Releases a USB device from a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="856db-110">語法</span><span class="sxs-lookup"><span data-stu-id="856db-110">Syntax</span></span>


```C++
HRESULT DetachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a><span data-ttu-id="856db-111">參數</span><span class="sxs-lookup"><span data-stu-id="856db-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="856db-112">*inUSBDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="856db-112">*inUSBDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="856db-113">[**IVMUSBDevice**](ivmusbdevice.md)指標，代表要從虛擬機器卸離的 USB 裝置。</span><span class="sxs-lookup"><span data-stu-id="856db-113">A [**IVMUSBDevice**](ivmusbdevice.md) pointer that represents the USB device to be detached from the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="856db-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="856db-114">Return value</span></span>

<span data-ttu-id="856db-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="856db-115">This method can return one of these values.</span></span>



| <span data-ttu-id="856db-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="856db-116">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="856db-117">Description</span><span class="sxs-lookup"><span data-stu-id="856db-117">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="856db-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="856db-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="856db-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="856db-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="856db-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="856db-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                  | <span data-ttu-id="856db-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="856db-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="856db-122"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="856db-122"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>     | <span data-ttu-id="856db-123">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="856db-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="856db-124"><dt>**VM \_E \_ USB 卸 \_ 離 \_ 失敗**</dt> <dt>0xA00400927</dt></span><span class="sxs-lookup"><span data-stu-id="856db-124"><dt>**VM\_E\_USB\_DETACH\_FAILED**</dt> <dt>0xA00400927</dt></span></span> </dl> | <span data-ttu-id="856db-125">卸離作業失敗。</span><span class="sxs-lookup"><span data-stu-id="856db-125">The detach operation failed.</span></span><br/>        |
| <dl> <span data-ttu-id="856db-126"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="856db-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="856db-127">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="856db-127">An unexpected error has occurred.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="856db-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="856db-128">Requirements</span></span>



| <span data-ttu-id="856db-129">需求</span><span class="sxs-lookup"><span data-stu-id="856db-129">Requirement</span></span> | <span data-ttu-id="856db-130">值</span><span class="sxs-lookup"><span data-stu-id="856db-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="856db-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="856db-131">Minimum supported client</span></span><br/> | <span data-ttu-id="856db-132">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="856db-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="856db-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="856db-133">Minimum supported server</span></span><br/> | <span data-ttu-id="856db-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="856db-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="856db-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="856db-135">End of client support</span></span><br/>    | <span data-ttu-id="856db-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="856db-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="856db-137">產品</span><span class="sxs-lookup"><span data-stu-id="856db-137">Product</span></span><br/>                  | <span data-ttu-id="856db-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="856db-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="856db-139">標頭</span><span class="sxs-lookup"><span data-stu-id="856db-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="856db-140"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="856db-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="856db-141">IID</span><span class="sxs-lookup"><span data-stu-id="856db-141">IID</span></span><br/>                      | <span data-ttu-id="856db-142">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="856db-142">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="856db-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="856db-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="856db-144">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="856db-144">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

