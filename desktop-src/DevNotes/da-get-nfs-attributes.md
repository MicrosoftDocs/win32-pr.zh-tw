---
description: DA \_ GET \_ nfs \_ 屬性控制程式代碼會查詢其他有關 NFS 共用的資訊。
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: DA_GET_NFS_ATTRIBUTES 控制程式代碼
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DA_GET_NFS_ATTRIBUTES
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4427dd48190bd12f7837c4841a98e15f7ddaff5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510504"
---
# <a name="da_get_nfs_attributes-control-code"></a><span data-ttu-id="7483f-103">DA \_ GET \_ NFS \_ 屬性控制項程式碼</span><span class="sxs-lookup"><span data-stu-id="7483f-103">DA\_GET\_NFS\_ATTRIBUTES control code</span></span>

<span data-ttu-id="7483f-104">**DA \_ GET \_ nfs \_ 屬性** 控制程式代碼會查詢其他有關 NFS 共用的資訊。</span><span class="sxs-lookup"><span data-stu-id="7483f-104">The **DA\_GET\_NFS\_ATTRIBUTES** control code queries additional information about an NFS share.</span></span>

<span data-ttu-id="7483f-105">若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="7483f-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,               // handle to device
                    (DWORD)        DA_GET_NFS_ATTRIBUTES, // dwIoControlCode
                                   NULL,                  // lpInBuffer
                                   0,                     // nInBufferSize
                    (LPDWORD)      lpOutBuffer,           // output buffer
                    (DWORD)        nOutBufferSize,        // size of output buffer
                    (LPDWORD)      lpBytesReturned,       // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="7483f-106">參數</span><span class="sxs-lookup"><span data-stu-id="7483f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7483f-107">*hDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7483f-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7483f-108">NFS 共用上檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7483f-108">A handle to a file on the NFS share.</span></span> <span data-ttu-id="7483f-109">若要取得此控制碼，請呼叫 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) 函數。</span><span class="sxs-lookup"><span data-stu-id="7483f-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-110">*dwIoControlCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7483f-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7483f-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="7483f-111">The control code for the operation.</span></span> <span data-ttu-id="7483f-112">請使用 **DA \_ GET \_ NFS \_ 屬性** 進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="7483f-112">Use **DA\_GET\_NFS\_ATTRIBUTES** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="7483f-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="7483f-114">未搭配此作業使用;設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7483f-114">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-115">*nInBufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7483f-115">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7483f-116">未搭配此作業使用;設定為零。</span><span class="sxs-lookup"><span data-stu-id="7483f-116">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-117">*lpOutBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7483f-117">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7483f-118">輸出緩衝區的指標，其中包含 **NFS \_ 檔 \_ 屬性** 結構。</span><span class="sxs-lookup"><span data-stu-id="7483f-118">A pointer to the output buffer, which contains an **NFS\_FILE\_ATTRIBUTES** structure.</span></span> <span data-ttu-id="7483f-119">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="7483f-119">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-120">*nOutBufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7483f-120">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7483f-121">輸出緩衝區的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="7483f-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-122">*lpBytesReturned* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7483f-122">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7483f-123">變數的指標，此變數會接收儲存在輸出緩衝區中的資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7483f-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="7483f-124">如果輸出緩衝區太小，則呼叫會失敗，而 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 **錯誤的 \_ \_ 緩衝區**，而 *lpBytesReturned* 為零。</span><span class="sxs-lookup"><span data-stu-id="7483f-124">If the output buffer is too small, the call fails, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="7483f-125">如果 *lpOverlapped* 為 **null**，則 *lpBytesReturned* 不可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="7483f-125">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="7483f-126">即使作業未傳回輸出資料，而且 *lpOutBuffer* 為 **Null**， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 也會使用 *lpBytesReturned*。</span><span class="sxs-lookup"><span data-stu-id="7483f-126">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="7483f-127">在這類作業之後， *lpBytesReturned* 的值就沒有意義。</span><span class="sxs-lookup"><span data-stu-id="7483f-127">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="7483f-128">如果 *lpOverlapped* 不是 **null**， *lpBytesReturned* 可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="7483f-128">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="7483f-129">如果這個參數不是 **Null** ，而且作業傳回資料，則 *lpBytesReturned* 會在重迭的作業完成之前無意義。</span><span class="sxs-lookup"><span data-stu-id="7483f-129">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="7483f-130">若要取出傳回的位元組數目，請呼叫 [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult)。</span><span class="sxs-lookup"><span data-stu-id="7483f-130">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="7483f-131">如果 *hDevice* 參數與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="7483f-131">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="7483f-132">*lpOverlapped* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7483f-132">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7483f-133">重 [**迭結構的**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="7483f-133">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="7483f-134">如果在未指定檔案 **\_ 旗 \_** 標的情況下開啟 *hDevice* ，則會忽略 *lpOverlapped* 。</span><span class="sxs-lookup"><span data-stu-id="7483f-134">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="7483f-135">如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="7483f-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="7483f-136">在此情況下， *lpOverlapped* 必須指向包含事件物件控制碼 [**的有效重**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 迭結構。</span><span class="sxs-lookup"><span data-stu-id="7483f-136">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="7483f-137">否則，函式會以無法預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="7483f-137">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="7483f-138">針對重迭的作業， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會立即傳回，而當作業完成時，就會發出事件物件的信號。</span><span class="sxs-lookup"><span data-stu-id="7483f-138">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="7483f-139">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="7483f-139">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7483f-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="7483f-140">Return value</span></span>

