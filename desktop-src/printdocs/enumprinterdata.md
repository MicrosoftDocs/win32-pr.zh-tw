---
description: EnumPrinterData 函式會列舉指定印表機的設定資料。
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: 'EnumPrinterData 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterData
- EnumPrinterDataA
- EnumPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d7c175b0c90853a592e0ff979095d41432c16b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192599"
---
# <a name="enumprinterdata-function"></a><span data-ttu-id="ce5f5-103">EnumPrinterData 函式</span><span class="sxs-lookup"><span data-stu-id="ce5f5-103">EnumPrinterData function</span></span>

<span data-ttu-id="ce5f5-104">**EnumPrinterData** 函式會列舉指定印表機的設定資料。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-104">The **EnumPrinterData** function enumerates configuration data for a specified printer.</span></span>

<span data-ttu-id="ce5f5-105">若要在單一呼叫中取出設定資料，請使用 [**EnumPrinterDataEx**](enumprinterdataex.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-105">To retrieve the configuration data in a single call, use the [**EnumPrinterDataEx**](enumprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce5f5-106">語法</span><span class="sxs-lookup"><span data-stu-id="ce5f5-106">Syntax</span></span>


```C++
DWORD EnumPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   dwIndex,
  _Out_ LPTSTR  pValueName,
  _In_  DWORD   cbValueName,
  _Out_ LPDWORD pcbValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbData,
  _Out_ LPDWORD pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="ce5f5-107">參數</span><span class="sxs-lookup"><span data-stu-id="ce5f5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce5f5-108">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ce5f5-108">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5f5-109">要取得其設定資料之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-109">A handle to the printer whose configuration data is to be obtained.</span></span> <span data-ttu-id="ce5f5-110">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-110">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="ce5f5-111">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ce5f5-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5f5-112">索引值，指定要取出的設定資料值。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-112">An index value that specifies the configuration data value to retrieve.</span></span>

<span data-ttu-id="ce5f5-113">針對指定的印表機控制碼，將此參數設定為零，以進行第一次的 **EnumPrinterData** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-113">Set this parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="ce5f5-114">然後，將參數遞增一次，以用於後續涉及相同印表機的呼叫，直到函式傳回錯誤的 \_ \_ 專案為止 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-114">Then increment the parameter by one for subsequent calls involving the same printer, until the function returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="ce5f5-115">如需詳細資訊，請參閱下列備註一節。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-115">See the following Remarks section for further information.</span></span>

<span data-ttu-id="ce5f5-116">如果您使用 *cbValueName* 和 *cbData* 參數描述中所述的技術來取得適當的緩衝區大小值，在第一次呼叫指定的印表機控制碼的 **EnumPrinterData** 時，將這些參數設定為零，就 *不會對* 該呼叫造成影響。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-116">If you use the technique mentioned in the descriptions of the *cbValueName* and *cbData* parameters to obtain adequate buffer size values, setting both those parameters to zero in a first call to **EnumPrinterData** for a specified printer handle, the value of *dwIndex* does not matter for that call.</span></span> <span data-ttu-id="ce5f5-117">在下一次呼叫 **EnumPrinterData** 時，將 *dwIndex* 設定為零，以啟動實際的列舉程式。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-117">Set *dwIndex* to zero in the next call to **EnumPrinterData** to start the actual enumeration process.</span></span>

<span data-ttu-id="ce5f5-118">設定資料值未排序。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-118">Configuration data values are not ordered.</span></span> <span data-ttu-id="ce5f5-119">新的值會有任意的索引。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-119">New values will have an arbitrary index.</span></span> <span data-ttu-id="ce5f5-120">這表示 **EnumPrinterData** 函數可能會以任何順序傳回值。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-120">This means that the **EnumPrinterData** function may return values in any order.</span></span>

</dd> <dt>

<span data-ttu-id="ce5f5-121">*pValueName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ce5f5-121">*pValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5f5-122">緩衝區的指標，此緩衝區會接收設定資料值的名稱，包括終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-122">A pointer to a buffer that receives the name of the configuration data value, including a terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="ce5f5-123">*cbValueName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ce5f5-123">*cbValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5f5-124">*PValueName* 所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-124">The size, in bytes, of the buffer pointed to by *pValueName*.</span></span>

<span data-ttu-id="ce5f5-125">如果您想要讓作業系統提供適當的緩衝區大小，請將此參數和 *cbData* 參數設定為零，以在第一次呼叫指定的印表機控制碼時使用 **EnumPrinterData** 。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-125">If you want to have the operating system supply an adequate buffer size, set both this parameter and the *cbData* parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="ce5f5-126">當函式傳回時， *pcbValueName* 所指向的變數將包含夠大的緩衝區大小，以成功列舉印表機的所有設定資料值名稱。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-126">When the function returns, the variable pointed to by *pcbValueName* will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.</span></span>

</dd> <dt>

<span data-ttu-id="ce5f5-127">*pcbValueName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ce5f5-127">*pcbValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5f5-128">變數的指標，此變數會接收儲存在 *pValueName* 所指向之緩衝區中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-128">A pointer to a variable that receives the number of bytes stored into the buffer pointed to by *pValueName*.</span></span>

</dd> <dt>

<span data-ttu-id="ce5f5-129">*pType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ce5f5-129">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5f5-130">變數的指標，此變數會接收程式碼，指出儲存在指定值中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-130">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="ce5f5-131">如需可能的類型代碼清單，請參閱登錄 [數值型別](/windows/desktop/SysInfo/registry-value-types)。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-131">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span> <span data-ttu-id="ce5f5-132">如果不需要類型程式碼，則 *pType* 參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-132">The *pType* parameter can be **NULL** if the type code is not required.</span></span>

</dd> <dt>

<span data-ttu-id="ce5f5-133">*.pdata* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ce5f5-133">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5f5-134">接收設定資料值的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-134">A pointer to a buffer that receives the configuration data value.</span></span>

<span data-ttu-id="ce5f5-135">如果不需要設定資料值，則這個參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-135">This parameter can be **NULL** if the configuration data value is not required.</span></span>

</dd> <dt>

<span data-ttu-id="ce5f5-136">*cbData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ce5f5-136">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5f5-137">*.Pdata* 所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-137">The size, in bytes, of the buffer pointed to by *pData*.</span></span>

<span data-ttu-id="ce5f5-138">如果您想要讓作業系統提供適當的緩衝區大小，請將此參數和 *cbValueName* 參數設定為零，以在第一次呼叫指定的印表機控制碼時使用 **EnumPrinterData** 。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-138">If you want to have the operating system supply an adequate buffer size, set both this parameter and the *cbValueName* parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="ce5f5-139">當函式傳回時， *pcbData* 所指向的變數將包含夠大的緩衝區大小，以成功列舉印表機的所有設定資料值名稱。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-139">When the function returns, the variable pointed to by *pcbData* will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.</span></span>

</dd> <dt>

<span data-ttu-id="ce5f5-140">*pcbData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ce5f5-140">*pcbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5f5-141">變數的指標，此變數會接收儲存在 *.pdata* 所指向之緩衝區中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-141">A pointer to a variable that receives the number of bytes stored into the buffer pointed to by *pData*.</span></span>

<span data-ttu-id="ce5f5-142">如果 *.pdata* 為 **null**，則這個參數可以是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-142">This parameter can be **NULL** if *pData* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce5f5-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce5f5-143">Return value</span></span>

<span data-ttu-id="ce5f5-144">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-144">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="ce5f5-145">如果函式失敗，則傳回值為系統錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-145">If the function fails, the return value is a system error code.</span></span>

<span data-ttu-id="ce5f5-146">\_ \_ \_ 如果沒有更多的設定資料值要抓取指定的印表機控制碼，此函數會傳回錯誤的專案。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-146">The function returns ERROR\_NO\_MORE\_ITEMS when there are no more configuration data values to retrieve for a specified printer handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce5f5-147">備註</span><span class="sxs-lookup"><span data-stu-id="ce5f5-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ce5f5-148">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ce5f5-149">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ce5f5-150">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ce5f5-151">**EnumPrinterData** 會透過 [**SetPrinterData**](setprinterdata.md) 函式來抓取印表機設定資料集。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-151">**EnumPrinterData** retrieves printer configuration data set by the [**SetPrinterData**](setprinterdata.md) function.</span></span> <span data-ttu-id="ce5f5-152">印表機的設定資料是由一組命名的和具類型的值所組成。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-152">A printer's configuration data consists of a set of named and typed values.</span></span> <span data-ttu-id="ce5f5-153">**EnumPrinterData** 函式會在您每次呼叫時取得其中一個值，以及其名稱和類型程式碼。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-153">The **EnumPrinterData** function obtains one of these values, and its name and a type code, each time you call it.</span></span> <span data-ttu-id="ce5f5-154">連續多次呼叫 **EnumPrinterData** 函數，以取得印表機的所有設定資料值。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-154">Call the **EnumPrinterData** function several times in succession to obtain all of a printer's configuration data values.</span></span>

<span data-ttu-id="ce5f5-155">印表機設定資料會儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-155">Printer configuration data is stored in the registry.</span></span> <span data-ttu-id="ce5f5-156">列舉印表機設定資料時，您應該避免呼叫可能會變更該資料的登錄功能。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-156">While enumerating printer configuration data, you should avoid calling registry functions that might change that data.</span></span>

<span data-ttu-id="ce5f5-157">如果您想要讓作業系統提供適當的緩衝區大小，請先呼叫 **EnumPrinterData** ，並將 *cbValueName* 和 *cbData* 參數設定為零，如稍早在參數區段中所述。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-157">If you want to have the operating system supply an adequate buffer size, first call **EnumPrinterData** with both the *cbValueName* and *cbData* parameters set to zero, as noted earlier in the Parameters section.</span></span> <span data-ttu-id="ce5f5-158">此呼叫的 *dwIndex* 值並不重要。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-158">The value of *dwIndex* does not matter for this call.</span></span> <span data-ttu-id="ce5f5-159">當函式傳回時， \* *pcbValueName* 和 \* *pcbData* 將包含夠大的緩衝區大小，以列舉印表機的所有設定資料值名稱和值。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-159">When the function returns, \**pcbValueName* and \**pcbData* will contain buffer sizes that are large enough to enumerate all of the printer's configuration data value names and values.</span></span> <span data-ttu-id="ce5f5-160">在下一個呼叫中，配置值名稱和資料緩衝區，將 *cbValueName* 和 *cbData* 設定為所配置緩衝區的大小（以位元組為單位），並將 *dwIndex* 設定為零。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-160">On the next call, allocate value name and data buffers, set *cbValueName* and *cbData* to the sizes in bytes of the allocated buffers, and set *dwIndex* to zero.</span></span> <span data-ttu-id="ce5f5-161">之後，繼續呼叫 **EnumPrinterData** 函式，每次遞增 *dwIndex* 一次，直到函式傳回錯誤的 \_ 專案 \_ 為止 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ce5f5-161">Thereafter, continue to call the **EnumPrinterData** function, incrementing *dwIndex* by one each time, until the function returns ERROR\_NO\_MORE\_ITEMS.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce5f5-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce5f5-162">Requirements</span></span>



| <span data-ttu-id="ce5f5-163">需求</span><span class="sxs-lookup"><span data-stu-id="ce5f5-163">Requirement</span></span> | <span data-ttu-id="ce5f5-164">值</span><span class="sxs-lookup"><span data-stu-id="ce5f5-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce5f5-165">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce5f5-165">Minimum supported client</span></span><br/> | <span data-ttu-id="ce5f5-166">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce5f5-166">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ce5f5-167">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce5f5-167">Minimum supported server</span></span><br/> | <span data-ttu-id="ce5f5-168">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce5f5-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ce5f5-169">標頭</span><span class="sxs-lookup"><span data-stu-id="ce5f5-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce5f5-170"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ce5f5-170"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ce5f5-171">程式庫</span><span class="sxs-lookup"><span data-stu-id="ce5f5-171">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce5f5-172"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce5f5-172"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ce5f5-173">DLL</span><span class="sxs-lookup"><span data-stu-id="ce5f5-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce5f5-174"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="ce5f5-174"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ce5f5-175">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="ce5f5-175">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ce5f5-176">**EnumPrinterDataW** (Unicode) 和 **EnumPrinterDataA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="ce5f5-176">**EnumPrinterDataW** (Unicode) and **EnumPrinterDataA** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="ce5f5-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce5f5-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce5f5-178">列印</span><span class="sxs-lookup"><span data-stu-id="ce5f5-178">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ce5f5-179">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="ce5f5-179">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ce5f5-180">**DeletePrinterData**</span><span class="sxs-lookup"><span data-stu-id="ce5f5-180">**DeletePrinterData**</span></span>](deleteprinterdata.md)
</dt> <dt>

[<span data-ttu-id="ce5f5-181">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="ce5f5-181">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="ce5f5-182">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="ce5f5-182">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="ce5f5-183">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="ce5f5-183">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="ce5f5-184">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="ce5f5-184">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="ce5f5-185">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="ce5f5-185">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> </dl>

 

