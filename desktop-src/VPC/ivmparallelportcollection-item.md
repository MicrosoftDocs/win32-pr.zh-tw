---
title: 'IVMParallelPortCollection 專案屬性 (VPCCOMInterfaces .h) '
description: 抓取對應至指定之索引的平行埠物件。
ms.assetid: f67a4224-ca96-4d68-9f0f-4977ffff859e
keywords:
- 專案屬性 Virtual PC
- 專案屬性 Virtual PC，IVMParallelPortCollection 介面
- IVMParallelPortCollection 介面 Virtual PC，Item 屬性
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Item
- IVMParallelPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa450f1859db8af6ed884b37fc693fc4fb1990f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466625"
---
# <a name="ivmparallelportcollectionitem-property"></a><span data-ttu-id="358ac-106">IVMParallelPortCollection：： Item 屬性</span><span class="sxs-lookup"><span data-stu-id="358ac-106">IVMParallelPortCollection::Item property</span></span>

<span data-ttu-id="358ac-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="358ac-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="358ac-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="358ac-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="358ac-109">抓取對應至指定之索引的平行埠物件。</span><span class="sxs-lookup"><span data-stu-id="358ac-109">Retrieves the parallel port object that corresponds to the specified index.</span></span>

<span data-ttu-id="358ac-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="358ac-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="358ac-111">語法</span><span class="sxs-lookup"><span data-stu-id="358ac-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long            index,
  [out, retval] IVMParallelPort **vmParallelPort
);
```



## <a name="property-value"></a><span data-ttu-id="358ac-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="358ac-112">Property value</span></span>

<span data-ttu-id="358ac-113">[**IVMParallelPort**](ivmparallelport.md)物件。</span><span class="sxs-lookup"><span data-stu-id="358ac-113">The [**IVMParallelPort**](ivmparallelport.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="358ac-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="358ac-114">Error codes</span></span>



| <span data-ttu-id="358ac-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="358ac-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="358ac-116">意義</span><span class="sxs-lookup"><span data-stu-id="358ac-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="358ac-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="358ac-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="358ac-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="358ac-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="358ac-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="358ac-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="358ac-120">*VmParallelPort* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="358ac-120">The *vmParallelPort* parameter is **NULL**.</span></span> <br/>                                        |
| <dl> <span data-ttu-id="358ac-121"><dt>會 \_E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="358ac-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="358ac-122">要求專案的索引未對應到此集合中的專案。</span><span class="sxs-lookup"><span data-stu-id="358ac-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="358ac-123"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="358ac-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="358ac-124">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="358ac-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="358ac-125"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="358ac-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="358ac-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="358ac-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="358ac-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="358ac-127">Requirements</span></span>



| <span data-ttu-id="358ac-128">需求</span><span class="sxs-lookup"><span data-stu-id="358ac-128">Requirement</span></span> | <span data-ttu-id="358ac-129">值</span><span class="sxs-lookup"><span data-stu-id="358ac-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="358ac-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="358ac-130">Minimum supported client</span></span><br/> | <span data-ttu-id="358ac-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="358ac-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="358ac-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="358ac-132">Minimum supported server</span></span><br/> | <span data-ttu-id="358ac-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="358ac-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="358ac-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="358ac-134">End of client support</span></span><br/>    | <span data-ttu-id="358ac-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="358ac-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="358ac-136">產品</span><span class="sxs-lookup"><span data-stu-id="358ac-136">Product</span></span><br/>                  | <span data-ttu-id="358ac-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="358ac-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="358ac-138">標頭</span><span class="sxs-lookup"><span data-stu-id="358ac-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="358ac-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="358ac-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="358ac-140">IID</span><span class="sxs-lookup"><span data-stu-id="358ac-140">IID</span></span><br/>                      | <span data-ttu-id="358ac-141">IID \_ IVMParallelPortCollection 定義為27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="358ac-141">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="358ac-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="358ac-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="358ac-143">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="358ac-143">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> <dt>

[<span data-ttu-id="358ac-144">**IVMParallelPortCollection**</span><span class="sxs-lookup"><span data-stu-id="358ac-144">**IVMParallelPortCollection**</span></span>](ivmparallelportcollection.md)
</dt> </dl>

 

