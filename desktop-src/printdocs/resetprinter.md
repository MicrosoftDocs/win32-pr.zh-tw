---
description: ResetPrinter 函式會指定要用於列印 StartDocPrinter 函式所提交檔的資料類型和裝置模式值。 在檔列印開始之後，您可以使用 SetJob 函數來覆寫這些值。
ms.assetid: 9efc6629-dbb7-4320-90b9-07c66f0add47
title: 'ResetPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResetPrinter
- ResetPrinterA
- ResetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8bdfef0229a646e802878a96370d27d49a6bfc2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991864"
---
# <a name="resetprinter-function"></a><span data-ttu-id="1e1ea-104">ResetPrinter 函式</span><span class="sxs-lookup"><span data-stu-id="1e1ea-104">ResetPrinter function</span></span>

<span data-ttu-id="1e1ea-105">**ResetPrinter** 函式會指定要用於列印 [**StartDocPrinter**](startdocprinter.md)函式所提交檔的資料類型和裝置模式值。</span><span class="sxs-lookup"><span data-stu-id="1e1ea-105">The **ResetPrinter** function specifies the data type and device mode values to be used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="1e1ea-106">在檔列印開始之後，您可以使用 [**SetJob**](setjob.md) 函數來覆寫這些值。</span><span class="sxs-lookup"><span data-stu-id="1e1ea-106">These values can be overridden by using the [**SetJob**](setjob.md) function after document printing has started.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e1ea-107">語法</span><span class="sxs-lookup"><span data-stu-id="1e1ea-107">Syntax</span></span>


```C++
BOOL ResetPrinter(
  _In_ HANDLE             hPrinter,
  _In_ LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a><span data-ttu-id="1e1ea-108">參數</span><span class="sxs-lookup"><span data-stu-id="1e1ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e1ea-109">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e1ea-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1ea-110">印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1e1ea-110">Handle to the printer.</span></span> <span data-ttu-id="1e1ea-111">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="1e1ea-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="1e1ea-112">*pDefault* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e1ea-112">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1ea-113">[**印表機 \_ 預設**](printer-defaults.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1e1ea-113">Pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span>

<span data-ttu-id="1e1ea-114">**ResetPrinter** 函數會忽略 [**印表機 \_ 預設**](printer-defaults.md)結構的 **DesiredAccess** 成員。</span><span class="sxs-lookup"><span data-stu-id="1e1ea-114">The **ResetPrinter** function ignores the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="1e1ea-115">將該成員設定為零。</span><span class="sxs-lookup"><span data-stu-id="1e1ea-115">Set that member to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e1ea-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e1ea-116">Return value</span></span>

<span data-ttu-id="1e1ea-117">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="1e1ea-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="1e1ea-118">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="1e1ea-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e1ea-119">備註</span><span class="sxs-lookup"><span data-stu-id="1e1ea-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1e1ea-120">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="1e1ea-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="1e1ea-121">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="1e1ea-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="1e1ea-122">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="1e1ea-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1e1ea-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e1ea-123">Requirements</span></span>



| <span data-ttu-id="1e1ea-124">需求</span><span class="sxs-lookup"><span data-stu-id="1e1ea-124">Requirement</span></span> | <span data-ttu-id="1e1ea-125">值</span><span class="sxs-lookup"><span data-stu-id="1e1ea-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e1ea-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e1ea-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1e1ea-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e1ea-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1e1ea-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e1ea-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1e1ea-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e1ea-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1e1ea-130">標頭</span><span class="sxs-lookup"><span data-stu-id="1e1ea-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e1ea-131"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1e1ea-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1e1ea-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="1e1ea-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e1ea-133"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e1ea-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1e1ea-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1e1ea-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e1ea-135"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="1e1ea-135"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="1e1ea-136">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="1e1ea-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1e1ea-137">**ResetPrinterW** (Unicode) 和 **ResetPrinterA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="1e1ea-137">**ResetPrinterW** (Unicode) and **ResetPrinterA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="1e1ea-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e1ea-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e1ea-139">列印</span><span class="sxs-lookup"><span data-stu-id="1e1ea-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1e1ea-140">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="1e1ea-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1e1ea-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="1e1ea-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="1e1ea-142">**印表機 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="1e1ea-142">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="1e1ea-143">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="1e1ea-143">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="1e1ea-144">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="1e1ea-144">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

 




