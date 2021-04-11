---
description: 設定各種電池資訊。
ms.assetid: b827983d-5fb8-43f2-b732-541d16b3eb7b
title: 'IOCTL_BATTERY_SET_INFORMATION 控制程式代碼 (Poclass) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: f540037486f16e920b3346620ff934b279652e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849272"
---
# <a name="ioctl_battery_set_information-control-code"></a><span data-ttu-id="0ae71-103">IOCTL \_ 電池 \_ 設定 \_ 資訊控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="0ae71-103">IOCTL\_BATTERY\_SET\_INFORMATION control code</span></span>

<span data-ttu-id="0ae71-104">設定各種電池資訊。</span><span class="sxs-lookup"><span data-stu-id="0ae71-104">Sets various battery information.</span></span> <span data-ttu-id="0ae71-105">輸入參數結構（ [**電池 \_ 設定 \_ 資訊**](battery-set-information-str.md)）表示要設定的電池狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="0ae71-105">The input parameter structure, [**BATTERY\_SET\_INFORMATION**](battery-set-information-str.md), indicates which battery status information is to be set.</span></span>

<span data-ttu-id="0ae71-106">若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="0ae71-106">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to battery
  IOCTL_BATTERY_SET_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // lpOutBuffer
  0,                             // nOutBufferSize
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="0ae71-107">參數</span><span class="sxs-lookup"><span data-stu-id="0ae71-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ae71-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="0ae71-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="0ae71-109">要設定資訊之電池的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0ae71-109">A handle to the battery on which the information is to be set.</span></span> <span data-ttu-id="0ae71-110">若要取出設備控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式。</span><span class="sxs-lookup"><span data-stu-id="0ae71-110">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="0ae71-111">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="0ae71-111">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="0ae71-112">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="0ae71-112">The control code for the operation.</span></span> <span data-ttu-id="0ae71-113">此值會識別要執行的特定作業，以及要在其上執行的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="0ae71-113">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="0ae71-114">請使用 **IOCTL \_ 電池 \_ 集 \_ 資訊** 進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="0ae71-114">Use **IOCTL\_BATTERY\_SET\_INFORMATION** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="0ae71-115">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="0ae71-115">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="0ae71-116">[**電池 \_ 設定 \_ 資訊**](battery-set-information-str.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="0ae71-116">A pointer to a [**BATTERY\_SET\_INFORMATION**](battery-set-information-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0ae71-117">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="0ae71-117">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="0ae71-118">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0ae71-118">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0ae71-119">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="0ae71-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="0ae71-120">未搭配此作業使用;設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0ae71-120">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0ae71-121">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="0ae71-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="0ae71-122">未搭配此作業使用;設定為零。</span><span class="sxs-lookup"><span data-stu-id="0ae71-122">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="0ae71-123">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="0ae71-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="0ae71-124">變數的指標，此變數會接收 *lpOutBuffer* 緩衝區中傳回的資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0ae71-124">A pointer to a variable that receives the size of data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="0ae71-125">如果輸出緩衝區太小而無法傳回任何資料，則呼叫會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤碼錯誤的 \_ \_ 緩衝區，而傳回的位元組計數為零。</span><span class="sxs-lookup"><span data-stu-id="0ae71-125">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="0ae71-126">如果 *lpOverlapped* 為 **null** (nonoverlapped I/o) ，即使 *lpOutBuffer* 為 **Null**， *lpBytesReturned* 也不能是 **null**。</span><span class="sxs-lookup"><span data-stu-id="0ae71-126">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**, even if *lpOutBuffer* is **NULL**.</span></span>

<span data-ttu-id="0ae71-127">如果 *lpOverlapped* 不是 **null** (重迭的 i/o) ， *lpBytesReturned* 可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="0ae71-127">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="0ae71-128">如果這是重迭的作業，您可以藉由呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="0ae71-128">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="0ae71-129">如果 *hDevice* 與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="0ae71-129">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="0ae71-130">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="0ae71-130">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="0ae71-131">重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="0ae71-131">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="0ae71-132">如果使用檔案旗標重迭旗標開啟 *hDevice* \_ \_ ， *lpOverlapped* 必須指向有效的 [](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)重迭結構。</span><span class="sxs-lookup"><span data-stu-id="0ae71-132">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="0ae71-133">在此情況下， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會以 (非同步) 作業的重迭方式執行。</span><span class="sxs-lookup"><span data-stu-id="0ae71-133">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="0ae71-134">如果裝置是以檔案旗標重迭旗標開啟， \_ \_ 且 *lpOverlapped* 為 **Null**，則函式會以無法預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="0ae71-134">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="0ae71-135">如果在未指定檔案旗標重迭旗標的情況下開啟 *hDevice* \_ ，則 \_ 會忽略 *lpOverlapped* ，並且在作業完成或發生錯誤之前，不會傳回 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="0ae71-135">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ae71-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ae71-136">Return value</span></span>

<span data-ttu-id="0ae71-137">如果作業順利完成， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="0ae71-137">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="0ae71-138">如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="0ae71-138">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="0ae71-139">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="0ae71-139">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ae71-140">備註</span><span class="sxs-lookup"><span data-stu-id="0ae71-140">Remarks</span></span>

<span data-ttu-id="0ae71-141">如果要求的電池標籤與 \_ \_ 目前的電池標記不符，則所有設定電池資訊的要求都會完成，並出現「找不到錯誤檔案的狀態」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0ae71-141">All requests to set battery information will complete with the status of ERROR\_FILE\_NOT\_FOUND if the battery tag of the request does not match that of the current battery tag.</span></span>

<span data-ttu-id="0ae71-142">如需這項作業的重迭 i/o 含意，請參閱 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="0ae71-142">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ae71-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ae71-143">Requirements</span></span>



| <span data-ttu-id="0ae71-144">需求</span><span class="sxs-lookup"><span data-stu-id="0ae71-144">Requirement</span></span> | <span data-ttu-id="0ae71-145">值</span><span class="sxs-lookup"><span data-stu-id="0ae71-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ae71-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ae71-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0ae71-147">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ae71-147">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="0ae71-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ae71-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0ae71-149">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ae71-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="0ae71-150">標頭</span><span class="sxs-lookup"><span data-stu-id="0ae71-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ae71-151"><dt>Poclass .h;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP 上的 Batclass .h</dt></span><span class="sxs-lookup"><span data-stu-id="0ae71-151"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ae71-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ae71-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ae71-153">電池資訊</span><span class="sxs-lookup"><span data-stu-id="0ae71-153">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="0ae71-154">電源管理控制碼</span><span class="sxs-lookup"><span data-stu-id="0ae71-154">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="0ae71-155">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="0ae71-155">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="0ae71-156">**電池 \_ 設定 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="0ae71-156">**BATTERY\_SET\_INFORMATION**</span></span>](battery-set-information-str.md)
</dt> <dt>

[<span data-ttu-id="0ae71-157">**IOCTL \_ 電池 \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="0ae71-157">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="0ae71-158">**IOCTL \_ 電池 \_ 查詢 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="0ae71-158">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="0ae71-159">**IOCTL \_ 電池 \_ 查詢 \_ 標記**</span><span class="sxs-lookup"><span data-stu-id="0ae71-159">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> </dl>

 

