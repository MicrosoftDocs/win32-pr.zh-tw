---
description: FreePrinterNotifyInfo 函式會釋放由 FindNextPrinterChangeNotification 函數所建立的系統組態緩衝區。
ms.assetid: e50d4718-3682-486b-9d07-ddddd0b284dc
title: 'FreePrinterNotifyInfo 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePrinterNotifyInfo
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8d2cc22971c2645af250a9e92872b89959387163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979138"
---
# <a name="freeprinternotifyinfo-function"></a><span data-ttu-id="e539b-103">FreePrinterNotifyInfo 函式</span><span class="sxs-lookup"><span data-stu-id="e539b-103">FreePrinterNotifyInfo function</span></span>

<span data-ttu-id="e539b-104">**FreePrinterNotifyInfo** 函式會釋放由 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)函數所建立的系統組態緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e539b-104">The **FreePrinterNotifyInfo** function frees a system-allocated buffer created by the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e539b-105">語法</span><span class="sxs-lookup"><span data-stu-id="e539b-105">Syntax</span></span>


```C++
BOOL FreePrinterNotifyInfo(
  _In_ PPRINTER_NOTIFY_INFO pPrinterNotifyInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e539b-106">參數</span><span class="sxs-lookup"><span data-stu-id="e539b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e539b-107">*pPrinterNotifyInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e539b-107">*pPrinterNotifyInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e539b-108">從 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)函式的呼叫傳回的 [**印表機 \_ 通知 \_ 資訊**](printer-notify-info.md)緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="e539b-108">Pointer to a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) buffer returned from a call to the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span> <span data-ttu-id="e539b-109">**FreePrinterNotifyInfo** 會將這個緩衝區解除配置。</span><span class="sxs-lookup"><span data-stu-id="e539b-109">**FreePrinterNotifyInfo** deallocates this buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e539b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e539b-110">Return value</span></span>

<span data-ttu-id="e539b-111">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="e539b-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e539b-112">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="e539b-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e539b-113">備註</span><span class="sxs-lookup"><span data-stu-id="e539b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e539b-114">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="e539b-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e539b-115">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="e539b-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e539b-116">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="e539b-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e539b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e539b-117">Requirements</span></span>



| <span data-ttu-id="e539b-118">需求</span><span class="sxs-lookup"><span data-stu-id="e539b-118">Requirement</span></span> | <span data-ttu-id="e539b-119">值</span><span class="sxs-lookup"><span data-stu-id="e539b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e539b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e539b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e539b-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e539b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e539b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e539b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e539b-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e539b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e539b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e539b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e539b-125"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e539b-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e539b-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="e539b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="e539b-127"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e539b-127"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e539b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e539b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e539b-129"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e539b-129"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="e539b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e539b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e539b-131">列印</span><span class="sxs-lookup"><span data-stu-id="e539b-131">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e539b-132">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="e539b-132">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e539b-133">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="e539b-133">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="e539b-134">**印表機 \_ 通知 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="e539b-134">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> </dl>

 

 




