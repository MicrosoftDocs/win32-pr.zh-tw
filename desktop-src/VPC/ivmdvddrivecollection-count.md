---
title: 'IVMDVDDriveCollection Count 屬性 (VPCCOMInterfaces .h) '
description: 抓取此集合中的 CD 和 DVD 光碟機數目。
ms.assetid: 22e39c42-1f98-4680-a97e-0d329dc608e2
keywords:
- Count 屬性 Virtual PC
- Count 屬性 Virtual PC，IVMDVDDriveCollection 介面
- IVMDVDDriveCollection 介面 Virtual PC、Count 屬性
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Count
- IVMDVDDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9ea713810348c0bd78c7de307600fc6ac9adc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969983"
---
# <a name="ivmdvddrivecollectioncount-property"></a><span data-ttu-id="cee33-106">IVMDVDDriveCollection：： Count 屬性</span><span class="sxs-lookup"><span data-stu-id="cee33-106">IVMDVDDriveCollection::Count property</span></span>

<span data-ttu-id="cee33-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="cee33-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cee33-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="cee33-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cee33-109">抓取此集合中的 CD 和 DVD 光碟機數目。</span><span class="sxs-lookup"><span data-stu-id="cee33-109">Retrieves the number of CD and DVD drives in this collection.</span></span>

<span data-ttu-id="cee33-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="cee33-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cee33-111">語法</span><span class="sxs-lookup"><span data-stu-id="cee33-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="cee33-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="cee33-112">Property value</span></span>

<span data-ttu-id="cee33-113">CD 與 DVD 光碟機的數目。</span><span class="sxs-lookup"><span data-stu-id="cee33-113">The number of CD and DVD drives.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cee33-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="cee33-114">Error codes</span></span>



| <span data-ttu-id="cee33-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="cee33-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="cee33-116">意義</span><span class="sxs-lookup"><span data-stu-id="cee33-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="cee33-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cee33-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="cee33-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="cee33-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="cee33-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="cee33-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="cee33-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="cee33-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="cee33-121"><dt>E \_FAIL</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="cee33-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="cee33-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cee33-122">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="cee33-123"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="cee33-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="cee33-124">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="cee33-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="cee33-125"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cee33-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="cee33-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cee33-126">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cee33-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="cee33-127">Requirements</span></span>



| <span data-ttu-id="cee33-128">需求</span><span class="sxs-lookup"><span data-stu-id="cee33-128">Requirement</span></span> | <span data-ttu-id="cee33-129">值</span><span class="sxs-lookup"><span data-stu-id="cee33-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cee33-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cee33-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cee33-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cee33-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cee33-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cee33-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cee33-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="cee33-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cee33-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="cee33-134">End of client support</span></span><br/>    | <span data-ttu-id="cee33-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cee33-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cee33-136">產品</span><span class="sxs-lookup"><span data-stu-id="cee33-136">Product</span></span><br/>                  | <span data-ttu-id="cee33-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cee33-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cee33-138">標頭</span><span class="sxs-lookup"><span data-stu-id="cee33-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="cee33-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="cee33-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cee33-140">IID</span><span class="sxs-lookup"><span data-stu-id="cee33-140">IID</span></span><br/>                      | <span data-ttu-id="cee33-141">IID \_ IVMDVDDriveCollection 定義為 bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="cee33-141">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="cee33-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cee33-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cee33-143">**IVMDVDDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="cee33-143">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

