---
description: CommitSpoolData 函式會通知列印多工緩衝處理器，指定的資料量已寫入指定的多工緩衝處理檔案，而且已準備好可供轉譯。
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: 'CommitSpoolData 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommitSpoolData
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: fa90cb1344e7c087a601a74991598e509daed226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849112"
---
# <a name="commitspooldata-function"></a><span data-ttu-id="d9e8c-103">CommitSpoolData 函式</span><span class="sxs-lookup"><span data-stu-id="d9e8c-103">CommitSpoolData function</span></span>

<span data-ttu-id="d9e8c-104">**CommitSpoolData** 函式會通知列印多工緩衝處理器，指定的資料量已寫入指定的多工緩衝處理檔案，而且已準備好可供轉譯。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-104">The **CommitSpoolData** function notifies the print spooler that a specified amount of data has been written to a specified spool file and is ready to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9e8c-105">語法</span><span class="sxs-lookup"><span data-stu-id="d9e8c-105">Syntax</span></span>


```C++
HANDLE CommitSpoolData(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile,
       DWORD  cbCommit
);
```



## <a name="parameters"></a><span data-ttu-id="d9e8c-106">參數</span><span class="sxs-lookup"><span data-stu-id="d9e8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9e8c-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d9e8c-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e8c-108">提交工作之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="d9e8c-109">這應該是用來取得 *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md)的相同控制碼。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-109">This should be the same handle that was used to obtain *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9e8c-110">*hSpoolFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d9e8c-110">*hSpoolFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e8c-111">要變更之多工緩衝處理檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-111">A handle to the spool file being changed.</span></span> <span data-ttu-id="d9e8c-112">在第一次呼叫 **CommitSpoolData** 時，這應該與 [**GetSpoolFileHandle**](getspoolfilehandle.md)所傳回的控制碼相同。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-112">On the first call of **CommitSpoolData**, this should be the same handle that was returned by [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span> <span data-ttu-id="d9e8c-113">對 **CommitSpoolData** 的後續呼叫應該傳遞先前呼叫所傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-113">Subsequent calls to **CommitSpoolData** should pass the handle returned by the preceding call.</span></span> <span data-ttu-id="d9e8c-114">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d9e8c-115">*cbCommit*</span><span class="sxs-lookup"><span data-stu-id="d9e8c-115">*cbCommit*</span></span> 
</dt> <dd>

<span data-ttu-id="d9e8c-116">認可至列印多工緩衝處理器的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-116">The number of bytes committed to the print spooler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9e8c-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9e8c-117">Return value</span></span>

<span data-ttu-id="d9e8c-118">如果函式成功，它會將控制碼傳回至多工緩衝處理檔案。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-118">If the function succeeds, it returns a handle to the spool file.</span></span>

<span data-ttu-id="d9e8c-119">如果函式失敗，則會傳回不正確 \_ 控制碼 \_ 值。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-119">If the function fails, it returns INVALID\_HANDLE\_VALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9e8c-120">備註</span><span class="sxs-lookup"><span data-stu-id="d9e8c-120">Remarks</span></span>

<span data-ttu-id="d9e8c-121">提交多工緩衝處理器列印工作的應用程式可以呼叫 [**GetSpoolFileHandle**](getspoolfilehandle.md) ，然後藉由呼叫 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)，直接將資料寫入多工緩衝處理檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-121">Applications submitting a spooler print job can call [**GetSpoolFileHandle**](getspoolfilehandle.md) and then directly write data to the spool file handle by calling [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile).</span></span> <span data-ttu-id="d9e8c-122">若要通知「列印多工緩衝處理器」檔案包含可供轉譯的資料，應用程式必須呼叫 **CommitSpoolData** 並提供可用的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-122">To notify the print spooler that the file contains data which is ready to be rendered, the application must call **CommitSpoolData** and provide the number of available bytes.</span></span>

<span data-ttu-id="d9e8c-123">如果呼叫 **CommitSpoolData** 多次，則每次呼叫都必須使用先前呼叫所傳回的多工緩衝處理檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-123">If **CommitSpoolData** is called multiple times, each call must use the spool file handle returned by the previous call.</span></span> <span data-ttu-id="d9e8c-124">如果不再將任何資料寫入多工緩衝處理檔案，則應該針對上次呼叫 **CommitSpoolData** 所傳回的檔案控制代碼呼叫 [**CloseSpoolFileHandle**](closespoolfilehandle.md) 。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-124">When no more data will be written to the spool file, [**CloseSpoolFileHandle**](closespoolfilehandle.md) should be called for the file handle returned by the last call to **CommitSpoolData**.</span></span>

<span data-ttu-id="d9e8c-125">在呼叫 **CommitSpoolData** 之前，應用程式必須將檔案指標設定為將資料寫入檔案之前的位置。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-125">Before calling **CommitSpoolData**, applications must set the file pointer to the position it had before it wrote data to the file.</span></span> <span data-ttu-id="d9e8c-126">在以多工緩衝處理器檔案轉譯資料的過程中，列印多工緩衝處理器會將多工緩衝處理檔案指標從目前的檔案指標值移至 *cbCommit* 位元組。</span><span class="sxs-lookup"><span data-stu-id="d9e8c-126">In the process of rendering the data in the spooler file, the print spooler will move the spool file pointer *cbCommit* bytes from the current value of file pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9e8c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9e8c-127">Requirements</span></span>



| <span data-ttu-id="d9e8c-128">需求</span><span class="sxs-lookup"><span data-stu-id="d9e8c-128">Requirement</span></span> | <span data-ttu-id="d9e8c-129">值</span><span class="sxs-lookup"><span data-stu-id="d9e8c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9e8c-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d9e8c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d9e8c-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9e8c-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d9e8c-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d9e8c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d9e8c-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9e8c-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d9e8c-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d9e8c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9e8c-135"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d9e8c-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d9e8c-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="d9e8c-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9e8c-137"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9e8c-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d9e8c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d9e8c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9e8c-139"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="d9e8c-139"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="d9e8c-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9e8c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9e8c-141">列印</span><span class="sxs-lookup"><span data-stu-id="d9e8c-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d9e8c-142">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="d9e8c-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d9e8c-143">**GetSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="d9e8c-143">**GetSpoolFileHandle**</span></span>](getspoolfilehandle.md)
</dt> <dt>

[<span data-ttu-id="d9e8c-144">**CloseSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="d9e8c-144">**CloseSpoolFileHandle**</span></span>](closespoolfilehandle.md)
</dt> </dl>

 

