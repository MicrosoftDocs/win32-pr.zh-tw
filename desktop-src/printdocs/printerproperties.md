---
description: PrinterProperties 函式會顯示指定印表機的印表機屬性屬性工作表。
ms.assetid: 1d4c961b-178b-47af-b983-5b7327919f93
title: 'PrinterProperties 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrinterProperties
api_type:
- DllExport
api_location:
- plotui.dll
- winspool.drv
ms.openlocfilehash: e7e2c8586c06b2cb64a0e499bd05a6b6016de0a6
ms.sourcegitcommit: c77ed4d933c9f30af0ca0e095a75ad2bdd4d8bf8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/31/2021
ms.locfileid: "106976305"
---
# <a name="printerproperties-function"></a><span data-ttu-id="e257c-103">PrinterProperties 函式</span><span class="sxs-lookup"><span data-stu-id="e257c-103">PrinterProperties function</span></span>

<span data-ttu-id="e257c-104">**PrinterProperties** 函式會顯示指定印表機的印表機屬性屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="e257c-104">The **PrinterProperties** function displays a printer-properties property sheet for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e257c-105">語法</span><span class="sxs-lookup"><span data-stu-id="e257c-105">Syntax</span></span>


```C++
BOOL PrinterProperties(
  _In_ HWND   hWnd,
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="e257c-106">參數</span><span class="sxs-lookup"><span data-stu-id="e257c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e257c-107">*hWnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e257c-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e257c-108">屬性工作表父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e257c-108">A handle to the parent window of the property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="e257c-109">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e257c-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e257c-110">印表機物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e257c-110">A handle to a printer object.</span></span> <span data-ttu-id="e257c-111">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="e257c-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e257c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e257c-112">Return value</span></span>

<span data-ttu-id="e257c-113">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="e257c-113">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e257c-114">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="e257c-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e257c-115">備註</span><span class="sxs-lookup"><span data-stu-id="e257c-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e257c-116">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="e257c-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e257c-117">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="e257c-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e257c-118">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="e257c-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e257c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e257c-119">Requirements</span></span>



| <span data-ttu-id="e257c-120">需求</span><span class="sxs-lookup"><span data-stu-id="e257c-120">Requirement</span></span> | <span data-ttu-id="e257c-121">值</span><span class="sxs-lookup"><span data-stu-id="e257c-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e257c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e257c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e257c-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e257c-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e257c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e257c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e257c-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e257c-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e257c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e257c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e257c-127"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e257c-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e257c-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="e257c-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="e257c-129"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e257c-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e257c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e257c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e257c-131"><dt>winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="e257c-131"><dt>winspool.drv</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e257c-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e257c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e257c-133">列印</span><span class="sxs-lookup"><span data-stu-id="e257c-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e257c-134">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="e257c-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e257c-135">**DocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="e257c-135">**DocumentProperties**</span></span>](documentproperties.md)
</dt> <dt>

[<span data-ttu-id="e257c-136">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="e257c-136">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




