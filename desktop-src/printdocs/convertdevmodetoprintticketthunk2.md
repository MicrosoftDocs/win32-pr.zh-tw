---
description: 將 DEVMODE 結構轉換為列印票證。
ms.assetid: c03371f8-a978-4fb7-82cc-f76a65f3904c
title: ConvertDevModeToPrintTicketThunk2 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertDevModeToPrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: f13d597a11a4d6cfd1ad6f5d70b3a386560f5106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982402"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a><span data-ttu-id="8707e-103">ConvertDevModeToPrintTicketThunk2 函式</span><span class="sxs-lookup"><span data-stu-id="8707e-103">ConvertDevModeToPrintTicketThunk2 function</span></span>

<span data-ttu-id="8707e-104">\[這項功能不受支援，而且可能會在未來的 Windows 版本中停用或刪除。</span><span class="sxs-lookup"><span data-stu-id="8707e-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="8707e-105">[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) 會提供對等的功能，因此應該改用。\]</span><span class="sxs-lookup"><span data-stu-id="8707e-105">[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="8707e-106">將 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構轉換為列印票證。</span><span class="sxs-lookup"><span data-stu-id="8707e-106">Converts a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure to a print ticket.</span></span>

## <a name="syntax"></a><span data-ttu-id="8707e-107">語法</span><span class="sxs-lookup"><span data-stu-id="8707e-107">Syntax</span></span>


```C++
HRESULT ConvertDevModeToPrintTicketThunk2(
  _In_  HPTPROVIDER hProvider,
  _In_  BYTE        *pDevmode,
  _In_  ULONG       cbSize,
  _In_  DWORD       scope,
  _Out_ BYTE        **ppPrintTicket,
  _Out_ INT         *pcbPrintTicketLength
);
```



## <a name="parameters"></a><span data-ttu-id="8707e-108">參數</span><span class="sxs-lookup"><span data-stu-id="8707e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8707e-109">*hProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8707e-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8707e-110">開啟的列印票證提供者的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8707e-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="8707e-111">[**BindPTProviderThunk**](bindptproviderthunk.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="8707e-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8707e-112">*pDevmode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8707e-112">*pDevmode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8707e-113">要轉換的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 指標。</span><span class="sxs-lookup"><span data-stu-id="8707e-113">A pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) to convert.</span></span>

</dd> <dt>

<span data-ttu-id="8707e-114">*cbSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8707e-114">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8707e-115">傳入 *pDevmode* 的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8707e-115">The size, in bytes, of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passed in *pDevmode*.</span></span>

</dd> <dt>

<span data-ttu-id="8707e-116">*範圍* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8707e-116">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8707e-117">值，這個值會指定 *ppPrintTicket* 的範圍。</span><span class="sxs-lookup"><span data-stu-id="8707e-117">A value that specifies the scope of *ppPrintTicket*.</span></span> <span data-ttu-id="8707e-118">這個值可以指定單一頁面、整份檔，或列印工作中的所有檔。</span><span class="sxs-lookup"><span data-stu-id="8707e-118">This value can specify a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="8707e-119">此參數的值必須是 [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) 列舉的成員（轉換為 **DWORD**）。</span><span class="sxs-lookup"><span data-stu-id="8707e-119">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="8707e-120">*ppPrintTicket* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8707e-120">*ppPrintTicket* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8707e-121">包含列印票證的緩衝區位址，代表在 *pDevmode* 中傳遞的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 。</span><span class="sxs-lookup"><span data-stu-id="8707e-121">The address of the buffer that contains a print ticket that represents the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passed in *pDevmode*.</span></span> <span data-ttu-id="8707e-122">此函數會呼叫 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) 來配置這個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8707e-122">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="8707e-123">當不再需要緩衝區時，呼叫端必須藉由呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放它。</span><span class="sxs-lookup"><span data-stu-id="8707e-123">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="8707e-124">*pcbPrintTicketLength* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8707e-124">*pcbPrintTicketLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8707e-125">*PpPrintTicket* 中傳回之列印票證的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8707e-125">The size, in bytes, of the print ticket returned in *ppPrintTicket*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8707e-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="8707e-126">Return value</span></span>

<span data-ttu-id="8707e-127">如果方法成功，它會傳回 **S \_ OK**，否則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8707e-127">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="8707e-128">如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="8707e-128">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8707e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="8707e-129">Requirements</span></span>



| <span data-ttu-id="8707e-130">需求</span><span class="sxs-lookup"><span data-stu-id="8707e-130">Requirement</span></span> | <span data-ttu-id="8707e-131">值</span><span class="sxs-lookup"><span data-stu-id="8707e-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8707e-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8707e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8707e-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8707e-133">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8707e-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8707e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8707e-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8707e-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8707e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8707e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8707e-137"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8707e-137"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8707e-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8707e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8707e-139">列印架構</span><span class="sxs-lookup"><span data-stu-id="8707e-139">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="8707e-140">**PTConvertDevModeToPrintTicket**</span><span class="sxs-lookup"><span data-stu-id="8707e-140">**PTConvertDevModeToPrintTicket**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[<span data-ttu-id="8707e-141">列印</span><span class="sxs-lookup"><span data-stu-id="8707e-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8707e-142">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="8707e-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

