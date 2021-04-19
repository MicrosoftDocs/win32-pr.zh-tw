---
description: GetDefaultPrinter 函式會針對本機電腦上的目前使用者，抓取預設印表機的印表機名稱。
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: 'GetDefaultPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDefaultPrinter
- GetDefaultPrinterA
- GetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8db5b2aef859ea5d8247fc203611af74c8daddd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985447"
---
# <a name="getdefaultprinter-function"></a><span data-ttu-id="02b0a-103">GetDefaultPrinter 函式</span><span class="sxs-lookup"><span data-stu-id="02b0a-103">GetDefaultPrinter function</span></span>

<span data-ttu-id="02b0a-104">**GetDefaultPrinter** 函式會針對本機電腦上的目前使用者，抓取預設印表機的印表機名稱。</span><span class="sxs-lookup"><span data-stu-id="02b0a-104">The **GetDefaultPrinter** function retrieves the printer name of the default printer for the current user on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="02b0a-105">語法</span><span class="sxs-lookup"><span data-stu-id="02b0a-105">Syntax</span></span>


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="02b0a-106">參數</span><span class="sxs-lookup"><span data-stu-id="02b0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02b0a-107">*pszBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="02b0a-107">*pszBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02b0a-108">緩衝區的指標，此緩衝區會接收以 null 終止的字元字串，其中包含預設印表機名稱。</span><span class="sxs-lookup"><span data-stu-id="02b0a-108">A pointer to a buffer that receives a null-terminated character string containing the default printer name.</span></span> <span data-ttu-id="02b0a-109">如果這個參數為 **Null**，則函式會失敗，而且 *pcchBuffer* 所指向的變數會傳回所需的緩衝區大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="02b0a-109">If this parameter is **NULL**, the function fails and the variable pointed to by *pcchBuffer* returns the required buffer size, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="02b0a-110">*pcchBuffer* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="02b0a-110">*pcchBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="02b0a-111">在 [輸入] 上，指定 *pszBuffer* 緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="02b0a-111">On input, specifies the size, in characters, of the *pszBuffer* buffer.</span></span> <span data-ttu-id="02b0a-112">在輸出時，會接收印表機名稱字串的大小（以字元為單位），包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="02b0a-112">On output, receives the size, in characters, of the printer name string, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02b0a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="02b0a-113">Return value</span></span>

<span data-ttu-id="02b0a-114">如果函式成功，則傳回值為非零值，且 *pcchBuffer* 所指向的變數包含複製到 *pszBuffer* 緩衝區的字元數，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="02b0a-114">If the function succeeds, the return value is a nonzero value and the variable pointed to by *pcchBuffer* contains the number of characters copied to the *pszBuffer* buffer, including the terminating null character.</span></span>

<span data-ttu-id="02b0a-115">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="02b0a-115">If the function fails, the return value is zero.</span></span>



| <span data-ttu-id="02b0a-116">值</span><span class="sxs-lookup"><span data-stu-id="02b0a-116">Value</span></span>                       | <span data-ttu-id="02b0a-117">意義</span><span class="sxs-lookup"><span data-stu-id="02b0a-117">Meaning</span></span>                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b0a-118">\_緩衝區不足的錯誤 \_</span><span class="sxs-lookup"><span data-stu-id="02b0a-118">ERROR\_INSUFFICIENT\_BUFFER</span></span> | <span data-ttu-id="02b0a-119">*PszBuffer* 緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="02b0a-119">The *pszBuffer* buffer is too small.</span></span> <span data-ttu-id="02b0a-120">*PcchBuffer* 所指向的變數包含所需的緩衝區大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="02b0a-120">The variable pointed to by *pcchBuffer* contains the required buffer size, in characters.</span></span> |
| <span data-ttu-id="02b0a-121">\_ \_ \_ 找不到錯誤檔案</span><span class="sxs-lookup"><span data-stu-id="02b0a-121">ERROR\_FILE\_NOT\_FOUND</span></span>     | <span data-ttu-id="02b0a-122">沒有預設印表機。</span><span class="sxs-lookup"><span data-stu-id="02b0a-122">There is no default printer.</span></span>                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="02b0a-123">備註</span><span class="sxs-lookup"><span data-stu-id="02b0a-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="02b0a-124">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="02b0a-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="02b0a-125">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="02b0a-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="02b0a-126">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="02b0a-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="02b0a-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="02b0a-127">Requirements</span></span>



| <span data-ttu-id="02b0a-128">需求</span><span class="sxs-lookup"><span data-stu-id="02b0a-128">Requirement</span></span> | <span data-ttu-id="02b0a-129">值</span><span class="sxs-lookup"><span data-stu-id="02b0a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b0a-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02b0a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="02b0a-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02b0a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="02b0a-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02b0a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="02b0a-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02b0a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="02b0a-134">標頭</span><span class="sxs-lookup"><span data-stu-id="02b0a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="02b0a-135"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="02b0a-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="02b0a-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="02b0a-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="02b0a-137"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="02b0a-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="02b0a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="02b0a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02b0a-139"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="02b0a-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="02b0a-140">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="02b0a-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="02b0a-141">**GetDefaultPrinterW** (Unicode) 和 **GetDefaultPrinterA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="02b0a-141">**GetDefaultPrinterW** (Unicode) and **GetDefaultPrinterA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="02b0a-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02b0a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02b0a-143">列印</span><span class="sxs-lookup"><span data-stu-id="02b0a-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="02b0a-144">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="02b0a-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="02b0a-145">**SetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="02b0a-145">**SetDefaultPrinter**</span></span>](setdefaultprinter.md)
</dt> </dl>

 

 




