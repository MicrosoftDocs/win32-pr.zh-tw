---
description: 抓取 batterys 目前的標記。
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: 'IOCTL_BATTERY_QUERY_TAG 控制程式代碼 (Poclass) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_TAG
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: 1d8435e62c4f061ac13b3e18e5bcd64afcb399c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982422"
---
# <a name="ioctl_battery_query_tag-control-code"></a><span data-ttu-id="f3804-103">IOCTL \_ 電池 \_ 查詢 \_ 標記控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="f3804-103">IOCTL\_BATTERY\_QUERY\_TAG control code</span></span>

<span data-ttu-id="f3804-104">抓取電池的目前標記。</span><span class="sxs-lookup"><span data-stu-id="f3804-104">Retrieves the battery's current tag.</span></span>

<span data-ttu-id="f3804-105">若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="f3804-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to battery
  IOCTL_BATTERY_QUERY_TAG,     // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped);// OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="f3804-106">參數</span><span class="sxs-lookup"><span data-stu-id="f3804-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3804-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="f3804-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="f3804-108">要從中抓取標記之電池的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f3804-108">A handle to the battery from which the tag is to be retrieved.</span></span> <span data-ttu-id="f3804-109">若要取出設備控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式。</span><span class="sxs-lookup"><span data-stu-id="f3804-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="f3804-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="f3804-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="f3804-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="f3804-111">The control code for the operation.</span></span> <span data-ttu-id="f3804-112">此值會識別要執行的特定作業，以及要在其上執行的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="f3804-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="f3804-113">針對此作業使用 **IOCTL \_ 電池 \_ 查詢 \_ 標記** 。</span><span class="sxs-lookup"><span data-stu-id="f3804-113">Use **IOCTL\_BATTERY\_QUERY\_TAG** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="f3804-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="f3804-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f3804-115">**ULONG** 輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="f3804-115">A pointer to a **ULONG** input buffer.</span></span> <span data-ttu-id="f3804-116">值指出沒有電池時要等候的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="f3804-116">The value indicates the number of milliseconds to wait if there is no battery.</span></span> <span data-ttu-id="f3804-117">-1 的值表示要求將會無限期等候 (或直到其他事件) 取消為止。</span><span class="sxs-lookup"><span data-stu-id="f3804-117">A value of -1 indicates the request will wait indefinitely (or until canceled by some other event).</span></span>

</dd> <dt>

<span data-ttu-id="f3804-118">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="f3804-118">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f3804-119">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3804-119">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f3804-120">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="f3804-120">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f3804-121">**ULONG** 輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="f3804-121">A pointer to a **ULONG** output buffer.</span></span> <span data-ttu-id="f3804-122">成功時，此緩衝區會包含目前的電池標記，它可以是任何值，但電池 \_ 標記 \_ 無效。</span><span class="sxs-lookup"><span data-stu-id="f3804-122">On success this buffer contains the current battery tag, which can be any value except BATTERY\_TAG\_INVALID.</span></span> <span data-ttu-id="f3804-123">失敗時，如果 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)傳回錯誤碼錯誤檔案，則此緩衝區包含值 **電池 \_ 標記 \_ 無效**。 **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f3804-123">On failure, if [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_FILE\_NOT\_FOUND**, this buffer contains the value **BATTERY\_TAG\_INVALID**.</span></span>

</dd> <dt>

<span data-ttu-id="f3804-124">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="f3804-124">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f3804-125">輸出緩衝區的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="f3804-125">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f3804-126">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="f3804-126">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="f3804-127">變數的指標，此變數會接收儲存在 *lpOutBuffer* 緩衝區中的資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3804-127">A pointer to a variable that receives the size of the data stored in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="f3804-128">如果輸出緩衝區太小而無法傳回任何資料，則呼叫會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤碼 **錯誤 \_ 的 \_ 緩衝區**，而傳回的位元組計數為零。</span><span class="sxs-lookup"><span data-stu-id="f3804-128">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="f3804-129">如果 *lpOverlapped* 為 **null** (nonoverlapped I/o) ，則 *lpBytesReturned* 不可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="f3804-129">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="f3804-130">如果 *lpOverlapped* 不是 **null** (重迭的 i/o) ， *lpBytesReturned* 可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="f3804-130">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="f3804-131">如果這是重迭的作業，您可以藉由呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="f3804-131">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="f3804-132">如果 *hDevice* 與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="f3804-132">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="f3804-133">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="f3804-133">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="f3804-134">重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="f3804-134">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="f3804-135">如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice， *lpOverlapped* 必須 [**指向有效的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)重迭結構。</span><span class="sxs-lookup"><span data-stu-id="f3804-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="f3804-136">在此情況下， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會以 (非同步) 作業的重迭方式執行。</span><span class="sxs-lookup"><span data-stu-id="f3804-136">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="f3804-137">如果裝置是以檔案 **旗標重 \_ \_** 迭旗標開啟，且 *lpOverlapped* 為 **Null**，則函式會以無法預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="f3804-137">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="f3804-138">如果在未指定檔案 **\_ 旗 \_** 標重迭旗標的情況下開啟 hDevice，則會忽略 *lpOverlapped* ，並且在作業完成或發生錯誤之前，不會傳回 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)函數。</span><span class="sxs-lookup"><span data-stu-id="f3804-138">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3804-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3804-139">Return value</span></span>

