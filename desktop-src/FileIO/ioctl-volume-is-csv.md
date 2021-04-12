---
description: 判斷磁片區是否為 CSV 磁片區。
ms.assetid: 6B09B519-1E2F-4757-AAD5-1E4C81023E14
title: 'IOCTL_VOLUME_IS_CSV 控制程式代碼 (Ntddvol) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VOLUME_IS_CSV
api_type:
- HeaderDef
api_location:
- Ntddvol.h
ms.openlocfilehash: 8121e1b89c88ad05a2c2be8537d7170bfabfc412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320392"
---
# <a name="ioctl_volume_is_csv-control-code"></a><span data-ttu-id="972b4-103">IOCTL \_ 磁片區 \_ 是 \_ CSV 控制項程式碼</span><span class="sxs-lookup"><span data-stu-id="972b4-103">IOCTL\_VOLUME\_IS\_CSV control code</span></span>

<span data-ttu-id="972b4-104">判斷磁片區是否為 CSV 磁片區。</span><span class="sxs-lookup"><span data-stu-id="972b4-104">Determines whether a volume is a CSV volume.</span></span>

<span data-ttu-id="972b4-105">若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="972b4-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to device
                 IOCTL_VOLUME_IS_CSV,           // dwIoControlCode
                 NULL,                          // input buffer
                 0,                             // size of input buffer
                 (LPVOID) lpOutBuffer,          // lpOutBuffer
                 (DWORD) nOutBufferSize,        // nOutBufferSize
                 (LPDWORD) lpBytesReturned,     // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="972b4-106">參數</span><span class="sxs-lookup"><span data-stu-id="972b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="972b4-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="972b4-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="972b4-108">磁片區的控制碼。</span><span class="sxs-lookup"><span data-stu-id="972b4-108">A handle to the volume.</span></span> <span data-ttu-id="972b4-109">若要取出磁片區控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函數。</span><span class="sxs-lookup"><span data-stu-id="972b4-109">To retrieve a volume handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="972b4-110">只有系統管理員可以開啟磁片區控制碼。</span><span class="sxs-lookup"><span data-stu-id="972b4-110">Only administrators can open volume handles.</span></span>

</dd> <dt>

<span data-ttu-id="972b4-111">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="972b4-111">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="972b4-112">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="972b4-112">The control code for the operation.</span></span> <span data-ttu-id="972b4-113">針對這項作業，使用 **IOCTL \_ 磁片區 \_ 是 \_ CSV** 。</span><span class="sxs-lookup"><span data-stu-id="972b4-113">Use **IOCTL\_VOLUME\_IS\_CSV** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="972b4-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="972b4-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="972b4-115">未搭配此作業使用;設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="972b4-115">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="972b4-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="972b4-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="972b4-117">未搭配此作業使用;設定為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="972b4-117">Not used with this operation; set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="972b4-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="972b4-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="972b4-119">如果磁片區是 CSV 磁片區，則為 **TRUE** 的指標;否則，函式呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="972b4-119">A pointer to **TRUE** if the volume is a CSV volume; otherwise, the function call fails.</span></span>

</dd> <dt>

<span data-ttu-id="972b4-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="972b4-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="972b4-121">輸出緩衝區的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="972b4-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="972b4-122">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="972b4-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="972b4-123">變數的指標，此變數會接收儲存在輸出緩衝區中的資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="972b4-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="972b4-124">如果 *lpOverlapped* 為 **null**，則 *lpBytesReturned* 不可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="972b4-124">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="972b4-125">即使作業未傳回輸出資料，而且 *lpOutBuffer* 為 **Null**， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 也會使用 *lpBytesReturned*。</span><span class="sxs-lookup"><span data-stu-id="972b4-125">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="972b4-126">在這類作業之後， *lpBytesReturned* 的值就沒有意義。</span><span class="sxs-lookup"><span data-stu-id="972b4-126">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="972b4-127">如果 *lpOverlapped* 不是 **null**， *lpBytesReturned* 可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="972b4-127">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="972b4-128">如果這個參數不是 **Null** ，而且作業傳回資料，則 *lpBytesReturned* 會在重迭的作業完成之前無意義。</span><span class="sxs-lookup"><span data-stu-id="972b4-128">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="972b4-129">若要取出傳回的位元組數目，請呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult)。</span><span class="sxs-lookup"><span data-stu-id="972b4-129">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="972b4-130">如果 *hDevice* 與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="972b4-130">If *hDevice* is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="972b4-131">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="972b4-131">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="972b4-132">重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="972b4-132">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="972b4-133">如果在未指定檔案 **\_ 旗 \_** 標的情況下開啟 *hDevice* ，則會忽略 *lpOverlapped* 。</span><span class="sxs-lookup"><span data-stu-id="972b4-133">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="972b4-134">如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="972b4-134">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="972b4-135">在此情況下， *lpOverlapped* 必須指向包含事件物件控制碼 [**的有效重**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 迭結構。</span><span class="sxs-lookup"><span data-stu-id="972b4-135">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="972b4-136">否則，函式會以無法預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="972b4-136">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="972b4-137">針對重迭的作業， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會立即傳回，而當作業完成時，就會發出事件物件的信號。</span><span class="sxs-lookup"><span data-stu-id="972b4-137">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="972b4-138">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="972b4-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="972b4-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="972b4-139">Return value</span></span>

<span data-ttu-id="972b4-140">如果作業順利完成， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="972b4-140">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="972b4-141">如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="972b4-141">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero (0).</span></span> <span data-ttu-id="972b4-142">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="972b4-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="972b4-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="972b4-143">Requirements</span></span>



| <span data-ttu-id="972b4-144">需求</span><span class="sxs-lookup"><span data-stu-id="972b4-144">Requirement</span></span> | <span data-ttu-id="972b4-145">值</span><span class="sxs-lookup"><span data-stu-id="972b4-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="972b4-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="972b4-146">Minimum supported client</span></span><br/> | <span data-ttu-id="972b4-147">都不支援</span><span class="sxs-lookup"><span data-stu-id="972b4-147">None supported</span></span><br/>                                                            |
| <span data-ttu-id="972b4-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="972b4-148">Minimum supported server</span></span><br/> | <span data-ttu-id="972b4-149">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="972b4-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="972b4-150">標頭</span><span class="sxs-lookup"><span data-stu-id="972b4-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="972b4-151"><dt>Ntddvol。h</dt></span><span class="sxs-lookup"><span data-stu-id="972b4-151"><dt>Ntddvol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="972b4-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="972b4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="972b4-153">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="972b4-153">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="972b4-154">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="972b4-154">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="972b4-155">磁碟區管理控制碼</span><span class="sxs-lookup"><span data-stu-id="972b4-155">Volume Management Control Codes</span></span>](volume-management-control-codes.md)
</dt> </dl>

 

