---
description: GetSpoolFileHandle 函式會抓取與應用程式目前所提交之作業相關聯的多工緩衝處理檔案的控制碼。
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: 'GetSpoolFileHandle 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSpoolFileHandle
- GetSpoolFileHandleA
- GetSpoolFileHandleW
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9ac4dd4b0db9a59cc0140872ff04f89adaf8b6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027460"
---
# <a name="getspoolfilehandle-function"></a><span data-ttu-id="f2140-103">GetSpoolFileHandle 函式</span><span class="sxs-lookup"><span data-stu-id="f2140-103">GetSpoolFileHandle function</span></span>

<span data-ttu-id="f2140-104">**GetSpoolFileHandle** 函式會抓取與應用程式目前所提交之作業相關聯的多工緩衝處理檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f2140-104">The **GetSpoolFileHandle** function retrieves a handle for the spool file associated with the job currently submitted by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2140-105">語法</span><span class="sxs-lookup"><span data-stu-id="f2140-105">Syntax</span></span>


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="f2140-106">參數</span><span class="sxs-lookup"><span data-stu-id="f2140-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2140-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2140-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2140-108">提交工作之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f2140-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="f2140-109">這應該是用來提交作業的相同控制碼。</span><span class="sxs-lookup"><span data-stu-id="f2140-109">This should be the same handle that was used to submit the job.</span></span> <span data-ttu-id="f2140-110"> (使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函數來取出印表機控制碼。 ) </span><span class="sxs-lookup"><span data-stu-id="f2140-110">(Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2140-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2140-111">Return value</span></span>

<span data-ttu-id="f2140-112">如果函式成功，它會將控制碼傳回至多工緩衝處理檔案。</span><span class="sxs-lookup"><span data-stu-id="f2140-112">If the function succeeds, it returns a handle to the spool file.</span></span>

<span data-ttu-id="f2140-113">如果函式失敗，則會傳回 **不正確 \_ 控制碼 \_ 值**。</span><span class="sxs-lookup"><span data-stu-id="f2140-113">If the function fails, it returns **INVALID\_HANDLE\_VALUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2140-114">備註</span><span class="sxs-lookup"><span data-stu-id="f2140-114">Remarks</span></span>

<span data-ttu-id="f2140-115">使用多工緩衝處理檔案的控制碼時，您的應用程式可以使用 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) 的呼叫來寫入多工緩衝處理檔案，後面接著 [**CommitSpoolData**](commitspooldata.md)。</span><span class="sxs-lookup"><span data-stu-id="f2140-115">With the handle to the spool file, your application can write to the spool file with calls to [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) followed by [**CommitSpoolData**](commitspooldata.md).</span></span>

<span data-ttu-id="f2140-116">您的應用程式不能在 *hPrinter* 上呼叫 [**ClosePrinter**](closeprinter.md) ，直到它上次存取多工緩衝處理檔案為止。</span><span class="sxs-lookup"><span data-stu-id="f2140-116">Your application must not call [**ClosePrinter**](closeprinter.md) on *hPrinter* until after it has accessed the spool file for the last time.</span></span> <span data-ttu-id="f2140-117">然後，它應該呼叫 [**CloseSpoolFileHandle**](closespoolfilehandle.md) ，後面接著 **ClosePrinter**。</span><span class="sxs-lookup"><span data-stu-id="f2140-117">Then it should call [**CloseSpoolFileHandle**](closespoolfilehandle.md) followed by **ClosePrinter**.</span></span> <span data-ttu-id="f2140-118">在原始 *hPrinter* 關閉之後，嘗試存取多工緩衝處理檔案控制代碼會失敗，即使檔案控制代碼本身尚未關閉也一樣。</span><span class="sxs-lookup"><span data-stu-id="f2140-118">Attempts to access the spool file handle after the original *hPrinter* has been closed will fail even if the file handle itself has not been closed.</span></span> <span data-ttu-id="f2140-119">如果先呼叫 **ClosePrinter** ， **CloseSpoolFileHandle** 本身將會失敗。</span><span class="sxs-lookup"><span data-stu-id="f2140-119">**CloseSpoolFileHandle** will itself fail if **ClosePrinter** is called first.</span></span>

<span data-ttu-id="f2140-120">如果在列印工作完成幕後處理之前呼叫這個函式，此函式將會失敗。</span><span class="sxs-lookup"><span data-stu-id="f2140-120">This function will fail if it is called before the print job has finished spooling.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2140-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2140-121">Requirements</span></span>



| <span data-ttu-id="f2140-122">需求</span><span class="sxs-lookup"><span data-stu-id="f2140-122">Requirement</span></span> | <span data-ttu-id="f2140-123">值</span><span class="sxs-lookup"><span data-stu-id="f2140-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2140-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2140-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f2140-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2140-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f2140-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2140-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f2140-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2140-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f2140-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f2140-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2140-129"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f2140-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f2140-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="f2140-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2140-131"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2140-131"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f2140-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f2140-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2140-133"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="f2140-133"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f2140-134">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="f2140-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f2140-135">**GetSpoolFileHandleW** (Unicode) 和 **GetSpoolFileHandleA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="f2140-135">**GetSpoolFileHandleW** (Unicode) and **GetSpoolFileHandleA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="f2140-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2140-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2140-137">列印</span><span class="sxs-lookup"><span data-stu-id="f2140-137">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f2140-138">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="f2140-138">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f2140-139">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="f2140-139">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="f2140-140">**Interactivesession.addprinter**</span><span class="sxs-lookup"><span data-stu-id="f2140-140">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="f2140-141">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="f2140-141">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="f2140-142">**CloseSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="f2140-142">**CloseSpoolFileHandle**</span></span>](closespoolfilehandle.md)
</dt> <dt>

[<span data-ttu-id="f2140-143">**CommitSpoolData**</span><span class="sxs-lookup"><span data-stu-id="f2140-143">**CommitSpoolData**</span></span>](commitspooldata.md)
</dt> </dl>

 