<span data-ttu-id="7483f-141">如果作業順利完成， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="7483f-141">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="7483f-142">如果作業失敗或擱置中， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="7483f-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="7483f-143">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="7483f-143">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="7483f-144">備註</span><span class="sxs-lookup"><span data-stu-id="7483f-144">Remarks</span></span>

<span data-ttu-id="7483f-145">此控制項程式碼沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="7483f-145">This control code has no associated header file.</span></span> <span data-ttu-id="7483f-146">您必須定義控制項程式碼和資料結構，如下所示。</span><span class="sxs-lookup"><span data-stu-id="7483f-146">You must define the control code and data structures as follows.</span></span>

``` syntax
#define DEVICE_DA_RDR 0x80000  
 
#define DA_GET_NFS_ATTRIBUTES CTL_CODE(DEVICE_DA_RDR, 0x804, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _NFS_SPEC_DATA {  
    ULONG               SpecData1;
    ULONG               SpecData2;
} NFS_SPEC_DATA, *PNFS_SPEC_DATA;

typedef struct _NFS_TIME {
    ULONG        Seconds;
    ULONG        nSeconds;
} NFS_TIME, *PNFS_TIME;

#define NFS_TYPE_REG         1
#define NFS_TYPE_DIR         2
#define NFS_TYPE_BLK         3
#define NFS_TYPE_CHR         4
#define NFS_TYPE_LNK         5
#define NFS_TYPE_SOCK        6
#define NFS_TYPE_FIFO        7

typedef struct _NFS_FILE_ATTRIBUTES {  
    ULONG               FileType;  
    ULONG               Mode;  
    ULONG               NLink;  
    ULONG               Uid;  
    ULONG               Gid;  
    ULONGLONG           Size;  
    ULONGLONG           Used;
    NFS_SPEC_DATA       Rdev;
    ULONGLONG           Fsid;  
    ULONGLONG           FileId;  
    NFS_TIME            AccessTime;  
    NFS_TIME            ModifyTime;  
    NFS_TIME            ChangeTime;  
} NFS_FILE_ATTRIBUTES, *PNFS_FILE_ATTRIBUTES;

typedef struct _DA_FILE_ATTRIBUTES {  
    NFS_FILE_ATTRIBUTES FileAttributes;  
    ULONG               Version;  
} DA_FILE_ATTRIBUTES, *PDA_FILE_ATTRIBUTES;
```

