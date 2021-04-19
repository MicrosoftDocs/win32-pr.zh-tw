---
description: CloseSpoolFileHandle 函式會關閉與應用程式目前所提交列印工作相關聯之多工緩衝處理檔案的控制碼。
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
title: 'CloseSpoolFileHandle 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CloseSpoolFileHandle
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: c808bddde5b9b4e4a87a8608c1efb3999ce1f391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974259"
---
# <a name="closespoolfilehandle-function"></a><span data-ttu-id="fbc06-103">CloseSpoolFileHandle 函式</span><span class="sxs-lookup"><span data-stu-id="fbc06-103">CloseSpoolFileHandle function</span></span>

<span data-ttu-id="fbc06-104">**CloseSpoolFileHandle** 函式會關閉與應用程式目前所提交列印工作相關聯之多工緩衝處理檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fbc06-104">The **CloseSpoolFileHandle** function closes a handle to a spool file associated with the print job currently submitted by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbc06-105">語法</span><span class="sxs-lookup"><span data-stu-id="fbc06-105">Syntax</span></span>


```C++
BOOL CloseSpoolFileHandle(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile
);
```



## <a name="parameters"></a><span data-ttu-id="fbc06-106">參數</span><span class="sxs-lookup"><span data-stu-id="fbc06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbc06-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbc06-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbc06-108">提交工作之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fbc06-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="fbc06-109">這應該是用來取得 *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md)的相同控制碼。</span><span class="sxs-lookup"><span data-stu-id="fbc06-109">This should be the same handle that was used to obtain *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="fbc06-110">*hSpoolFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbc06-110">*hSpoolFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbc06-111">要關閉之多工緩衝處理檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fbc06-111">A handle to the spool file being closed.</span></span> <span data-ttu-id="fbc06-112">如果在呼叫 [**GetSpoolFileHandle**](getspoolfilehandle.md)之後尚未呼叫 [**CommitSpoolData**](commitspooldata.md) ，則這應該與 **GetSpoolFileHandle** 所傳回的控制碼相同。</span><span class="sxs-lookup"><span data-stu-id="fbc06-112">If [**CommitSpoolData**](commitspooldata.md) has not been called since [**GetSpoolFileHandle**](getspoolfilehandle.md) was called, then this should be the same handle that was returned by **GetSpoolFileHandle**.</span></span> <span data-ttu-id="fbc06-113">否則，它應該是最近呼叫 **CommitSpoolData** 所傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fbc06-113">Otherwise, it should be the handle that was returned by the most recent call to **CommitSpoolData**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbc06-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fbc06-114">Return value</span></span>

<span data-ttu-id="fbc06-115">如果成功，**則為 TRUE**，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="fbc06-115">**TRUE**, if it succeeds, **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbc06-116">備註</span><span class="sxs-lookup"><span data-stu-id="fbc06-116">Remarks</span></span>

<span data-ttu-id="fbc06-117">您的應用程式不能在 *hPrinter* 上呼叫 [**ClosePrinter**](closeprinter.md) ，直到它上次存取多工緩衝處理檔案為止。</span><span class="sxs-lookup"><span data-stu-id="fbc06-117">Your application must not call [**ClosePrinter**](closeprinter.md) on *hPrinter* until after it has accessed the spool file for the last time.</span></span> <span data-ttu-id="fbc06-118">然後，它應該呼叫 **CloseSpoolFileHandle** ，後面接著 **ClosePrinter**。</span><span class="sxs-lookup"><span data-stu-id="fbc06-118">Then it should call **CloseSpoolFileHandle** followed by **ClosePrinter**.</span></span> <span data-ttu-id="fbc06-119">在原始 *hPrinter* 關閉之後，嘗試存取多工緩衝處理檔案控制代碼會失敗，即使檔案控制代碼本身尚未關閉也一樣。</span><span class="sxs-lookup"><span data-stu-id="fbc06-119">Attempts to access the spool file handle after the original *hPrinter* has been closed will fail even if the file handle itself has not been closed.</span></span> <span data-ttu-id="fbc06-120">如果先呼叫 **ClosePrinter** ， **CloseSpoolFileHandle** 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="fbc06-120">**CloseSpoolFileHandle** will fail if **ClosePrinter** is called first.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbc06-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbc06-121">Requirements</span></span>



| <span data-ttu-id="fbc06-122">需求</span><span class="sxs-lookup"><span data-stu-id="fbc06-122">Requirement</span></span> | <span data-ttu-id="fbc06-123">值</span><span class="sxs-lookup"><span data-stu-id="fbc06-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc06-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fbc06-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fbc06-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbc06-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="fbc06-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fbc06-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fbc06-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbc06-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fbc06-128">標頭</span><span class="sxs-lookup"><span data-stu-id="fbc06-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbc06-129"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fbc06-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fbc06-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="fbc06-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="fbc06-131"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbc06-131"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="fbc06-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fbc06-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbc06-133"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="fbc06-133"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="fbc06-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbc06-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbc06-135">列印</span><span class="sxs-lookup"><span data-stu-id="fbc06-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fbc06-136">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="fbc06-136">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="fbc06-137">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="fbc06-137">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="fbc06-138">**GetSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="fbc06-138">**GetSpoolFileHandle**</span></span>](getspoolfilehandle.md)
</dt> </dl>

 

 




