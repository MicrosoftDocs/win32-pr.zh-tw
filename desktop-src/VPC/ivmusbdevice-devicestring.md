---
title: 'IVMUSBDevice DeviceString 屬性 (VPCCOMInterfaces .h) '
description: 抓取 USB 裝置的名稱。
ms.assetid: 2ae82e2a-b33a-4039-acdb-958b094b1045
keywords:
- DeviceString 屬性 Virtual PC
- DeviceString 屬性 Virtual PC，IVMUSBDevice 介面
- IVMUSBDevice 介面 Virtual PC，DeviceString 屬性
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceString
- IVMUSBDevice.get_DeviceString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ed76f55f5b1218db70991f5917edf6d5b7b655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843688"
---
# <a name="ivmusbdevicedevicestring-property"></a><span data-ttu-id="2d3a6-106">IVMUSBDevice：:D eviceString 屬性</span><span class="sxs-lookup"><span data-stu-id="2d3a6-106">IVMUSBDevice::DeviceString property</span></span>

<span data-ttu-id="2d3a6-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="2d3a6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2d3a6-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="2d3a6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2d3a6-109">抓取 USB 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d3a6-109">Retrieves the name of the USB device.</span></span>

<span data-ttu-id="2d3a6-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2d3a6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d3a6-111">語法</span><span class="sxs-lookup"><span data-stu-id="2d3a6-111">Syntax</span></span>


```C++
HRESULT get_DeviceString(
  [out, retval] BSTR *deviceName
);
```



## <a name="property-value"></a><span data-ttu-id="2d3a6-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="2d3a6-112">Property value</span></span>

<span data-ttu-id="2d3a6-113">USB 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d3a6-113">The name of the USB device.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2d3a6-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2d3a6-114">Error codes</span></span>



| <span data-ttu-id="2d3a6-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="2d3a6-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="2d3a6-116">意義</span><span class="sxs-lookup"><span data-stu-id="2d3a6-116">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="2d3a6-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2d3a6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="2d3a6-118">已成功完成命令。</span><span class="sxs-lookup"><span data-stu-id="2d3a6-118">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="2d3a6-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2d3a6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="2d3a6-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2d3a6-120">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="2d3a6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d3a6-121">Requirements</span></span>



| <span data-ttu-id="2d3a6-122">需求</span><span class="sxs-lookup"><span data-stu-id="2d3a6-122">Requirement</span></span> | <span data-ttu-id="2d3a6-123">值</span><span class="sxs-lookup"><span data-stu-id="2d3a6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d3a6-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d3a6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2d3a6-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d3a6-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2d3a6-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d3a6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2d3a6-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="2d3a6-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2d3a6-128">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2d3a6-128">End of client support</span></span><br/>    | <span data-ttu-id="2d3a6-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2d3a6-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2d3a6-130">產品</span><span class="sxs-lookup"><span data-stu-id="2d3a6-130">Product</span></span><br/>                  | <span data-ttu-id="2d3a6-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2d3a6-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2d3a6-132">標頭</span><span class="sxs-lookup"><span data-stu-id="2d3a6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d3a6-133"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d3a6-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2d3a6-134">IID</span><span class="sxs-lookup"><span data-stu-id="2d3a6-134">IID</span></span><br/>                      | <span data-ttu-id="2d3a6-135">IID \_ IVMUSBDevice 定義為 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="2d3a6-135">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2d3a6-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d3a6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d3a6-137">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-137">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

