---
title: 'IVMHardDiskConnectionCollection Count 屬性 (VPCCOMInterfaces .h) '
description: 抓取此集合中的硬碟連接數目。
ms.assetid: 913c1bb7-0237-4f11-9873-7b42a94004f8
keywords:
- Count 屬性 Virtual PC
- Count 屬性 Virtual PC，IVMHardDiskConnectionCollection 介面
- IVMHardDiskConnectionCollection 介面 Virtual PC、Count 屬性
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Count
- IVMHardDiskConnectionCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f34bbf4d07d7c5967ccfc38e16a743105de8e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685971"
---
# <a name="ivmharddiskconnectioncollectioncount-property"></a><span data-ttu-id="49a23-106">IVMHardDiskConnectionCollection：： Count 屬性</span><span class="sxs-lookup"><span data-stu-id="49a23-106">IVMHardDiskConnectionCollection::Count property</span></span>

<span data-ttu-id="49a23-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="49a23-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="49a23-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="49a23-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="49a23-109">抓取此集合中的硬碟連接數目。</span><span class="sxs-lookup"><span data-stu-id="49a23-109">Retrieves the number of hard disk connections in this collection.</span></span>

<span data-ttu-id="49a23-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="49a23-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="49a23-111">語法</span><span class="sxs-lookup"><span data-stu-id="49a23-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="49a23-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="49a23-112">Property value</span></span>

<span data-ttu-id="49a23-113">硬碟連接的數目。</span><span class="sxs-lookup"><span data-stu-id="49a23-113">The number of hard disk connections.</span></span>

## <a name="error-codes"></a><span data-ttu-id="49a23-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="49a23-114">Error codes</span></span>



| <span data-ttu-id="49a23-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="49a23-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="49a23-116">意義</span><span class="sxs-lookup"><span data-stu-id="49a23-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="49a23-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="49a23-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="49a23-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="49a23-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="49a23-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="49a23-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="49a23-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="49a23-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="49a23-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="49a23-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="49a23-122">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="49a23-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="49a23-123"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="49a23-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="49a23-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="49a23-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="49a23-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="49a23-125">Requirements</span></span>



| <span data-ttu-id="49a23-126">需求</span><span class="sxs-lookup"><span data-stu-id="49a23-126">Requirement</span></span> | <span data-ttu-id="49a23-127">值</span><span class="sxs-lookup"><span data-stu-id="49a23-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49a23-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49a23-128">Minimum supported client</span></span><br/> | <span data-ttu-id="49a23-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49a23-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="49a23-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49a23-130">Minimum supported server</span></span><br/> | <span data-ttu-id="49a23-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="49a23-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="49a23-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="49a23-132">End of client support</span></span><br/>    | <span data-ttu-id="49a23-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="49a23-133">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="49a23-134">產品</span><span class="sxs-lookup"><span data-stu-id="49a23-134">Product</span></span><br/>                  | <span data-ttu-id="49a23-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="49a23-135">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="49a23-136">標頭</span><span class="sxs-lookup"><span data-stu-id="49a23-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="49a23-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="49a23-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="49a23-138">IID</span><span class="sxs-lookup"><span data-stu-id="49a23-138">IID</span></span><br/>                      | <span data-ttu-id="49a23-139">IID \_ IVMHardDiskconnectionCollection 定義為 b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="49a23-139">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49a23-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49a23-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49a23-141">**IVMHardDiskConnectionCollection**</span><span class="sxs-lookup"><span data-stu-id="49a23-141">**IVMHardDiskConnectionCollection**</span></span>](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