<span data-ttu-id="7483f-147">結構成員可以如下描述。</span><span class="sxs-lookup"><span data-stu-id="7483f-147">The structure members can be described as follows.</span></span>

<dl> <dt>

<span data-ttu-id="7483f-148"><span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**</span><span class="sxs-lookup"><span data-stu-id="7483f-148"><span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-149">用於特殊檔案類型的不透明值，例如區塊特殊、字元特殊和 FIFO 檔案。</span><span class="sxs-lookup"><span data-stu-id="7483f-149">An opaque value that is used for special file types such as block-special, character-special and FIFO files.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-150"><span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**</span><span class="sxs-lookup"><span data-stu-id="7483f-150"><span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-151">用於特殊檔案類型的不透明值，例如區塊特殊、字元特殊和 FIFO 檔案。</span><span class="sxs-lookup"><span data-stu-id="7483f-151">An opaque value that is used for special file types such as block-special, character-special and FIFO files.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-152"><span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**秒**</span><span class="sxs-lookup"><span data-stu-id="7483f-152"><span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Seconds**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-153">表示自1970年1月1日起的秒數 (UTC) 的64位值。</span><span class="sxs-lookup"><span data-stu-id="7483f-153">A 64-bit value representing the seconds since January 1, 1970 (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="7483f-154"><span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**</span><span class="sxs-lookup"><span data-stu-id="7483f-154"><span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-155">要加入至 **秒** 成員的毫微秒數。</span><span class="sxs-lookup"><span data-stu-id="7483f-155">The number of nanoseconds to be added to the **Seconds** member.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-156"><span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**</span><span class="sxs-lookup"><span data-stu-id="7483f-156"><span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-157">共用的 NFS 檔案類型。</span><span class="sxs-lookup"><span data-stu-id="7483f-157">The NFS file type of the share.</span></span>



| <span data-ttu-id="7483f-158">NFS 檔案類型</span><span class="sxs-lookup"><span data-stu-id="7483f-158">NFS File Type</span></span>                                                                              | <span data-ttu-id="7483f-159">Description</span><span class="sxs-lookup"><span data-stu-id="7483f-159">Description</span></span>                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="7483f-160"><span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>NFS \_ 類型 \_ REG</span><span class="sxs-lookup"><span data-stu-id="7483f-160"><span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>NFS\_TYPE\_REG</span></span><br/>    | <span data-ttu-id="7483f-161">一般檔案。</span><span class="sxs-lookup"><span data-stu-id="7483f-161">A regular file.</span></span><br/>           |
| <span data-ttu-id="7483f-162"><span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>NFS \_ 類型 \_ 目錄</span><span class="sxs-lookup"><span data-stu-id="7483f-162"><span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>NFS\_TYPE\_DIR</span></span><br/>    | <span data-ttu-id="7483f-163">目錄。</span><span class="sxs-lookup"><span data-stu-id="7483f-163">A directory.</span></span><br/>              |
| <span data-ttu-id="7483f-164"><span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>NFS \_ 類型 \_ BLK</span><span class="sxs-lookup"><span data-stu-id="7483f-164"><span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>NFS\_TYPE\_BLK</span></span><br/>    | <span data-ttu-id="7483f-165">區塊-特殊檔案。</span><span class="sxs-lookup"><span data-stu-id="7483f-165">A block-special file.</span></span><br/>     |
| <span data-ttu-id="7483f-166"><span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>NFS \_ 類型 \_ CHR</span><span class="sxs-lookup"><span data-stu-id="7483f-166"><span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>NFS\_TYPE\_CHR</span></span><br/>    | <span data-ttu-id="7483f-167">字元-特殊檔案。</span><span class="sxs-lookup"><span data-stu-id="7483f-167">A character-special file.</span></span><br/> |
| <span data-ttu-id="7483f-168"><span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>NFS \_ 類型 \_ .LNK</span><span class="sxs-lookup"><span data-stu-id="7483f-168"><span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>NFS\_TYPE\_LNK</span></span><br/>    | <span data-ttu-id="7483f-169">符號連結。</span><span class="sxs-lookup"><span data-stu-id="7483f-169">A symbolic link.</span></span><br/>          |
| <span data-ttu-id="7483f-170"><span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>NFS \_ 類型 \_ SOCK</span><span class="sxs-lookup"><span data-stu-id="7483f-170"><span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>NFS\_TYPE\_SOCK</span></span><br/> | <span data-ttu-id="7483f-171">Windows 通訊端。</span><span class="sxs-lookup"><span data-stu-id="7483f-171">A Windows socket.</span></span><br/>         |
| <span data-ttu-id="7483f-172"><span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>NFS \_ 類型 \_ FIFO</span><span class="sxs-lookup"><span data-stu-id="7483f-172"><span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>NFS\_TYPE\_FIFO</span></span><br/> | <span data-ttu-id="7483f-173">FIFO 檔。</span><span class="sxs-lookup"><span data-stu-id="7483f-173">A FIFO file.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="7483f-174"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**模式**</span><span class="sxs-lookup"><span data-stu-id="7483f-174"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-175">檔案模式。</span><span class="sxs-lookup"><span data-stu-id="7483f-175">The file mode.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-176"><span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**</span><span class="sxs-lookup"><span data-stu-id="7483f-176"><span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-177">共用的連結數目。</span><span class="sxs-lookup"><span data-stu-id="7483f-177">The number of links to the share.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-178"><span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Uid**</span><span class="sxs-lookup"><span data-stu-id="7483f-178"><span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Uid**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-179">UNIX 使用者識別碼 (UID) 。</span><span class="sxs-lookup"><span data-stu-id="7483f-179">The UNIX user identifier (UID).</span></span>

