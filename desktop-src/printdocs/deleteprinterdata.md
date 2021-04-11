---
description: DeletePrinterData 函式會刪除印表機的指定設定資料。 印表機設定資料包含一組命名的和具類型的值。 DeletePrinterData 函式會刪除其中一個值，並以其值名稱來指定。
ms.assetid: 03c0bd75-d6de-46e3-b8e9-5a55df5135ea
title: 'DeletePrinterData 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterData
- DeletePrinterDataA
- DeletePrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a88df8484d367ae2cc50f4a465b5db1dcd53c355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319100"
---
# <a name="deleteprinterdata-function"></a><span data-ttu-id="9d8d8-105">DeletePrinterData 函式</span><span class="sxs-lookup"><span data-stu-id="9d8d8-105">DeletePrinterData function</span></span>

<span data-ttu-id="9d8d8-106">**DeletePrinterData** 函式會刪除印表機的指定設定資料。</span><span class="sxs-lookup"><span data-stu-id="9d8d8-106">The **DeletePrinterData** function deletes specified configuration data for a printer.</span></span> <span data-ttu-id="9d8d8-107">印表機的設定資料是由一組命名的和具類型的值所組成。</span><span class="sxs-lookup"><span data-stu-id="9d8d8-107">A printer's configuration data consists of a set of named and typed values.</span></span> <span data-ttu-id="9d8d8-108">**DeletePrinterData** 函式會刪除其中一個值，並以其值名稱來指定。</span><span class="sxs-lookup"><span data-stu-id="9d8d8-108">The **DeletePrinterData** function deletes one of these values, specified by its value name.</span></span>

<span data-ttu-id="9d8d8-109">呼叫 **DeletePrinterData** 相當於呼叫 [**DeletePrinterDataEx**](deleteprinterdataex.md) 函數，並將 *PKeyName* 參數設定為 "PrinterDriverData"。</span><span class="sxs-lookup"><span data-stu-id="9d8d8-109">Calling **DeletePrinterData** is equivalent to calling the [**DeletePrinterDataEx**](deleteprinterdataex.md) function with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="9d8d8-110">語法</span><span class="sxs-lookup"><span data-stu-id="9d8d8-110">Syntax</span></span>


```C++
DWORD DeletePrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName
);
```



## <a name="parameters"></a><span data-ttu-id="9d8d8-111">參數</span><span class="sxs-lookup"><span data-stu-id="9d8d8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d8d8-112">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d8d8-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d8d8-113">要刪除其設定資料之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9d8d8-113">A handle to the printer whose configuration data is to be deleted.</span></span> <span data-ttu-id="9d8d8-114">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="9d8d8-114">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="9d8d8-115">*pValueName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d8d8-115">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d8d8-116">要刪除的設定資料值之以 null 結束之名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="9d8d8-116">A pointer to the null-terminated name of the configuration data value to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d8d8-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d8d8-117">Return value</span></span>

<span data-ttu-id="9d8d8-118">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="9d8d8-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="9d8d8-119">如果函式失敗，則傳回值為系統錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9d8d8-119">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d8d8-120">備註</span><span class="sxs-lookup"><span data-stu-id="9d8d8-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9d8d8-121">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="9d8d8-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9d8d8-122">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="9d8d8-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9d8d8-123">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="9d8d8-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9d8d8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d8d8-124">Requirements</span></span>



| <span data-ttu-id="9d8d8-125">需求</span><span class="sxs-lookup"><span data-stu-id="9d8d8-125">Requirement</span></span> | <span data-ttu-id="9d8d8-126">值</span><span class="sxs-lookup"><span data-stu-id="9d8d8-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d8d8-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d8d8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9d8d8-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d8d8-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9d8d8-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d8d8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9d8d8-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d8d8-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9d8d8-131">標頭</span><span class="sxs-lookup"><span data-stu-id="9d8d8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d8d8-132"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="9d8d8-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9d8d8-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="9d8d8-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d8d8-134"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d8d8-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9d8d8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9d8d8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d8d8-136"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="9d8d8-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="9d8d8-137">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="9d8d8-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9d8d8-138">**DeletePrinterDataW** (Unicode) 和 **DeletePrinterDataA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="9d8d8-138">**DeletePrinterDataW** (Unicode) and **DeletePrinterDataA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="9d8d8-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d8d8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d8d8-140">列印</span><span class="sxs-lookup"><span data-stu-id="9d8d8-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9d8d8-141">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="9d8d8-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9d8d8-142">**EnumPrinterData**</span><span class="sxs-lookup"><span data-stu-id="9d8d8-142">**EnumPrinterData**</span></span>](enumprinterdata.md)
</dt> <dt>

[<span data-ttu-id="9d8d8-143">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="9d8d8-143">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="9d8d8-144">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="9d8d8-144">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="9d8d8-145">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="9d8d8-145">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="9d8d8-146">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="9d8d8-146">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> </dl>

 

 




