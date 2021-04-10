---
description: 抓取各種不同的電池資訊。
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: 'IOCTL_BATTERY_QUERY_INFORMATION 控制程式代碼 (Poclass) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: ee4010e055686c0df2987c34b48b133975b434ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944239"
---
# <a name="ioctl_battery_query_information-control-code"></a><span data-ttu-id="ee03d-103">IOCTL \_ 電池 \_ 查詢 \_ 資訊控制項程式碼</span><span class="sxs-lookup"><span data-stu-id="ee03d-103">IOCTL\_BATTERY\_QUERY\_INFORMATION control code</span></span>

<span data-ttu-id="ee03d-104">抓取各種不同的電池資訊。</span><span class="sxs-lookup"><span data-stu-id="ee03d-104">Retrieves a variety of information for the battery.</span></span>

<span data-ttu-id="ee03d-105">若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="ee03d-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to battery
  IOCTL_BATTERY_QUERY_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="ee03d-106">參數</span><span class="sxs-lookup"><span data-stu-id="ee03d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee03d-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="ee03d-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="ee03d-108">要傳回其資訊之電池的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ee03d-108">A handle to the battery on which information is to be returned.</span></span> <span data-ttu-id="ee03d-109">若要取出設備控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式。</span><span class="sxs-lookup"><span data-stu-id="ee03d-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="ee03d-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="ee03d-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="ee03d-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="ee03d-111">The control code for the operation.</span></span> <span data-ttu-id="ee03d-112">此值會識別要執行的特定作業，以及要在其上執行的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="ee03d-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="ee03d-113">使用 **IOCTL \_ 電池 \_ 查詢 \_ 資訊** 進行此作業。</span><span class="sxs-lookup"><span data-stu-id="ee03d-113">Use **IOCTL\_BATTERY\_QUERY\_INFORMATION** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="ee03d-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="ee03d-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="ee03d-115">[**電池 \_ 查詢 \_ 資訊**](battery-query-information-str.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ee03d-115">A pointer to a [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ee03d-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="ee03d-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="ee03d-117">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ee03d-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ee03d-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="ee03d-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="ee03d-119">傳回緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="ee03d-119">A pointer to the return buffer.</span></span> <span data-ttu-id="ee03d-120"> (的資料類型，因此，大小) 的傳回緩衝區，取決於輸入 [**電池 \_ 查詢 \_ 資訊**](battery-query-information-str.md)結構的 **電池 \_ 查詢 \_ 資訊 \_ 層級** 成員所要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="ee03d-120">The data type (and, therefore, size) of the return buffer depends on the information requested in the **BATTERY\_QUERY\_INFORMATION\_LEVEL** member of the input [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure.</span></span>

<span data-ttu-id="ee03d-121">下表顯示指定的資訊層級所傳回的資料。</span><span class="sxs-lookup"><span data-stu-id="ee03d-121">The following table shows the data returned by a given information level.</span></span>



| <span data-ttu-id="ee03d-122">資訊層級</span><span class="sxs-lookup"><span data-stu-id="ee03d-122">Information level</span></span>                 | <span data-ttu-id="ee03d-123">傳回的資料</span><span class="sxs-lookup"><span data-stu-id="ee03d-123">Data returned</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee03d-124">**BatteryDeviceName**</span><span class="sxs-lookup"><span data-stu-id="ee03d-124">**BatteryDeviceName**</span></span>             | <span data-ttu-id="ee03d-125">以 **Null** 結束的 Unicode 字串，指定電池的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee03d-125">**Null**-terminated Unicode string that specifies the battery's name.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ee03d-126">**BatteryEstimatedTime**</span><span class="sxs-lookup"><span data-stu-id="ee03d-126">**BatteryEstimatedTime**</span></span>          | <span data-ttu-id="ee03d-127">指定預估電池執行時間（以秒為單位）的 **ULONG** 。</span><span class="sxs-lookup"><span data-stu-id="ee03d-127">A **ULONG** that specifies estimated battery run time, in seconds.</span></span> <span data-ttu-id="ee03d-128">如果 [**電池 \_ 查詢 \_ 資訊**](battery-query-information-str.md)結構的 **AtRate** 成員中提供的清空率為零，則此計算是以目前的清空率為基礎。</span><span class="sxs-lookup"><span data-stu-id="ee03d-128">If the rate of drain provided in the **AtRate** member of the [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure is zero, this calculation is based on the present rate of drain.</span></span> <span data-ttu-id="ee03d-129">如果 **AtRate** 為非零值，則傳回的時間會是指定速率的預期執行時間。</span><span class="sxs-lookup"><span data-stu-id="ee03d-129">If **AtRate** is nonzero, the time returned is the expected run time for the given rate.</span></span> <span data-ttu-id="ee03d-130">如果預估的時間不明 (例如，電池未放電，且 **AtRate** 為零) ，則會傳回 **電池 \_ 未知 \_ 時間** 。</span><span class="sxs-lookup"><span data-stu-id="ee03d-130">If the estimated time is unknown (for example, the battery is not discharging and **AtRate** is zero), **BATTERY\_UNKNOWN\_TIME** is returned.</span></span> <span data-ttu-id="ee03d-131">請注意，在某些電池系統上，此值不太精確。</span><span class="sxs-lookup"><span data-stu-id="ee03d-131">Note that this value is not very accurate on some battery systems.</span></span> <span data-ttu-id="ee03d-132">此值可能會因為目前的電源使用量而有很大的差異，這可能會受到磁片活動和其他因素所影響。</span><span class="sxs-lookup"><span data-stu-id="ee03d-132">The value may vary widely depending on present power usage, which could be affected by disk activity and other factors.</span></span> <span data-ttu-id="ee03d-133">此值的變更不會有任何通知機制。</span><span class="sxs-lookup"><span data-stu-id="ee03d-133">There is no notification mechanism for changes in this value.</span></span> |
| <span data-ttu-id="ee03d-134">**BatteryGranularityInformation**</span><span class="sxs-lookup"><span data-stu-id="ee03d-134">**BatteryGranularityInformation**</span></span> | <span data-ttu-id="ee03d-135">[**電池 \_ 報告 \_ 規模**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)結構的可變長度陣列，包含從 [**IOCTL \_ 電池 \_ 查詢 \_ 狀態**](ioctl-battery-query-status.md)傳回之電池容量的報告資料細微性。</span><span class="sxs-lookup"><span data-stu-id="ee03d-135">A variable-length array of [**BATTERY\_REPORTING\_SCALE**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) structures that contains the reporting granularity for the battery capacity that is returned from [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md).</span></span> <span data-ttu-id="ee03d-136">當資料細微性相依于電池的目前容量時，就會傳回多個專案。</span><span class="sxs-lookup"><span data-stu-id="ee03d-136">Multiple entries are returned when the granularity depends on the present capacity of the battery.</span></span> <span data-ttu-id="ee03d-137">如需專案陣列的解讀，請參閱 **電池 \_ 報告 \_ 規模** 。</span><span class="sxs-lookup"><span data-stu-id="ee03d-137">See **BATTERY\_REPORTING\_SCALE** for the interpretation of the array of entries.</span></span> <span data-ttu-id="ee03d-138">專案數目是以傳回的緩衝區大小來表示，並可計算為 (*lpBytesReturned* /Sizeof (**電池 \_ 報表 \_ 規模**) ) 。</span><span class="sxs-lookup"><span data-stu-id="ee03d-138">The number of entries is indicated by the size of the buffer returned, and can be calculated as (*lpBytesReturned* / sizeof (**BATTERY\_REPORTING\_SCALE**)).</span></span> <span data-ttu-id="ee03d-139">將傳回的專案數上限為四個。</span><span class="sxs-lookup"><span data-stu-id="ee03d-139">The maximum number of entries that will be returned is four.</span></span>                                                                                                |
| <span data-ttu-id="ee03d-140">**BatteryInformation**</span><span class="sxs-lookup"><span data-stu-id="ee03d-140">**BatteryInformation**</span></span>            | <span data-ttu-id="ee03d-141">[**電池 \_ 資訊**](battery-information-str.md)結構。</span><span class="sxs-lookup"><span data-stu-id="ee03d-141">A [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ee03d-142">**BatteryManufactureDate**</span><span class="sxs-lookup"><span data-stu-id="ee03d-142">**BatteryManufactureDate**</span></span>        | <span data-ttu-id="ee03d-143">[**電池 \_ 製造 \_ 日期**](battery-manufacture-date-str.md)結構。</span><span class="sxs-lookup"><span data-stu-id="ee03d-143">A [**BATTERY\_MANUFACTURE\_DATE**](battery-manufacture-date-str.md) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="ee03d-144">**BatteryManufactureName**</span><span class="sxs-lookup"><span data-stu-id="ee03d-144">**BatteryManufactureName**</span></span>        | <span data-ttu-id="ee03d-145">以 **Null** 終止的 Unicode 字串，其中包含電池製造商的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee03d-145">**Null**-terminated Unicode string that contains the name of the manufacturer of the battery.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="ee03d-146">**BatterySerialNumber**</span><span class="sxs-lookup"><span data-stu-id="ee03d-146">**BatterySerialNumber**</span></span>           | <span data-ttu-id="ee03d-147">以 **Null** 終止的 Unicode 字串，其中包含電池的序號。</span><span class="sxs-lookup"><span data-stu-id="ee03d-147">**Null**-terminated Unicode string that contains the battery's serial number.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="ee03d-148">**BatteryTemperature**</span><span class="sxs-lookup"><span data-stu-id="ee03d-148">**BatteryTemperature**</span></span>            | <span data-ttu-id="ee03d-149">包含電池目前溫度的 **ULONG** ，以10ths 角度的角度。</span><span class="sxs-lookup"><span data-stu-id="ee03d-149">A **ULONG** that contains the battery's current temperature, in 10ths of a degree Kelvin.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ee03d-150">**BatteryUniqueID**</span><span class="sxs-lookup"><span data-stu-id="ee03d-150">**BatteryUniqueID**</span></span>               | <span data-ttu-id="ee03d-151">以 **Null** 結束的 Unicode 字串，可唯一識別電池。</span><span class="sxs-lookup"><span data-stu-id="ee03d-151">**Null**-terminated Unicode string that uniquely identifies the battery.</span></span> <span data-ttu-id="ee03d-152">這個值可以用來追蹤特定電池。</span><span class="sxs-lookup"><span data-stu-id="ee03d-152">This value can be used to track a specific battery.</span></span> <span data-ttu-id="ee03d-153">在智慧電池的情況下，此識別碼將會是製造商名稱、裝置名稱、製造日期，以及序號可列印標記法的串連。</span><span class="sxs-lookup"><span data-stu-id="ee03d-153">In the case of smart batteries, this ID will be the concatenation of the manufacturer's name, device name, date of manufacture, and a printable representation of the serial number.</span></span> <span data-ttu-id="ee03d-154">此值不適合顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="ee03d-154">This value is not intended to be displayed to the user.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="ee03d-155">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="ee03d-155">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="ee03d-156">輸出緩衝區的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="ee03d-156">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="ee03d-157">根據所要求資料的資訊層級，這可能是大小可變大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ee03d-157">Depending on the information level of data requested, this may be a variably sized buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ee03d-158">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="ee03d-158">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="ee03d-159">變數的指標，此變數會接收 *lpOutBuffer* 緩衝區中傳回的資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ee03d-159">A pointer to a variable that receives the size of the data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="ee03d-160">如果輸出緩衝區太小而無法傳回任何資料，則呼叫會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤碼 **錯誤 \_ 的 \_ 緩衝區**，而傳回的位元組計數為零。</span><span class="sxs-lookup"><span data-stu-id="ee03d-160">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="ee03d-161">如果 *lpOverlapped* 為 **null** (nonoverlapped I/o) ，則 *lpBytesReturned* 不可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="ee03d-161">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="ee03d-162">如果 *lpOverlapped* 不是 **null** (重迭的 i/o) ， *lpBytesReturned* 可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="ee03d-162">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="ee03d-163">如果這是重迭的作業，您可以藉由呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ee03d-163">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="ee03d-164">如果 *hDevice* 與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ee03d-164">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="ee03d-165">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="ee03d-165">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="ee03d-166">重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="ee03d-166">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="ee03d-167">如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice， *lpOverlapped* 必須 [**指向有效的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)重迭結構。</span><span class="sxs-lookup"><span data-stu-id="ee03d-167">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="ee03d-168">在此情況下， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會以 (非同步) 作業的重迭方式執行。</span><span class="sxs-lookup"><span data-stu-id="ee03d-168">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="ee03d-169">如果裝置是以檔案 **旗標重 \_ \_** 迭旗標開啟，且 *lpOverlapped* 為 **Null**，則函式會以無法預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="ee03d-169">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="ee03d-170">如果在未指定檔案 **\_ 旗 \_** 標重迭旗標的情況下開啟 hDevice，則會忽略 *lpOverlapped* ，並且在作業完成或發生錯誤之前，不會傳回 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)函數。</span><span class="sxs-lookup"><span data-stu-id="ee03d-170">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee03d-171">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee03d-171">Return value</span></span>

<span data-ttu-id="ee03d-172">如果作業順利完成， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="ee03d-172">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="ee03d-173">如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="ee03d-173">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="ee03d-174">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="ee03d-174">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="ee03d-175">某些電池的相關資訊是選擇性的，或可能對某些電池沒有意義。</span><span class="sxs-lookup"><span data-stu-id="ee03d-175">Some information about batteries is optional or may be meaningless for some batteries.</span></span> <span data-ttu-id="ee03d-176">如果目前的電池無法使用所要求的特定資料類型，則會傳回 **錯誤 \_ 無效 \_** 的函式。</span><span class="sxs-lookup"><span data-stu-id="ee03d-176">If the particular type of data requested is not available for the current battery, then **ERROR\_INVALID\_FUNCTION** is returned.</span></span>

<span data-ttu-id="ee03d-177">所有的電池資訊要求都會完成，並在要求的 **BatteryTag** 元素不符合目前電池標記的時 **\_ \_ \_ 找不到錯誤** 檔案的狀態。</span><span class="sxs-lookup"><span data-stu-id="ee03d-177">All requests for battery information will complete with the status of **ERROR\_FILE\_NOT\_FOUND** whenever the **BatteryTag** element of the request does not match that of the current battery tag.</span></span> <span data-ttu-id="ee03d-178">這可確保傳回的電池資訊符合要求電池的資訊。</span><span class="sxs-lookup"><span data-stu-id="ee03d-178">This ensures that the returned battery information matches that of the requested battery.</span></span> <span data-ttu-id="ee03d-179"> (查看 [電池標記](battery-information.md) 以取得詳細資訊。 ) </span><span class="sxs-lookup"><span data-stu-id="ee03d-179">(See [Battery Tags](battery-information.md) for more information.)</span></span>

## <a name="remarks"></a><span data-ttu-id="ee03d-180">備註</span><span class="sxs-lookup"><span data-stu-id="ee03d-180">Remarks</span></span>

<span data-ttu-id="ee03d-181">此電池 IOCTL 會抓取各種不同的電池資訊。</span><span class="sxs-lookup"><span data-stu-id="ee03d-181">This battery IOCTL retrieves a variety of information for the battery.</span></span> <span data-ttu-id="ee03d-182">輸入參數結構（ [**電池 \_ 查詢 \_ 資訊**](battery-query-information-str.md)）表示要傳回的資訊類型，以及應傳回的電池資訊。</span><span class="sxs-lookup"><span data-stu-id="ee03d-182">The input parameter structure, [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md), indicates the type of information to be returned and when the battery information should be returned.</span></span> <span data-ttu-id="ee03d-183">輸出緩衝區的資料類型和內容會根據所要求的資料而有所不同。</span><span class="sxs-lookup"><span data-stu-id="ee03d-183">The data type and contents of the output buffer vary based on the data requested.</span></span>

<span data-ttu-id="ee03d-184">如需這項作業的重迭 i/o 含意，請參閱 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="ee03d-184">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="ee03d-185">範例</span><span class="sxs-lookup"><span data-stu-id="ee03d-185">Examples</span></span>

<span data-ttu-id="ee03d-186">如需範例，請參閱 [列舉電池裝置](enumerating-battery-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="ee03d-186">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee03d-187">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee03d-187">Requirements</span></span>



| <span data-ttu-id="ee03d-188">需求</span><span class="sxs-lookup"><span data-stu-id="ee03d-188">Requirement</span></span> | <span data-ttu-id="ee03d-189">值</span><span class="sxs-lookup"><span data-stu-id="ee03d-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee03d-190">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee03d-190">Minimum supported client</span></span><br/> | <span data-ttu-id="ee03d-191">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee03d-191">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="ee03d-192">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee03d-192">Minimum supported server</span></span><br/> | <span data-ttu-id="ee03d-193">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee03d-193">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="ee03d-194">標頭</span><span class="sxs-lookup"><span data-stu-id="ee03d-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee03d-195"><dt>Poclass .h;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP 上的 BatClass .h</dt></span><span class="sxs-lookup"><span data-stu-id="ee03d-195"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee03d-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee03d-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee03d-197">電池資訊</span><span class="sxs-lookup"><span data-stu-id="ee03d-197">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="ee03d-198">電源管理控制碼</span><span class="sxs-lookup"><span data-stu-id="ee03d-198">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="ee03d-199">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="ee03d-199">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="ee03d-200">**電池 \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="ee03d-200">**BATTERY\_QUERY\_INFORMATION**</span></span>](battery-query-information-str.md)
</dt> <dt>

[<span data-ttu-id="ee03d-201">**電池 \_ 報告 \_ 規模**</span><span class="sxs-lookup"><span data-stu-id="ee03d-201">**BATTERY\_REPORTING\_SCALE**</span></span>](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[<span data-ttu-id="ee03d-202">**IOCTL \_ 電池 \_ 查詢 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="ee03d-202">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="ee03d-203">**IOCTL \_ 電池 \_ 查詢 \_ 標記**</span><span class="sxs-lookup"><span data-stu-id="ee03d-203">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> <dt>

[<span data-ttu-id="ee03d-204">**IOCTL \_ 電池 \_ 設定 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="ee03d-204">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