<span data-ttu-id="f3804-140">如果作業順利完成， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="f3804-140">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="f3804-141">如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="f3804-141">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="f3804-142">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="f3804-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="f3804-143">備註</span><span class="sxs-lookup"><span data-stu-id="f3804-143">Remarks</span></span>

<span data-ttu-id="f3804-144">此電池 IOCTL 會抓取電池的目前標記。</span><span class="sxs-lookup"><span data-stu-id="f3804-144">This battery IOCTL retrieves the battery's current tag.</span></span> <span data-ttu-id="f3804-145">電池標籤是唯一的非零值，會在實體電池重新插入、更換或進行任何特性變更時變更。</span><span class="sxs-lookup"><span data-stu-id="f3804-145">The battery tag is a unique nonzero value that changes when the physical battery is reinserted, replaced, or undergoes any characteristic changes.</span></span> <span data-ttu-id="f3804-146">如需電池標記何時變更、如何偵測變更，以及應用程式應該在電池標記變更後如何進行的詳細資訊，請參閱 [電池資訊](battery-information.md) 總覽主題中的電池標記一節。</span><span class="sxs-lookup"><span data-stu-id="f3804-146">See the Battery Tags section in the [Battery Information](battery-information.md) overview topic for more detail on when a battery tag changes, how to detect the change, and how an application should proceed after a battery tag change.</span></span> <span data-ttu-id="f3804-147">當電池不存在時，此要求會等待指定的時間，如果仍然沒有電池，則會傳回 **\_ \_ \_ 找不** 到的錯誤檔案，並將電池標籤設為 **\_ \_ 無效** 的電池標記。</span><span class="sxs-lookup"><span data-stu-id="f3804-147">When a battery is not present, this request will wait the indicated time, and if there is still no battery present, then it will return **ERROR\_FILE\_NOT\_FOUND** and set the battery tag to **BATTERY\_TAG\_INVALID**.</span></span> <span data-ttu-id="f3804-148">如需詳細資訊， (查看電池資訊。 ) </span><span class="sxs-lookup"><span data-stu-id="f3804-148">(See Battery Information for more information.)</span></span>

<span data-ttu-id="f3804-149">所有的電池資訊要求都需要呼叫者提供相符的電池標記。</span><span class="sxs-lookup"><span data-stu-id="f3804-149">All requests for other battery information require the caller to supply the matching battery tag.</span></span> <span data-ttu-id="f3804-150">這可確保呼叫端會針對每個要求接收相同電池的資訊，並確保呼叫端知道電池變更，而不會進行持續輪詢。</span><span class="sxs-lookup"><span data-stu-id="f3804-150">This ensures that the caller is receiving information for the same battery for every request and ensures that the caller is aware of battery changes without constant polling.</span></span>

<span data-ttu-id="f3804-151">如需這項作業的重迭 i/o 含意，請參閱 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="f3804-151">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="f3804-152">範例</span><span class="sxs-lookup"><span data-stu-id="f3804-152">Examples</span></span>

<span data-ttu-id="f3804-153">如需範例，請參閱 [列舉電池裝置](enumerating-battery-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="f3804-153">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3804-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3804-154">Requirements</span></span>



| <span data-ttu-id="f3804-155">需求</span><span class="sxs-lookup"><span data-stu-id="f3804-155">Requirement</span></span> | <span data-ttu-id="f3804-156">值</span><span class="sxs-lookup"><span data-stu-id="f3804-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3804-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3804-157">Minimum supported client</span></span><br/> | <span data-ttu-id="f3804-158">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3804-158">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="f3804-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3804-159">Minimum supported server</span></span><br/> | <span data-ttu-id="f3804-160">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3804-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="f3804-161">標頭</span><span class="sxs-lookup"><span data-stu-id="f3804-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3804-162"><dt>Poclass .h;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP 上的 BatClass .h</dt></span><span class="sxs-lookup"><span data-stu-id="f3804-162"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3804-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3804-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3804-164">電池資訊</span><span class="sxs-lookup"><span data-stu-id="f3804-164">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="f3804-165">電源管理控制碼</span><span class="sxs-lookup"><span data-stu-id="f3804-165">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="f3804-166">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="f3804-166">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="f3804-167">**IOCTL \_ 電池 \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f3804-167">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="f3804-168">**IOCTL \_ 電池 \_ 查詢 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="f3804-168">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="f3804-169">**IOCTL \_ 電池 \_ 設定 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f3804-169">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

