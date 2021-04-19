---
description: 等候指定磁片上的所有磁片區都可供使用。
ms.assetid: 6cf619bb-7ff5-485e-b533-0f7f6503c6e0
title: 'IOCTL_DISK_ARE_VOLUMES_READY 控制程式代碼 (Ntdddisk) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_ARE_VOLUMES_READY
api_type:
- HeaderDef
api_location:
- ntdddisk.h
ms.openlocfilehash: dc4457af2ce6e7759ef879900803504933a09978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979357"
---
# <a name="ioctl_disk_are_volumes_ready-control-code"></a><span data-ttu-id="290c3-103">IOCTL \_ 磁片 \_ 是磁片區 \_ \_ 就緒控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="290c3-103">IOCTL\_DISK\_ARE\_VOLUMES\_READY control code</span></span>

<span data-ttu-id="290c3-104">等候指定磁片上的所有磁片區都可供使用。</span><span class="sxs-lookup"><span data-stu-id="290c3-104">Waits for all volumes on the specified disk to be ready for use.</span></span>

<span data-ttu-id="290c3-105">若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="290c3-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_ARE_VOLUMES_READY,   // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       NULL,            // lpOutBuffer 
                 (DWORD)        0,               // nOutBufferSize
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="290c3-106">參數</span><span class="sxs-lookup"><span data-stu-id="290c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="290c3-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="290c3-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="290c3-108">磁片的控制碼。</span><span class="sxs-lookup"><span data-stu-id="290c3-108">A handle to the disk.</span></span>

<span data-ttu-id="290c3-109">若要取出設備控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式。</span><span class="sxs-lookup"><span data-stu-id="290c3-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="290c3-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="290c3-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="290c3-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="290c3-111">The control code for the operation.</span></span>

<span data-ttu-id="290c3-112">您 **\_ \_ \_ \_ 可以使用 IOCTL 磁片** 來進行此作業。</span><span class="sxs-lookup"><span data-stu-id="290c3-112">Use **IOCTL\_DISK\_ARE\_VOLUMES\_READY** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="290c3-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="290c3-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="290c3-114">未搭配此作業使用。</span><span class="sxs-lookup"><span data-stu-id="290c3-114">Not used with this operation.</span></span> <span data-ttu-id="290c3-115">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="290c3-115">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="290c3-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="290c3-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="290c3-117">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="290c3-117">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="290c3-118">設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="290c3-118">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="290c3-119">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="290c3-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="290c3-120">未搭配此作業使用。</span><span class="sxs-lookup"><span data-stu-id="290c3-120">Not used with this operation.</span></span> <span data-ttu-id="290c3-121">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="290c3-121">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="290c3-122">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="290c3-122">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="290c3-123">未搭配此作業使用。</span><span class="sxs-lookup"><span data-stu-id="290c3-123">Not used with this operation.</span></span> <span data-ttu-id="290c3-124">設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="290c3-124">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="290c3-125">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="290c3-125">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="290c3-126">未搭配此作業使用。</span><span class="sxs-lookup"><span data-stu-id="290c3-126">Not used with this operation.</span></span> <span data-ttu-id="290c3-127">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="290c3-127">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="290c3-128">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="290c3-128">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="290c3-129">重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="290c3-129">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="290c3-130">如果在未指定檔案 **\_ 旗 \_** 標的情況下開啟 *hDevice* ，則會忽略 *lpOverlapped* 。</span><span class="sxs-lookup"><span data-stu-id="290c3-130">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="290c3-131">如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="290c3-131">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="290c3-132">在此情況下， *lpOverlapped* 必須指向包含事件物件控制碼 [**的有效重**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 迭結構。</span><span class="sxs-lookup"><span data-stu-id="290c3-132">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="290c3-133">否則，函式會以無法預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="290c3-133">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="290c3-134">針對重迭的作業， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會立即傳回，而當作業完成時，就會發出事件物件的信號。</span><span class="sxs-lookup"><span data-stu-id="290c3-134">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="290c3-135">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="290c3-135">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="290c3-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="290c3-136">Return value</span></span>

<span data-ttu-id="290c3-137">如果作業順利完成，表示磁片上的所有磁片區都已備妥可供使用， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="290c3-137">If the operation completes successfully, indicating that all volumes on the disk are ready for use, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="290c3-138">如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="290c3-138">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="290c3-139">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="290c3-139">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="290c3-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="290c3-140">Requirements</span></span>



| <span data-ttu-id="290c3-141">需求</span><span class="sxs-lookup"><span data-stu-id="290c3-141">Requirement</span></span> | <span data-ttu-id="290c3-142">值</span><span class="sxs-lookup"><span data-stu-id="290c3-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="290c3-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="290c3-143">Minimum supported client</span></span><br/> | <span data-ttu-id="290c3-144">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="290c3-144">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="290c3-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="290c3-145">Minimum supported server</span></span><br/> | <span data-ttu-id="290c3-146">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="290c3-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="290c3-147">標頭</span><span class="sxs-lookup"><span data-stu-id="290c3-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="290c3-148"><dt>Ntdddisk。h</dt></span><span class="sxs-lookup"><span data-stu-id="290c3-148"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="290c3-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="290c3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="290c3-150">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="290c3-150">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="290c3-151">磁片管理控制碼</span><span class="sxs-lookup"><span data-stu-id="290c3-151">Disk Management Control Codes</span></span>](disk-management-control-codes.md)
</dt> </dl>

 

