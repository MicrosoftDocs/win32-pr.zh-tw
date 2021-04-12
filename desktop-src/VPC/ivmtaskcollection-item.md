---
title: 'IVMTaskCollection 專案屬性 (VPCCOMInterfaces .h) '
description: 抓取對應至指定之索引的工作物件。
ms.assetid: e4738b7a-12d6-4aed-992d-2f70c5cdd4d0
keywords:
- 專案屬性 Virtual PC
- 專案屬性 Virtual PC，IVMTaskCollection 介面
- IVMTaskCollection 介面 Virtual PC，Item 屬性
topic_type:
- apiref
api_name:
- IVMTaskCollection.Item
- IVMTaskCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f445280834383ee594fbb53a3390c91b1928f4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508980"
---
# <a name="ivmtaskcollectionitem-property"></a><span data-ttu-id="3bb35-106">IVMTaskCollection：： Item 屬性</span><span class="sxs-lookup"><span data-stu-id="3bb35-106">IVMTaskCollection::Item property</span></span>

<span data-ttu-id="3bb35-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="3bb35-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3bb35-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="3bb35-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3bb35-109">抓取對應至指定之索引的工作物件。</span><span class="sxs-lookup"><span data-stu-id="3bb35-109">Retrieves the task object that corresponds to the specified index.</span></span>

<span data-ttu-id="3bb35-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="3bb35-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bb35-111">語法</span><span class="sxs-lookup"><span data-stu-id="3bb35-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long    index,
  [out, retval] IVMTask **task
);
```



## <a name="property-value"></a><span data-ttu-id="3bb35-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="3bb35-112">Property value</span></span>

<span data-ttu-id="3bb35-113">[**IVMTask**](ivmtask.md)物件。</span><span class="sxs-lookup"><span data-stu-id="3bb35-113">The [**IVMTask**](ivmtask.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3bb35-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3bb35-114">Error codes</span></span>



| <span data-ttu-id="3bb35-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="3bb35-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3bb35-116">意義</span><span class="sxs-lookup"><span data-stu-id="3bb35-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3bb35-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3bb35-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3bb35-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="3bb35-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="3bb35-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3bb35-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3bb35-120">*Task* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3bb35-120">The *task* parameter is **NULL**.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="3bb35-121"><dt>會 \_E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="3bb35-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="3bb35-122">要求專案的索引未對應到此集合中的專案。</span><span class="sxs-lookup"><span data-stu-id="3bb35-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="3bb35-123"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3bb35-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3bb35-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3bb35-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="3bb35-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bb35-125">Requirements</span></span>



| <span data-ttu-id="3bb35-126">需求</span><span class="sxs-lookup"><span data-stu-id="3bb35-126">Requirement</span></span> | <span data-ttu-id="3bb35-127">值</span><span class="sxs-lookup"><span data-stu-id="3bb35-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb35-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3bb35-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3bb35-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3bb35-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3bb35-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3bb35-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3bb35-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="3bb35-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3bb35-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="3bb35-132">End of client support</span></span><br/>    | <span data-ttu-id="3bb35-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3bb35-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3bb35-134">產品</span><span class="sxs-lookup"><span data-stu-id="3bb35-134">Product</span></span><br/>                  | <span data-ttu-id="3bb35-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3bb35-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3bb35-136">標頭</span><span class="sxs-lookup"><span data-stu-id="3bb35-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bb35-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="3bb35-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3bb35-138">IID</span><span class="sxs-lookup"><span data-stu-id="3bb35-138">IID</span></span><br/>                      | <span data-ttu-id="3bb35-139">IID \_ IVMTaskCollection 定義為5c4387c8-0e8b-4b97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="3bb35-139">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="3bb35-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bb35-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bb35-141">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="3bb35-141">**IVMTask**</span></span>](ivmtask.md)
</dt> <dt>

[<span data-ttu-id="3bb35-142">**IVMTaskCollection**</span><span class="sxs-lookup"><span data-stu-id="3bb35-142">**IVMTaskCollection**</span></span>](ivmtaskcollection.md)
</dt> </dl>

 

