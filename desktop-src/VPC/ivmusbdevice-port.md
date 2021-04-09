---
title: 'IVMUSBDevice Port 屬性 (VPCCOMInterfaces .h) '
description: 抓取裝置所連接之埠的識別碼。
ms.assetid: 612c0eba-aa80-4539-a883-f05d32d13b41
keywords:
- 埠屬性 Virtual PC
- 埠屬性 Virtual PC，IVMUSBDevice 介面
- IVMUSBDevice 介面 Virtual PC，Port 屬性
topic_type:
- apiref
api_name:
- IVMUSBDevice.Port
- IVMUSBDevice.get_Port
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb821921d10b23fdb17256372708650d060e253b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686342"
---
# <a name="ivmusbdeviceport-property"></a><span data-ttu-id="147e4-106">IVMUSBDevice：:P 從排序 o 屬性</span><span class="sxs-lookup"><span data-stu-id="147e4-106">IVMUSBDevice::Port property</span></span>

<span data-ttu-id="147e4-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="147e4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="147e4-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="147e4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="147e4-109">抓取裝置所連接之埠的識別碼。</span><span class="sxs-lookup"><span data-stu-id="147e4-109">Retrieves the identifier of the port on which the device is connected.</span></span>

<span data-ttu-id="147e4-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="147e4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="147e4-111">語法</span><span class="sxs-lookup"><span data-stu-id="147e4-111">Syntax</span></span>


```C++
HRESULT get_Port(
  [out, retval] long *port
);
```



## <a name="property-value"></a><span data-ttu-id="147e4-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="147e4-112">Property value</span></span>

<span data-ttu-id="147e4-113">埠識別碼。</span><span class="sxs-lookup"><span data-stu-id="147e4-113">The port identifier.</span></span> <span data-ttu-id="147e4-114">此值是由 USB 連接器驅動程式所指派。</span><span class="sxs-lookup"><span data-stu-id="147e4-114">This value is assigned by the USB connector driver.</span></span>

## <a name="error-codes"></a><span data-ttu-id="147e4-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="147e4-115">Error codes</span></span>



| <span data-ttu-id="147e4-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="147e4-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="147e4-117">意義</span><span class="sxs-lookup"><span data-stu-id="147e4-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="147e4-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="147e4-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="147e4-119">已成功完成命令。</span><span class="sxs-lookup"><span data-stu-id="147e4-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="147e4-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="147e4-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="147e4-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="147e4-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="147e4-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="147e4-122">Requirements</span></span>



| <span data-ttu-id="147e4-123">需求</span><span class="sxs-lookup"><span data-stu-id="147e4-123">Requirement</span></span> | <span data-ttu-id="147e4-124">值</span><span class="sxs-lookup"><span data-stu-id="147e4-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="147e4-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="147e4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="147e4-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="147e4-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="147e4-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="147e4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="147e4-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="147e4-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="147e4-129">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="147e4-129">End of client support</span></span><br/>    | <span data-ttu-id="147e4-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="147e4-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="147e4-131">產品</span><span class="sxs-lookup"><span data-stu-id="147e4-131">Product</span></span><br/>                  | <span data-ttu-id="147e4-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="147e4-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="147e4-133">標頭</span><span class="sxs-lookup"><span data-stu-id="147e4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="147e4-134"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="147e4-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="147e4-135">IID</span><span class="sxs-lookup"><span data-stu-id="147e4-135">IID</span></span><br/>                      | <span data-ttu-id="147e4-136">IID \_ IVMUSBDevice 定義為 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="147e4-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="147e4-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="147e4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="147e4-138">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="147e4-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

