---
description: EnumPrinterDataEx 函式會列舉指定之印表機和索引鍵的所有值名稱和資料。
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: 'EnumPrinterDataEx 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDataEx
- EnumPrinterDataExA
- EnumPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 517d480d1c831627cadb289c41f99d24b1025ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693876"
---
# <a name="enumprinterdataex-function"></a><span data-ttu-id="394fb-103">EnumPrinterDataEx 函式</span><span class="sxs-lookup"><span data-stu-id="394fb-103">EnumPrinterDataEx function</span></span>

<span data-ttu-id="394fb-104">**EnumPrinterDataEx** 函式會列舉指定之印表機和索引鍵的所有值名稱和資料。</span><span class="sxs-lookup"><span data-stu-id="394fb-104">The **EnumPrinterDataEx** function enumerates all value names and data for a specified printer and key.</span></span>

<span data-ttu-id="394fb-105">印表機資料會儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="394fb-105">Printer data is stored in the registry.</span></span> <span data-ttu-id="394fb-106">列舉印表機資料時，請勿呼叫可能會變更資料的登錄功能。</span><span class="sxs-lookup"><span data-stu-id="394fb-106">While enumerating printer data, do not call registry functions that might change the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="394fb-107">語法</span><span class="sxs-lookup"><span data-stu-id="394fb-107">Syntax</span></span>


```C++
DWORD EnumPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPBYTE  pEnumValues,
  _In_  DWORD   cbEnumValues,
  _Out_ LPDWORD pcbEnumValues,
  _Out_ LPDWORD pnEnumValues
);
```



## <a name="parameters"></a><span data-ttu-id="394fb-108">參數</span><span class="sxs-lookup"><span data-stu-id="394fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="394fb-109">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="394fb-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="394fb-110">由函式抓取設定資料的印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="394fb-110">A handle to the printer for which the function retrieves configuration data.</span></span> <span data-ttu-id="394fb-111">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="394fb-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="394fb-112">*pKeyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="394fb-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="394fb-113">以 null 結束的字串指標，指定包含要列舉之值的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="394fb-113">A pointer to a null-terminated string that specifies the key containing the values to enumerate.</span></span> <span data-ttu-id="394fb-114">使用反斜線 ( \\ ) 字元作為分隔符號，以指定包含一或多個子機碼的路徑。</span><span class="sxs-lookup"><span data-stu-id="394fb-114">Use the backslash ( \\ ) character as a delimiter to specify a path with one or more subkeys.</span></span> <span data-ttu-id="394fb-115">**EnumPrinterDataEx** 會列舉索引鍵的所有值，但不會列舉指定之索引鍵的子機碼值。</span><span class="sxs-lookup"><span data-stu-id="394fb-115">**EnumPrinterDataEx** enumerates all values of the key, but does not enumerate values of subkeys of the specified key.</span></span> <span data-ttu-id="394fb-116">使用 [**EnumPrinterKey**](enumprinterkey.md) 函式來列舉子機碼。</span><span class="sxs-lookup"><span data-stu-id="394fb-116">Use the [**EnumPrinterKey**](enumprinterkey.md) function to enumerate subkeys.</span></span>

