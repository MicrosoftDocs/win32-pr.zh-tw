---
title: 'IVMVirtualMachine AttachUSBDevice 方法 (VPCCOMInterfaces .h) '
description: 將 USB 裝置連接至 VM。
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- AttachUSBDevice 方法 Virtual PC
- AttachUSBDevice 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，AttachUSBDevice 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c36224823e4bd74b6a1c757816d55608e6d95a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025226"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a><span data-ttu-id="f3f6d-106">IVMVirtualMachine：： AttachUSBDevice 方法</span><span class="sxs-lookup"><span data-stu-id="f3f6d-106">IVMVirtualMachine::AttachUSBDevice method</span></span>

<span data-ttu-id="f3f6d-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f3f6d-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="f3f6d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f3f6d-109">將 USB 裝置連接到 (VM) 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-109">Attaches a USB device to a virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f6d-110">語法</span><span class="sxs-lookup"><span data-stu-id="f3f6d-110">Syntax</span></span>


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a><span data-ttu-id="f3f6d-111">參數</span><span class="sxs-lookup"><span data-stu-id="f3f6d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3f6d-112">*inUSBDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3f6d-112">*inUSBDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f6d-113">[**IVMUSBDevice**](ivmusbdevice.md)指標，表示連接至主機的 USB 裝置。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-113">A [**IVMUSBDevice**](ivmusbdevice.md) pointer that represents the USB device connected to the host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3f6d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3f6d-114">Return value</span></span>

<span data-ttu-id="f3f6d-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-115">This method can return one of these values.</span></span>



| <span data-ttu-id="f3f6d-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="f3f6d-116">Return code/value</span></span>                                                                                                                                                                             | <span data-ttu-id="f3f6d-117">Description</span><span class="sxs-lookup"><span data-stu-id="f3f6d-117">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f3f6d-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6d-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                   | <span data-ttu-id="f3f6d-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-119">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="f3f6d-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6d-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                     | <span data-ttu-id="f3f6d-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-121">The parameter is **NULL**.</span></span><br/>                                              |
| <dl> <span data-ttu-id="f3f6d-122"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6d-122"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                        | <span data-ttu-id="f3f6d-123">VM 未執行。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-123">The VM is not running.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="f3f6d-124"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6d-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                             | <span data-ttu-id="f3f6d-125">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-125">The configuration is unknown.</span></span><br/>                                           |
| <dl> <span data-ttu-id="f3f6d-126"><dt>**VM \_E \_ 新增 \_ 專案 \_ 無法**</dt> <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6d-126"><dt>**VM\_E\_ADDITIONS\_NOT\_AVAIL**</dt> <dt>0xA0040504</dt></span></span> </dl>                   | <span data-ttu-id="f3f6d-127">在客體作業系統中無法使用整合元件。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-127">Integration Components are not available in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="f3f6d-128"><dt>**VM \_E \_ 新增 \_ 功能 \_ 無法 \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6d-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>          | <span data-ttu-id="f3f6d-129">USB 功能無法使用。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-129">The USB feature is not available.</span></span><br/>                                       |
| <dl> <span data-ttu-id="f3f6d-130"><dt>**VM \_E \_ USB \_ 連接器 \_ 驅動程式 \_ 錯誤**</dt> <dt>0xA00400925</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6d-130"><dt>**VM\_E\_USB\_CONNECTOR\_DRIVER\_ERROR**</dt> <dt>0xA00400925</dt></span></span> </dl>          | <span data-ttu-id="f3f6d-131">發生 USB 連接器驅動程式錯誤。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-131">There was a USB Connector driver error.</span></span><br/>                                 |
| <dl> <span data-ttu-id="f3f6d-132"><dt>**VM \_E \_ USB \_ 附加 \_ 失敗 \_ 的 \_ 裝置**</dt> <dt>0xA00400931</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6d-132"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_MORE\_DEVICES**</dt> <dt>0xA00400931</dt></span></span> </dl>     | <span data-ttu-id="f3f6d-133">無法將更多裝置連結至 VM。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-133">Cannot attach more devices to the VM.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f3f6d-134"><dt>**VM \_E \_ USB \_ 附加 \_ 失敗的 \_ GP \_ 錯誤**</dt> <dt>0xA00400932</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6d-134"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_GP\_ERROR**</dt> <dt>0xA00400932</dt></span></span> </dl>         | <span data-ttu-id="f3f6d-135">群組原則設定阻礙了 USB 重新導向。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-135">A group policy setting is preventing the USB redirection.</span></span><br/>               |
| <dl> <span data-ttu-id="f3f6d-136"><dt>**VM \_E \_ USB \_ 附加 \_ 失敗 \_ 已 \_ 指派**</dt> <dt>0xA00400933</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6d-136"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_ALREADY\_ASSIGNED**</dt> <dt>0xA00400933</dt></span></span> </dl> | <span data-ttu-id="f3f6d-137">已有其他用戶端連接 USB 裝置。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-137">A USB device has already been attached by some other client.</span></span><br/>            |
| <dl> <span data-ttu-id="f3f6d-138"><dt>**VM \_E \_ USB \_ 附加 \_ 失敗**</dt> <dt>0xA00400926</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6d-138"><dt>**VM\_E\_USB\_ATTACH\_FAILED**</dt> <dt>0xA00400926</dt></span></span> </dl>                    | <span data-ttu-id="f3f6d-139">附加作業失敗。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-139">The attach operation failed.</span></span><br/>                                            |
| <dl> <span data-ttu-id="f3f6d-140"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6d-140"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                             | <span data-ttu-id="f3f6d-141">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f3f6d-141">An unexpected error has occurred.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="f3f6d-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3f6d-142">Requirements</span></span>



| <span data-ttu-id="f3f6d-143">需求</span><span class="sxs-lookup"><span data-stu-id="f3f6d-143">Requirement</span></span> | <span data-ttu-id="f3f6d-144">值</span><span class="sxs-lookup"><span data-stu-id="f3f6d-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f6d-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3f6d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f3f6d-146">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3f6d-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f3f6d-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3f6d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f3f6d-148">都不支援</span><span class="sxs-lookup"><span data-stu-id="f3f6d-148">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f3f6d-149">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f3f6d-149">End of client support</span></span><br/>    | <span data-ttu-id="f3f6d-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3f6d-150">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f3f6d-151">產品</span><span class="sxs-lookup"><span data-stu-id="f3f6d-151">Product</span></span><br/>                  | <span data-ttu-id="f3f6d-152">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f3f6d-152">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f3f6d-153">標頭</span><span class="sxs-lookup"><span data-stu-id="f3f6d-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3f6d-154"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6d-154"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f3f6d-155">IID</span><span class="sxs-lookup"><span data-stu-id="f3f6d-155">IID</span></span><br/>                      | <span data-ttu-id="f3f6d-156">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="f3f6d-156">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="f3f6d-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3f6d-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3f6d-158">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="f3f6d-158">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

