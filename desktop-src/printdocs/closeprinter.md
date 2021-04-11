---
description: ClosePrinter 函式會關閉指定的印表機物件。
ms.assetid: 95cc3eca-e65c-4fa6-8975-479e8e728dca
title: 'ClosePrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClosePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bd21268b86a07357065d4f33b60d1af4b05fa019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194853"
---
# <a name="closeprinter-function"></a><span data-ttu-id="d0b2a-103">ClosePrinter 函式</span><span class="sxs-lookup"><span data-stu-id="d0b2a-103">ClosePrinter function</span></span>

<span data-ttu-id="d0b2a-104">**ClosePrinter** 函式會關閉指定的印表機物件。</span><span class="sxs-lookup"><span data-stu-id="d0b2a-104">The **ClosePrinter** function closes the specified printer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0b2a-105">語法</span><span class="sxs-lookup"><span data-stu-id="d0b2a-105">Syntax</span></span>


```C++
BOOL ClosePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="d0b2a-106">參數</span><span class="sxs-lookup"><span data-stu-id="d0b2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0b2a-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d0b2a-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0b2a-108">要關閉之印表機物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d0b2a-108">A handle to the printer object to be closed.</span></span> <span data-ttu-id="d0b2a-109">[**OpenPrinter**](openprinter.md)或 [**interactivesession.addprinter**](addprinter.md)函數會傳回此控制碼。</span><span class="sxs-lookup"><span data-stu-id="d0b2a-109">This handle is returned by the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0b2a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0b2a-110">Return value</span></span>

<span data-ttu-id="d0b2a-111">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="d0b2a-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d0b2a-112">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="d0b2a-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0b2a-113">備註</span><span class="sxs-lookup"><span data-stu-id="d0b2a-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d0b2a-114">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="d0b2a-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d0b2a-115">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="d0b2a-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d0b2a-116">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="d0b2a-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d0b2a-117">當 **ClosePrinter** 函式傳回時，無論函式是否成功或失敗，控制碼 *hPrinter* 都是不正確。</span><span class="sxs-lookup"><span data-stu-id="d0b2a-117">When the **ClosePrinter** function returns, the handle *hPrinter* is invalid, regardless of whether the function has succeeded or failed.</span></span>

## <a name="examples"></a><span data-ttu-id="d0b2a-118">範例</span><span class="sxs-lookup"><span data-stu-id="d0b2a-118">Examples</span></span>

<span data-ttu-id="d0b2a-119">如需使用此函式的範例程式，請參閱 [如何：使用 GDI 列印 API 進行列印](how-to--print-using-the-gdi-print-api.md)。</span><span class="sxs-lookup"><span data-stu-id="d0b2a-119">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0b2a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0b2a-120">Requirements</span></span>



| <span data-ttu-id="d0b2a-121">需求</span><span class="sxs-lookup"><span data-stu-id="d0b2a-121">Requirement</span></span> | <span data-ttu-id="d0b2a-122">值</span><span class="sxs-lookup"><span data-stu-id="d0b2a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b2a-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0b2a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d0b2a-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0b2a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d0b2a-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0b2a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d0b2a-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0b2a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d0b2a-127">標頭</span><span class="sxs-lookup"><span data-stu-id="d0b2a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0b2a-128"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d0b2a-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d0b2a-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="d0b2a-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="d0b2a-130"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0b2a-130"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d0b2a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d0b2a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0b2a-132"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0b2a-132"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="d0b2a-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0b2a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0b2a-134">列印</span><span class="sxs-lookup"><span data-stu-id="d0b2a-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d0b2a-135">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="d0b2a-135">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d0b2a-136">**Interactivesession.addprinter**</span><span class="sxs-lookup"><span data-stu-id="d0b2a-136">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="d0b2a-137">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="d0b2a-137">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