<span data-ttu-id="394fb-117">如果 *pKeyName* 為 **Null** 或空字串，則 **EnumPrinterDataEx** 會傳回錯誤 \_ 不正確 \_ 參數。</span><span class="sxs-lookup"><span data-stu-id="394fb-117">If *pKeyName* is **NULL** or an empty string, **EnumPrinterDataEx** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="394fb-118">*pEnumValues* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="394fb-118">*pEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="394fb-119">緩衝區的指標，此緩衝區會接收 [**印表機 \_ 列舉 \_ 值**](printer-enum-values.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="394fb-119">A pointer to a buffer that receives an array of [**PRINTER\_ENUM\_VALUES**](printer-enum-values.md) structures.</span></span> <span data-ttu-id="394fb-120">每個結構都包含值的名稱、類型、資料和值在索引鍵下的大小。</span><span class="sxs-lookup"><span data-stu-id="394fb-120">Each structure contains the value name, type, data, and sizes of a value under the key.</span></span>

</dd> <dt>

<span data-ttu-id="394fb-121">*cbEnumValues* \[在\]</span><span class="sxs-lookup"><span data-stu-id="394fb-121">*cbEnumValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="394fb-122">*PcbEnumValues* 所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="394fb-122">The size, in bytes, of the buffer pointed to by *pcbEnumValues*.</span></span> <span data-ttu-id="394fb-123">如果您將 *cbEnumValues* 設定為零， *pcbEnumValues* 參數會傳回所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="394fb-123">If you set *cbEnumValues* to zero, the *pcbEnumValues* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="394fb-124">*pcbEnumValues* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="394fb-124">*pcbEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="394fb-125">變數的指標，此變數會接收所抓取設定資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="394fb-125">A pointer to a variable that receives the size, in bytes, of the retrieved configuration data.</span></span> <span data-ttu-id="394fb-126">如果 *cbEnumValues* 所指定的緩衝區大小太小，則函式會傳回 \_ 錯誤 \_ 的資料，而 *pcbEnumValues* 則會指出所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="394fb-126">If the buffer size specified by *cbEnumValues* is too small, the function returns ERROR\_MORE\_DATA and *pcbEnumValues* indicates the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="394fb-127">*pnEnumValues* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="394fb-127">*pnEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="394fb-128">變數的指標，此變數會接收 *pEnumValues* 中傳回之 [**印表機 \_ 列舉 \_ 值**](printer-enum-values.md)結構的數目。</span><span class="sxs-lookup"><span data-stu-id="394fb-128">A pointer to a variable that receives the number of [**PRINTER\_ENUM\_VALUES**](printer-enum-values.md) structures returned in *pEnumValues*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="394fb-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="394fb-129">Return value</span></span>

<span data-ttu-id="394fb-130">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="394fb-130">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="394fb-131">如果函式失敗，則傳回值為系統錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="394fb-131">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="394fb-132">備註</span><span class="sxs-lookup"><span data-stu-id="394fb-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="394fb-133">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="394fb-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="394fb-134">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="394fb-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="394fb-135">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="394fb-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="394fb-136">**EnumPrinterDataEx** 會透過 [**SetPrinterDataEx**](setprinterdataex.md) 和 [**SetPrinterData**](setprinterdata.md) 函式來抓取印表機設定資料集。</span><span class="sxs-lookup"><span data-stu-id="394fb-136">**EnumPrinterDataEx** retrieves printer configuration data set by the [**SetPrinterDataEx**](setprinterdataex.md) and [**SetPrinterData**](setprinterdata.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="394fb-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="394fb-137">Requirements</span></span>



| <span data-ttu-id="394fb-138">需求</span><span class="sxs-lookup"><span data-stu-id="394fb-138">Requirement</span></span> | <span data-ttu-id="394fb-139">值</span><span class="sxs-lookup"><span data-stu-id="394fb-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="394fb-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="394fb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="394fb-141">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="394fb-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="394fb-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="394fb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="394fb-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="394fb-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="394fb-144">標頭</span><span class="sxs-lookup"><span data-stu-id="394fb-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="394fb-145"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="394fb-145"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="394fb-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="394fb-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="394fb-147"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="394fb-147"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="394fb-148">DLL</span><span class="sxs-lookup"><span data-stu-id="394fb-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="394fb-149"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="394fb-149"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="394fb-150">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="394fb-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="394fb-151">**EnumPrinterDataExW** (Unicode) 和 **EnumPrinterDataExA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="394fb-151">**EnumPrinterDataExW** (Unicode) and **EnumPrinterDataExA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="394fb-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="394fb-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="394fb-153">列印</span><span class="sxs-lookup"><span data-stu-id="394fb-153">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="394fb-154">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="394fb-154">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="394fb-155">**DeletePrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="394fb-155">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="394fb-156">**EnumPrinterKey**</span><span class="sxs-lookup"><span data-stu-id="394fb-156">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="394fb-157">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="394fb-157">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="394fb-158">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="394fb-158">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="394fb-159">**印表機 \_ 列舉 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="394fb-159">**PRINTER\_ENUM\_VALUES**</span></span>](printer-enum-values.md)
</dt> <dt>

[<span data-ttu-id="394fb-160">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="394fb-160">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> <dt>

[<span data-ttu-id="394fb-161">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="394fb-161">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