</dd> <dt>

<span data-ttu-id="7483f-180"><span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Gid**</span><span class="sxs-lookup"><span data-stu-id="7483f-180"><span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Gid**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-181">UNIX 群組識別碼 (GID) 。</span><span class="sxs-lookup"><span data-stu-id="7483f-181">The UNIX group identifier (GID).</span></span>

</dd> <dt>

<span data-ttu-id="7483f-182"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**大小**</span><span class="sxs-lookup"><span data-stu-id="7483f-182"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Size**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-183">檔案大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7483f-183">The file size, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-184"><span id="Used"></span><span id="used"></span><span id="USED"></span>**使用**</span><span class="sxs-lookup"><span data-stu-id="7483f-184"><span id="Used"></span><span id="used"></span><span id="USED"></span>**Used**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-185">使用的檔案大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7483f-185">The file size used, in bytes.</span></span> <span data-ttu-id="7483f-186">這與檔案大小相同。</span><span class="sxs-lookup"><span data-stu-id="7483f-186">This is the same as the file size.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-187"><span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**</span><span class="sxs-lookup"><span data-stu-id="7483f-187"><span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-188">裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="7483f-188">The device identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-189"><span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**</span><span class="sxs-lookup"><span data-stu-id="7483f-189"><span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-190">檔案系統識別碼。</span><span class="sxs-lookup"><span data-stu-id="7483f-190">The file system identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-191"><span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileId**</span><span class="sxs-lookup"><span data-stu-id="7483f-191"><span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileId**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-192">檔案識別碼。</span><span class="sxs-lookup"><span data-stu-id="7483f-192">The file identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-193"><span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**</span><span class="sxs-lookup"><span data-stu-id="7483f-193"><span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-194">上次存取時間。</span><span class="sxs-lookup"><span data-stu-id="7483f-194">The last access time.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-195"><span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**</span><span class="sxs-lookup"><span data-stu-id="7483f-195"><span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-196">上次修改時間。</span><span class="sxs-lookup"><span data-stu-id="7483f-196">The last modification time.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-197"><span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**</span><span class="sxs-lookup"><span data-stu-id="7483f-197"><span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-198">上次變更時間。</span><span class="sxs-lookup"><span data-stu-id="7483f-198">The last change time.</span></span>

