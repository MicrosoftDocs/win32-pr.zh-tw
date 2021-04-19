---
description: DeletePrinter 函式會刪除指定的印表機物件。
ms.assetid: 04d9c073-b795-4307-ba89-d4984bc5b354
title: 'DeletePrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 16d82a263b09c87f5c9b9725db48dd6634404ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969343"
---
# <a name="deleteprinter-function"></a><span data-ttu-id="9badf-103">DeletePrinter 函式</span><span class="sxs-lookup"><span data-stu-id="9badf-103">DeletePrinter function</span></span>

<span data-ttu-id="9badf-104">**DeletePrinter** 函式會刪除指定的印表機物件。</span><span class="sxs-lookup"><span data-stu-id="9badf-104">The **DeletePrinter** function deletes the specified printer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9badf-105">語法</span><span class="sxs-lookup"><span data-stu-id="9badf-105">Syntax</span></span>


```C++
BOOL DeletePrinter(
  _Inout_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="9badf-106">參數</span><span class="sxs-lookup"><span data-stu-id="9badf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9badf-107">*hPrinter* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="9badf-107">*hPrinter* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9badf-108">將刪除之印表機物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9badf-108">Handle to a printer object that will be deleted.</span></span> <span data-ttu-id="9badf-109">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="9badf-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9badf-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9badf-110">Return value</span></span>

<span data-ttu-id="9badf-111">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="9badf-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9badf-112">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="9badf-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9badf-113">備註</span><span class="sxs-lookup"><span data-stu-id="9badf-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9badf-114">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="9badf-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9badf-115">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="9badf-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9badf-116">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="9badf-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="9badf-117">如果有其他要針對指定印表機處理的列印工作， **DeletePrinter** 會將印表機標示為待刪除，然後在列印所有列印工作時將其刪除。</span><span class="sxs-lookup"><span data-stu-id="9badf-117">If there are print jobs remaining to be processed for the specified printer, **DeletePrinter** marks the printer for pending deletion, and then deletes it when all the print jobs have been printed.</span></span> <span data-ttu-id="9badf-118">沒有列印工作可新增至標示為待刪除的印表機。</span><span class="sxs-lookup"><span data-stu-id="9badf-118">No print jobs can be added to a printer that is marked for pending deletion.</span></span>

<span data-ttu-id="9badf-119">無法保留標示為待刪除的印表機，但可以保留、繼續和重新開機其列印工作。</span><span class="sxs-lookup"><span data-stu-id="9badf-119">A printer marked for pending deletion cannot be held, but its print jobs can be held, resumed, and restarted.</span></span> <span data-ttu-id="9badf-120">如果印表機已保留，且印表機有工作， **DeletePrinter** 會失敗，並會 \_ 拒絕存取錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9badf-120">If the printer is held and there are jobs for the printer, **DeletePrinter** fails with ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="9badf-121">請注意， **DeletePrinter** 不會關閉傳遞給它的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9badf-121">Note that **DeletePrinter** does not close the handle that is passed to it.</span></span> <span data-ttu-id="9badf-122">因此，應用程式仍然必須呼叫 [**ClosePrinter**](closeprinter.md)。</span><span class="sxs-lookup"><span data-stu-id="9badf-122">Thus, the application must still call [**ClosePrinter**](closeprinter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9badf-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="9badf-123">Requirements</span></span>



| <span data-ttu-id="9badf-124">需求</span><span class="sxs-lookup"><span data-stu-id="9badf-124">Requirement</span></span> | <span data-ttu-id="9badf-125">值</span><span class="sxs-lookup"><span data-stu-id="9badf-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9badf-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9badf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9badf-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9badf-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9badf-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9badf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9badf-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9badf-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9badf-130">標頭</span><span class="sxs-lookup"><span data-stu-id="9badf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9badf-131"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="9badf-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9badf-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="9badf-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="9badf-133"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9badf-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9badf-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9badf-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9badf-135"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9badf-135"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="9badf-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9badf-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9badf-137">列印</span><span class="sxs-lookup"><span data-stu-id="9badf-137">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9badf-138">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="9badf-138">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9badf-139">**Interactivesession.addprinter**</span><span class="sxs-lookup"><span data-stu-id="9badf-139">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="9badf-140">**>enumprinters**</span><span class="sxs-lookup"><span data-stu-id="9badf-140">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="9badf-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="9badf-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




