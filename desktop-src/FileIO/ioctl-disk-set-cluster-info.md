---
description: 設定磁片上的叢集資訊。
ms.assetid: AB2243D9-4913-4412-87E0-2C8DB8AB10B8
title: 'IOCTL_DISK_SET_CLUSTER_INFO 控制程式代碼 (Ntdddisk) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_SET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 4ba0994dd1c9030e84c22e24b1eb4583eba7e3d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988990"
---
# <a name="ioctl_disk_set_cluster_info-control-code"></a><span data-ttu-id="f4ef1-103">IOCTL \_ 磁片 \_ 設定 \_ 叢集 \_ 資訊控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="f4ef1-103">IOCTL\_DISK\_SET\_CLUSTER\_INFO control code</span></span>

<span data-ttu-id="f4ef1-104">設定磁片上的叢集資訊。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-104">Sets the cluster information on a disk.</span></span>

<span data-ttu-id="f4ef1-105">若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_SET_CLUSTER_INFO,    // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="f4ef1-106">參數</span><span class="sxs-lookup"><span data-stu-id="f4ef1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4ef1-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="f4ef1-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="f4ef1-108">磁片的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-108">A handle to the disk.</span></span>

<span data-ttu-id="f4ef1-109">若要取出設備控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="f4ef1-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="f4ef1-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="f4ef1-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-111">The control code for the operation.</span></span>

<span data-ttu-id="f4ef1-112">請使用 **IOCTL \_ 磁片集叢集 \_ \_ \_ 資訊** 進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-112">Use **IOCTL\_DISK\_SET\_CLUSTER\_INFO** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="f4ef1-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="f4ef1-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f4ef1-114">[**磁片 \_ 群集 \_ 資訊**](disk-cluster-info.md)資料結構的指標，其中包含磁片的叢集資訊。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-114">A pointer to a [**DISK\_CLUSTER\_INFO**](disk-cluster-info.md) data structure that contains cluster information for the disk.</span></span>

</dd> <dt>

<span data-ttu-id="f4ef1-115">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="f4ef1-115">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f4ef1-116">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-116">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f4ef1-117">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="f4ef1-117">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f4ef1-118">未搭配此作業使用。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-118">Not used with this operation.</span></span> <span data-ttu-id="f4ef1-119">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-119">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f4ef1-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="f4ef1-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f4ef1-121">輸出緩衝區的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-121">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="f4ef1-122">設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-122">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="f4ef1-123">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="f4ef1-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="f4ef1-124">未搭配此作業使用。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-124">Not used with this operation.</span></span> <span data-ttu-id="f4ef1-125">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-125">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f4ef1-126">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="f4ef1-126">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="f4ef1-127">重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-127">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="f4ef1-128">如果在未指定檔案 **\_ 旗 \_** 標的情況下開啟 *hDevice* ，則會忽略 *lpOverlapped* 。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-128">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="f4ef1-129">如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-129">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="f4ef1-130">在此情況下， *lpOverlapped* 必須指向包含事件物件控制碼 [**的有效重**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 迭結構。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-130">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="f4ef1-131">否則，函式會以無法預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-131">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="f4ef1-132">針對重迭的作業， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會立即傳回，而當作業完成時，就會發出事件物件的信號。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-132">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="f4ef1-133">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-133">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4ef1-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4ef1-134">Return value</span></span>

<span data-ttu-id="f4ef1-135">如果作業順利完成，表示磁片上的所有磁片區都已備妥可供使用， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-135">If the operation completes successfully, indicating that all volumes on the disk are ready for use, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="f4ef1-136">如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-136">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="f4ef1-137">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="f4ef1-137">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4ef1-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4ef1-138">Requirements</span></span>



| <span data-ttu-id="f4ef1-139">需求</span><span class="sxs-lookup"><span data-stu-id="f4ef1-139">Requirement</span></span> | <span data-ttu-id="f4ef1-140">值</span><span class="sxs-lookup"><span data-stu-id="f4ef1-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ef1-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4ef1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f4ef1-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="f4ef1-142">None supported</span></span><br/>                                                             |
| <span data-ttu-id="f4ef1-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4ef1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f4ef1-144">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4ef1-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4ef1-145">標頭</span><span class="sxs-lookup"><span data-stu-id="f4ef1-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4ef1-146"><dt>Ntdddisk。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4ef1-146"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4ef1-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4ef1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ef1-148">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="f4ef1-148">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="f4ef1-149">磁片管理控制碼</span><span class="sxs-lookup"><span data-stu-id="f4ef1-149">Disk Management Control Codes</span></span>](disk-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="f4ef1-150">**磁片 \_ 群集 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f4ef1-150">**DISK\_CLUSTER\_INFO**</span></span>](disk-cluster-info.md)
</dt> <dt>

[<span data-ttu-id="f4ef1-151">**IOCTL \_ 磁片 \_ 取得 \_ 叢集 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f4ef1-151">**IOCTL\_DISK\_GET\_CLUSTER\_INFO**</span></span>](ioctl-disk-get-cluster-info.md)
</dt> </dl>

 

