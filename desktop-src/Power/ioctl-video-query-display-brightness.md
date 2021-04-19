---
description: 抓取目前的 AC 和 DC 背光等級和目前的電源狀態。
ms.assetid: c7b7c302-6e92-46a7-b9a6-e3f2a3e44d1b
title: 'IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS 控制程式代碼 (Ntddvdeo) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: 547501a28492aecfe06f63f95b0e007fc80d3d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969357"
---
# <a name="ioctl_video_query_display_brightness-control-code"></a><span data-ttu-id="10bb7-103">IOCTL \_ 影片 \_ 查詢 \_ 顯示 \_ 亮度控制項程式碼</span><span class="sxs-lookup"><span data-stu-id="10bb7-103">IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS control code</span></span>

<span data-ttu-id="10bb7-104">\[此控制項程式碼可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="10bb7-104">\[This control code is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="10bb7-105">已在 Windows Server 2008 和 Windows Vista 中移除對此控制項程式碼的支援。</span><span class="sxs-lookup"><span data-stu-id="10bb7-105">Support for this control code was removed in Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="10bb7-106">請改用 [**WmiMonitorBrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) 類別。\]</span><span class="sxs-lookup"><span data-stu-id="10bb7-106">Use the [**WmiMonitorBrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) class instead.\]</span></span>

<span data-ttu-id="10bb7-107">抓取目前的 AC 和 DC 背光等級和目前的電源狀態。</span><span class="sxs-lookup"><span data-stu-id="10bb7-107">Retrieves the current AC and DC backlight levels and the current power state.</span></span>

