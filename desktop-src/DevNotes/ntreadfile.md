---
description: 從開啟的檔案讀取資料。
ms.assetid: 7EA2FE38-20DA-43E1-A764-66A81725D1EA
title: 'NtReadFile 函式 (Wdm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtReadFile
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: be1a73c6451012dfd97d7d4c55c23f0842cf1551
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510455"
---
# <a name="ntreadfile-function"></a><span data-ttu-id="d1e91-103">NtReadFile 函式</span><span class="sxs-lookup"><span data-stu-id="d1e91-103">NtReadFile function</span></span>

<span data-ttu-id="d1e91-104">從開啟的檔案讀取資料。</span><span class="sxs-lookup"><span data-stu-id="d1e91-104">Reads data from an open file.</span></span>

<span data-ttu-id="d1e91-105">此函式是使用者模式，相當於 Windows 驅動程式套件 (WDK) 中記載的 [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) 函式。</span><span class="sxs-lookup"><span data-stu-id="d1e91-105">This function is the user-mode equivalent to the [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) function documented in the Windows Driver Kit (WDK).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1e91-106">語法</span><span class="sxs-lookup"><span data-stu-id="d1e91-106">Syntax</span></span>


```C++
NTSTATUS NtReadFile(
  _In_     HANDLE           FileHandle,
  _In_opt_ HANDLE           Event,
  _In_opt_ PIO_APC_ROUTINE  ApcRoutine,
  _In_opt_ PVOID            ApcContext,
  _Out_    PIO_STATUS_BLOCK IoStatusBlock,
  _Out_    PVOID            Buffer,
  _In_     ULONG            Length,
  _In_opt_ PLARGE_INTEGER   ByteOffset,
  _In_opt_ PULONG           Key
);
```



## <a name="parameters"></a><span data-ttu-id="d1e91-107">參數</span><span class="sxs-lookup"><span data-stu-id="d1e91-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1e91-108">*FileHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1e91-108">*FileHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e91-109">File 物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d1e91-109">Handle to the file object.</span></span> <span data-ttu-id="d1e91-110">這個控制碼是由成功呼叫 [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) 或 [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile)所建立。</span><span class="sxs-lookup"><span data-stu-id="d1e91-110">This handle is created by a successful call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) or [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).</span></span>

</dd> <dt>

<span data-ttu-id="d1e91-111">*活動* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d1e91-111">*Event* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e91-112">（選擇性）在讀取作業完成後，將事件物件的控制碼設定為已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="d1e91-112">Optionally, a handle to an event object to set to the signaled state after the read operation completes.</span></span> <span data-ttu-id="d1e91-113">裝置和中繼驅動程式應該將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d1e91-113">Device and intermediate drivers should set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d1e91-114">*ApcRoutine* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d1e91-114">*ApcRoutine* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e91-115">此參數已保留備用。</span><span class="sxs-lookup"><span data-stu-id="d1e91-115">This parameter is reserved.</span></span> <span data-ttu-id="d1e91-116">裝置和中繼驅動程式應該將此指標設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d1e91-116">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d1e91-117">*ApcCoNtext* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d1e91-117">*ApcContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e91-118">此參數已保留備用。</span><span class="sxs-lookup"><span data-stu-id="d1e91-118">This parameter is reserved.</span></span> <span data-ttu-id="d1e91-119">裝置和中繼驅動程式應該將此指標設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d1e91-119">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d1e91-120">*IoStatusBlock* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d1e91-120">*IoStatusBlock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e91-121">[**IO \_ 狀態 \_ 區塊**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block)結構的指標，此結構會接收最終完成狀態，以及有關所要求讀取作業的資訊。</span><span class="sxs-lookup"><span data-stu-id="d1e91-121">Pointer to an [**IO\_STATUS\_BLOCK**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) structure that receives the final completion status and information about the requested read operation.</span></span> <span data-ttu-id="d1e91-122">**資訊** 成員會收到實際從檔案讀取的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="d1e91-122">The **Information** member receives the number of bytes actually read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="d1e91-123">*緩衝區* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d1e91-123">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e91-124">呼叫端配置之緩衝區的指標，此緩衝區會接收從檔案讀取的資料。</span><span class="sxs-lookup"><span data-stu-id="d1e91-124">Pointer to a caller-allocated buffer that receives the data read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="d1e91-125">*長度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1e91-125">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e91-126">*緩衝區* 所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d1e91-126">The size, in bytes, of the buffer pointed to by *Buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="d1e91-127">*ByteOffset* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d1e91-127">*ByteOffset* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e91-128">變數的指標，該變數會在檔案中指定開始讀取作業的起始位元組位移。</span><span class="sxs-lookup"><span data-stu-id="d1e91-128">Pointer to a variable that specifies the starting byte offset in the file where the read operation will begin.</span></span> <span data-ttu-id="d1e91-129">如果嘗試讀取超過檔案結尾， **NtReadFile** 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d1e91-129">If an attempt is made to read beyond the end of the file, **NtReadFile** returns an error.</span></span>

