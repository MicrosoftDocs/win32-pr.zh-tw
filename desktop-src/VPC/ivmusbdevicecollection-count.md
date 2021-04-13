---
title: 'IVMUSBDeviceCollection Count 屬性 (VPCCOMInterfaces .h) '
description: 抓取此集合中的 USB 裝置數目。
ms.assetid: 8d17397b-4f4a-475d-99fe-4df0d74fe5a5
keywords:
- Count 屬性 Virtual PC
- Count 屬性 Virtual PC，IVMUSBDeviceCollection 介面
- IVMUSBDeviceCollection 介面 Virtual PC、Count 屬性
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Count
- IVMUSBDeviceCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a0c2146df70f0432a19d65daad44ba6f1ec372
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465529"
---
# <a name="ivmusbdevicecollectioncount-property"></a><span data-ttu-id="1c75b-106">IVMUSBDeviceCollection：： Count 屬性</span><span class="sxs-lookup"><span data-stu-id="1c75b-106">IVMUSBDeviceCollection::Count property</span></span>

<span data-ttu-id="1c75b-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="1c75b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1c75b-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="1c75b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1c75b-109">抓取此集合中的 USB 裝置數目。</span><span class="sxs-lookup"><span data-stu-id="1c75b-109">Retrieves the number of USB devices in this collection.</span></span>

<span data-ttu-id="1c75b-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="1c75b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c75b-111">語法</span><span class="sxs-lookup"><span data-stu-id="1c75b-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="1c75b-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="1c75b-112">Property value</span></span>

<span data-ttu-id="1c75b-113">USB 裝置的數目。</span><span class="sxs-lookup"><span data-stu-id="1c75b-113">The number of USB devices.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1c75b-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1c75b-114">Error codes</span></span>



| <span data-ttu-id="1c75b-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="1c75b-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="1c75b-116">意義</span><span class="sxs-lookup"><span data-stu-id="1c75b-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1c75b-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1c75b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="1c75b-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="1c75b-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="1c75b-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1c75b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="1c75b-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1c75b-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="1c75b-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1c75b-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="1c75b-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1c75b-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1c75b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c75b-123">Requirements</span></span>



| <span data-ttu-id="1c75b-124">需求</span><span class="sxs-lookup"><span data-stu-id="1c75b-124">Requirement</span></span> | <span data-ttu-id="1c75b-125">值</span><span class="sxs-lookup"><span data-stu-id="1c75b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c75b-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c75b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1c75b-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c75b-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1c75b-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c75b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1c75b-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="1c75b-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1c75b-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1c75b-130">End of client support</span></span><br/>    | <span data-ttu-id="1c75b-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c75b-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1c75b-132">產品</span><span class="sxs-lookup"><span data-stu-id="1c75b-132">Product</span></span><br/>                  | <span data-ttu-id="1c75b-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1c75b-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1c75b-134">標頭</span><span class="sxs-lookup"><span data-stu-id="1c75b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c75b-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="1c75b-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1c75b-136">IID</span><span class="sxs-lookup"><span data-stu-id="1c75b-136">IID</span></span><br/>                      | <span data-ttu-id="1c75b-137">IID \_ IVMUSBDeviceCollection 定義為4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="1c75b-137">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="1c75b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c75b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c75b-139">**IVMUSBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="1c75b-139">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

