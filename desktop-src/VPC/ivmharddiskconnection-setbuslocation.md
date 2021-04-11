---
title: 'IVMHardDiskConnection SetBusLocation 方法 (VPCCOMInterfaces .h) '
description: 設定此硬碟所連接的匯流排位置。
ms.assetid: 0aa303ae-d8bf-4d38-94ab-bdbb4e744c7b
keywords:
- SetBusLocation 方法 Virtual PC
- SetBusLocation 方法 Virtual PC，IVMHardDiskConnection 介面
- IVMHardDiskConnection 介面 Virtual PC，SetBusLocation 方法
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61de0f595bc06d497e7f5913da9173ccb3bf1ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317111"
---
# <a name="ivmharddiskconnectionsetbuslocation-method"></a><span data-ttu-id="9e757-106">IVMHardDiskConnection：： SetBusLocation 方法</span><span class="sxs-lookup"><span data-stu-id="9e757-106">IVMHardDiskConnection::SetBusLocation method</span></span>

<span data-ttu-id="9e757-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="9e757-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9e757-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="9e757-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9e757-109">設定此硬碟所連接的匯流排位置。</span><span class="sxs-lookup"><span data-stu-id="9e757-109">Sets the bus location to which this hard disk is attached.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e757-110">語法</span><span class="sxs-lookup"><span data-stu-id="9e757-110">Syntax</span></span>


```C++
HRESULT SetBusLocation(
  [in] long vmBusNumber,
  [in] long vmDeviceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="9e757-111">參數</span><span class="sxs-lookup"><span data-stu-id="9e757-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e757-112">*vmBusNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9e757-112">*vmBusNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e757-113">要使用的匯流排編號。</span><span class="sxs-lookup"><span data-stu-id="9e757-113">The bus number to be used.</span></span>

</dd> <dt>

<span data-ttu-id="9e757-114">*vmDeviceNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9e757-114">*vmDeviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e757-115">要使用的裝置編號。</span><span class="sxs-lookup"><span data-stu-id="9e757-115">The device number to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e757-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e757-116">Return value</span></span>

<span data-ttu-id="9e757-117">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9e757-117">This method can return one of these values.</span></span>



| <span data-ttu-id="9e757-118">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="9e757-118">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="9e757-119">Description</span><span class="sxs-lookup"><span data-stu-id="9e757-119">Description</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9e757-120"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9e757-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                     | <span data-ttu-id="9e757-121">作業成功。</span><span class="sxs-lookup"><span data-stu-id="9e757-121">The operation was successful.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="9e757-122"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="9e757-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                    | <span data-ttu-id="9e757-123">指定的匯流排位置無效。</span><span class="sxs-lookup"><span data-stu-id="9e757-123">The bus location specified is not valid.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="9e757-124"><dt>**VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="9e757-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>    | <span data-ttu-id="9e757-125">因為虛擬機器處於執行中或已儲存狀態，所以無法設定匯流排位置。</span><span class="sxs-lookup"><span data-stu-id="9e757-125">The bus location could not be set because the virtual machine is in a running or saved state.</span></span><br/>    |
| <dl> <span data-ttu-id="9e757-126"><dt>**VM \_E \_ 磁片 \_ 磁碟機 \_ 匯流排 \_ \_ 使用中的 LOC**</dt> <dt>0xA00400503</dt></span><span class="sxs-lookup"><span data-stu-id="9e757-126"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl> | <span data-ttu-id="9e757-127">無法設定匯流排位置，因為另一個裝置目前已連接到此位置。</span><span class="sxs-lookup"><span data-stu-id="9e757-127">The bus location could not be set because another device is currently attached to this location.</span></span><br/> |
| <dl> <span data-ttu-id="9e757-128"><dt>**VM \_E \_ 磁片磁碟機 \_ 無效**</dt>的 <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="9e757-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>            | <span data-ttu-id="9e757-129">目前的磁片磁碟機無效。</span><span class="sxs-lookup"><span data-stu-id="9e757-129">The current drive is not valid.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="9e757-130"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="9e757-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>               | <span data-ttu-id="9e757-131">目前的虛擬機器無效。</span><span class="sxs-lookup"><span data-stu-id="9e757-131">The current virtual machine is not valid.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="9e757-132"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9e757-132"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>               | <span data-ttu-id="9e757-133">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9e757-133">An unexpected error has occurred.</span></span><br/>                                                                |



 

## <a name="requirements"></a><span data-ttu-id="9e757-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e757-134">Requirements</span></span>



| <span data-ttu-id="9e757-135">需求</span><span class="sxs-lookup"><span data-stu-id="9e757-135">Requirement</span></span> | <span data-ttu-id="9e757-136">值</span><span class="sxs-lookup"><span data-stu-id="9e757-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e757-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e757-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9e757-138">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e757-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9e757-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e757-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9e757-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="9e757-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9e757-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9e757-141">End of client support</span></span><br/>    | <span data-ttu-id="9e757-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9e757-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9e757-143">產品</span><span class="sxs-lookup"><span data-stu-id="9e757-143">Product</span></span><br/>                  | <span data-ttu-id="9e757-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9e757-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9e757-145">標頭</span><span class="sxs-lookup"><span data-stu-id="9e757-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e757-146"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="9e757-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9e757-147">IID</span><span class="sxs-lookup"><span data-stu-id="9e757-147">IID</span></span><br/>                      | <span data-ttu-id="9e757-148">IID \_ IVMHardDiskconnection 定義為 aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="9e757-148">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="9e757-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e757-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e757-150">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="9e757-150">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

