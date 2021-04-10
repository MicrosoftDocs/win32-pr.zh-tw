---
description: DeleteForm 函數會從支援的表單清單中移除表單名稱。
ms.assetid: a2d0345f-2469-46ab-935f-777f2b33b621
title: 'DeleteForm 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteForm
- DeleteFormA
- DeleteFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 70ead5026c3b5cf21b28d230f79819bf71eeaf10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026736"
---
# <a name="deleteform-function"></a><span data-ttu-id="6bf9b-103">DeleteForm 函式</span><span class="sxs-lookup"><span data-stu-id="6bf9b-103">DeleteForm function</span></span>

<span data-ttu-id="6bf9b-104">**DeleteForm** 函數會從支援的表單清單中移除表單名稱。</span><span class="sxs-lookup"><span data-stu-id="6bf9b-104">The **DeleteForm** function removes a form name from the list of supported forms.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bf9b-105">語法</span><span class="sxs-lookup"><span data-stu-id="6bf9b-105">Syntax</span></span>


```C++
BOOL DeleteForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName
);
```



## <a name="parameters"></a><span data-ttu-id="6bf9b-106">參數</span><span class="sxs-lookup"><span data-stu-id="6bf9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bf9b-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6bf9b-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bf9b-108">指出此函式執行時所用的開啟印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="6bf9b-108">Indicates the open printer handle that this function is to be performed upon.</span></span> <span data-ttu-id="6bf9b-109">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="6bf9b-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="6bf9b-110">*pFormName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6bf9b-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bf9b-111">要移除之表單名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="6bf9b-111">Pointer to the form name to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bf9b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6bf9b-112">Return value</span></span>

<span data-ttu-id="6bf9b-113">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="6bf9b-113">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6bf9b-114">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="6bf9b-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bf9b-115">備註</span><span class="sxs-lookup"><span data-stu-id="6bf9b-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6bf9b-116">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="6bf9b-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6bf9b-117">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="6bf9b-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6bf9b-118">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="6bf9b-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6bf9b-119">**DeleteForm** 只能刪除使用 [**AddForm**](addform.md) 函數加入的表單名稱。</span><span class="sxs-lookup"><span data-stu-id="6bf9b-119">**DeleteForm** can only delete form names that were added by using the [**AddForm**](addform.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bf9b-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bf9b-120">Requirements</span></span>



| <span data-ttu-id="6bf9b-121">需求</span><span class="sxs-lookup"><span data-stu-id="6bf9b-121">Requirement</span></span> | <span data-ttu-id="6bf9b-122">值</span><span class="sxs-lookup"><span data-stu-id="6bf9b-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf9b-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bf9b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6bf9b-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bf9b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6bf9b-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bf9b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6bf9b-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bf9b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6bf9b-127">標頭</span><span class="sxs-lookup"><span data-stu-id="6bf9b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bf9b-128"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6bf9b-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6bf9b-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="6bf9b-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="6bf9b-130"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bf9b-130"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6bf9b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6bf9b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bf9b-132"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="6bf9b-132"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="6bf9b-133">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="6bf9b-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6bf9b-134">**DeleteFormW** (Unicode) 和 **DeleteFormA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="6bf9b-134">**DeleteFormW** (Unicode) and **DeleteFormA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="6bf9b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bf9b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bf9b-136">列印</span><span class="sxs-lookup"><span data-stu-id="6bf9b-136">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6bf9b-137">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="6bf9b-137">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6bf9b-138">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="6bf9b-138">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="6bf9b-139">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="6bf9b-139">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