<span data-ttu-id="d1e91-130">如果對 [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) 的呼叫設定 *CreateOptions* 旗標檔案 \_ 同步 \_ io \_ 警示或檔案 \_ 同步 \_ io \_ NONALERT，則 i/o 管理員會維護目前的檔案位置。</span><span class="sxs-lookup"><span data-stu-id="d1e91-130">If the call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) set either of the *CreateOptions* flags FILE\_SYNCHRONOUS\_IO\_ALERT or FILE\_SYNCHRONOUS\_IO\_NONALERT, the I/O Manager maintains the current file position.</span></span> <span data-ttu-id="d1e91-131">如果是， **NtReadFile** 的呼叫端可以指定使用目前的檔案位置位移，而不是明確的 *ByteOffset* 值。</span><span class="sxs-lookup"><span data-stu-id="d1e91-131">If so, the caller of **NtReadFile** can specify that the current file position offset be used instead of an explicit *ByteOffset* value.</span></span> <span data-ttu-id="d1e91-132">您可以使用下列其中一種方法來建立此規格：</span><span class="sxs-lookup"><span data-stu-id="d1e91-132">This specification can be made by using one of the following methods:</span></span>

-   <span data-ttu-id="d1e91-133">指定 **HighPart** 成員設為-1 的 **大型 \_ 整數** 值的指標，並將 **LowPart** 成員設為系統定義的值檔案 \_ 使用檔案 \_ \_ 指標 \_ 位置。</span><span class="sxs-lookup"><span data-stu-id="d1e91-133">Specify a pointer to a **LARGE\_INTEGER** value with the **HighPart** member set to -1 and the **LowPart** member set to the system-defined value FILE\_USE\_FILE\_POINTER\_POSITION.</span></span>

-   <span data-ttu-id="d1e91-134">傳遞 *ByteOffset* 的 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="d1e91-134">Pass a **NULL** pointer for *ByteOffset*.</span></span>

<span data-ttu-id="d1e91-135">**NtReadFile** 會在完成讀取作業時新增讀取的位元組數目，以更新目前的檔案位置（如果它使用 i/o 管理員所維護的目前檔案位置）。</span><span class="sxs-lookup"><span data-stu-id="d1e91-135">**NtReadFile** updates the current file position by adding the number of bytes read when it completes the read operation, if it is using the current file position maintained by the I/O Manager.</span></span>

<span data-ttu-id="d1e91-136">即使 i/o 管理員正在維護目前的檔案位置，呼叫者也可以將明確的 *ByteOffset* 值傳遞給 **NtReadFile**，以重設這個位置。</span><span class="sxs-lookup"><span data-stu-id="d1e91-136">Even when the I/O Manager is maintaining the current file position, the caller can reset this position by passing an explicit *ByteOffset* value to **NtReadFile**.</span></span> <span data-ttu-id="d1e91-137">這樣做會自動將目前的檔案位置變更為該 *ByteOffset* 值，執行讀取作業，然後根據實際讀取的位元組數來更新位置。</span><span class="sxs-lookup"><span data-stu-id="d1e91-137">Doing this automatically changes the current file position to that *ByteOffset* value, performs the read operation, and then updates the position according to the number of bytes actually read.</span></span> <span data-ttu-id="d1e91-138">這項技術提供呼叫者不可部分完成的搜尋和讀取服務。</span><span class="sxs-lookup"><span data-stu-id="d1e91-138">This technique gives the caller atomic seek-and-read service.</span></span>

