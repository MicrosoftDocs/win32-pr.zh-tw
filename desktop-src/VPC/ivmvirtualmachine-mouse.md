---
title: 'IVMVirtualMachine 滑鼠屬性 (VPCCOMInterfaces .h) '
description: 抓取虛擬機器的滑鼠裝置。
ms.assetid: 917bbcc1-615d-4fd7-87e1-62abf2ece539
keywords:
- 滑鼠屬性虛擬電腦
- 滑鼠屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，滑鼠屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Mouse
- IVMVirtualMachine.get_Mouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111d511f4e7948a83a968b154721bf81dbfe53b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996586"
---
# <a name="ivmvirtualmachinemouse-property"></a><span data-ttu-id="dbe05-106">IVMVirtualMachine：：滑鼠屬性</span><span class="sxs-lookup"><span data-stu-id="dbe05-106">IVMVirtualMachine::Mouse property</span></span>

<span data-ttu-id="dbe05-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="dbe05-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dbe05-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="dbe05-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dbe05-109">抓取虛擬機器的滑鼠裝置。</span><span class="sxs-lookup"><span data-stu-id="dbe05-109">Retrieves the mouse device for the virtual machine.</span></span>

<span data-ttu-id="dbe05-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="dbe05-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe05-111">語法</span><span class="sxs-lookup"><span data-stu-id="dbe05-111">Syntax</span></span>


```C++
HRESULT get_Mouse(
  [out, retval] IVMMouse **mouse
);
```



## <a name="property-value"></a><span data-ttu-id="dbe05-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="dbe05-112">Property value</span></span>

<span data-ttu-id="dbe05-113">[**IVMMouse**](ivmmouse.md)物件。</span><span class="sxs-lookup"><span data-stu-id="dbe05-113">An [**IVMMouse**](ivmmouse.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dbe05-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="dbe05-114">Error codes</span></span>



| <span data-ttu-id="dbe05-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="dbe05-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="dbe05-116">意義</span><span class="sxs-lookup"><span data-stu-id="dbe05-116">Meaning</span></span>                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="dbe05-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dbe05-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="dbe05-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="dbe05-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="dbe05-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="dbe05-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="dbe05-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="dbe05-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="dbe05-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="dbe05-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="dbe05-122">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="dbe05-122">The configuration is unknown.</span></span><br/>       |
| <dl> <span data-ttu-id="dbe05-123"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="dbe05-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="dbe05-124">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="dbe05-124">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="dbe05-125"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="dbe05-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="dbe05-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="dbe05-126">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="dbe05-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbe05-127">Requirements</span></span>



| <span data-ttu-id="dbe05-128">需求</span><span class="sxs-lookup"><span data-stu-id="dbe05-128">Requirement</span></span> | <span data-ttu-id="dbe05-129">值</span><span class="sxs-lookup"><span data-stu-id="dbe05-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe05-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dbe05-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dbe05-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbe05-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dbe05-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dbe05-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dbe05-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="dbe05-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dbe05-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="dbe05-134">End of client support</span></span><br/>    | <span data-ttu-id="dbe05-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dbe05-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dbe05-136">產品</span><span class="sxs-lookup"><span data-stu-id="dbe05-136">Product</span></span><br/>                  | <span data-ttu-id="dbe05-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dbe05-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dbe05-138">標頭</span><span class="sxs-lookup"><span data-stu-id="dbe05-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbe05-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="dbe05-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dbe05-140">IID</span><span class="sxs-lookup"><span data-stu-id="dbe05-140">IID</span></span><br/>                      | <span data-ttu-id="dbe05-141">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="dbe05-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="dbe05-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbe05-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe05-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="dbe05-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

