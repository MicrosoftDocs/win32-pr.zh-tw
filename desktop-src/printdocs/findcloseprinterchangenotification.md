---
description: FindClosePrinterChangeNotification 函式會關閉藉由呼叫 FindFirstPrinterChangeNotification 函數所建立的變更通知物件。
ms.assetid: 2b4758f8-af0a-494b-8f1b-8ea6ee73c79b
title: 'FindClosePrinterChangeNotification 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindClosePrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8040944d5890aa521681827bef786201a35da039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026702"
---
# <a name="findcloseprinterchangenotification-function"></a><span data-ttu-id="13b87-103">FindClosePrinterChangeNotification 函式</span><span class="sxs-lookup"><span data-stu-id="13b87-103">FindClosePrinterChangeNotification function</span></span>

<span data-ttu-id="13b87-104">**FindClosePrinterChangeNotification** 函式會關閉藉由呼叫 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)函數所建立的變更通知物件。</span><span class="sxs-lookup"><span data-stu-id="13b87-104">The **FindClosePrinterChangeNotification** function closes a change notification object created by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span> <span data-ttu-id="13b87-105">與變更通知物件相關聯的印表機或列印伺服器，將不會再由該物件監視。</span><span class="sxs-lookup"><span data-stu-id="13b87-105">The printer or print server associated with the change notification object will no longer be monitored by that object.</span></span>

## <a name="syntax"></a><span data-ttu-id="13b87-106">語法</span><span class="sxs-lookup"><span data-stu-id="13b87-106">Syntax</span></span>


```C++
BOOL FindClosePrinterChangeNotification(
  _In_ HANDLE hChange
);
```



## <a name="parameters"></a><span data-ttu-id="13b87-107">參數</span><span class="sxs-lookup"><span data-stu-id="13b87-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13b87-108">*hChange* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13b87-108">*hChange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13b87-109">要關閉之變更通知物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="13b87-109">A handle to the change notification object to be closed.</span></span> <span data-ttu-id="13b87-110">這是藉由呼叫 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) 函式所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="13b87-110">This is a handle created by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13b87-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="13b87-111">Return value</span></span>

<span data-ttu-id="13b87-112">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="13b87-112">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="13b87-113">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="13b87-113">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="13b87-114">備註</span><span class="sxs-lookup"><span data-stu-id="13b87-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="13b87-115">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="13b87-115">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="13b87-116">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="13b87-116">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="13b87-117">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="13b87-117">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="13b87-118">在呼叫 **FindClosePrinterChangeNotification** 函式之後，您無法在後續的 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)或 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)呼叫中使用 *hChange* 控制碼。</span><span class="sxs-lookup"><span data-stu-id="13b87-118">After calling the **FindClosePrinterChangeNotification** function, you cannot use the *hChange* handle in subsequent calls to either [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) or [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13b87-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="13b87-119">Requirements</span></span>



| <span data-ttu-id="13b87-120">需求</span><span class="sxs-lookup"><span data-stu-id="13b87-120">Requirement</span></span> | <span data-ttu-id="13b87-121">值</span><span class="sxs-lookup"><span data-stu-id="13b87-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13b87-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13b87-122">Minimum supported client</span></span><br/> | <span data-ttu-id="13b87-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13b87-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="13b87-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13b87-124">Minimum supported server</span></span><br/> | <span data-ttu-id="13b87-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13b87-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="13b87-126">標頭</span><span class="sxs-lookup"><span data-stu-id="13b87-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="13b87-127"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="13b87-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="13b87-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="13b87-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="13b87-129"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="13b87-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="13b87-130">DLL</span><span class="sxs-lookup"><span data-stu-id="13b87-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13b87-131"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13b87-131"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="13b87-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13b87-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13b87-133">列印</span><span class="sxs-lookup"><span data-stu-id="13b87-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="13b87-134">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="13b87-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="13b87-135">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="13b87-135">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="13b87-136">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="13b87-136">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> </dl>

 

 




