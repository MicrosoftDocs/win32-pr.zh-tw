---
description: AddPrintProcessor 函式會在指定的伺服器上安裝列印處理器，並將列印處理器名稱新增至支援的列印處理器清單。
ms.assetid: 99899cee-f74d-4405-8ea5-616e3769aba9
title: 'AddPrintProcessor 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProcessor
- AddPrintProcessorA
- AddPrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 871df9fee211ae13e1552978ce651840d7f542f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988974"
---
# <a name="addprintprocessor-function"></a><span data-ttu-id="5204d-103">AddPrintProcessor 函式</span><span class="sxs-lookup"><span data-stu-id="5204d-103">AddPrintProcessor function</span></span>

<span data-ttu-id="5204d-104">**AddPrintProcessor** 函式會在指定的伺服器上安裝列印處理器，並將列印處理器名稱新增至支援的列印處理器清單。</span><span class="sxs-lookup"><span data-stu-id="5204d-104">The **AddPrintProcessor** function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.</span></span>

## <a name="syntax"></a><span data-ttu-id="5204d-105">語法</span><span class="sxs-lookup"><span data-stu-id="5204d-105">Syntax</span></span>


```C++
BOOL AddPrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPathName,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a><span data-ttu-id="5204d-106">參數</span><span class="sxs-lookup"><span data-stu-id="5204d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5204d-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5204d-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5204d-108">以 null 結束的字串指標，指定應該安裝列印處理器之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5204d-108">A pointer to a null-terminated string that specifies the name of the server on which the print processor should be installed.</span></span> <span data-ttu-id="5204d-109">如果此參數為 **Null**，則會在本機安裝列印處理器。</span><span class="sxs-lookup"><span data-stu-id="5204d-109">If this parameter is **NULL**, the print processor is installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="5204d-110">*pEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5204d-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5204d-111">以 null 結束的字串指標，指定環境 (例如，Windows x86、Windows IA64 或 Windows x64) 。</span><span class="sxs-lookup"><span data-stu-id="5204d-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="5204d-112">如果這個參數是 **Null**，則會使用目前的呼叫端/用戶端環境 (不是目的地/伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="5204d-112">If this parameter is **NULL**, the current environment of the caller/client (not of the destination/server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="5204d-113">*pPathName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5204d-113">*pPathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5204d-114">以 null 結束的字串指標，指定包含列印處理器之檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="5204d-114">A pointer to a null-terminated string that specifies the name of the file that contains the print processor.</span></span> <span data-ttu-id="5204d-115">此檔案必須位於系統列印處理器目錄中。</span><span class="sxs-lookup"><span data-stu-id="5204d-115">This file must be in the system print-processor directory.</span></span>

</dd> <dt>

<span data-ttu-id="5204d-116">*pPrintProcessorName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5204d-116">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5204d-117">指定列印處理器名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="5204d-117">A pointer to a null-terminated string that specifies the name of the print processor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5204d-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="5204d-118">Return value</span></span>

<span data-ttu-id="5204d-119">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="5204d-119">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="5204d-120">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="5204d-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5204d-121">備註</span><span class="sxs-lookup"><span data-stu-id="5204d-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5204d-122">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="5204d-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="5204d-123">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="5204d-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="5204d-124">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="5204d-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="5204d-125">呼叫端必須有 [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)。</span><span class="sxs-lookup"><span data-stu-id="5204d-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="5204d-126">在呼叫 **AddPrintProcessor** 函式之前，應用程式應該確認包含列印處理器的檔案儲存在系統列印處理器目錄中。</span><span class="sxs-lookup"><span data-stu-id="5204d-126">Before calling the **AddPrintProcessor** function, an application should verify that the file containing the print processor is stored in the system print-processor directory.</span></span> <span data-ttu-id="5204d-127">應用程式可以藉由呼叫 [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) 函式來取出系統列印處理器目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="5204d-127">An application can retrieve the name of the system print-processor directory by calling the [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) function.</span></span>

<span data-ttu-id="5204d-128">應用程式可以藉由呼叫 [**EnumPrintProcessors**](enumprintprocessors.md) 函數來判斷現有列印處理器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5204d-128">An application can determine the name of existing print processors by calling the [**EnumPrintProcessors**](enumprintprocessors.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5204d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="5204d-129">Requirements</span></span>



| <span data-ttu-id="5204d-130">需求</span><span class="sxs-lookup"><span data-stu-id="5204d-130">Requirement</span></span> | <span data-ttu-id="5204d-131">值</span><span class="sxs-lookup"><span data-stu-id="5204d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5204d-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5204d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5204d-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5204d-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5204d-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5204d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5204d-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5204d-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5204d-136">標頭</span><span class="sxs-lookup"><span data-stu-id="5204d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5204d-137"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5204d-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5204d-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="5204d-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="5204d-139"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5204d-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="5204d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5204d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5204d-141"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="5204d-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="5204d-142">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="5204d-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5204d-143">**AddPrintProcessorW** (Unicode) 和 **AddPrintProcessorA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="5204d-143">**AddPrintProcessorW** (Unicode) and **AddPrintProcessorA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="5204d-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5204d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5204d-145">列印</span><span class="sxs-lookup"><span data-stu-id="5204d-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5204d-146">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="5204d-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="5204d-147">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="5204d-147">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> <dt>

[<span data-ttu-id="5204d-148">**GetPrintProcessorDirectory**</span><span class="sxs-lookup"><span data-stu-id="5204d-148">**GetPrintProcessorDirectory**</span></span>](getprintprocessordirectory.md)
</dt> </dl>

 

