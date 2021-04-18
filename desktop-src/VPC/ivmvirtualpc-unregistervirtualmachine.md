---
title: 'IVMVirtualPC UnregisterVirtualMachine 方法 (VPCCOMInterfaces .h) '
description: 取消註冊 VM 設定，而不刪除設定檔。
ms.assetid: 82ca6ef3-e9e5-471e-b2dc-0ff689a618d9
keywords:
- UnregisterVirtualMachine 方法 Virtual PC
- UnregisterVirtualMachine 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，UnregisterVirtualMachine 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnregisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d74380a822253918791b78bc34ac1c796f595ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466825"
---
# <a name="ivmvirtualpcunregistervirtualmachine-method"></a><span data-ttu-id="31870-106">IVMVirtualPC：： UnregisterVirtualMachine 方法</span><span class="sxs-lookup"><span data-stu-id="31870-106">IVMVirtualPC::UnregisterVirtualMachine method</span></span>

<span data-ttu-id="31870-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="31870-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="31870-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="31870-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="31870-109">在不刪除設定檔的情況下，取消註冊 (VM) 設定的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="31870-109">Unregisters a virtual machine (VM) configuration without deleting the configuration file.</span></span>

## <a name="syntax"></a><span data-ttu-id="31870-110">語法</span><span class="sxs-lookup"><span data-stu-id="31870-110">Syntax</span></span>


```C++
HRESULT UnregisterVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="31870-111">參數</span><span class="sxs-lookup"><span data-stu-id="31870-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31870-112">*virtualMachine* \[在\]</span><span class="sxs-lookup"><span data-stu-id="31870-112">*virtualMachine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31870-113">[**IVMVirtualMachine**](ivmvirtualmachine.md)物件的指標，代表要取消註冊的 VM 設定。</span><span class="sxs-lookup"><span data-stu-id="31870-113">A pointer to an [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents the VM configuration to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31870-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="31870-114">Return value</span></span>

<span data-ttu-id="31870-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="31870-115">This method can return one of these values.</span></span>



| <span data-ttu-id="31870-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="31870-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="31870-117">Description</span><span class="sxs-lookup"><span data-stu-id="31870-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="31870-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="31870-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="31870-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="31870-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="31870-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="31870-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="31870-121">*VirtualMachine* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="31870-121">The *virtualMachine* parameter was **NULL**.</span></span><br/>                                         |
| <dl> <span data-ttu-id="31870-122"><dt>**VM \_E \_ VM \_ 正在**</dt>執行 <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="31870-122"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                        | <span data-ttu-id="31870-123">VM 正在執行。</span><span class="sxs-lookup"><span data-stu-id="31870-123">The VM is running.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="31870-124"><dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="31870-124"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="31870-125">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="31870-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="31870-126"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="31870-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="31870-127">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="31870-127">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="31870-128">備註</span><span class="sxs-lookup"><span data-stu-id="31870-128">Remarks</span></span>

<span data-ttu-id="31870-129">只有已停止的 Vm 可以取消註冊。</span><span class="sxs-lookup"><span data-stu-id="31870-129">Only stopped VMs can be unregistered.</span></span> <span data-ttu-id="31870-130">當 VM 取消註冊時，此設定的現有儲存狀態或復原磁片磁碟機資料將會保留。</span><span class="sxs-lookup"><span data-stu-id="31870-130">Existing saved state or undo drive data for this configuration will be retained when a VM is unregistered.</span></span>

## <a name="requirements"></a><span data-ttu-id="31870-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="31870-131">Requirements</span></span>



| <span data-ttu-id="31870-132">需求</span><span class="sxs-lookup"><span data-stu-id="31870-132">Requirement</span></span> | <span data-ttu-id="31870-133">值</span><span class="sxs-lookup"><span data-stu-id="31870-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="31870-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31870-134">Minimum supported client</span></span><br/> | <span data-ttu-id="31870-135">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31870-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31870-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31870-136">Minimum supported server</span></span><br/> | <span data-ttu-id="31870-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="31870-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="31870-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="31870-138">End of client support</span></span><br/>    | <span data-ttu-id="31870-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="31870-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="31870-140">產品</span><span class="sxs-lookup"><span data-stu-id="31870-140">Product</span></span><br/>                  | <span data-ttu-id="31870-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="31870-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="31870-142">標頭</span><span class="sxs-lookup"><span data-stu-id="31870-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="31870-143"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="31870-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="31870-144">IID</span><span class="sxs-lookup"><span data-stu-id="31870-144">IID</span></span><br/>                      | <span data-ttu-id="31870-145">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="31870-145">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="31870-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31870-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31870-147">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="31870-147">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

