---
description: EnumPrinterKey 函式會列舉指定印表機之指定機碼的子機碼。
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: 'EnumPrinterKey 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterKey
- EnumPrinterKeyA
- EnumPrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d9af6a9ef26612385cee68eba9733c148cd36b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319975"
---
# <a name="enumprinterkey-function"></a><span data-ttu-id="c848e-103">EnumPrinterKey 函式</span><span class="sxs-lookup"><span data-stu-id="c848e-103">EnumPrinterKey function</span></span>

<span data-ttu-id="c848e-104">**EnumPrinterKey** 函式會列舉指定印表機之指定機碼的子機碼。</span><span class="sxs-lookup"><span data-stu-id="c848e-104">The **EnumPrinterKey** function enumerates the subkeys of a specified key for a specified printer.</span></span>

<span data-ttu-id="c848e-105">印表機資料會儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="c848e-105">Printer data is stored in the registry.</span></span> <span data-ttu-id="c848e-106">列舉印表機資料時，請勿呼叫可能會變更資料的登錄功能。</span><span class="sxs-lookup"><span data-stu-id="c848e-106">While enumerating printer data, do not call registry functions that might change the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c848e-107">語法</span><span class="sxs-lookup"><span data-stu-id="c848e-107">Syntax</span></span>


```C++
DWORD EnumPrinterKey(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPTSTR  pSubkey,
  _In_  DWORD   cbSubkey,
  _Out_ LPDWORD pcbSubkey
);
```



## <a name="parameters"></a><span data-ttu-id="c848e-108">參數</span><span class="sxs-lookup"><span data-stu-id="c848e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c848e-109">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c848e-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c848e-110">此函式會列舉子機碼之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c848e-110">A handle to the printer for which the function enumerates subkeys.</span></span> <span data-ttu-id="c848e-111">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="c848e-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="c848e-112">*pKeyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c848e-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c848e-113">以 null 結束的字串指標，指定包含要列舉之子機碼的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c848e-113">A pointer to a null-terminated string that specifies the key containing the subkeys to enumerate.</span></span> <span data-ttu-id="c848e-114">使用反斜線 ' \\ ' 字元做為分隔符號，以指定包含一或多個子機碼的路徑。</span><span class="sxs-lookup"><span data-stu-id="c848e-114">Use the backslash '\\' character as a delimiter to specify a path with one or more subkeys.</span></span> <span data-ttu-id="c848e-115">**EnumPrinterKey** 會列舉機碼的所有子機碼，但不會列舉這些子機碼的子機碼。</span><span class="sxs-lookup"><span data-stu-id="c848e-115">**EnumPrinterKey** enumerates all subkeys of the key, but does not enumerate the subkeys of those subkeys.</span></span>

<span data-ttu-id="c848e-116">如果 *pKeyName* 是空字串 ( "" ) ，則 **EnumPrinterKey** 會列舉印表機的最上層索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c848e-116">If *pKeyName* is an empty string (""), **EnumPrinterKey** enumerates the top-level key for the printer.</span></span> <span data-ttu-id="c848e-117">如果 *pKeyName* 為 **Null**，則 **EnumPrinterKey** 會傳回錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="c848e-117">If *pKeyName* is **NULL**, **EnumPrinterKey** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="c848e-118">*pSubkey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c848e-118">*pSubkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c848e-119">接收以 null 終止之子機碼名稱陣列的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="c848e-119">A pointer to a buffer that receives an array of null-terminated subkey names.</span></span> <span data-ttu-id="c848e-120">陣列以兩個 null 字元結束。</span><span class="sxs-lookup"><span data-stu-id="c848e-120">The array is terminated by two null characters.</span></span>

</dd> <dt>

<span data-ttu-id="c848e-121">*cbSubkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c848e-121">*cbSubkey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c848e-122">*PSubkey* 所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c848e-122">The size, in bytes, of the buffer pointed to by *pSubkey*.</span></span> <span data-ttu-id="c848e-123">如果您將 *cbSubkey* 設定為零， *pcbSubkey* 參數會傳回所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="c848e-123">If you set *cbSubkey* to zero, the *pcbSubkey* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="c848e-124">*pcbSubkey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c848e-124">*pcbSubkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c848e-125">變數的指標，此變數會接收在 *pSubkey* 緩衝區中取出的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="c848e-125">A pointer to a variable that receives the number of bytes retrieved in the *pSubkey* buffer.</span></span> <span data-ttu-id="c848e-126">如果 *cbSubkey* 所指定的緩衝區大小太小，則函式會傳回 \_ 錯誤 \_ 的資料，而 *pcbSubkey* 則會指出所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="c848e-126">If the buffer size specified by *cbSubkey* is too small, the function returns ERROR\_MORE\_DATA and *pcbSubkey* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c848e-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="c848e-127">Return value</span></span>

<span data-ttu-id="c848e-128">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="c848e-128">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="c848e-129">如果函式失敗，則傳回值為系統錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c848e-129">If the function fails, the return value is a system error code.</span></span> <span data-ttu-id="c848e-130">如果 *pKeyName* 不存在，則傳回值為「找 \_ 不到錯誤檔案」 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="c848e-130">If *pKeyName* does not exist, the return value is ERROR\_FILE\_NOT\_FOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="c848e-131">備註</span><span class="sxs-lookup"><span data-stu-id="c848e-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c848e-132">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="c848e-132">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c848e-133">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="c848e-133">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c848e-134">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="c848e-134">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c848e-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="c848e-135">Requirements</span></span>



| <span data-ttu-id="c848e-136">需求</span><span class="sxs-lookup"><span data-stu-id="c848e-136">Requirement</span></span> | <span data-ttu-id="c848e-137">值</span><span class="sxs-lookup"><span data-stu-id="c848e-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c848e-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c848e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c848e-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c848e-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c848e-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c848e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c848e-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c848e-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c848e-142">標頭</span><span class="sxs-lookup"><span data-stu-id="c848e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="c848e-143"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c848e-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c848e-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="c848e-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="c848e-145"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c848e-145"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c848e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="c848e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c848e-147"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="c848e-147"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="c848e-148">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="c848e-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c848e-149">**EnumPrinterKeyW** (Unicode) 和 **EnumPrinterKeyA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="c848e-149">**EnumPrinterKeyW** (Unicode) and **EnumPrinterKeyA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="c848e-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c848e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c848e-151">列印</span><span class="sxs-lookup"><span data-stu-id="c848e-151">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c848e-152">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="c848e-152">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c848e-153">**DeletePrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="c848e-153">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="c848e-154">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="c848e-154">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="c848e-155">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="c848e-155">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="c848e-156">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="c848e-156">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




