---
title: 'IVMVirtualMachine State 屬性 (VPCCOMInterfaces .h) '
description: 抓取虛擬機器的目前狀態。
ms.assetid: a4214dfc-09d2-4d6b-a053-e75e99063411
keywords:
- 狀態屬性虛擬電腦
- 狀態屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，State 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.State
- IVMVirtualMachine.get_State
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11616f2a88b9238da11a4edec00c048e69885a07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934862"
---
# <a name="ivmvirtualmachinestate-property"></a><span data-ttu-id="52320-106">IVMVirtualMachine：： State 屬性</span><span class="sxs-lookup"><span data-stu-id="52320-106">IVMVirtualMachine::State property</span></span>

<span data-ttu-id="52320-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="52320-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="52320-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="52320-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="52320-109">抓取虛擬機器的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="52320-109">Retrieves the current state of the virtual machine.</span></span>

<span data-ttu-id="52320-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="52320-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="52320-111">語法</span><span class="sxs-lookup"><span data-stu-id="52320-111">Syntax</span></span>


```C++
HRESULT get_State(
  [out, retval] VMVMState *virtualMachineState
);
```



## <a name="property-value"></a><span data-ttu-id="52320-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="52320-112">Property value</span></span>

<span data-ttu-id="52320-113">虛擬機器的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="52320-113">The current state of the virtual machine.</span></span> <span data-ttu-id="52320-114">如需值的清單，請參閱 [**VMVMState**](vmvmstate.md)。</span><span class="sxs-lookup"><span data-stu-id="52320-114">For a list of values, see [**VMVMState**](vmvmstate.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="52320-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="52320-115">Error codes</span></span>



| <span data-ttu-id="52320-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="52320-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="52320-117">意義</span><span class="sxs-lookup"><span data-stu-id="52320-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="52320-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="52320-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="52320-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="52320-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="52320-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="52320-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="52320-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="52320-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="52320-122"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="52320-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="52320-123">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="52320-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="52320-124"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="52320-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="52320-125">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="52320-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="52320-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="52320-126">Requirements</span></span>



| <span data-ttu-id="52320-127">需求</span><span class="sxs-lookup"><span data-stu-id="52320-127">Requirement</span></span> | <span data-ttu-id="52320-128">值</span><span class="sxs-lookup"><span data-stu-id="52320-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="52320-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52320-129">Minimum supported client</span></span><br/> | <span data-ttu-id="52320-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52320-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52320-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52320-131">Minimum supported server</span></span><br/> | <span data-ttu-id="52320-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="52320-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="52320-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="52320-133">End of client support</span></span><br/>    | <span data-ttu-id="52320-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52320-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="52320-135">產品</span><span class="sxs-lookup"><span data-stu-id="52320-135">Product</span></span><br/>                  | <span data-ttu-id="52320-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="52320-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="52320-137">標頭</span><span class="sxs-lookup"><span data-stu-id="52320-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="52320-138"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="52320-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="52320-139">IID</span><span class="sxs-lookup"><span data-stu-id="52320-139">IID</span></span><br/>                      | <span data-ttu-id="52320-140">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="52320-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="52320-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52320-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52320-142">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="52320-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

