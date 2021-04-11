---
description: 向「列印多工緩衝處理器」服務回報 XPS 列印工作是否在幕後處理或轉譯階段，以及處理的哪個部分正在進行中。
ms.assetid: 66f7483d-be98-410d-b0c7-430743397de2
title: 'ReportJobProcessingProgress 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportJobProcessingProgress
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 327d2f7cffe2f90a5719de38cef4cd3fde17e086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944685"
---
# <a name="reportjobprocessingprogress-function"></a><span data-ttu-id="55f2b-103">ReportJobProcessingProgress 函式</span><span class="sxs-lookup"><span data-stu-id="55f2b-103">ReportJobProcessingProgress function</span></span>

<span data-ttu-id="55f2b-104">向「列印多工緩衝處理器」服務回報 XPS 列印工作是否在幕後處理或轉譯階段，以及處理的哪個部分正在進行中。</span><span class="sxs-lookup"><span data-stu-id="55f2b-104">Reports to the Print Spooler service whether an XPS print job is in the spooling or the rendering phase and what part of the processing is currently underway.</span></span>

## <a name="syntax"></a><span data-ttu-id="55f2b-105">語法</span><span class="sxs-lookup"><span data-stu-id="55f2b-105">Syntax</span></span>


```C++
HRESULT ReportJobProcessingProgress(
  _In_ HANDLE                printerHandle,
  _In_ ULONG                 jobId,
       EPrintXPSJobOperation jobOperation,
       EPrintXPSJobProgress  jobProgress
);
```



## <a name="parameters"></a><span data-ttu-id="55f2b-106">參數</span><span class="sxs-lookup"><span data-stu-id="55f2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55f2b-107">*printerHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55f2b-107">*printerHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55f2b-108">函式用來取得資訊的印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="55f2b-108">A printer handle for which the function is to retrieve information.</span></span> <span data-ttu-id="55f2b-109">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="55f2b-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="55f2b-110">*jobId* \[in\]</span><span class="sxs-lookup"><span data-stu-id="55f2b-110">*jobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55f2b-111">識別要取出資料的列印工作。</span><span class="sxs-lookup"><span data-stu-id="55f2b-111">Identifies the print job for which to retrieve data.</span></span> <span data-ttu-id="55f2b-112">您可以使用 [**system.printing.printqueue.addjob**](addjob.md) 函數或 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) 函數來取得列印工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="55f2b-112">Use the [**AddJob**](addjob.md) function or [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function to get a print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="55f2b-113">*jobOperation*</span><span class="sxs-lookup"><span data-stu-id="55f2b-113">*jobOperation*</span></span> 
</dt> <dd>

<span data-ttu-id="55f2b-114">指定作業是在幕後處理階段或轉譯階段。</span><span class="sxs-lookup"><span data-stu-id="55f2b-114">Specifies whether the job is in the spooling phase or the rendering phase.</span></span>

</dd> <dt>

<span data-ttu-id="55f2b-115">*jobProgress*</span><span class="sxs-lookup"><span data-stu-id="55f2b-115">*jobProgress*</span></span> 
</dt> <dd>

<span data-ttu-id="55f2b-116">指定處理中的哪個部分正在進行中。</span><span class="sxs-lookup"><span data-stu-id="55f2b-116">Specifies what part of the processing is currently underway.</span></span> <span data-ttu-id="55f2b-117">根據 *jobOperation* 的值，此值會參考在幕後處理或轉譯階段中的事件。</span><span class="sxs-lookup"><span data-stu-id="55f2b-117">This value refers to events in either the spooling or rendering phase depending on the value of *jobOperation*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55f2b-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="55f2b-118">Return value</span></span>

<span data-ttu-id="55f2b-119">如果作業成功，則傳回值為 S \_ OK，否則 **HRESULT** 會包含錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="55f2b-119">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="55f2b-120">如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="55f2b-120">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="55f2b-121">備註</span><span class="sxs-lookup"><span data-stu-id="55f2b-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="55f2b-122">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="55f2b-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="55f2b-123">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="55f2b-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="55f2b-124">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="55f2b-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

> [!Note]  
> <span data-ttu-id="55f2b-125">**ReportJobProcessingProgress** 只會報告 XPS 列印工作在幕後處理或轉譯階段的進度。</span><span class="sxs-lookup"><span data-stu-id="55f2b-125">**ReportJobProcessingProgress** will only report the progress of the XPS print job if the print job is in the spooling or rendering phase.</span></span> <span data-ttu-id="55f2b-126">如果 XPS 列印工作不在幕後處理或轉譯階段時呼叫， **ReportJobProcessingProgress** 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="55f2b-126">**ReportJobProcessingProgress** will fail if it is called when the XPS print job is not in the spooling or rendering phase.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="55f2b-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="55f2b-127">Requirements</span></span>



| <span data-ttu-id="55f2b-128">需求</span><span class="sxs-lookup"><span data-stu-id="55f2b-128">Requirement</span></span> | <span data-ttu-id="55f2b-129">值</span><span class="sxs-lookup"><span data-stu-id="55f2b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55f2b-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55f2b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="55f2b-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55f2b-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="55f2b-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55f2b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="55f2b-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55f2b-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="55f2b-134">標頭</span><span class="sxs-lookup"><span data-stu-id="55f2b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="55f2b-135"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="55f2b-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="55f2b-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="55f2b-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="55f2b-137"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="55f2b-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="55f2b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="55f2b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55f2b-139"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55f2b-139"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="55f2b-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55f2b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55f2b-141">列印</span><span class="sxs-lookup"><span data-stu-id="55f2b-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="55f2b-142">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="55f2b-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="55f2b-143">**EPrintXPSJobOperation**</span><span class="sxs-lookup"><span data-stu-id="55f2b-143">**EPrintXPSJobOperation**</span></span>](eprintxpsjoboperation.md)
</dt> <dt>

[<span data-ttu-id="55f2b-144">**EPrintXPSJobProgress**</span><span class="sxs-lookup"><span data-stu-id="55f2b-144">**EPrintXPSJobProgress**</span></span>](eprintxpsjobprogress.md)
</dt> </dl>

 

