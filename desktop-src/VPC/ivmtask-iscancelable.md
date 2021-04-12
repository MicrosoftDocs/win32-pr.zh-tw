---
title: 'IVMTask 屬性屬性 (VPCCOMInterfaces .h) '
description: 決定是否可以取消工作。
ms.assetid: abb8a29a-7f5b-45ba-ae79-d422dfb2f39d
keywords:
- 屬性屬性 Virtual PC
- 屬性屬性 Virtual PC，IVMTask 介面
- IVMTask 介面 Virtual PC，屬性屬性
topic_type:
- apiref
api_name:
- IVMTask.IsCancelable
- IVMTask.get_IsCancelable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcd06db3fc338277d7551233b0d609ceae03f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105666"
---
# <a name="ivmtaskiscancelable-property"></a><span data-ttu-id="2985b-106">IVMTask：：屬性屬性</span><span class="sxs-lookup"><span data-stu-id="2985b-106">IVMTask::IsCancelable property</span></span>

<span data-ttu-id="2985b-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="2985b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2985b-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="2985b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2985b-109">決定是否可以取消工作。</span><span class="sxs-lookup"><span data-stu-id="2985b-109">Determines whether the task can be canceled.</span></span>

<span data-ttu-id="2985b-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2985b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2985b-111">語法</span><span class="sxs-lookup"><span data-stu-id="2985b-111">Syntax</span></span>


```C++
HRESULT get_IsCancelable(
  [out, retval] VARIANT_BOOL *isCancelable
);
```



## <a name="property-value"></a><span data-ttu-id="2985b-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="2985b-112">Property value</span></span>

<span data-ttu-id="2985b-113">如果工作可以在完成前取消，則 **為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="2985b-113">**TRUE** if the task can be canceled before completion and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2985b-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2985b-114">Error codes</span></span>



| <span data-ttu-id="2985b-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="2985b-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="2985b-116">意義</span><span class="sxs-lookup"><span data-stu-id="2985b-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2985b-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2985b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2985b-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="2985b-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="2985b-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2985b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2985b-120">參數值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2985b-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="2985b-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2985b-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2985b-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2985b-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2985b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2985b-123">Requirements</span></span>



| <span data-ttu-id="2985b-124">需求</span><span class="sxs-lookup"><span data-stu-id="2985b-124">Requirement</span></span> | <span data-ttu-id="2985b-125">值</span><span class="sxs-lookup"><span data-stu-id="2985b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2985b-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2985b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2985b-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2985b-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2985b-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2985b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2985b-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="2985b-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2985b-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2985b-130">End of client support</span></span><br/>    | <span data-ttu-id="2985b-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2985b-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2985b-132">產品</span><span class="sxs-lookup"><span data-stu-id="2985b-132">Product</span></span><br/>                  | <span data-ttu-id="2985b-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2985b-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2985b-134">標頭</span><span class="sxs-lookup"><span data-stu-id="2985b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2985b-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="2985b-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2985b-136">IID</span><span class="sxs-lookup"><span data-stu-id="2985b-136">IID</span></span><br/>                      | <span data-ttu-id="2985b-137">IID \_ IVMTask 定義為 ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="2985b-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="2985b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2985b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2985b-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="2985b-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

