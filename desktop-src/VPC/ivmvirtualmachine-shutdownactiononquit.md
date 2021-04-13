---
title: 'IVMVirtualMachine ShutdownActionOnQuit 屬性 (VPCCOMInterfaces .h) '
description: 當 Windows Virtual PC 結束時，要在此虛擬機器上執行的動作。
ms.assetid: 3f6b256e-c48a-4a7c-acee-83d996e13ec7
keywords:
- ShutdownActionOnQuit 屬性 Virtual PC
- ShutdownActionOnQuit 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，ShutdownActionOnQuit 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ShutdownActionOnQuit
- IVMVirtualMachine.get_ShutdownActionOnQuit
- IVMVirtualMachine.put_ShutdownActionOnQuit
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01469e48e767777c6ea3daa4d0f3a923dce67726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466384"
---
# <a name="ivmvirtualmachineshutdownactiononquit-property"></a><span data-ttu-id="6e5ab-106">IVMVirtualMachine：： ShutdownActionOnQuit 屬性</span><span class="sxs-lookup"><span data-stu-id="6e5ab-106">IVMVirtualMachine::ShutdownActionOnQuit property</span></span>

<span data-ttu-id="6e5ab-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="6e5ab-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6e5ab-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="6e5ab-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6e5ab-109">抓取並設定要在此虛擬機器上執行的動作 (VM) 如果是在 Windows Virtual PC 結束時執行。</span><span class="sxs-lookup"><span data-stu-id="6e5ab-109">Retrieves and sets the action to be performed on this virtual machine (VM) if it is running when Windows Virtual PC is quit.</span></span>

<span data-ttu-id="6e5ab-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6e5ab-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e5ab-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e5ab-111">Syntax</span></span>


```C++
HRESULT put_ShutdownActionOnQuit(
  [in]          VMShutdownAction shutdownAction
);

HRESULT get_ShutdownActionOnQuit(
  [out, retval] VMShutdownAction *shutdownAction
);
```



## <a name="property-value"></a><span data-ttu-id="6e5ab-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="6e5ab-112">Property value</span></span>

<span data-ttu-id="6e5ab-113">指定當 Windows Virtual PC 結束時，如果 VM 正在執行，如何關閉此 VM。</span><span class="sxs-lookup"><span data-stu-id="6e5ab-113">Specifies how to shut down this VM if it is running when Windows Virtual PC is quit.</span></span> <span data-ttu-id="6e5ab-114">如需值的清單，請參閱 [**VMShutdownAction**](vmshutdownaction.md)。</span><span class="sxs-lookup"><span data-stu-id="6e5ab-114">For a list of values, see [**VMShutdownAction**](vmshutdownaction.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="6e5ab-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="6e5ab-115">Error codes</span></span>



| <span data-ttu-id="6e5ab-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="6e5ab-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6e5ab-117">意義</span><span class="sxs-lookup"><span data-stu-id="6e5ab-117">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6e5ab-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6e5ab-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6e5ab-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="6e5ab-119">The operation was successful.</span></span><br/>                                       |
| <dl> <span data-ttu-id="6e5ab-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6e5ab-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6e5ab-121">參數為 **Null** 或不是有效的值。</span><span class="sxs-lookup"><span data-stu-id="6e5ab-121">The parameter is **NULL** or not a valid value.</span></span><br/>                     |
| <dl> <span data-ttu-id="6e5ab-122"><dt>E \_ACCESSDENIED</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="6e5ab-122"><dt>E\_ACCESSDENIED</dt> <dt>0x80070005</dt></span></span> </dl>    | <span data-ttu-id="6e5ab-123">目前的使用者沒有設定檔的足夠存取權。</span><span class="sxs-lookup"><span data-stu-id="6e5ab-123">The current user has insufficient access to the configuration file.</span></span><br/> |
| <dl> <span data-ttu-id="6e5ab-124"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="6e5ab-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="6e5ab-125">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="6e5ab-125">The configuration is unknown.</span></span><br/>                                       |
| <dl> <span data-ttu-id="6e5ab-126"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6e5ab-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6e5ab-127">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6e5ab-127">An unexpected error has occurred.</span></span><br/>                                   |



## <a name="remarks"></a><span data-ttu-id="6e5ab-128">備註</span><span class="sxs-lookup"><span data-stu-id="6e5ab-128">Remarks</span></span>

<span data-ttu-id="6e5ab-129">根據預設，當 Windows Virtual PC 結束時，會儲存執行中的 Vm。</span><span class="sxs-lookup"><span data-stu-id="6e5ab-129">By default, running VMs are saved when Windows Virtual PC is quit.</span></span> <span data-ttu-id="6e5ab-130">關機動作 **vmShutdownAction \_ 儲存** (0) 將會儲存 VM 的狀態。</span><span class="sxs-lookup"><span data-stu-id="6e5ab-130">The shutdown action **vmShutdownAction\_Save** (0) will save the VM's state.</span></span> <span data-ttu-id="6e5ab-131">**VmShutdownAction \_ TurnOff** (1) 動作將會關閉 VM。</span><span class="sxs-lookup"><span data-stu-id="6e5ab-131">The **vmShutdownAction\_TurnOff** (1) action will turn off the VM.</span></span> <span data-ttu-id="6e5ab-132">如果有整合元件可用， **vmShutdownAction \_ 關機** (2) 動作將會關閉客體作業系統，否則會儲存 VM。</span><span class="sxs-lookup"><span data-stu-id="6e5ab-132">The **vmShutdownAction\_Shutdown** (2) action will shut down the guest operating system if the integration components are available and will save the VM otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e5ab-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e5ab-133">Requirements</span></span>



| <span data-ttu-id="6e5ab-134">需求</span><span class="sxs-lookup"><span data-stu-id="6e5ab-134">Requirement</span></span> | <span data-ttu-id="6e5ab-135">值</span><span class="sxs-lookup"><span data-stu-id="6e5ab-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e5ab-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e5ab-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6e5ab-137">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e5ab-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6e5ab-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e5ab-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6e5ab-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="6e5ab-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6e5ab-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6e5ab-140">End of client support</span></span><br/>    | <span data-ttu-id="6e5ab-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6e5ab-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6e5ab-142">產品</span><span class="sxs-lookup"><span data-stu-id="6e5ab-142">Product</span></span><br/>                  | <span data-ttu-id="6e5ab-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6e5ab-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6e5ab-144">標頭</span><span class="sxs-lookup"><span data-stu-id="6e5ab-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e5ab-145"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e5ab-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6e5ab-146">IID</span><span class="sxs-lookup"><span data-stu-id="6e5ab-146">IID</span></span><br/>                      | <span data-ttu-id="6e5ab-147">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="6e5ab-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="6e5ab-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e5ab-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e5ab-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="6e5ab-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="6e5ab-150">**VMShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="6e5ab-150">**VMShutdownAction**</span></span>](vmshutdownaction.md)
</dt> </dl>

 

