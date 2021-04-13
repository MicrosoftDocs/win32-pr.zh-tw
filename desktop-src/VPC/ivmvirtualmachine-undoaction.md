---
title: 'IVMVirtualMachine UndoAction 屬性 (VPCCOMInterfaces .h) '
description: 當 VM 關閉時，要在所有復原磁片磁碟機上執行的預設動作。
ms.assetid: fcdd5217-4909-435a-b11d-63578ab46e37
keywords:
- UndoAction 屬性 Virtual PC
- UndoAction 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，UndoAction 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.UndoAction
- IVMVirtualMachine.get_UndoAction
- IVMVirtualMachine.put_UndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 039a9e65863e41ba2c7edc1befd2598aa16bb362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466377"
---
# <a name="ivmvirtualmachineundoaction-property"></a><span data-ttu-id="99c3d-106">IVMVirtualMachine：： UndoAction 屬性</span><span class="sxs-lookup"><span data-stu-id="99c3d-106">IVMVirtualMachine::UndoAction property</span></span>

<span data-ttu-id="99c3d-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="99c3d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="99c3d-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="99c3d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="99c3d-109">當虛擬機器 (VM) 使用 [**TurnOff**](ivmvirtualmachine-turnoff.md) 方法關閉，或使用 [**關閉**](ivmguestos-shutdown.md) 方法關閉，或從客體作業系統中關閉時，會抓取並設定要在所有復原磁片磁碟機上執行的預設動作。</span><span class="sxs-lookup"><span data-stu-id="99c3d-109">Retrieves and sets the default action to be performed on all undo drives when the virtual machine (VM) is turned off using the [**TurnOff**](ivmvirtualmachine-turnoff.md) method or shut down using the [**Shutdown**](ivmguestos-shutdown.md) method or turned off from within the guest operating system.</span></span>

<span data-ttu-id="99c3d-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="99c3d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="99c3d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="99c3d-111">Syntax</span></span>


```C++
HRESULT put_UndoAction(
  [in]          VMUndoAction undoAction
);

HRESULT get_UndoAction(
  [out, retval] VMUndoAction *undoAction
);
```



## <a name="property-value"></a><span data-ttu-id="99c3d-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="99c3d-112">Property value</span></span>

<span data-ttu-id="99c3d-113">指定當 VM 從客體作業系統中關閉時，要在所有復原磁片磁碟機上執行的預設動作。</span><span class="sxs-lookup"><span data-stu-id="99c3d-113">Specifies the default action to be performed on all undo drives when the VM is shut down from within the guest operating system.</span></span> <span data-ttu-id="99c3d-114">如需值的清單，請參閱 [**VMUndoAction**](vmundoaction.md)。</span><span class="sxs-lookup"><span data-stu-id="99c3d-114">For a list of values, see [**VMUndoAction**](vmundoaction.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="99c3d-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="99c3d-115">Error codes</span></span>



| <span data-ttu-id="99c3d-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="99c3d-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="99c3d-117">意義</span><span class="sxs-lookup"><span data-stu-id="99c3d-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="99c3d-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="99c3d-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="99c3d-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="99c3d-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="99c3d-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="99c3d-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="99c3d-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="99c3d-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="99c3d-122"><dt>E \_INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="99c3d-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="99c3d-123">參數無效。</span><span class="sxs-lookup"><span data-stu-id="99c3d-123">The parameter is not valid.</span></span><br/>       |
| <dl> <span data-ttu-id="99c3d-124"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="99c3d-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="99c3d-125">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="99c3d-125">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="99c3d-126"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="99c3d-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="99c3d-127">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="99c3d-127">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="99c3d-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="99c3d-128">Requirements</span></span>



| <span data-ttu-id="99c3d-129">需求</span><span class="sxs-lookup"><span data-stu-id="99c3d-129">Requirement</span></span> | <span data-ttu-id="99c3d-130">值</span><span class="sxs-lookup"><span data-stu-id="99c3d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="99c3d-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99c3d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="99c3d-132">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99c3d-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="99c3d-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99c3d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="99c3d-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="99c3d-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="99c3d-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="99c3d-135">End of client support</span></span><br/>    | <span data-ttu-id="99c3d-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="99c3d-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="99c3d-137">產品</span><span class="sxs-lookup"><span data-stu-id="99c3d-137">Product</span></span><br/>                  | <span data-ttu-id="99c3d-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="99c3d-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="99c3d-139">標頭</span><span class="sxs-lookup"><span data-stu-id="99c3d-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="99c3d-140"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="99c3d-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="99c3d-141">IID</span><span class="sxs-lookup"><span data-stu-id="99c3d-141">IID</span></span><br/>                      | <span data-ttu-id="99c3d-142">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="99c3d-142">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="99c3d-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99c3d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99c3d-144">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="99c3d-144">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

