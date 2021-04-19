---
title: 'IVMDisplay SetDimensions 方法 (VPCCOMInterfaces .h) '
description: 設定 VM 顯示器的高度和寬度（以圖元為單位）。
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- SetDimensions 方法 Virtual PC
- SetDimensions 方法 Virtual PC，IVMDisplay 介面
- IVMDisplay 介面 Virtual PC，SetDimensions 方法
topic_type:
- apiref
api_name:
- IVMDisplay.SetDimensions
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4730d73e06074714c8e6ed31fda992259d5c19ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107000026"
---
# <a name="ivmdisplaysetdimensions-method"></a><span data-ttu-id="5632b-106">IVMDisplay：： SetDimensions 方法</span><span class="sxs-lookup"><span data-stu-id="5632b-106">IVMDisplay::SetDimensions method</span></span>

<span data-ttu-id="5632b-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="5632b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5632b-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="5632b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5632b-109">設定虛擬機器 (VM) 顯示的高度和寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5632b-109">Sets the height and width of the virtual machine's (VM's) display, in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="5632b-110">語法</span><span class="sxs-lookup"><span data-stu-id="5632b-110">Syntax</span></span>


```C++
HRESULT SetDimensions(
  [in] long displayPixelWidth,
  [in] long displayPixelHeight
);
```



## <a name="parameters"></a><span data-ttu-id="5632b-111">參數</span><span class="sxs-lookup"><span data-stu-id="5632b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5632b-112">*displayPixelWidth* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5632b-112">*displayPixelWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5632b-113">寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5632b-113">The width, in pixels.</span></span> <span data-ttu-id="5632b-114">值必須介於640到2048的值之間。</span><span class="sxs-lookup"><span data-stu-id="5632b-114">The value must be between the values of 640 and 2048.</span></span> <span data-ttu-id="5632b-115">如果值未平均地除以8，則會縮減為下一個較低的8倍。</span><span class="sxs-lookup"><span data-stu-id="5632b-115">If the value is not evenly divisible by 8, then it will be reduced to the next lower multiple of 8.</span></span>

</dd> <dt>

<span data-ttu-id="5632b-116">*displayPixelHeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5632b-116">*displayPixelHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5632b-117">高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5632b-117">The height, in pixels.</span></span> <span data-ttu-id="5632b-118">值必須介於480到1920的值之間。</span><span class="sxs-lookup"><span data-stu-id="5632b-118">The value must be between the values of 480 and 1920.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5632b-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="5632b-119">Return value</span></span>

<span data-ttu-id="5632b-120">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5632b-120">This method can return one of these values.</span></span>



| <span data-ttu-id="5632b-121">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="5632b-121">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="5632b-122">Description</span><span class="sxs-lookup"><span data-stu-id="5632b-122">Description</span></span>                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5632b-123"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5632b-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="5632b-124">作業成功。</span><span class="sxs-lookup"><span data-stu-id="5632b-124">The operation was successful.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="5632b-125"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="5632b-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="5632b-126">*DisplayPixelWidth* 參數無法平均地被8整除，或 *displayPixelWidth* 或 *displayPixelHeight* 參數超出允許的最小 (640) 或 2048x1920) 值上限。</span><span class="sxs-lookup"><span data-stu-id="5632b-126">The *displayPixelWidth* parameter is not evenly divisible by 8 or the *displayPixelWidth* or *displayPixelHeight* parameter is outside of the allowed minimum (640x480) or maximum 2048x1920) values.</span></span><br/> |
| <dl> <span data-ttu-id="5632b-127"><dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5632b-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="5632b-128">解決方式變更未及時完成。</span><span class="sxs-lookup"><span data-stu-id="5632b-128">The resolution change did not finish in a timely manner.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="5632b-129"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="5632b-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="5632b-130">虛擬機器必須正在執行，才能進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="5632b-130">The virtual machine must be running for this operation.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="5632b-131"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="5632b-131"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="5632b-132">虛擬機器無效或目前未執行。</span><span class="sxs-lookup"><span data-stu-id="5632b-132">The virtual machine is not valid or is not currently running.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="5632b-133"><dt>**VM \_E \_ NO \_ DISPLAY**</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="5632b-133"><dt>**VM\_E\_NO\_DISPLAY**</dt> <dt>0xA0040850</dt></span></span> </dl>                    | <span data-ttu-id="5632b-134">找不到 VM 的有效顯示。</span><span class="sxs-lookup"><span data-stu-id="5632b-134">Unable to locate a valid display for the VM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="5632b-135"><dt>**VM \_E \_ 新增 \_ 功能 \_ 無法 \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="5632b-135"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="5632b-136">在客體作業系統中安裝的整合元件版本不支援這項操作。</span><span class="sxs-lookup"><span data-stu-id="5632b-136">The version of the integration components installed in the guest operating system does not support this operation.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="5632b-137"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5632b-137"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="5632b-138">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5632b-138">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="5632b-139">備註</span><span class="sxs-lookup"><span data-stu-id="5632b-139">Remarks</span></span>

<span data-ttu-id="5632b-140">虛擬機器顯示的大小下限為 640 x 480 圖元。</span><span class="sxs-lookup"><span data-stu-id="5632b-140">The minimum size of the virtual machine's display is 640 x 480 pixels.</span></span> <span data-ttu-id="5632b-141">大小上限為 2048 x 1920。</span><span class="sxs-lookup"><span data-stu-id="5632b-141">The maximum size is 2048 x 1920.</span></span> <span data-ttu-id="5632b-142">嘗試將顯示大小設定為超出這些限制的值，或設定為未平均整除8的任何寬度，會導致傳回 **電子 \_ INVALIDARG** 錯誤。</span><span class="sxs-lookup"><span data-stu-id="5632b-142">Attempts to set the display size to values outside these limits, or to any width not evenly divisible by 8, will result in an **E\_INVALIDARG** error being returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="5632b-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="5632b-143">Requirements</span></span>



| <span data-ttu-id="5632b-144">需求</span><span class="sxs-lookup"><span data-stu-id="5632b-144">Requirement</span></span> | <span data-ttu-id="5632b-145">值</span><span class="sxs-lookup"><span data-stu-id="5632b-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5632b-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5632b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5632b-147">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5632b-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5632b-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5632b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5632b-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="5632b-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5632b-150">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5632b-150">End of client support</span></span><br/>    | <span data-ttu-id="5632b-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5632b-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5632b-152">產品</span><span class="sxs-lookup"><span data-stu-id="5632b-152">Product</span></span><br/>                  | <span data-ttu-id="5632b-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5632b-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5632b-154">標頭</span><span class="sxs-lookup"><span data-stu-id="5632b-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="5632b-155"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="5632b-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5632b-156">IID</span><span class="sxs-lookup"><span data-stu-id="5632b-156">IID</span></span><br/>                      | <span data-ttu-id="5632b-157">IID \_ IVMDisplay 定義為960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="5632b-157">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="5632b-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5632b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5632b-159">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="5632b-159">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

