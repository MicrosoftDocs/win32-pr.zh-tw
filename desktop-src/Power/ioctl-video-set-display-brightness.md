---
description: 設定目前的 AC 和 DC 背光等級。
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: 'IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS 控制程式代碼 (Ntddvdeo) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a0c679f352012eea66b80335bc3ad1547501dd92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944238"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a><span data-ttu-id="47eb9-103">IOCTL \_ 影片 \_ 集 \_ 顯示 \_ 亮度控制項程式碼</span><span class="sxs-lookup"><span data-stu-id="47eb9-103">IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS control code</span></span>

<span data-ttu-id="47eb9-104">設定目前的 AC 和 DC 背光等級。</span><span class="sxs-lookup"><span data-stu-id="47eb9-104">Sets the current AC and DC backlight levels.</span></span>

<span data-ttu-id="47eb9-105">若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="47eb9-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="47eb9-106">參數</span><span class="sxs-lookup"><span data-stu-id="47eb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47eb9-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="47eb9-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="47eb9-108">的控制碼 \\ \\ 。 \\LCD 裝置。</span><span class="sxs-lookup"><span data-stu-id="47eb9-108">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="47eb9-109">若要取出設備控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式。</span><span class="sxs-lookup"><span data-stu-id="47eb9-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="47eb9-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="47eb9-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="47eb9-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="47eb9-111">The control code for the operation.</span></span> <span data-ttu-id="47eb9-112">此值會識別要執行的特定作業，以及要在其上執行的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="47eb9-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="47eb9-113">使用 **IOCTL \_ VIDEO \_ SET \_ 顯示器 \_ 亮度** 進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="47eb9-113">Use **IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="47eb9-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="47eb9-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="47eb9-115">[**顯示 \_ 亮度**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))結構的指標。</span><span class="sxs-lookup"><span data-stu-id="47eb9-115">A pointer to a [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="47eb9-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="47eb9-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="47eb9-117">*LpOutBuffer* 所指向的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="47eb9-117">The size of the buffer pointed to by *lpOutBuffer*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="47eb9-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="47eb9-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="47eb9-119">未搭配此作業使用;設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="47eb9-119">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="47eb9-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="47eb9-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="47eb9-121">未搭配此作業使用;設定為零。</span><span class="sxs-lookup"><span data-stu-id="47eb9-121">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="47eb9-122">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="47eb9-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="47eb9-123">變數的指標，此變數會接收輸出緩衝區中函數所傳回的實際位元組計數。</span><span class="sxs-lookup"><span data-stu-id="47eb9-123">A pointer to a variable that receives the actual count of bytes returned by the function in the output buffer.</span></span>

<span data-ttu-id="47eb9-124">如果 *lpOverlapped* 為 **Null** (nonoverlapped i/o) ，則會在內部使用 *lpBytesReturned* ，且不能是 **null**。</span><span class="sxs-lookup"><span data-stu-id="47eb9-124">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* is used internally and cannot be **NULL**.</span></span>

<span data-ttu-id="47eb9-125">如果 *lpOverlapped* 不是 **null** (重迭的 i/o) ， *lpBytesReturned* 可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="47eb9-125">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="47eb9-126">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="47eb9-126">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="47eb9-127">重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="47eb9-127">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="47eb9-128">如果使用檔案旗標重迭旗標開啟 *hDevice* \_ \_ ， *lpOverlapped* 必須指向有效的 [](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)重迭結構。</span><span class="sxs-lookup"><span data-stu-id="47eb9-128">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="47eb9-129">在此情況下，作業會以 (非同步) 作業的重迭方式執行。</span><span class="sxs-lookup"><span data-stu-id="47eb9-129">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="47eb9-130">如果裝置是以檔案旗標重迭旗標開啟， \_ \_ 且 *lpOverlapped* 為 **Null**，則函式會以無法預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="47eb9-130">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="47eb9-131">如果在未指定檔案旗標重迭旗標的情況下開啟 *hDevice* \_ \_ ，則會忽略 *lpOverlapped* ，除非作業完成或發生錯誤，否則 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 不會傳回。</span><span class="sxs-lookup"><span data-stu-id="47eb9-131">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47eb9-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="47eb9-132">Return value</span></span>

<span data-ttu-id="47eb9-133">如果作業順利完成， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="47eb9-133">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="47eb9-134">如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="47eb9-134">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="47eb9-135">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="47eb9-135">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="47eb9-136">備註</span><span class="sxs-lookup"><span data-stu-id="47eb9-136">Remarks</span></span>

<span data-ttu-id="47eb9-137">在 [**顯示 \_ 亮度**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))結構的 **ucACBrightness** 和 **ucDCBrightness** 成員中指定的值，必須先前由 [**IOCTL \_ 影片 \_ 查詢 \_ 支援的 \_ 亮度**](ioctl-video-query-supported-brightness.md)傳回。</span><span class="sxs-lookup"><span data-stu-id="47eb9-137">The values specified in the **ucACBrightness** and **ucDCBrightness** members of the [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure must have been previously returned by [**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**](ioctl-video-query-supported-brightness.md).</span></span> <span data-ttu-id="47eb9-138">例如，如果支援的值為10、20、30、40、50、60、70、80、90和100，則使用值33會是錯誤。</span><span class="sxs-lookup"><span data-stu-id="47eb9-138">For example, if the supported values are 10, 20, 30, 40, 50, 60, 70, 80, 90, and 100, then using a value of 33 would be an error.</span></span>

<span data-ttu-id="47eb9-139">用來建立包含這項功能（Ntddvdeo）之應用程式的標頭檔，隨附于 Microsoft Windows 驅動程式開發工具組 (DDK) 。</span><span class="sxs-lookup"><span data-stu-id="47eb9-139">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="47eb9-140">如需取得 DDK 的詳細資訊，請參閱 [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) 。</span><span class="sxs-lookup"><span data-stu-id="47eb9-140">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="47eb9-141">或者，您可以定義此控制項程式碼，如下所示：</span><span class="sxs-lookup"><span data-stu-id="47eb9-141">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="47eb9-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="47eb9-142">Requirements</span></span>



| <span data-ttu-id="47eb9-143">需求</span><span class="sxs-lookup"><span data-stu-id="47eb9-143">Requirement</span></span> | <span data-ttu-id="47eb9-144">值</span><span class="sxs-lookup"><span data-stu-id="47eb9-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47eb9-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="47eb9-145">Minimum supported client</span></span><br/> | <span data-ttu-id="47eb9-146">Windows Vista、Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47eb9-146">Windows Vista, Windows XP with SP1 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="47eb9-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="47eb9-147">Minimum supported server</span></span><br/> | <span data-ttu-id="47eb9-148">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47eb9-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47eb9-149">標頭</span><span class="sxs-lookup"><span data-stu-id="47eb9-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="47eb9-150"><dt>Ntddvdeo。h</dt></span><span class="sxs-lookup"><span data-stu-id="47eb9-150"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47eb9-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47eb9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47eb9-152">背光控制項介面</span><span class="sxs-lookup"><span data-stu-id="47eb9-152">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="47eb9-153">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="47eb9-153">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

<span data-ttu-id="47eb9-154">[**顯示 \_ 亮度**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="47eb9-154">[**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="47eb9-155">**IOCTL \_ 影片 \_ 查詢 \_ 顯示 \_ 亮度**</span><span class="sxs-lookup"><span data-stu-id="47eb9-155">**IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-query-display-brightness.md)
</dt> <dt>

[<span data-ttu-id="47eb9-156">**IOCTL \_ 影片 \_ 查詢 \_ 支援的 \_ 亮度**</span><span class="sxs-lookup"><span data-stu-id="47eb9-156">**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**</span></span>](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 

