---
title: 'IVMVirtualMachine AddHardDiskConnection 方法 (VPCCOMInterfaces .h) '
description: 將新的硬碟連接新增至虛擬機器。
ms.assetid: 0f4e0666-2cfd-4c73-884d-6f8b43186c05
keywords:
- AddHardDiskConnection 方法 Virtual PC
- AddHardDiskConnection 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，AddHardDiskConnection 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0111577fd5cab614988e7295f3b8cdd59b8805c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967972"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a><span data-ttu-id="4d874-106">IVMVirtualMachine：： AddHardDiskConnection 方法</span><span class="sxs-lookup"><span data-stu-id="4d874-106">IVMVirtualMachine::AddHardDiskConnection method</span></span>

<span data-ttu-id="4d874-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="4d874-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4d874-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="4d874-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4d874-109">將新的硬碟連線新增到虛擬機器 (VM) 。</span><span class="sxs-lookup"><span data-stu-id="4d874-109">Adds a new hard disk connection to the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="4d874-110">語法</span><span class="sxs-lookup"><span data-stu-id="4d874-110">Syntax</span></span>


```C++
HRESULT AddHardDiskConnection(
  [in]          BSTR                  hardDiskPath,
  [in]          long                  busNumber,
  [in]          long                  deviceNumber,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="parameters"></a><span data-ttu-id="4d874-111">參數</span><span class="sxs-lookup"><span data-stu-id="4d874-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d874-112">*hardDiskPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d874-112">*hardDiskPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d874-113">要連接的虛擬硬碟 (VHD) 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4d874-113">The full path of the virtual hard disk (VHD) file to connect.</span></span>

</dd> <dt>

<span data-ttu-id="4d874-114">*busNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d874-114">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d874-115">將連接磁片磁碟機的匯流排。</span><span class="sxs-lookup"><span data-stu-id="4d874-115">The bus to which the drive will be attached.</span></span>



| <span data-ttu-id="4d874-116">值</span><span class="sxs-lookup"><span data-stu-id="4d874-116">Value</span></span>                                                                        | <span data-ttu-id="4d874-117">意義</span><span class="sxs-lookup"><span data-stu-id="4d874-117">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="4d874-118"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-118"><dt>0</dt></span></span> </dl> | <span data-ttu-id="4d874-119">磁片磁碟機將會附加至第一個匯流排。</span><span class="sxs-lookup"><span data-stu-id="4d874-119">The drive will be attached to the first bus.</span></span><br/>  |
| <dl> <span data-ttu-id="4d874-120"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-120"><dt>1</dt></span></span> </dl> | <span data-ttu-id="4d874-121">磁片磁碟機將會附加至第二個匯流排。</span><span class="sxs-lookup"><span data-stu-id="4d874-121">The drive will be attached to the second bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4d874-122">*deviceNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d874-122">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d874-123">將連接磁片磁碟機的裝置。</span><span class="sxs-lookup"><span data-stu-id="4d874-123">The device to which the drive will be attached.</span></span>



| <span data-ttu-id="4d874-124">值</span><span class="sxs-lookup"><span data-stu-id="4d874-124">Value</span></span>                                                                        | <span data-ttu-id="4d874-125">意義</span><span class="sxs-lookup"><span data-stu-id="4d874-125">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4d874-126"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-126"><dt>0</dt></span></span> </dl> | <span data-ttu-id="4d874-127">磁片磁碟機將會連接到匯流排上的第一個裝置。</span><span class="sxs-lookup"><span data-stu-id="4d874-127">The drive will be attached to the first device on the bus.</span></span><br/>  |
| <dl> <span data-ttu-id="4d874-128"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-128"><dt>1</dt></span></span> </dl> | <span data-ttu-id="4d874-129">磁片磁碟機將會連接到匯流排上的第二個裝置。</span><span class="sxs-lookup"><span data-stu-id="4d874-129">The drive will be attached to the second device on the bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4d874-130">*hardDiskConnection* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="4d874-130">*hardDiskConnection* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4d874-131">[**IVMHardDiskConnection**](ivmharddiskconnection.md)物件。</span><span class="sxs-lookup"><span data-stu-id="4d874-131">An [**IVMHardDiskConnection**](ivmharddiskconnection.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d874-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d874-132">Return value</span></span>

<span data-ttu-id="4d874-133">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4d874-133">This method can return one of these values.</span></span>



| <span data-ttu-id="4d874-134">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="4d874-134">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="4d874-135">Description</span><span class="sxs-lookup"><span data-stu-id="4d874-135">Description</span></span>                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4d874-136"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-136"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="4d874-137">作業成功。</span><span class="sxs-lookup"><span data-stu-id="4d874-137">The operation was successful.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="4d874-138"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-138"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="4d874-139">*HardDiskConnection* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4d874-139">The *hardDiskConnection* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="4d874-140"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-140"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="4d874-141">*HardDiskPath* 參數為 **Null** 或 *busNumber* 或 *deviceNumber* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="4d874-141">A *hardDiskPath* parameter is **NULL** or the *busNumber* or *deviceNumber* parameter is not valid.</span></span><br/>                                            |
| <dl> <span data-ttu-id="4d874-142"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl>   | <span data-ttu-id="4d874-143">系統找不到 *hardDiskPath* 參數所指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="4d874-143">The system cannot find the file specified by the *hardDiskPath* parameter.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="4d874-144"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="4d874-145">系統找不到 *hardDiskPath* 參數所指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="4d874-145">The system cannot find the path specified by the *hardDiskPath* parameter.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="4d874-146"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="4d874-147">*HardDiskPath* 參數包含不正確字元 (" \* ？ <>/ \| "： ") 之一。</span><span class="sxs-lookup"><span data-stu-id="4d874-147">The *hardDiskPath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                                        |
| <dl> <span data-ttu-id="4d874-148"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-148"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="4d874-149">*HardDiskPath* 參數會指定空的或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="4d874-149">The *hardDiskPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="4d874-150">需要絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="4d874-150">An absolute path is required.</span></span><br/>                                                |
| <dl> <span data-ttu-id="4d874-151"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-151"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="4d874-152">*HardDiskPath* 參數所指定的路徑太長。</span><span class="sxs-lookup"><span data-stu-id="4d874-152">The path specified by the *hardDiskPath* parameter is too long.</span></span> <span data-ttu-id="4d874-153">路徑必須少於260個字元。</span><span class="sxs-lookup"><span data-stu-id="4d874-153">The path must be less than 260 characters.</span></span><br/>                                     |
| <dl> <span data-ttu-id="4d874-154"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-154"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                              | <span data-ttu-id="4d874-155">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="4d874-155">The configuration is unknown.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="4d874-156"><dt>**VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-156"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>                   | <span data-ttu-id="4d874-157">VM 處於執行中或已儲存狀態。</span><span class="sxs-lookup"><span data-stu-id="4d874-157">The VM is in a running or saved state.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="4d874-158"><dt>**VM \_E \_ 磁片 \_ 磁碟機 \_ 匯流排 \_ \_ 使用中的 LOC**</dt> <dt>0xA00400503</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-158"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl>                | <span data-ttu-id="4d874-159">指定的匯流排位置正在使用中。</span><span class="sxs-lookup"><span data-stu-id="4d874-159">The specified bus location is in use.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="4d874-160"><dt>**VM \_E \_ 不正確 \_ HD \_ FILE**</dt> <dt>0xA0040682</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-160"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="4d874-161">VHD 超過 127 GB，因此無法連線至 IDE 匯流排。</span><span class="sxs-lookup"><span data-stu-id="4d874-161">The VHD is greater than 127 GB and cannot be connected to the IDE bus.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="4d874-162"><dt>**VM \_E \_ 不支援的 \_ HD \_ 磁片 \_ 類型**</dt> <dt>0xA00400686</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-162"><dt>**VM\_E\_UNSUPPORTED\_HD\_DISK\_TYPE**</dt> <dt>0xA00400686</dt></span></span> </dl>             | <span data-ttu-id="4d874-163">*HardDiskPath* 參數會將連結的 vhd 或差異 vhd 參考至連結的 vhd。</span><span class="sxs-lookup"><span data-stu-id="4d874-163">The *hardDiskPath* parameter refers to a linked VHD or a differencing VHD to a linked VHD.</span></span> <span data-ttu-id="4d874-164">連結的 Vhd 無法附加至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="4d874-164">Linked VHDs cannot be attached to virtual machines.</span></span><br/> |
| <dl> <span data-ttu-id="4d874-165"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 共用 \_ 違規)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-165"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="4d874-166">指定的 VHD 已連線到此 VM 的其他匯流排位置。</span><span class="sxs-lookup"><span data-stu-id="4d874-166">The specified VHD is already connected to another bus location for this VM.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="4d874-167"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-167"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="4d874-168">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4d874-168">An unexpected error has occurred.</span></span><br/>                                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="4d874-169">備註</span><span class="sxs-lookup"><span data-stu-id="4d874-169">Remarks</span></span>

<span data-ttu-id="4d874-170">您只能將新的硬碟連接新增至已停止的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="4d874-170">You can only add a new hard disk connection to a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d874-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d874-171">Requirements</span></span>



| <span data-ttu-id="4d874-172">需求</span><span class="sxs-lookup"><span data-stu-id="4d874-172">Requirement</span></span> | <span data-ttu-id="4d874-173">值</span><span class="sxs-lookup"><span data-stu-id="4d874-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d874-174">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d874-174">Minimum supported client</span></span><br/> | <span data-ttu-id="4d874-175">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d874-175">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4d874-176">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d874-176">Minimum supported server</span></span><br/> | <span data-ttu-id="4d874-177">都不支援</span><span class="sxs-lookup"><span data-stu-id="4d874-177">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4d874-178">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4d874-178">End of client support</span></span><br/>    | <span data-ttu-id="4d874-179">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d874-179">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4d874-180">產品</span><span class="sxs-lookup"><span data-stu-id="4d874-180">Product</span></span><br/>                  | <span data-ttu-id="4d874-181">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4d874-181">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4d874-182">標頭</span><span class="sxs-lookup"><span data-stu-id="4d874-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d874-183"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="4d874-183"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4d874-184">IID</span><span class="sxs-lookup"><span data-stu-id="4d874-184">IID</span></span><br/>                      | <span data-ttu-id="4d874-185">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="4d874-185">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4d874-186">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d874-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d874-187">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="4d874-187">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

