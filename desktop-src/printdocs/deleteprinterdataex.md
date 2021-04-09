---
description: DeletePrinterDataEx 函式會從印表機的設定資料中刪除指定的值。
ms.assetid: bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55
title: 'DeletePrinterDataEx 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDataEx
- DeletePrinterDataExA
- DeletePrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 07cf6262db0a1e3a3c4c098ee26e03b3fdad4002
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693567"
---
# <a name="deleteprinterdataex-function"></a><span data-ttu-id="3a03d-103">DeletePrinterDataEx 函式</span><span class="sxs-lookup"><span data-stu-id="3a03d-103">DeletePrinterDataEx function</span></span>

<span data-ttu-id="3a03d-104">**DeletePrinterDataEx** 函式會從印表機的設定資料中刪除指定的值。</span><span class="sxs-lookup"><span data-stu-id="3a03d-104">The **DeletePrinterDataEx** function deletes a specified value from the configuration data for a printer.</span></span> <span data-ttu-id="3a03d-105">印表機的設定資料是由一組儲存在登錄機碼階層中的命名和類型值所組成。</span><span class="sxs-lookup"><span data-stu-id="3a03d-105">A printer's configuration data consists of a set of named and typed values stored in a hierarchy of registry keys.</span></span> <span data-ttu-id="3a03d-106">函數會刪除指定之索引鍵下的指定值。</span><span class="sxs-lookup"><span data-stu-id="3a03d-106">The function deletes a specified value under a specified key.</span></span>

<span data-ttu-id="3a03d-107">如同 [**DeletePrinterData**](deleteprinterdata.md) 函數， **DeletePrinterDataEx** 可以刪除 [**SetPrinterData**](setprinterdata.md) 函數所儲存的值。</span><span class="sxs-lookup"><span data-stu-id="3a03d-107">Like the [**DeletePrinterData**](deleteprinterdata.md) function, **DeletePrinterDataEx** can delete values stored by the [**SetPrinterData**](setprinterdata.md) function.</span></span> <span data-ttu-id="3a03d-108">此外， **DeletePrinterDataEx** 也可以刪除 [**SetPrinterDataEx**](setprinterdataex.md) 函數在指定索引鍵下儲存的值。</span><span class="sxs-lookup"><span data-stu-id="3a03d-108">In addition, **DeletePrinterDataEx** can delete values stored under a specified key by the [**SetPrinterDataEx**](setprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a03d-109">語法</span><span class="sxs-lookup"><span data-stu-id="3a03d-109">Syntax</span></span>


```C++
DWORD DeletePrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName
);
```



## <a name="parameters"></a><span data-ttu-id="3a03d-110">參數</span><span class="sxs-lookup"><span data-stu-id="3a03d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a03d-111">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3a03d-111">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a03d-112">此函式會刪除其值之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3a03d-112">A handle to the printer for which the function deletes a value.</span></span> <span data-ttu-id="3a03d-113">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="3a03d-113">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="3a03d-114">*pKeyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3a03d-114">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a03d-115">以 null 結束的字串指標，指定包含要刪除之值的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="3a03d-115">A pointer to a null-terminated string that specifies the key containing the value to delete.</span></span> <span data-ttu-id="3a03d-116">使用反斜線 ( \\ ) 字元作為分隔符號，以指定包含一或多個子機碼的路徑。</span><span class="sxs-lookup"><span data-stu-id="3a03d-116">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="3a03d-117">如果 *pKeyName* 為 **Null** 或空字串，則 **DeletePrinterDataEx** 會傳回錯誤 \_ 不正確 \_ 參數。</span><span class="sxs-lookup"><span data-stu-id="3a03d-117">If *pKeyName* is **NULL** or an empty string, **DeletePrinterDataEx** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="3a03d-118">*pValueName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3a03d-118">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a03d-119">以 null 結束的字串指標，指定要刪除之值的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a03d-119">A pointer to a null-terminated string that specifies the name of the value to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a03d-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a03d-120">Return value</span></span>

<span data-ttu-id="3a03d-121">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="3a03d-121">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="3a03d-122">如果函式失敗，則傳回值為系統錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3a03d-122">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a03d-123">備註</span><span class="sxs-lookup"><span data-stu-id="3a03d-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3a03d-124">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="3a03d-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="3a03d-125">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="3a03d-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3a03d-126">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="3a03d-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3a03d-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a03d-127">Requirements</span></span>



| <span data-ttu-id="3a03d-128">需求</span><span class="sxs-lookup"><span data-stu-id="3a03d-128">Requirement</span></span> | <span data-ttu-id="3a03d-129">值</span><span class="sxs-lookup"><span data-stu-id="3a03d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a03d-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a03d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3a03d-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a03d-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3a03d-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a03d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3a03d-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a03d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3a03d-134">標頭</span><span class="sxs-lookup"><span data-stu-id="3a03d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a03d-135"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3a03d-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3a03d-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="3a03d-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="3a03d-137"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a03d-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3a03d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3a03d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a03d-139"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="3a03d-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="3a03d-140">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="3a03d-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3a03d-141">**DeletePrinterDataExW** (Unicode) 和 **DeletePrinterDataExA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="3a03d-141">**DeletePrinterDataExW** (Unicode) and **DeletePrinterDataExA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="3a03d-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a03d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a03d-143">列印</span><span class="sxs-lookup"><span data-stu-id="3a03d-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3a03d-144">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="3a03d-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3a03d-145">**DeletePrinterKey**</span><span class="sxs-lookup"><span data-stu-id="3a03d-145">**DeletePrinterKey**</span></span>](deleteprinterkey.md)
</dt> <dt>

[<span data-ttu-id="3a03d-146">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="3a03d-146">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="3a03d-147">**EnumPrinterKey**</span><span class="sxs-lookup"><span data-stu-id="3a03d-147">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="3a03d-148">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="3a03d-148">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="3a03d-149">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="3a03d-149">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="3a03d-150">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="3a03d-150">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