<span data-ttu-id="10bb7-108">若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="10bb7-108">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="10bb7-109">參數</span><span class="sxs-lookup"><span data-stu-id="10bb7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10bb7-110">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="10bb7-110">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="10bb7-111">的控制碼 \\ \\ 。 \\LCD 裝置。</span><span class="sxs-lookup"><span data-stu-id="10bb7-111">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="10bb7-112">若要取出設備控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式。</span><span class="sxs-lookup"><span data-stu-id="10bb7-112">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="10bb7-113">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="10bb7-113">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="10bb7-114">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="10bb7-114">The control code for the operation.</span></span> <span data-ttu-id="10bb7-115">此值會識別要執行的特定作業，以及要在其上執行的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="10bb7-115">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="10bb7-116">使用 **IOCTL \_ 影片 \_ 查詢 \_ 顯示 \_ 亮度** 來進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="10bb7-116">Use **IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="10bb7-117">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="10bb7-117">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="10bb7-118">未搭配此作業使用;設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="10bb7-118">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="10bb7-119">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="10bb7-119">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="10bb7-120">未搭配此作業使用;設定為零。</span><span class="sxs-lookup"><span data-stu-id="10bb7-120">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="10bb7-121">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="10bb7-121">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="10bb7-122">將接收 [**顯示 \_ 亮度**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) 結構之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="10bb7-122">A pointer to a buffer that will receive a [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="10bb7-123">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="10bb7-123">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="10bb7-124">輸出緩衝區的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="10bb7-124">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="10bb7-125">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="10bb7-125">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="10bb7-126">變數的指標，此變數會接收傳回的輸出資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="10bb7-126">A pointer to a variable that receives the size, in bytes, of output data returned.</span></span>

<span data-ttu-id="10bb7-127">如果輸出緩衝區太小而無法傳回任何資料，則呼叫會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤碼錯誤的 \_ \_ 緩衝區，而傳回的位元組計數為零。</span><span class="sxs-lookup"><span data-stu-id="10bb7-127">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="10bb7-128">如果輸出緩衝區太小而無法容納所有資料，但可以保存某些專案，則作業系統會盡可能傳回最適合的值、呼叫會失敗、 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤碼錯誤的 \_ \_ 資料，而 *lpBytesReturned* 則表示傳回的資料量。</span><span class="sxs-lookup"><span data-stu-id="10bb7-128">If the output buffer is too small to hold all of the data but can hold some entries, then the operating system returns as much as fits, the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_MORE\_DATA, and *lpBytesReturned* indicates the amount of data returned.</span></span> <span data-ttu-id="10bb7-129">您的應用程式應該使用相同的作業再次呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ，以指定新的起點。</span><span class="sxs-lookup"><span data-stu-id="10bb7-129">Your application should call [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) again with the same operation, specifying a new starting point.</span></span>

<span data-ttu-id="10bb7-130">如果 *lpOverlapped* 為 **null** (nonoverlapped I/o) ，則 *lpBytesReturned* 不可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="10bb7-130">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="10bb7-131">如果 *lpOverlapped* 不是 **null** (重迭的 i/o) ， *lpBytesReturned* 可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="10bb7-131">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="10bb7-132">如果這是重迭的作業，您可以藉由呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="10bb7-132">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="10bb7-133">如果 *hDevice* 與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="10bb7-133">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="10bb7-134">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="10bb7-134">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="10bb7-135">重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="10bb7-135">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="10bb7-136">如果使用檔案旗標重迭旗標開啟 *hDevice* \_ \_ ， *lpOverlapped* 必須指向有效的 [](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)重迭結構。</span><span class="sxs-lookup"><span data-stu-id="10bb7-136">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="10bb7-137">在此情況下，作業會以 (非同步) 作業的重迭方式執行。</span><span class="sxs-lookup"><span data-stu-id="10bb7-137">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="10bb7-138">如果裝置是以檔案旗標重迭旗標開啟， \_ \_ 且 *lpOverlapped* 為 **Null**，則函式會以無法預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="10bb7-138">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="10bb7-139">如果在未指定檔案旗標重迭旗標的情況下開啟 *hDevice* \_ \_ ，則會忽略 *lpOverlapped* ，除非作業完成或發生錯誤，否則 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 不會傳回。</span><span class="sxs-lookup"><span data-stu-id="10bb7-139">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10bb7-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="10bb7-140">Return value</span></span>

<span data-ttu-id="10bb7-141">如果作業順利完成， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="10bb7-141">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="10bb7-142">如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="10bb7-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="10bb7-143">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="10bb7-143">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="10bb7-144">備註</span><span class="sxs-lookup"><span data-stu-id="10bb7-144">Remarks</span></span>

<span data-ttu-id="10bb7-145">用來建立包含這項功能（Ntddvdeo）之應用程式的標頭檔，隨附于 Microsoft Windows 驅動程式開發工具組 (DDK) 。</span><span class="sxs-lookup"><span data-stu-id="10bb7-145">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="10bb7-146">如需取得 DDK 的詳細資訊，請參閱 [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) 。</span><span class="sxs-lookup"><span data-stu-id="10bb7-146">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="10bb7-147">或者，您可以定義此控制項程式碼，如下所示：</span><span class="sxs-lookup"><span data-stu-id="10bb7-147">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x126, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="10bb7-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="10bb7-148">Requirements</span></span>



| <span data-ttu-id="10bb7-149">需求</span><span class="sxs-lookup"><span data-stu-id="10bb7-149">Requirement</span></span> | <span data-ttu-id="10bb7-150">值</span><span class="sxs-lookup"><span data-stu-id="10bb7-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10bb7-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10bb7-151">Minimum supported client</span></span><br/> | <span data-ttu-id="10bb7-152">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10bb7-152">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10bb7-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10bb7-153">Minimum supported server</span></span><br/> | <span data-ttu-id="10bb7-154">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10bb7-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10bb7-155">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="10bb7-155">End of client support</span></span><br/>    | <span data-ttu-id="10bb7-156">Windows XP 含 SP2</span><span class="sxs-lookup"><span data-stu-id="10bb7-156">Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="10bb7-157">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="10bb7-157">End of server support</span></span><br/>    | <span data-ttu-id="10bb7-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="10bb7-158">Windows Server 2003 R2</span></span><br/>                                                     |
| <span data-ttu-id="10bb7-159">標頭</span><span class="sxs-lookup"><span data-stu-id="10bb7-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="10bb7-160"><dt>Ntddvdeo。h</dt></span><span class="sxs-lookup"><span data-stu-id="10bb7-160"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10bb7-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10bb7-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10bb7-162">背光控制項介面</span><span class="sxs-lookup"><span data-stu-id="10bb7-162">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="10bb7-163">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="10bb7-163">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

<span data-ttu-id="10bb7-164">[**顯示 \_ 亮度**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10bb7-164">[**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="10bb7-165">**IOCTL \_ 影片 \_ 集 \_ 顯示 \_ 亮度**</span><span class="sxs-lookup"><span data-stu-id="10bb7-165">**IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-set-display-brightness.md)
</dt> </dl>

 

