---
title: 'IVMVirtualMachine AddDVDROMDrive 方法 (VPCCOMInterfaces .h) '
description: 將新的 CD 或 DVD 光碟機新增至虛擬機器。
ms.assetid: d39f2728-6146-42ed-b67f-6586566a7209
keywords:
- AddDVDROMDrive 方法 Virtual PC
- AddDVDROMDrive 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，AddDVDROMDrive 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7acbe70f6b338b3490c12ab67bcdfdc997d90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965500"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a><span data-ttu-id="bf5eb-106">IVMVirtualMachine：： AddDVDROMDrive 方法</span><span class="sxs-lookup"><span data-stu-id="bf5eb-106">IVMVirtualMachine::AddDVDROMDrive method</span></span>

<span data-ttu-id="bf5eb-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bf5eb-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="bf5eb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bf5eb-109">將新的 CD 或 DVD 光碟機新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-109">Adds a new CD or DVD drive to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf5eb-110">語法</span><span class="sxs-lookup"><span data-stu-id="bf5eb-110">Syntax</span></span>


```C++
HRESULT AddDVDROMDrive(
  [in]          long        busNumber,
  [in]          long        deviceNumber,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="parameters"></a><span data-ttu-id="bf5eb-111">參數</span><span class="sxs-lookup"><span data-stu-id="bf5eb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf5eb-112">*busNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf5eb-112">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf5eb-113">將連接磁片磁碟機的匯流排。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-113">The bus to which the drive will be attached.</span></span>



| <span data-ttu-id="bf5eb-114">值</span><span class="sxs-lookup"><span data-stu-id="bf5eb-114">Value</span></span>                                                                        | <span data-ttu-id="bf5eb-115">意義</span><span class="sxs-lookup"><span data-stu-id="bf5eb-115">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="bf5eb-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bf5eb-116"><dt>0</dt></span></span> </dl> | <span data-ttu-id="bf5eb-117">磁片磁碟機將會附加至第一個匯流排。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-117">The drive will be attached to the first bus.</span></span><br/>  |
| <dl> <span data-ttu-id="bf5eb-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bf5eb-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="bf5eb-119">磁片磁碟機將會附加至第二個匯流排。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-119">The drive will be attached to the second bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bf5eb-120">*deviceNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf5eb-120">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf5eb-121">將連接磁片磁碟機的裝置。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-121">The device to which the drive will be attached.</span></span>



| <span data-ttu-id="bf5eb-122">值</span><span class="sxs-lookup"><span data-stu-id="bf5eb-122">Value</span></span>                                                                        | <span data-ttu-id="bf5eb-123">意義</span><span class="sxs-lookup"><span data-stu-id="bf5eb-123">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf5eb-124"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bf5eb-124"><dt>0</dt></span></span> </dl> | <span data-ttu-id="bf5eb-125">磁片磁碟機將會連接到匯流排上的第一個裝置。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-125">The drive will be attached to the first device on the bus.</span></span><br/>  |
| <dl> <span data-ttu-id="bf5eb-126"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bf5eb-126"><dt>1</dt></span></span> </dl> | <span data-ttu-id="bf5eb-127">磁片磁碟機將會連接到匯流排上的第二個裝置。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-127">The drive will be attached to the second device on the bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bf5eb-128">*dvdDrive* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="bf5eb-128">*dvdDrive* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bf5eb-129">[**IVMDVDDrive**](ivmdvddrive.md)物件。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-129">An [**IVMDVDDrive**](ivmdvddrive.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf5eb-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf5eb-130">Return value</span></span>

<span data-ttu-id="bf5eb-131">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-131">This method can return one of these values.</span></span>



| <span data-ttu-id="bf5eb-132">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="bf5eb-132">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="bf5eb-133">Description</span><span class="sxs-lookup"><span data-stu-id="bf5eb-133">Description</span></span>                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="bf5eb-134"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bf5eb-134"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                     | <span data-ttu-id="bf5eb-135">作業成功。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-135">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="bf5eb-136"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bf5eb-136"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                       | <span data-ttu-id="bf5eb-137">*DvdDrive* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-137">The *dvdDrive* parameter is **NULL**.</span></span><br/>               |
| <dl> <span data-ttu-id="bf5eb-138"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="bf5eb-138"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                    | <span data-ttu-id="bf5eb-139">參數無效。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-139">A parameter is not valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="bf5eb-140"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="bf5eb-140"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>               | <span data-ttu-id="bf5eb-141">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-141">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="bf5eb-142"><dt>**VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="bf5eb-142"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>    | <span data-ttu-id="bf5eb-143">虛擬機器處於執行中或已儲存狀態。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-143">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="bf5eb-144"><dt>**VM \_E \_ 磁片 \_ 磁碟機 \_ 匯流排 \_ \_ 使用中的 LOC**</dt> <dt>0xA00400503</dt></span><span class="sxs-lookup"><span data-stu-id="bf5eb-144"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl> | <span data-ttu-id="bf5eb-145">指定的匯流排位置正在使用中。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-145">The specified bus location is in use.</span></span><br/>               |
| <dl> <span data-ttu-id="bf5eb-146"><dt>**VM \_E \_ 磁片磁碟機 \_ 無效**</dt>的 <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="bf5eb-146"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>            | <span data-ttu-id="bf5eb-147">指定的磁片磁碟機無效。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-147">The drive specified is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="bf5eb-148"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bf5eb-148"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>               | <span data-ttu-id="bf5eb-149">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-149">An unexpected error has occurred.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="bf5eb-150">備註</span><span class="sxs-lookup"><span data-stu-id="bf5eb-150">Remarks</span></span>

<span data-ttu-id="bf5eb-151">您只能將新的 CD 或 DVD 光碟機新增至已停止的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bf5eb-151">You can only add a new CD or DVD drive to a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf5eb-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf5eb-152">Requirements</span></span>



| <span data-ttu-id="bf5eb-153">需求</span><span class="sxs-lookup"><span data-stu-id="bf5eb-153">Requirement</span></span> | <span data-ttu-id="bf5eb-154">值</span><span class="sxs-lookup"><span data-stu-id="bf5eb-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf5eb-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf5eb-155">Minimum supported client</span></span><br/> | <span data-ttu-id="bf5eb-156">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf5eb-156">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf5eb-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf5eb-157">Minimum supported server</span></span><br/> | <span data-ttu-id="bf5eb-158">都不支援</span><span class="sxs-lookup"><span data-stu-id="bf5eb-158">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bf5eb-159">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="bf5eb-159">End of client support</span></span><br/>    | <span data-ttu-id="bf5eb-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bf5eb-160">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bf5eb-161">產品</span><span class="sxs-lookup"><span data-stu-id="bf5eb-161">Product</span></span><br/>                  | <span data-ttu-id="bf5eb-162">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bf5eb-162">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bf5eb-163">標頭</span><span class="sxs-lookup"><span data-stu-id="bf5eb-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf5eb-164"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="bf5eb-164"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bf5eb-165">IID</span><span class="sxs-lookup"><span data-stu-id="bf5eb-165">IID</span></span><br/>                      | <span data-ttu-id="bf5eb-166">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="bf5eb-166">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="bf5eb-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf5eb-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf5eb-168">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="bf5eb-168">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

