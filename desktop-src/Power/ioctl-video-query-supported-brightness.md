---
description: 抓取支援的背光等級。
ms.assetid: b4c1ee3f-af75-477e-b7ed-53be905374d7
title: 'IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS 控制程式代碼 (Ntddvdeo) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a5618ec29fd47ba690106b5f826e6fb145eac208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988792"
---
# <a name="ioctl_video_query_supported_brightness-control-code"></a><span data-ttu-id="87f47-103">IOCTL \_ 影片 \_ 查詢 \_ 支援的 \_ 亮度控制項程式碼</span><span class="sxs-lookup"><span data-stu-id="87f47-103">IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS control code</span></span>

<span data-ttu-id="87f47-104">抓取支援的背光等級。</span><span class="sxs-lookup"><span data-stu-id="87f47-104">Retrieves the supported backlight levels.</span></span>

<span data-ttu-id="87f47-105">若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="87f47-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="87f47-106">參數</span><span class="sxs-lookup"><span data-stu-id="87f47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87f47-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="87f47-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="87f47-108">的控制碼 \\ \\ 。 \\LCD 裝置。</span><span class="sxs-lookup"><span data-stu-id="87f47-108">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="87f47-109">若要取出設備控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式。</span><span class="sxs-lookup"><span data-stu-id="87f47-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="87f47-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="87f47-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="87f47-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="87f47-111">The control code for the operation.</span></span> <span data-ttu-id="87f47-112">此值會識別要執行的特定作業，以及要在其上執行的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="87f47-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="87f47-113">針對此作業使用 **IOCTL \_ 影片 \_ 查詢 \_ 支援的 \_ 亮度** 。</span><span class="sxs-lookup"><span data-stu-id="87f47-113">Use **IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="87f47-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="87f47-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="87f47-115">未搭配此作業使用;設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="87f47-115">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87f47-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="87f47-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="87f47-117">未搭配此作業使用;設定為零。</span><span class="sxs-lookup"><span data-stu-id="87f47-117">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="87f47-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="87f47-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="87f47-119">接收可用電源等級陣列的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="87f47-119">A pointer to a buffer that receives an array of the available power levels.</span></span> <span data-ttu-id="87f47-120">這個緩衝區的長度應為256個位元組。</span><span class="sxs-lookup"><span data-stu-id="87f47-120">This buffer should be 256 bytes long.</span></span>

</dd> <dt>

<span data-ttu-id="87f47-121">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="87f47-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="87f47-122">輸出緩衝區的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="87f47-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="87f47-123">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="87f47-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="87f47-124">變數的指標，此變數會接收傳回的輸出資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="87f47-124">A pointer to a variable that receives the size, in bytes, of output data returned.</span></span>

<span data-ttu-id="87f47-125">如果輸出緩衝區太小而無法傳回任何資料，則呼叫會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤碼錯誤的 \_ \_ 緩衝區，而傳回的位元組計數為零。</span><span class="sxs-lookup"><span data-stu-id="87f47-125">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="87f47-126">如果輸出緩衝區太小而無法容納所有資料，但可以保存某些專案，則作業系統會盡可能傳回最適合的值、呼叫會失敗、 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤碼錯誤的 \_ \_ 資料，而 *lpBytesReturned* 則表示傳回的資料量。</span><span class="sxs-lookup"><span data-stu-id="87f47-126">If the output buffer is too small to hold all of the data but can hold some entries, then the operating system returns as much as fits, the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_MORE\_DATA, and *lpBytesReturned* indicates the amount of data returned.</span></span> <span data-ttu-id="87f47-127">您的應用程式應該使用相同的作業再次呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ，以指定新的起點。</span><span class="sxs-lookup"><span data-stu-id="87f47-127">Your application should call [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) again with the same operation, specifying a new starting point.</span></span>

