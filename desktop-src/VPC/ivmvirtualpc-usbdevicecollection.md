---
title: 'IVMVirtualPC USBDeviceCollection 屬性 (VPCCOMInterfaces .h) '
description: 所有連接至主機之 USB 裝置的可列舉集合。
ms.assetid: 80844912-15b1-44d1-8d07-dca90c579927
keywords:
- USBDeviceCollection 屬性 Virtual PC
- USBDeviceCollection 屬性 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，USBDeviceCollection 屬性
topic_type:
- apiref
api_name:
- IVMVirtualPC.USBDeviceCollection
- IVMVirtualPC.get_USBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0428862cdd53ef6e657624d5dbd3e15c2445042f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686042"
---
# <a name="ivmvirtualpcusbdevicecollection-property"></a><span data-ttu-id="ff4e9-106">IVMVirtualPC：： USBDeviceCollection 屬性</span><span class="sxs-lookup"><span data-stu-id="ff4e9-106">IVMVirtualPC::USBDeviceCollection property</span></span>

<span data-ttu-id="ff4e9-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="ff4e9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ff4e9-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="ff4e9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ff4e9-109">抓取所有連接至主機之 USB 裝置的可列舉集合。</span><span class="sxs-lookup"><span data-stu-id="ff4e9-109">Retrieves an enumerable collection of all USB devices connected to the host.</span></span>

<span data-ttu-id="ff4e9-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ff4e9-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff4e9-111">語法</span><span class="sxs-lookup"><span data-stu-id="ff4e9-111">Syntax</span></span>


```C++
HRESULT get_USBDeviceCollection(
  [out, retval] IVMUSBDeviceCollection **usbDeviceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="ff4e9-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="ff4e9-112">Property value</span></span>

<span data-ttu-id="ff4e9-113">[**IVMUSBDeviceCollection**](ivmusbdevicecollection.md)指標的參考，代表 [**IVMUSBDevice**](ivmusbdevice.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="ff4e9-113">A reference to an [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md) pointer that represents a collection of [**IVMUSBDevice**](ivmusbdevice.md) objects.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ff4e9-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ff4e9-114">Error codes</span></span>



| <span data-ttu-id="ff4e9-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="ff4e9-115">Name/value</span></span>                                                                                                                                                                                | <span data-ttu-id="ff4e9-116">意義</span><span class="sxs-lookup"><span data-stu-id="ff4e9-116">Meaning</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff4e9-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ff4e9-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                   | <span data-ttu-id="ff4e9-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="ff4e9-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ff4e9-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ff4e9-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                     | <span data-ttu-id="ff4e9-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ff4e9-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="ff4e9-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ff4e9-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                             | <span data-ttu-id="ff4e9-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ff4e9-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="ff4e9-123"><dt>VM \_E \_ USB \_ 列舉 \_ 失敗 \_ 的 \_ 裝置更多</dt> <dt>0xA0040930</dt></span><span class="sxs-lookup"><span data-stu-id="ff4e9-123"><dt>VM\_E\_USB\_ENUMERATION\_FAILED\_MORE\_DEVICES</dt> <dt>0xA0040930</dt></span></span> </dl> | <span data-ttu-id="ff4e9-124">有16個以上的 USB 裝置連接到主機。</span><span class="sxs-lookup"><span data-stu-id="ff4e9-124">More than 16 USB devices are connected to the host.</span></span><br/>                                  |
| <dl> <span data-ttu-id="ff4e9-125"><dt>VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="ff4e9-125"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>      | <span data-ttu-id="ff4e9-126">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="ff4e9-126">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ff4e9-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff4e9-127">Requirements</span></span>



| <span data-ttu-id="ff4e9-128">需求</span><span class="sxs-lookup"><span data-stu-id="ff4e9-128">Requirement</span></span> | <span data-ttu-id="ff4e9-129">值</span><span class="sxs-lookup"><span data-stu-id="ff4e9-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff4e9-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff4e9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ff4e9-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff4e9-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ff4e9-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff4e9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ff4e9-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="ff4e9-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ff4e9-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ff4e9-134">End of client support</span></span><br/>    | <span data-ttu-id="ff4e9-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ff4e9-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ff4e9-136">產品</span><span class="sxs-lookup"><span data-stu-id="ff4e9-136">Product</span></span><br/>                  | <span data-ttu-id="ff4e9-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ff4e9-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ff4e9-138">標頭</span><span class="sxs-lookup"><span data-stu-id="ff4e9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff4e9-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff4e9-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ff4e9-140">IID</span><span class="sxs-lookup"><span data-stu-id="ff4e9-140">IID</span></span><br/>                      | <span data-ttu-id="ff4e9-141">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="ff4e9-141">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ff4e9-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff4e9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff4e9-143">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="ff4e9-143">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

