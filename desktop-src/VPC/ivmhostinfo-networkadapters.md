---
title: 'IVMHostInfo NetworkAdapters 屬性 (VPCCOMInterfaces .h) '
description: 在主機電腦上抓取 Nic 的可列舉集合。
ms.assetid: 17393d7a-c883-4d67-826b-83b886c0d7a6
keywords:
- NetworkAdapters 屬性 Virtual PC
- NetworkAdapters 屬性 Virtual PC，IVMHostInfo 介面
- IVMHostInfo 介面 Virtual PC，NetworkAdapters 屬性
topic_type:
- apiref
api_name:
- IVMHostInfo.NetworkAdapters
- IVMHostInfo.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeff5c6d459fb8f6999f896c3c13fcd980bf70ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933881"
---
# <a name="ivmhostinfonetworkadapters-property"></a><span data-ttu-id="0f901-106">IVMHostInfo：： NetworkAdapters 屬性</span><span class="sxs-lookup"><span data-stu-id="0f901-106">IVMHostInfo::NetworkAdapters property</span></span>

<span data-ttu-id="0f901-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="0f901-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0f901-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="0f901-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0f901-109">在主機電腦上抓取 Nic 的可列舉集合。</span><span class="sxs-lookup"><span data-stu-id="0f901-109">Retrieves an enumerable collection of NICs in the host machine.</span></span>

<span data-ttu-id="0f901-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="0f901-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f901-111">語法</span><span class="sxs-lookup"><span data-stu-id="0f901-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] VARIANT *hostNICs
);
```



## <a name="property-value"></a><span data-ttu-id="0f901-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="0f901-112">Property value</span></span>

<span data-ttu-id="0f901-113">網路介面卡的集合。</span><span class="sxs-lookup"><span data-stu-id="0f901-113">A collection of network interface cards.</span></span> <span data-ttu-id="0f901-114">這是 **BSTR** 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="0f901-114">This is an array of **BSTR** values.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0f901-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0f901-115">Error codes</span></span>



| <span data-ttu-id="0f901-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="0f901-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="0f901-117">意義</span><span class="sxs-lookup"><span data-stu-id="0f901-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0f901-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0f901-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="0f901-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="0f901-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="0f901-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0f901-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="0f901-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0f901-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="0f901-122"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0f901-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="0f901-123">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0f901-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0f901-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f901-124">Requirements</span></span>



| <span data-ttu-id="0f901-125">需求</span><span class="sxs-lookup"><span data-stu-id="0f901-125">Requirement</span></span> | <span data-ttu-id="0f901-126">值</span><span class="sxs-lookup"><span data-stu-id="0f901-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f901-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f901-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0f901-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f901-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f901-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f901-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0f901-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="0f901-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0f901-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0f901-131">End of client support</span></span><br/>    | <span data-ttu-id="0f901-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0f901-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0f901-133">產品</span><span class="sxs-lookup"><span data-stu-id="0f901-133">Product</span></span><br/>                  | <span data-ttu-id="0f901-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0f901-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0f901-135">標頭</span><span class="sxs-lookup"><span data-stu-id="0f901-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f901-136"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="0f901-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0f901-137">IID</span><span class="sxs-lookup"><span data-stu-id="0f901-137">IID</span></span><br/>                      | <span data-ttu-id="0f901-138">IID \_ IVMHostInfo 定義為5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="0f901-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="0f901-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f901-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f901-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="0f901-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