<span data-ttu-id="87f47-128">如果 *lpOverlapped* 為 **null** (nonoverlapped I/o) ，則 *lpBytesReturned* 不可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="87f47-128">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="87f47-129">如果 *lpOverlapped* 不是 **null** (重迭的 i/o) ， *lpBytesReturned* 可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="87f47-129">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="87f47-130">如果這是重迭的作業，您可以藉由呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="87f47-130">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="87f47-131">如果 *hDevice* 與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="87f47-131">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="87f47-132">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="87f47-132">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="87f47-133">重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="87f47-133">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="87f47-134">如果使用檔案旗標重迭旗標開啟 *hDevice* \_ \_ ， *lpOverlapped* 必須指向有效的 [](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)重迭結構。</span><span class="sxs-lookup"><span data-stu-id="87f47-134">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="87f47-135">在此情況下，作業會以 (非同步) 作業的重迭方式執行。</span><span class="sxs-lookup"><span data-stu-id="87f47-135">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="87f47-136">如果裝置是以檔案旗標重迭旗標開啟， \_ \_ 且 *lpOverlapped* 為 **Null**，則函式會以無法預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="87f47-136">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="87f47-137">如果在未指定檔案旗標重迭旗標的情況下開啟 *hDevice* \_ \_ ，則會忽略 *lpOverlapped* ，除非作業完成或發生錯誤，否則 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 不會傳回。</span><span class="sxs-lookup"><span data-stu-id="87f47-137">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87f47-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="87f47-138">Return value</span></span>

<span data-ttu-id="87f47-139">如果作業順利完成， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="87f47-139">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="87f47-140">如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="87f47-140">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="87f47-141">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="87f47-141">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="87f47-142">備註</span><span class="sxs-lookup"><span data-stu-id="87f47-142">Remarks</span></span>

<span data-ttu-id="87f47-143">*LpOutBuffer* 陣列中的每個元素都是一個位元組的長度。</span><span class="sxs-lookup"><span data-stu-id="87f47-143">Each element in the *lpOutBuffer* array is one byte in length.</span></span> <span data-ttu-id="87f47-144">因此，當傳回時， *lpBytesReturned* 參數會指出支援的層級數目。</span><span class="sxs-lookup"><span data-stu-id="87f47-144">Therefore, upon return, the *lpBytesReturned* parameter indicates the number of supported levels.</span></span> <span data-ttu-id="87f47-145">每個層級都是從0到100的值。</span><span class="sxs-lookup"><span data-stu-id="87f47-145">Each level is a value from 0 to 100.</span></span> <span data-ttu-id="87f47-146">值愈大，背光愈亮。</span><span class="sxs-lookup"><span data-stu-id="87f47-146">The larger the value, the brighter the backlight.</span></span> <span data-ttu-id="87f47-147">無論電源來源為 AC 或 DC，都支援所有層級。</span><span class="sxs-lookup"><span data-stu-id="87f47-147">All levels are supported whether the power source is AC or DC.</span></span>

<span data-ttu-id="87f47-148">用來建立包含這項功能（Ntddvdeo）之應用程式的標頭檔，隨附于 Microsoft Windows 驅動程式開發工具組 (DDK) 。</span><span class="sxs-lookup"><span data-stu-id="87f47-148">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="87f47-149">如需取得 DDK 的詳細資訊，請參閱 [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) 。</span><span class="sxs-lookup"><span data-stu-id="87f47-149">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="87f47-150">或者，您可以定義此控制項程式碼，如下所示：</span><span class="sxs-lookup"><span data-stu-id="87f47-150">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x125, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="87f47-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="87f47-151">Requirements</span></span>



| <span data-ttu-id="87f47-152">需求</span><span class="sxs-lookup"><span data-stu-id="87f47-152">Requirement</span></span> | <span data-ttu-id="87f47-153">值</span><span class="sxs-lookup"><span data-stu-id="87f47-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87f47-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87f47-154">Minimum supported client</span></span><br/> | <span data-ttu-id="87f47-155">Windows Vista、Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87f47-155">Windows Vista, Windows XP with SP1 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="87f47-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87f47-156">Minimum supported server</span></span><br/> | <span data-ttu-id="87f47-157">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87f47-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87f47-158">標頭</span><span class="sxs-lookup"><span data-stu-id="87f47-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="87f47-159"><dt>Ntddvdeo。h</dt></span><span class="sxs-lookup"><span data-stu-id="87f47-159"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87f47-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87f47-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87f47-161">背光控制項介面</span><span class="sxs-lookup"><span data-stu-id="87f47-161">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="87f47-162">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="87f47-162">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

