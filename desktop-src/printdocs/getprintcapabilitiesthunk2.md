---
description: 抓取格式符合 XML 列印架構的印表機功能。
ms.assetid: 15219c19-b64c-4c51-9357-15a797557693
title: GetPrintCapabilitiesThunk2 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintCapabilitiesThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: eb60f1cdabad6287e236fc099fc304e9e7de83ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974478"
---
# <a name="getprintcapabilitiesthunk2-function"></a><span data-ttu-id="2470e-103">GetPrintCapabilitiesThunk2 函式</span><span class="sxs-lookup"><span data-stu-id="2470e-103">GetPrintCapabilitiesThunk2 function</span></span>

<span data-ttu-id="2470e-104">\[這項功能不受支援，而且可能會在未來的 Windows 版本中停用或刪除。</span><span class="sxs-lookup"><span data-stu-id="2470e-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="2470e-105">[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) 會提供對等的功能，因此應該改用。\]</span><span class="sxs-lookup"><span data-stu-id="2470e-105">[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="2470e-106">抓取格式符合 XML [列印架構](./printschema.md)的印表機功能。</span><span class="sxs-lookup"><span data-stu-id="2470e-106">Retrieves the printer's capabilities formatted in compliance with the XML [Print Schema](./printschema.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2470e-107">語法</span><span class="sxs-lookup"><span data-stu-id="2470e-107">Syntax</span></span>


```C++
HRESULT GetPrintCapabilitiesThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      INT         cbPrintTicket,
  _Out_     BYTE        **ppbPrintCapabilities,
  _Out_     INT         *pcbPrintCapabilitiesLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="2470e-108">參數</span><span class="sxs-lookup"><span data-stu-id="2470e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2470e-109">*hProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2470e-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2470e-110">開啟的列印票證提供者的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2470e-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="2470e-111">[**BindPTProviderThunk**](bindptproviderthunk.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="2470e-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="2470e-112">*pPrintTicket* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2470e-112">*pPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2470e-113">包含列印票證資料的緩衝區，如 [列印架構](./printschema.md)中所述，以 XML 表示。</span><span class="sxs-lookup"><span data-stu-id="2470e-113">The buffer that contains the print ticket data, expressed in XML as described in the [Print Schema](./printschema.md).</span></span>

</dd> <dt>

<span data-ttu-id="2470e-114">*cbPrintTicket* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2470e-114">*cbPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2470e-115">*PPrintTicket* 所參考的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2470e-115">The size, in bytes, of the buffer referenced by *pPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="2470e-116">*ppbPrintCapabilities* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2470e-116">*ppbPrintCapabilities* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2470e-117">這個函式所配置並包含有效列印功能資訊（編碼為 XML）的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="2470e-117">The address of the buffer that is allocated by this function and contains the valid print capabilities information, encoded as XML.</span></span> <span data-ttu-id="2470e-118">此函數會呼叫 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) 來配置這個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2470e-118">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="2470e-119">當不再需要緩衝區時，呼叫端必須藉由呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放它。</span><span class="sxs-lookup"><span data-stu-id="2470e-119">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="2470e-120">*pcbPrintCapabilitiesLength* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2470e-120">*pcbPrintCapabilitiesLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2470e-121">*PpbPrintCapabilities* 所參考的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2470e-121">The size, in bytes, of the buffer referenced by *ppbPrintCapabilities*.</span></span>

</dd> <dt>

<span data-ttu-id="2470e-122">*pbstrErrorMessage* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="2470e-122">*pbstrErrorMessage* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2470e-123">字串的指標，這個字串會指定 *pPrintTicket* 不正確內容（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="2470e-123">A pointer to a string that specifies what, if anything, is invalid about *pPrintTicket*.</span></span> <span data-ttu-id="2470e-124">如果有效，則此值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2470e-124">If it is valid, this value is **NULL**.</span></span> <span data-ttu-id="2470e-125">當函式傳回時，如果 *pbstrErrorMessage* 不是 **Null** ，則呼叫端必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)釋放字串。</span><span class="sxs-lookup"><span data-stu-id="2470e-125">If *pbstrErrorMessage* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2470e-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="2470e-126">Return value</span></span>

<span data-ttu-id="2470e-127">如果方法成功，它會傳回 **S \_ OK**，否則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2470e-127">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="2470e-128">如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="2470e-128">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2470e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="2470e-129">Requirements</span></span>



| <span data-ttu-id="2470e-130">需求</span><span class="sxs-lookup"><span data-stu-id="2470e-130">Requirement</span></span> | <span data-ttu-id="2470e-131">值</span><span class="sxs-lookup"><span data-stu-id="2470e-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2470e-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2470e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2470e-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2470e-133">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2470e-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2470e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2470e-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2470e-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2470e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2470e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2470e-137"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2470e-137"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2470e-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2470e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2470e-139">**PTGetPrintCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2470e-139">**PTGetPrintCapabilities**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[<span data-ttu-id="2470e-140">列印架構</span><span class="sxs-lookup"><span data-stu-id="2470e-140">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="2470e-141">列印</span><span class="sxs-lookup"><span data-stu-id="2470e-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2470e-142">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="2470e-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