</dd> <dt>

<span data-ttu-id="7483f-199"><span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**</span><span class="sxs-lookup"><span data-stu-id="7483f-199"><span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-200">**NFS \_ 檔 \_ 屬性** 結構。</span><span class="sxs-lookup"><span data-stu-id="7483f-200">An **NFS\_FILE\_ATTRIBUTES** structure.</span></span>

> [!Note]  
> <span data-ttu-id="7483f-201">如需此結構成員的詳細說明，請參閱「NFS 版本3通訊協定規格」中的 **fattr3** 結構 (，如 [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)) 中所定義。</span><span class="sxs-lookup"><span data-stu-id="7483f-201">For more detailed descriptions of the members of this structure, see the **fattr3** structure in the NFS Version 3 Protocol Specification (as defined in [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).</span></span>

 

</dd> <dt>

<span data-ttu-id="7483f-202"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**版本**</span><span class="sxs-lookup"><span data-stu-id="7483f-202"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span></span>
</dt> <dd>

<span data-ttu-id="7483f-203">指定是否透過 NFS 版本2或 NFS 第3版通訊協定來建立 NFS 共用的控制碼連線。</span><span class="sxs-lookup"><span data-stu-id="7483f-203">Specifies whether the connection on which the handle to the NFS share was created is over NFS Version 2 or NFS Version 3 protocol.</span></span>



| <span data-ttu-id="7483f-204">值</span><span class="sxs-lookup"><span data-stu-id="7483f-204">Value</span></span>                            | <span data-ttu-id="7483f-205">描述</span><span class="sxs-lookup"><span data-stu-id="7483f-205">Description</span></span>              |
|----------------------------------|--------------------------|
| <span data-ttu-id="7483f-206"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="7483f-206"><span id="2"></span>2</span></span><br/> | <span data-ttu-id="7483f-207">NFS 版本2</span><span class="sxs-lookup"><span data-stu-id="7483f-207">NFS Version 2</span></span><br/> |
| <span data-ttu-id="7483f-208"><span id="3"></span>3</span><span class="sxs-lookup"><span data-stu-id="7483f-208"><span id="3"></span>3</span></span><br/> | <span data-ttu-id="7483f-209">NFS 版本3</span><span class="sxs-lookup"><span data-stu-id="7483f-209">NFS Version 3</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7483f-210">規格需求</span><span class="sxs-lookup"><span data-stu-id="7483f-210">Requirements</span></span>



| <span data-ttu-id="7483f-211">需求</span><span class="sxs-lookup"><span data-stu-id="7483f-211">Requirement</span></span> | <span data-ttu-id="7483f-212">值</span><span class="sxs-lookup"><span data-stu-id="7483f-212">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="7483f-213">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7483f-213">Minimum supported client</span></span><br/> | <span data-ttu-id="7483f-214">都不支援</span><span class="sxs-lookup"><span data-stu-id="7483f-214">None supported</span></span><br/>         |
| <span data-ttu-id="7483f-215">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7483f-215">Minimum supported server</span></span><br/> | <span data-ttu-id="7483f-216">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7483f-216">Windows Server 2008</span></span><br/>    |
| <span data-ttu-id="7483f-217">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7483f-217">End of client support</span></span><br/>    | <span data-ttu-id="7483f-218">都不支援</span><span class="sxs-lookup"><span data-stu-id="7483f-218">None supported</span></span><br/>         |
| <span data-ttu-id="7483f-219">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="7483f-219">End of server support</span></span><br/>    | <span data-ttu-id="7483f-220">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7483f-220">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7483f-221">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7483f-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7483f-222">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="7483f-222">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
