---
description: 將列印票證轉換成 DEVMODE 結構。
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: ConvertPrintTicketToDevModeThunk2 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertPrintTicketToDevModeThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: cf05ab6739dad09332ebc6746a05f3c40ef32de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027123"
---
# <a name="convertprinttickettodevmodethunk2-function"></a><span data-ttu-id="49fe8-103">ConvertPrintTicketToDevModeThunk2 函式</span><span class="sxs-lookup"><span data-stu-id="49fe8-103">ConvertPrintTicketToDevModeThunk2 function</span></span>

<span data-ttu-id="49fe8-104">\[這項功能不受支援，而且可能會在未來的 Windows 版本中停用或刪除。</span><span class="sxs-lookup"><span data-stu-id="49fe8-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="49fe8-105">[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) 會提供對等的功能，因此應該改用。\]</span><span class="sxs-lookup"><span data-stu-id="49fe8-105">[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="49fe8-106">將列印票證轉換成 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構。</span><span class="sxs-lookup"><span data-stu-id="49fe8-106">Converts a print ticket to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="49fe8-107">語法</span><span class="sxs-lookup"><span data-stu-id="49fe8-107">Syntax</span></span>


```C++
HRESULT ConvertPrintTicketToDevModeThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      ULONG       cbSize,
  _In_      INT         baseType,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppDevmode,
  _Out_     ULONG       *pcbDevModeLength,
  _Out_opt_ BSTR        *errMsg
);
```



## <a name="parameters"></a><span data-ttu-id="49fe8-108">參數</span><span class="sxs-lookup"><span data-stu-id="49fe8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49fe8-109">*hProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49fe8-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49fe8-110">開啟的列印票證提供者的控制碼。</span><span class="sxs-lookup"><span data-stu-id="49fe8-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="49fe8-111">[**BindPTProviderThunk**](bindptproviderthunk.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="49fe8-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="49fe8-112">*pPrintTicket* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49fe8-112">*pPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49fe8-113">包含要轉換之列印票證的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="49fe8-113">The buffer that contains the print ticket to convert.</span></span>

</dd> <dt>

<span data-ttu-id="49fe8-114">*cbSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49fe8-114">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49fe8-115">傳入 *pPrintTicket* 的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="49fe8-115">The size, in bytes, of the buffer passed in *pPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="49fe8-116">*baseType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49fe8-116">*baseType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49fe8-117">值，指出當 *pPrintTicket* 未指定 **DEVMODE** 的每個可能設定時，是否使用使用者的預設 [**devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)或列印佇列的預設 **devmode** 來提供值給輸出 **DEVMODE** 。</span><span class="sxs-lookup"><span data-stu-id="49fe8-117">A value indicating whether the user's default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) or the print queue's default **DEVMODE** is used to provide values to the output **DEVMODE** when *pPrintTicket* does not specify every possible setting for a **DEVMODE**.</span></span> <span data-ttu-id="49fe8-118">此參數的值必須是 [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) 列舉的成員，並轉換為 **INT**。</span><span class="sxs-lookup"><span data-stu-id="49fe8-118">The value of this parameter must be a member of the [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) enumeration, cast as an **INT**.</span></span>

</dd> <dt>

<span data-ttu-id="49fe8-119">*範圍* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49fe8-119">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49fe8-120">值，這個值會指定 *pPrintTicket* 的範圍。</span><span class="sxs-lookup"><span data-stu-id="49fe8-120">A value that specifies the scope of *pPrintTicket*.</span></span> <span data-ttu-id="49fe8-121">這個值可以指定單一頁面、整份檔，或列印工作中的所有檔。</span><span class="sxs-lookup"><span data-stu-id="49fe8-121">This value can specify a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="49fe8-122">此參數的值必須是 [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) 列舉的成員（轉換為 **DWORD**）。</span><span class="sxs-lookup"><span data-stu-id="49fe8-122">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="49fe8-123">*ppDevmode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="49fe8-123">*ppDevmode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49fe8-124">新建立之 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)的位址。</span><span class="sxs-lookup"><span data-stu-id="49fe8-124">The address of the newly created [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span></span> <span data-ttu-id="49fe8-125">此函數會呼叫 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) 來配置這個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="49fe8-125">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="49fe8-126">當不再需要緩衝區時，呼叫端必須藉由呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放它。</span><span class="sxs-lookup"><span data-stu-id="49fe8-126">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="49fe8-127">*pcbDevModeLength* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="49fe8-127">*pcbDevModeLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49fe8-128">*PpDevmode* 中傳回的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="49fe8-128">The size, in bytes, of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) returned in *ppDevmode*.</span></span>

</dd> <dt>

<span data-ttu-id="49fe8-129">*errMsg* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="49fe8-129">*errMsg* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49fe8-130">字串的指標，指定 *pPrintTicket* 中列印票證不正確內容（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="49fe8-130">A pointer to a string that specifies what, if anything, is invalid about the print ticket in *pPrintTicket*.</span></span> <span data-ttu-id="49fe8-131">如果有效，則為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="49fe8-131">If it is valid, this is **NULL**.</span></span> <span data-ttu-id="49fe8-132">當函式傳回時，如果 *errMsg* 不是 **Null** ，則呼叫端必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)釋放字串。</span><span class="sxs-lookup"><span data-stu-id="49fe8-132">If *errMsg* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49fe8-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="49fe8-133">Return value</span></span>

<span data-ttu-id="49fe8-134">如果方法成功，它會傳回 **S \_ OK**，否則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="49fe8-134">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="49fe8-135">如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="49fe8-135">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="49fe8-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="49fe8-136">Requirements</span></span>



| <span data-ttu-id="49fe8-137">需求</span><span class="sxs-lookup"><span data-stu-id="49fe8-137">Requirement</span></span> | <span data-ttu-id="49fe8-138">值</span><span class="sxs-lookup"><span data-stu-id="49fe8-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49fe8-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49fe8-139">Minimum supported client</span></span><br/> | <span data-ttu-id="49fe8-140">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49fe8-140">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="49fe8-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49fe8-141">Minimum supported server</span></span><br/> | <span data-ttu-id="49fe8-142">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49fe8-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="49fe8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="49fe8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49fe8-144"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49fe8-144"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49fe8-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49fe8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49fe8-146">列印架構</span><span class="sxs-lookup"><span data-stu-id="49fe8-146">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="49fe8-147">**PTConvertPrintTicketToDevMode**</span><span class="sxs-lookup"><span data-stu-id="49fe8-147">**PTConvertPrintTicketToDevMode**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[<span data-ttu-id="49fe8-148">列印</span><span class="sxs-lookup"><span data-stu-id="49fe8-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="49fe8-149">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="49fe8-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