</dd> <dt>

<span data-ttu-id="d1e91-139">*金鑰* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d1e91-139">*Key* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e91-140">裝置和中繼驅動程式應該將此指標設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d1e91-140">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1e91-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1e91-141">Return value</span></span>

<span data-ttu-id="d1e91-142">**NtReadFile** 會傳回狀態 \_ SUCCESS 或適當的 NTSTATUS 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d1e91-142">**NtReadFile** returns either STATUS\_SUCCESS or the appropriate NTSTATUS error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1e91-143">備註</span><span class="sxs-lookup"><span data-stu-id="d1e91-143">Remarks</span></span>

<span data-ttu-id="d1e91-144">**NtReadFile** 的呼叫端必須已使用 [](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) \_ DesiredAccess 參數中所設定的 FILE read \_ DATA 或 GENERIC \_ READ 值來呼叫 NtCreateFile。</span><span class="sxs-lookup"><span data-stu-id="d1e91-144">Callers of **NtReadFile** must have already called [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) with the FILE\_READ\_DATA or GENERIC\_READ value set in the *DesiredAccess* parameter.</span></span>

<span data-ttu-id="d1e91-145">如果上述對 [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile)的呼叫將 \_ \_ CREATEOPTIONS 參數中的 FILE NO 中繼緩衝旗標設 \_ 為 **NtCreateFile**，則 **NtReadFile** 的 *長度* 和 *ByteOffset* 參數必須是磁區大小的倍數。</span><span class="sxs-lookup"><span data-stu-id="d1e91-145">If the preceding call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) set the FILE\_NO\_INTERMEDIATE\_BUFFERING flag in the *CreateOptions* parameter to **NtCreateFile**, the *Length* and *ByteOffset* parameters to **NtReadFile** must be multiples of the sector size.</span></span> <span data-ttu-id="d1e91-146">如需詳細資訊，請參閱 **NtCreateFile**。</span><span class="sxs-lookup"><span data-stu-id="d1e91-146">For more information, see **NtCreateFile**.</span></span>

<span data-ttu-id="d1e91-147">**NtReadFile** 會開始從指定的 *ByteOffset* 或目前的檔案位置讀取至指定的 *緩衝區*。</span><span class="sxs-lookup"><span data-stu-id="d1e91-147">**NtReadFile** begins reading from the given *ByteOffset* or the current file position into the given *Buffer*.</span></span> <span data-ttu-id="d1e91-148">它會在下列其中一個條件下終止讀取作業：</span><span class="sxs-lookup"><span data-stu-id="d1e91-148">It terminates the read operation under one of the following conditions:</span></span>

-   <span data-ttu-id="d1e91-149">緩衝區已滿，因為已讀取 *長度* 參數所指定的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="d1e91-149">The buffer is full because the number of bytes specified by the *Length* parameter has been read.</span></span> <span data-ttu-id="d1e91-150">因此，沒有任何資料可以放到緩衝區中，而不會發生溢位。</span><span class="sxs-lookup"><span data-stu-id="d1e91-150">Therefore, no more data can be placed into the buffer without an overflow.</span></span>

-   <span data-ttu-id="d1e91-151">讀取作業期間已到達檔案結尾，因此檔案中沒有其他資料可傳輸到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d1e91-151">The end of file is reached during the read operation, so there is no more data in the file to be transferred into the buffer.</span></span>

