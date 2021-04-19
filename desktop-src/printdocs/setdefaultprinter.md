---
description: SetDefaultPrinter 函式會設定本機電腦上目前使用者之預設印表機的印表機名稱。
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: 'SetDefaultPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDefaultPrinter
- SetDefaultPrinterA
- SetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 346d356aea3d806284823541aa219699e51c2187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985243"
---
# <a name="setdefaultprinter-function"></a><span data-ttu-id="c4b81-103">SetDefaultPrinter 函式</span><span class="sxs-lookup"><span data-stu-id="c4b81-103">SetDefaultPrinter function</span></span>

<span data-ttu-id="c4b81-104">**SetDefaultPrinter** 函式會設定本機電腦上目前使用者之預設印表機的印表機名稱。</span><span class="sxs-lookup"><span data-stu-id="c4b81-104">The **SetDefaultPrinter** function sets the printer name of the default printer for the current user on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4b81-105">語法</span><span class="sxs-lookup"><span data-stu-id="c4b81-105">Syntax</span></span>


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="c4b81-106">參數</span><span class="sxs-lookup"><span data-stu-id="c4b81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4b81-107">*pszPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4b81-107">*pszPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4b81-108">以 null 結束的字串指標，其中包含預設印表機名稱。</span><span class="sxs-lookup"><span data-stu-id="c4b81-108">A pointer to a null-terminated string containing the default printer name.</span></span> <span data-ttu-id="c4b81-109">若為遠端印表機連線，名稱格式為 [ **\\\\** _伺服器_ *_\\_* _printername_]。</span><span class="sxs-lookup"><span data-stu-id="c4b81-109">For a remote printer connection, the name format is **\\\\**_server_*_\\_*_printername_.</span></span> <span data-ttu-id="c4b81-110">若為本機印表機，名稱格式為 *printername*。</span><span class="sxs-lookup"><span data-stu-id="c4b81-110">For a local printer, the name format is *printername*.</span></span>

<span data-ttu-id="c4b81-111">如果此參數為 **Null** 或空字串，也就是 ""， **SetDefaultPrinter** 會從其中一個已安裝的印表機選取預設印表機。</span><span class="sxs-lookup"><span data-stu-id="c4b81-111">If this parameter is **NULL** or an empty string, that is, "", **SetDefaultPrinter** will select a default printer from one of the installed printers.</span></span> <span data-ttu-id="c4b81-112">如果預設印表機已經存在，在此參數中使用 **Null** 或空字串呼叫 **SetDefaultPrinter** ，可能會變更預設印表機。</span><span class="sxs-lookup"><span data-stu-id="c4b81-112">If a default printer already exists, calling **SetDefaultPrinter** with a **NULL** or an empty string in this parameter might change the default printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4b81-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4b81-113">Return value</span></span>

<span data-ttu-id="c4b81-114">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="c4b81-114">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c4b81-115">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="c4b81-115">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4b81-116">備註</span><span class="sxs-lookup"><span data-stu-id="c4b81-116">Remarks</span></span>

<span data-ttu-id="c4b81-117">使用這個方法時，您必須指定有效的印表機、驅動程式和埠。</span><span class="sxs-lookup"><span data-stu-id="c4b81-117">When using this method, you must specify a valid printer, driver, and port.</span></span> <span data-ttu-id="c4b81-118">如果無效，則 Api 不會失敗，但不會定義結果。</span><span class="sxs-lookup"><span data-stu-id="c4b81-118">If they are invalid, the APIs do not fail but the result is not defined.</span></span> <span data-ttu-id="c4b81-119">這可能會導致其他程式將印表機設定回先前的有效印表機。</span><span class="sxs-lookup"><span data-stu-id="c4b81-119">This could cause other programs to set the printer back to the previous valid printer.</span></span> <span data-ttu-id="c4b81-120">您可以使用 [**>enumprinters**](enumprinters.md) 來取得印表機名稱、驅動程式名稱，以及所有可用印表機的埠名稱。</span><span class="sxs-lookup"><span data-stu-id="c4b81-120">You can use [**EnumPrinters**](enumprinters.md) to retrieve the printer name, driver name, and port name of all available printers.</span></span>

> [!Note]  
> <span data-ttu-id="c4b81-121">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="c4b81-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c4b81-122">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="c4b81-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c4b81-123">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="c4b81-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c4b81-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4b81-124">Requirements</span></span>



| <span data-ttu-id="c4b81-125">需求</span><span class="sxs-lookup"><span data-stu-id="c4b81-125">Requirement</span></span> | <span data-ttu-id="c4b81-126">值</span><span class="sxs-lookup"><span data-stu-id="c4b81-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4b81-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4b81-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c4b81-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4b81-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c4b81-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4b81-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c4b81-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4b81-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c4b81-131">標頭</span><span class="sxs-lookup"><span data-stu-id="c4b81-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4b81-132"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c4b81-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c4b81-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="c4b81-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4b81-134"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4b81-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c4b81-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c4b81-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4b81-136"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="c4b81-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="c4b81-137">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="c4b81-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c4b81-138">**SetDefaultPrinterW** (Unicode) 和 **SetDefaultPrinterA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="c4b81-138">**SetDefaultPrinterW** (Unicode) and **SetDefaultPrinterA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="c4b81-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4b81-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4b81-140">列印</span><span class="sxs-lookup"><span data-stu-id="c4b81-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c4b81-141">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="c4b81-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c4b81-142">**>enumprinters**</span><span class="sxs-lookup"><span data-stu-id="c4b81-142">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="c4b81-143">**GetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="c4b81-143">**GetDefaultPrinter**</span></span>](getdefaultprinter.md)
</dt> </dl>

 

 




