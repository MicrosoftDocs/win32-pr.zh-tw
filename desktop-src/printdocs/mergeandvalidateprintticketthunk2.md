---
description: 合併兩個列印票證，並傳回有效的可用列印票證。
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: MergeAndValidatePrintTicketThunk2 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeAndValidatePrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 4a21b9e505e39d64e8e0c696a3b8a6432a012d76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971609"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a><span data-ttu-id="654e2-103">MergeAndValidatePrintTicketThunk2 函式</span><span class="sxs-lookup"><span data-stu-id="654e2-103">MergeAndValidatePrintTicketThunk2 function</span></span>

<span data-ttu-id="654e2-104">\[這項功能不受支援，而且可能會在未來的 Windows 版本中停用或刪除。</span><span class="sxs-lookup"><span data-stu-id="654e2-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="654e2-105">[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) 會提供對等的功能，因此應該改用。\]</span><span class="sxs-lookup"><span data-stu-id="654e2-105">[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="654e2-106">合併兩個列印票證，並傳回有效的可用列印票證。</span><span class="sxs-lookup"><span data-stu-id="654e2-106">Merges two print tickets and returns a valid, viable print ticket.</span></span>

## <a name="syntax"></a><span data-ttu-id="654e2-107">語法</span><span class="sxs-lookup"><span data-stu-id="654e2-107">Syntax</span></span>


```C++
HRESULT MergeAndValidatePrintTicketThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pBasePrintTicket,
  _In_      INT         basePrintTicketLength,
  _In_opt_  BYTE        *pDeltaPrintTicket,
  _In_      INT         deltaPrintTicketLength,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppValidatedPrintTicket,
  _Out_     INT         *pValidatedPrintTicketLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="654e2-108">參數</span><span class="sxs-lookup"><span data-stu-id="654e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="654e2-109">*hProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="654e2-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="654e2-110">開啟的列印票證提供者的控制碼。</span><span class="sxs-lookup"><span data-stu-id="654e2-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="654e2-111">[**BindPTProviderThunk**](bindptproviderthunk.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="654e2-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="654e2-112">*pBasePrintTicket* \[在\]</span><span class="sxs-lookup"><span data-stu-id="654e2-112">*pBasePrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="654e2-113">包含基底列印票證資料的緩衝區，以 XML 表示，如 [列印架構](./printschema.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="654e2-113">The buffer that contains the base print ticket data, expressed in XML as described in the [Print Schema](./printschema.md).</span></span>

</dd> <dt>

<span data-ttu-id="654e2-114">*basePrintTicketLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="654e2-114">*basePrintTicketLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="654e2-115">*PBasePrintTicket* 所參考的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="654e2-115">The size, in bytes, of the buffer referenced by *pBasePrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="654e2-116">*pDeltaPrintTicket* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="654e2-116">*pDeltaPrintTicket* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="654e2-117">包含要合併之列印票證的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="654e2-117">The buffer that contains the print ticket to merge.</span></span> <span data-ttu-id="654e2-118">列印票證資料是以 XML 表示，如 [列印架構](./printschema.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="654e2-118">The print ticket data is expressed in XML as described in the [Print Schema](./printschema.md).</span></span> <span data-ttu-id="654e2-119">此參數的值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="654e2-119">The value of this parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="654e2-120">*deltaPrintTicketLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="654e2-120">*deltaPrintTicketLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="654e2-121">*PDeltaPrintTicket* 所參考的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="654e2-121">The size, in bytes, of the buffer referenced by *pDeltaPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="654e2-122">*範圍* \[在\]</span><span class="sxs-lookup"><span data-stu-id="654e2-122">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="654e2-123">值，指定 *pDeltaPrintTicket* 和 *ppValidatedPrintTicket* 的範圍是單一頁面、整份檔，還是列印工作中的所有檔。</span><span class="sxs-lookup"><span data-stu-id="654e2-123">The value that specifies whether the scope of *pDeltaPrintTicket* and *ppValidatedPrintTicket* is a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="654e2-124">此參數的值必須是 [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) 列舉的成員（轉換為 **DWORD**）。</span><span class="sxs-lookup"><span data-stu-id="654e2-124">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="654e2-125">*ppValidatedPrintTicket* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="654e2-125">*ppValidatedPrintTicket* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="654e2-126">包含已合併和已驗證之列印票證的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="654e2-126">The address of the buffer that contains the merged and validated print ticket.</span></span> <span data-ttu-id="654e2-127">此函數會呼叫 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) 來配置這個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="654e2-127">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="654e2-128">當不再需要緩衝區時，呼叫端必須藉由呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放它。</span><span class="sxs-lookup"><span data-stu-id="654e2-128">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="654e2-129">*pValidatedPrintTicketLength* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="654e2-129">*pValidatedPrintTicketLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="654e2-130">*PpValidatedPrintTicket* 所參考的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="654e2-130">The size, in bytes, of the buffer referenced by *ppValidatedPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="654e2-131">*pbstrErrorMessage* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="654e2-131">*pbstrErrorMessage* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="654e2-132">字串的指標，指定 *pBasePrintTicket* 或 *pDeltaPrintTicket* 中列印票證的無效內容（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="654e2-132">A pointer to a string that specifies what, if anything, is invalid about the print ticket in *pBasePrintTicket* or *pDeltaPrintTicket*.</span></span> <span data-ttu-id="654e2-133">如果兩者都是有效的，則此值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="654e2-133">If they are both valid, this value is **NULL**.</span></span> <span data-ttu-id="654e2-134">當函式傳回時，如果 *pbstrErrorMessage* 不是 **Null** ，則呼叫端必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)釋放字串。</span><span class="sxs-lookup"><span data-stu-id="654e2-134">If *pbstrErrorMessage* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="654e2-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="654e2-135">Return value</span></span>

<span data-ttu-id="654e2-136">如果方法成功，它會傳回 **S \_ OK**，否則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="654e2-136">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="654e2-137">如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="654e2-137">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="654e2-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="654e2-138">Requirements</span></span>



| <span data-ttu-id="654e2-139">需求</span><span class="sxs-lookup"><span data-stu-id="654e2-139">Requirement</span></span> | <span data-ttu-id="654e2-140">值</span><span class="sxs-lookup"><span data-stu-id="654e2-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="654e2-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="654e2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="654e2-142">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="654e2-142">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="654e2-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="654e2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="654e2-144">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="654e2-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="654e2-145">DLL</span><span class="sxs-lookup"><span data-stu-id="654e2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="654e2-146"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="654e2-146"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="654e2-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="654e2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="654e2-148">列印架構</span><span class="sxs-lookup"><span data-stu-id="654e2-148">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="654e2-149">**PTMergeAndValidatePrintTicket**</span><span class="sxs-lookup"><span data-stu-id="654e2-149">**PTMergeAndValidatePrintTicket**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[<span data-ttu-id="654e2-150">列印</span><span class="sxs-lookup"><span data-stu-id="654e2-150">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="654e2-151">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="654e2-151">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