<span data-ttu-id="d1e91-152">如果呼叫端以 *DesiredAccess* 中設定的同步旗標來開啟檔案，呼叫端執行緒可以等候檔案控制代碼 *FileHandle*，同步處理至完成讀取作業。</span><span class="sxs-lookup"><span data-stu-id="d1e91-152">If the caller opened the file with the SYNCHRONIZE flag set in *DesiredAccess*, the calling thread can synchronize to the completion of the read operation by waiting on the file handle, *FileHandle*.</span></span> <span data-ttu-id="d1e91-153">每次控制碼上發出的 i/o 作業完成時，就會發出控制碼的信號。</span><span class="sxs-lookup"><span data-stu-id="d1e91-153">The handle is signaled each time that an I/O operation that was issued on the handle completes.</span></span> <span data-ttu-id="d1e91-154">不過，呼叫端不能等待開啟以進行同步檔案存取的控制碼 (檔案 \_ 同步 \_ io \_ NONALERT 或檔案 \_ 同步 \_ io \_ 警示) 。</span><span class="sxs-lookup"><span data-stu-id="d1e91-154">However, the caller must not wait on a handle that was opened for synchronous file access (FILE\_SYNCHRONOUS\_IO\_NONALERT or FILE\_SYNCHRONOUS\_IO\_ALERT).</span></span> <span data-ttu-id="d1e91-155">在此情況下， **NtReadFile** 會代表呼叫端等候，直到讀取作業完成時才會返回。</span><span class="sxs-lookup"><span data-stu-id="d1e91-155">In this case, **NtReadFile** waits on behalf of the caller and does not return until the read operation is complete.</span></span> <span data-ttu-id="d1e91-156">只有在符合下列三個條件時，呼叫者才可以安全地在檔案控制代碼上等候：</span><span class="sxs-lookup"><span data-stu-id="d1e91-156">The caller can safely wait on the file handle only if all three of the following conditions are met:</span></span>

-   <span data-ttu-id="d1e91-157">開啟的控制碼為非同步存取 (也就是， \_ \_) 未指定任何檔案同步 IO \_ *XXX* 旗標。</span><span class="sxs-lookup"><span data-stu-id="d1e91-157">The handle was opened for asynchronous access (that is, neither FILE\_SYNCHRONOUS\_IO\_*XXX* flag was specified).</span></span>

-   <span data-ttu-id="d1e91-158">控制碼一次僅用於一個 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="d1e91-158">The handle is being used for only one I/O operation at a time.</span></span>

-   <span data-ttu-id="d1e91-159">**NtReadFile** 傳回的狀態為 \_ 暫止。</span><span class="sxs-lookup"><span data-stu-id="d1e91-159">**NtReadFile** returned STATUS\_PENDING.</span></span>

<span data-ttu-id="d1e91-160">如果有下列任何一種情況，驅動程式應該在系統進程的內容中呼叫 **NtReadFile** ：</span><span class="sxs-lookup"><span data-stu-id="d1e91-160">A driver should call **NtReadFile** in the context of the system process if any of the following conditions exist:</span></span>

-   <span data-ttu-id="d1e91-161">驅動程式建立了它傳遞給 **NtReadFile** 的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="d1e91-161">The driver created the file handle that it passes to **NtReadFile**.</span></span>

-   <span data-ttu-id="d1e91-162">**NtReadFile** 會透過驅動程式所建立的事件，將 i/o 完成的驅動程式通知。</span><span class="sxs-lookup"><span data-stu-id="d1e91-162">**NtReadFile** will notify the driver of I/O completion by means of an event that the driver created.</span></span>

-   <span data-ttu-id="d1e91-163">**NtReadFile** 會藉由驅動程式傳遞至 **NtReadFile** 的 APC 回呼常式，來通知 i/o 完成的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="d1e91-163">**NtReadFile** will notify the driver of I/O completion by means of an APC callback routine that the driver passes to **NtReadFile**.</span></span>

<span data-ttu-id="d1e91-164">只有在建立控制碼的進程內容中，檔案和事件控制碼才有效。</span><span class="sxs-lookup"><span data-stu-id="d1e91-164">File and event handles are valid only in the process context where the handles are created.</span></span> <span data-ttu-id="d1e91-165">因此，為了避免安全性漏洞，驅動程式應該在系統進程的內容中，建立傳遞給 **NtReadFile** 的任何檔案或事件控制碼，而不是驅動程式所在之進程的內容。</span><span class="sxs-lookup"><span data-stu-id="d1e91-165">Therefore, to avoid security holes, the driver should create any file or event handle that it passes to **NtReadFile** in the context of the system process rather than the context of the process that the driver is in.</span></span>

