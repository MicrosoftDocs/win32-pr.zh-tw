---
description: 捕獲電池的目前狀態。
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
title: 'IOCTL_BATTERY_QUERY_STATUS 控制程式代碼 (Poclass) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: e2de9d3ab48aec13a9a5c1957a5f98aefbe6a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975094"
---
# <a name="ioctl_battery_query_status-control-code"></a><span data-ttu-id="3a52c-103">IOCTL \_ 電池 \_ 查詢 \_ 狀態控制項程式碼</span><span class="sxs-lookup"><span data-stu-id="3a52c-103">IOCTL\_BATTERY\_QUERY\_STATUS control code</span></span>

<span data-ttu-id="3a52c-104">捕獲電池的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="3a52c-104">Retrieves the current status of the battery.</span></span>

<span data-ttu-id="3a52c-105">若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="3a52c-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to battery
  IOCTL_BATTERY_QUERY_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="3a52c-106">參數</span><span class="sxs-lookup"><span data-stu-id="3a52c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a52c-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="3a52c-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="3a52c-108">要傳回其資訊之電池的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3a52c-108">A handle to the battery from which information is to be returned.</span></span> <span data-ttu-id="3a52c-109">若要取出設備控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式。</span><span class="sxs-lookup"><span data-stu-id="3a52c-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="3a52c-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="3a52c-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="3a52c-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="3a52c-111">The control code for the operation.</span></span> <span data-ttu-id="3a52c-112">此值會識別要執行的特定作業，以及要在其上執行的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="3a52c-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="3a52c-113">使用 **IOCTL \_ 電池 \_ 查詢 \_ 狀態** 進行此作業。</span><span class="sxs-lookup"><span data-stu-id="3a52c-113">Use **IOCTL\_BATTERY\_QUERY\_STATUS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="3a52c-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="3a52c-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="3a52c-115">[**電池 \_ 等待 \_ 狀態**](battery-wait-status-str.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="3a52c-115">A pointer to a [**BATTERY\_WAIT\_STATUS**](battery-wait-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3a52c-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="3a52c-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="3a52c-117">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3a52c-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3a52c-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="3a52c-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="3a52c-119">[**電池 \_ 狀態**](battery-status-str.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="3a52c-119">A pointer to a [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3a52c-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="3a52c-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="3a52c-121">輸出緩衝區的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="3a52c-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3a52c-122">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="3a52c-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="3a52c-123">變數的指標，此變數會接收 *lpOutBuffer* 緩衝區中傳回的資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3a52c-123">A pointer to a variable that receives the size of the data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="3a52c-124">如果輸出緩衝區太小而無法傳回任何資料，則呼叫會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤碼 **錯誤 \_ 的 \_ 緩衝區**，而傳回的位元組計數為零。</span><span class="sxs-lookup"><span data-stu-id="3a52c-124">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="3a52c-125">如果 *lpOverlapped* 為 **null** (nonoverlapped I/o) ，則 *lpBytesReturned* 不可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="3a52c-125">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="3a52c-126">如果 *lpOverlapped* 不是 **null** (重迭的 i/o) ， *lpBytesReturned* 可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="3a52c-126">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="3a52c-127">如果這是重迭的作業，您可以藉由呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="3a52c-127">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="3a52c-128">如果 *hDevice* 與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="3a52c-128">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="3a52c-129">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="3a52c-129">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="3a52c-130">重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="3a52c-130">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="3a52c-131">如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice， *lpOverlapped* 必須 [**指向有效的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)重迭結構。</span><span class="sxs-lookup"><span data-stu-id="3a52c-131">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="3a52c-132">在此情況下， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會以 (非同步) 作業的重迭方式執行。</span><span class="sxs-lookup"><span data-stu-id="3a52c-132">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="3a52c-133">如果裝置是以檔案 **旗標重 \_ \_** 迭旗標開啟，且 *lpOverlapped* 為 **Null**，則函式會以無法預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="3a52c-133">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="3a52c-134">如果在未指定檔案 **\_ 旗 \_** 標重迭旗標的情況下開啟 hDevice，則會忽略 *lpOverlapped* ，並且在作業完成或發生錯誤之前，不會傳回 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)函數。</span><span class="sxs-lookup"><span data-stu-id="3a52c-134">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a52c-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a52c-135">Return value</span></span>

<span data-ttu-id="3a52c-136">如果作業順利完成， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="3a52c-136">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="3a52c-137">如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="3a52c-137">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="3a52c-138">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="3a52c-138">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="3a52c-139">備註</span><span class="sxs-lookup"><span data-stu-id="3a52c-139">Remarks</span></span>

<span data-ttu-id="3a52c-140">此電池 IOCTL 會在作業傳回時，捕獲電池的狀態。</span><span class="sxs-lookup"><span data-stu-id="3a52c-140">This battery IOCTL retrieves the status of the battery at the time the operation returns.</span></span> <span data-ttu-id="3a52c-141">輸入參數結構、 [**電池 \_ 等待 \_ 狀態**](battery-wait-status-str.md)，表示要處理和傳回電池狀態的時間。</span><span class="sxs-lookup"><span data-stu-id="3a52c-141">The input parameter structure, [**BATTERY\_WAIT\_STATUS**](battery-wait-status-str.md), indicates when the battery status is to be processed and returned.</span></span>

<span data-ttu-id="3a52c-142">電池狀態的要求可以立即傳回，或可設定為在完成之前等候特定的條件。</span><span class="sxs-lookup"><span data-stu-id="3a52c-142">Requests for battery status can be for immediate return or can be set to wait for a particular condition before completing.</span></span> <span data-ttu-id="3a52c-143">例如，您可以對電池資訊提出要求，直到電池容量達到指定的點或電池狀態變更為止。</span><span class="sxs-lookup"><span data-stu-id="3a52c-143">For example, a request for battery information can be made that waits until the battery capacity reaches a specified point or the battery state changes.</span></span>

<span data-ttu-id="3a52c-144">所有的電池資訊要求都會完成，並在要求的 **BatteryTag** 元素不符合目前電池標記的時 **\_ \_ \_ 找不到錯誤** 檔案的狀態。</span><span class="sxs-lookup"><span data-stu-id="3a52c-144">All requests for battery information will complete with the status of **ERROR\_FILE\_NOT\_FOUND** whenever the **BatteryTag** element of the request does not match that of the current battery tag.</span></span> <span data-ttu-id="3a52c-145"> (如需詳細資訊，請參閱 [電池標記](battery-information.md) 。 ) 這是用來確保傳回的電池資訊符合所要求電池的資訊。</span><span class="sxs-lookup"><span data-stu-id="3a52c-145">(See [Battery Tags](battery-information.md) for more information.) This is used to ensure that the returned battery information matches that of the requested battery.</span></span>

<span data-ttu-id="3a52c-146">如需這項作業的重迭 i/o 含意，請參閱 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="3a52c-146">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="3a52c-147">範例</span><span class="sxs-lookup"><span data-stu-id="3a52c-147">Examples</span></span>

<span data-ttu-id="3a52c-148">如需範例，請參閱 [列舉電池裝置](enumerating-battery-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="3a52c-148">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a52c-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a52c-149">Requirements</span></span>



| <span data-ttu-id="3a52c-150">需求</span><span class="sxs-lookup"><span data-stu-id="3a52c-150">Requirement</span></span> | <span data-ttu-id="3a52c-151">值</span><span class="sxs-lookup"><span data-stu-id="3a52c-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a52c-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a52c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="3a52c-153">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a52c-153">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="3a52c-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a52c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="3a52c-155">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a52c-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="3a52c-156">標頭</span><span class="sxs-lookup"><span data-stu-id="3a52c-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a52c-157"><dt>Poclass .h;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP 上的 BatClass .h</dt></span><span class="sxs-lookup"><span data-stu-id="3a52c-157"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a52c-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a52c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a52c-159">電池資訊</span><span class="sxs-lookup"><span data-stu-id="3a52c-159">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="3a52c-160">電源管理控制碼</span><span class="sxs-lookup"><span data-stu-id="3a52c-160">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="3a52c-161">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="3a52c-161">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="3a52c-162">**電池 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="3a52c-162">**BATTERY\_STATUS**</span></span>](battery-status-str.md)
</dt> <dt>

[<span data-ttu-id="3a52c-163">**電池 \_ 等待 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="3a52c-163">**BATTERY\_WAIT\_STATUS**</span></span>](battery-wait-status-str.md)
</dt> <dt>

[<span data-ttu-id="3a52c-164">**IOCTL \_ 電池 \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3a52c-164">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="3a52c-165">**IOCTL \_ 電池 \_ 查詢 \_ 標記**</span><span class="sxs-lookup"><span data-stu-id="3a52c-165">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> <dt>

[<span data-ttu-id="3a52c-166">**IOCTL \_ 電池 \_ 設定 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3a52c-166">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

