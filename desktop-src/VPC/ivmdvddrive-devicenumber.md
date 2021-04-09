---
title: 'IVMDVDDrive DeviceNumber 屬性 (VPCCOMInterfaces .h) '
description: 抓取此磁片磁碟機所連接的裝置編號。
ms.assetid: 57b09400-e0c8-4ca2-bcd4-e6dd047daf95
keywords:
- DeviceNumber 屬性 Virtual PC
- DeviceNumber 屬性 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，DeviceNumber 屬性
topic_type:
- apiref
api_name:
- IVMDVDDrive.DeviceNumber
- IVMDVDDrive.get_DeviceNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de189b162ed2c880819f4c8729e996236ace250a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025233"
---
# <a name="ivmdvddrivedevicenumber-property"></a><span data-ttu-id="0c9dd-106">IVMDVDDrive：:D eviceNumber 屬性</span><span class="sxs-lookup"><span data-stu-id="0c9dd-106">IVMDVDDrive::DeviceNumber property</span></span>

<span data-ttu-id="0c9dd-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="0c9dd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0c9dd-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="0c9dd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0c9dd-109">抓取此磁片磁碟機所連接的裝置編號。</span><span class="sxs-lookup"><span data-stu-id="0c9dd-109">Retrieves the device number to which this drive is attached.</span></span>

<span data-ttu-id="0c9dd-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="0c9dd-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c9dd-111">語法</span><span class="sxs-lookup"><span data-stu-id="0c9dd-111">Syntax</span></span>


```C++
HRESULT get_DeviceNumber(
  [out, retval] long *vmDeviceNumber
);
```



## <a name="property-value"></a><span data-ttu-id="0c9dd-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="0c9dd-112">Property value</span></span>

<span data-ttu-id="0c9dd-113">裝置編號。</span><span class="sxs-lookup"><span data-stu-id="0c9dd-113">The device number.</span></span> <span data-ttu-id="0c9dd-114">例如，在 IDE 匯流排上，此值會代表主要或次要位置。</span><span class="sxs-lookup"><span data-stu-id="0c9dd-114">For example, on an IDE bus, this value would represent either the primary or secondary location.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0c9dd-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0c9dd-115">Error codes</span></span>



| <span data-ttu-id="0c9dd-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="0c9dd-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="0c9dd-117">意義</span><span class="sxs-lookup"><span data-stu-id="0c9dd-117">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0c9dd-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0c9dd-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="0c9dd-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="0c9dd-119">The operation was successful.</span></span><br/>                                          |
| <dl> <span data-ttu-id="0c9dd-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0c9dd-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="0c9dd-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0c9dd-121">The parameter is **NULL**.</span></span><br/>                                             |
| <dl> <span data-ttu-id="0c9dd-122"><dt>VM \_E \_ 磁片磁碟機 \_ 無效</dt>的 <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="0c9dd-122"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="0c9dd-123">此 DVD 光碟機的匯流排位置未正確初始化。</span><span class="sxs-lookup"><span data-stu-id="0c9dd-123">The bus location for this DVD drive has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="0c9dd-124"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0c9dd-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="0c9dd-125">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0c9dd-125">An unexpected error has occurred.</span></span><br/>                                      |



## <a name="requirements"></a><span data-ttu-id="0c9dd-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c9dd-126">Requirements</span></span>



| <span data-ttu-id="0c9dd-127">需求</span><span class="sxs-lookup"><span data-stu-id="0c9dd-127">Requirement</span></span> | <span data-ttu-id="0c9dd-128">值</span><span class="sxs-lookup"><span data-stu-id="0c9dd-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c9dd-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c9dd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0c9dd-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c9dd-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c9dd-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c9dd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0c9dd-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="0c9dd-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0c9dd-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0c9dd-133">End of client support</span></span><br/>    | <span data-ttu-id="0c9dd-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c9dd-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0c9dd-135">產品</span><span class="sxs-lookup"><span data-stu-id="0c9dd-135">Product</span></span><br/>                  | <span data-ttu-id="0c9dd-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0c9dd-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0c9dd-137">標頭</span><span class="sxs-lookup"><span data-stu-id="0c9dd-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c9dd-138"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="0c9dd-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0c9dd-139">IID</span><span class="sxs-lookup"><span data-stu-id="0c9dd-139">IID</span></span><br/>                      | <span data-ttu-id="0c9dd-140">IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="0c9dd-140">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="0c9dd-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c9dd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c9dd-142">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="0c9dd-142">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

