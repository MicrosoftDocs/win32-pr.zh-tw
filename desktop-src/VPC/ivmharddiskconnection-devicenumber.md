---
title: 'IVMHardDiskConnection DeviceNumber 屬性 (VPCCOMInterfaces .h) '
description: 抓取磁片磁碟機映射所連接的裝置編號。
ms.assetid: fea8bac6-fb25-495a-bc56-1d517b831f33
keywords:
- DeviceNumber 屬性 Virtual PC
- DeviceNumber 屬性 Virtual PC，IVMHardDiskConnection 介面
- IVMHardDiskConnection 介面 Virtual PC，DeviceNumber 屬性
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.DeviceNumber
- IVMHardDiskConnection.get_DeviceNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b69f7d9d3f9a373c9b8086857af56c7e5da9f5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105809"
---
# <a name="ivmharddiskconnectiondevicenumber-property"></a><span data-ttu-id="faf95-106">IVMHardDiskConnection：:D eviceNumber 屬性</span><span class="sxs-lookup"><span data-stu-id="faf95-106">IVMHardDiskConnection::DeviceNumber property</span></span>

<span data-ttu-id="faf95-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="faf95-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="faf95-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="faf95-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="faf95-109">抓取磁片磁碟機映射所連接的裝置編號。</span><span class="sxs-lookup"><span data-stu-id="faf95-109">Retrieves the device number to which the drive image is attached.</span></span>

<span data-ttu-id="faf95-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="faf95-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="faf95-111">語法</span><span class="sxs-lookup"><span data-stu-id="faf95-111">Syntax</span></span>


```C++
HRESULT get_DeviceNumber(
  [out, retval] long *vmDeviceNumber
);
```



## <a name="property-value"></a><span data-ttu-id="faf95-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="faf95-112">Property value</span></span>

<span data-ttu-id="faf95-113">與此連接對應的裝置編號。</span><span class="sxs-lookup"><span data-stu-id="faf95-113">The device number that corresponds with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="faf95-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="faf95-114">Error codes</span></span>



| <span data-ttu-id="faf95-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="faf95-115">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="faf95-116">意義</span><span class="sxs-lookup"><span data-stu-id="faf95-116">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="faf95-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="faf95-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="faf95-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="faf95-118">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="faf95-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="faf95-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="faf95-120">參數為 **Null** 或無效。</span><span class="sxs-lookup"><span data-stu-id="faf95-120">The parameter is **NULL** or not valid.</span></span><br/>                                 |
| <dl> <span data-ttu-id="faf95-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="faf95-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="faf95-122">目前的虛擬機器設定無效。</span><span class="sxs-lookup"><span data-stu-id="faf95-122">The current virtual machine configuration is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="faf95-123"><dt>VM \_E \_ 磁片磁碟機 \_ 無效</dt>的 <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="faf95-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="faf95-124">此連接的匯流排位置未正確初始化。</span><span class="sxs-lookup"><span data-stu-id="faf95-124">The bus location for this connection has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="faf95-125"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="faf95-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="faf95-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="faf95-126">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="faf95-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="faf95-127">Requirements</span></span>



| <span data-ttu-id="faf95-128">需求</span><span class="sxs-lookup"><span data-stu-id="faf95-128">Requirement</span></span> | <span data-ttu-id="faf95-129">值</span><span class="sxs-lookup"><span data-stu-id="faf95-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="faf95-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="faf95-130">Minimum supported client</span></span><br/> | <span data-ttu-id="faf95-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="faf95-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="faf95-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="faf95-132">Minimum supported server</span></span><br/> | <span data-ttu-id="faf95-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="faf95-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="faf95-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="faf95-134">End of client support</span></span><br/>    | <span data-ttu-id="faf95-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="faf95-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="faf95-136">產品</span><span class="sxs-lookup"><span data-stu-id="faf95-136">Product</span></span><br/>                  | <span data-ttu-id="faf95-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="faf95-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="faf95-138">標頭</span><span class="sxs-lookup"><span data-stu-id="faf95-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="faf95-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="faf95-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="faf95-140">IID</span><span class="sxs-lookup"><span data-stu-id="faf95-140">IID</span></span><br/>                      | <span data-ttu-id="faf95-141">IID \_ IVMHardDiskconnection 定義為 aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="faf95-141">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="faf95-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="faf95-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf95-143">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="faf95-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