<span data-ttu-id="d1e91-166">同樣地，如果 **NtReadFile** 在系統進程的環境中透過 APC 通知驅動程式，就應該呼叫它，因為 apc 一律會在發出 i/o 要求的執行緒內容中引發。</span><span class="sxs-lookup"><span data-stu-id="d1e91-166">Likewise, **NtReadFile** should be called in the context of the system process if it notifies the driver of I/O completion by means of an APC, because APCs are always fired in the context of the thread that issues the I/O request.</span></span> <span data-ttu-id="d1e91-167">如果驅動程式在系統以外的進程內容中呼叫 **NtReadFile** ，APC 可能會無限期地延遲，或根本不會引發。</span><span class="sxs-lookup"><span data-stu-id="d1e91-167">If the driver calls **NtReadFile** in the context of a process other than the system one, the APC could be delayed indefinitely, or it might not fire at all.</span></span>

<span data-ttu-id="d1e91-168">如需使用檔案的詳細資訊，請參閱 [在驅動程式中使用](/windows-hardware/drivers/kernel/using-files-in-a-driver)檔案。</span><span class="sxs-lookup"><span data-stu-id="d1e91-168">For more information about working with files, see [Using Files in a Driver](/windows-hardware/drivers/kernel/using-files-in-a-driver).</span></span>

<span data-ttu-id="d1e91-169">**NtReadFile** 的呼叫端必須在 IRQL = 被動 \_ 層級執行，並 [啟用特殊的核心 apc](/windows-hardware/drivers/kernel/disabling-apcs)。</span><span class="sxs-lookup"><span data-stu-id="d1e91-169">Callers of **NtReadFile** must be running at IRQL = PASSIVE\_LEVEL and [with special kernel APCs enabled](/windows-hardware/drivers/kernel/disabling-apcs).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1e91-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1e91-170">Requirements</span></span>



| <span data-ttu-id="d1e91-171">需求</span><span class="sxs-lookup"><span data-stu-id="d1e91-171">Requirement</span></span> | <span data-ttu-id="d1e91-172">值</span><span class="sxs-lookup"><span data-stu-id="d1e91-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e91-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1e91-173">Minimum supported client</span></span><br/> | <span data-ttu-id="d1e91-174">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1e91-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="d1e91-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1e91-175">Minimum supported server</span></span><br/> | <span data-ttu-id="d1e91-176">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1e91-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="d1e91-177">目標平台</span><span class="sxs-lookup"><span data-stu-id="d1e91-177">Target platform</span></span><br/>          | <dl> <span data-ttu-id="d1e91-178"><dt>[通用](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="d1e91-178"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="d1e91-179">標頭</span><span class="sxs-lookup"><span data-stu-id="d1e91-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1e91-180"><dt>Wdm (包括 Wdm、Ntddk .h 或 Ntifs. h) </dt></span><span class="sxs-lookup"><span data-stu-id="d1e91-180"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="d1e91-181">程式庫</span><span class="sxs-lookup"><span data-stu-id="d1e91-181">Library</span></span><br/>                  | <dl> <span data-ttu-id="d1e91-182"><dt>Ntdll.dll .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1e91-182"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d1e91-183">DLL</span><span class="sxs-lookup"><span data-stu-id="d1e91-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1e91-184"><dt>Ntdll.dll (使用者模式) </dt></span><span class="sxs-lookup"><span data-stu-id="d1e91-184"><dt>Ntdll.dll (user mode)</dt></span></span> </dl>                                        |



## <a name="see-also"></a><span data-ttu-id="d1e91-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1e91-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1e91-186">**KeInitializeEvent**</span><span class="sxs-lookup"><span data-stu-id="d1e91-186">**KeInitializeEvent**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-keinitializeevent)
</dt> <dt>

[<span data-ttu-id="d1e91-187">**NtCreateFile**</span><span class="sxs-lookup"><span data-stu-id="d1e91-187">**NtCreateFile**</span></span>](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile)
</dt> <dt>

[<span data-ttu-id="d1e91-188">**NtQueryInformationFile**</span><span class="sxs-lookup"><span data-stu-id="d1e91-188">**NtQueryInformationFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntqueryinformationfile)
</dt> <dt>

[<span data-ttu-id="d1e91-189">**NtSetInformationFile**</span><span class="sxs-lookup"><span data-stu-id="d1e91-189">**NtSetInformationFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntsetinformationfile)
</dt> <dt>

[<span data-ttu-id="d1e91-190">**NtWriteFile**</span><span class="sxs-lookup"><span data-stu-id="d1e91-190">**NtWriteFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntwritefile)
</dt> </dl>

 

 
