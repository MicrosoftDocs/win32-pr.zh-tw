---
description: DeletePrinterKey 函式會刪除指定之印表機的指定機碼及其所有子機碼。
ms.assetid: 0bd81b43-5c1e-4989-8350-2ec0dc215f28
title: 'DeletePrinterKey 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterKey
- DeletePrinterKeyA
- DeletePrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 4be073f7832f647e156dbd3b5e12d23ffe6acc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693807"
---
# <a name="deleteprinterkey-function"></a><span data-ttu-id="dbf44-103">DeletePrinterKey 函式</span><span class="sxs-lookup"><span data-stu-id="dbf44-103">DeletePrinterKey function</span></span>

<span data-ttu-id="dbf44-104">**DeletePrinterKey** 函式會刪除指定之印表機的指定機碼及其所有子機碼。</span><span class="sxs-lookup"><span data-stu-id="dbf44-104">The **DeletePrinterKey** function deletes a specified key and all its subkeys for a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf44-105">語法</span><span class="sxs-lookup"><span data-stu-id="dbf44-105">Syntax</span></span>


```C++
DWORD DeletePrinterKey(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName
);
```



## <a name="parameters"></a><span data-ttu-id="dbf44-106">參數</span><span class="sxs-lookup"><span data-stu-id="dbf44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbf44-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dbf44-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf44-108">此函式會刪除索引鍵之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="dbf44-108">A handle to the printer for which the function deletes a key.</span></span> <span data-ttu-id="dbf44-109">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="dbf44-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="dbf44-110">*pKeyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dbf44-110">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf44-111">以 null 結束的字串指標，指定要刪除的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="dbf44-111">A pointer to a null-terminated string that specifies the key to delete.</span></span> <span data-ttu-id="dbf44-112">使用反斜線 ( \\ ) 字元作為分隔符號，以指定包含一或多個子機碼的路徑。</span><span class="sxs-lookup"><span data-stu-id="dbf44-112">Use the backslash ( \\ ) character as a delimiter to specify a path with one or more subkeys.</span></span>

<span data-ttu-id="dbf44-113">如果 *pKeyName* 是空字串 ( "" ) ， **DeletePrinterKey** 會刪除印表機最上層索引鍵下方的所有索引鍵。</span><span class="sxs-lookup"><span data-stu-id="dbf44-113">If *pKeyName* is an empty string (""), **DeletePrinterKey** deletes all keys below the top-level key for the printer.</span></span> <span data-ttu-id="dbf44-114">如果 *pKeyName* 為 **Null**，則 **DeletePrinterKey** 會傳回錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="dbf44-114">If *pKeyName* is **NULL**, **DeletePrinterKey** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbf44-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="dbf44-115">Return value</span></span>

<span data-ttu-id="dbf44-116">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="dbf44-116">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="dbf44-117">如果函式失敗，則傳回值為系統錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dbf44-117">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbf44-118">備註</span><span class="sxs-lookup"><span data-stu-id="dbf44-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dbf44-119">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="dbf44-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="dbf44-120">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="dbf44-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="dbf44-121">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="dbf44-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dbf44-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbf44-122">Requirements</span></span>



| <span data-ttu-id="dbf44-123">需求</span><span class="sxs-lookup"><span data-stu-id="dbf44-123">Requirement</span></span> | <span data-ttu-id="dbf44-124">值</span><span class="sxs-lookup"><span data-stu-id="dbf44-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf44-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dbf44-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dbf44-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbf44-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dbf44-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dbf44-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dbf44-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbf44-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dbf44-129">標頭</span><span class="sxs-lookup"><span data-stu-id="dbf44-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbf44-130"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="dbf44-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="dbf44-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="dbf44-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="dbf44-132"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbf44-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="dbf44-133">DLL</span><span class="sxs-lookup"><span data-stu-id="dbf44-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbf44-134"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="dbf44-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="dbf44-135">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="dbf44-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="dbf44-136">**DeletePrinterKeyW** (Unicode) 和 **DeletePrinterKeyA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="dbf44-136">**DeletePrinterKeyW** (Unicode) and **DeletePrinterKeyA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="dbf44-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbf44-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf44-138">列印</span><span class="sxs-lookup"><span data-stu-id="dbf44-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="dbf44-139">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="dbf44-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="dbf44-140">**DeletePrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="dbf44-140">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="dbf44-141">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="dbf44-141">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="dbf44-142">**EnumPrinterKey**</span><span class="sxs-lookup"><span data-stu-id="dbf44-142">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="dbf44-143">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="dbf44-143">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="dbf44-144">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="dbf44-144">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="dbf44-145">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="dbf44-145">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




