---
title: 'UtilAssembleStringsWithAlloc 函式 (Ndattributils) '
description: 配置字串並使用字串資料表所提供的字串將它格式化。 此函數會使用 StringCchPrintf 來建立格式化的字串。
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- UtilAssembleStringsWithAlloc 函式 NDF
topic_type:
- apiref
api_name:
- UtilAssembleStringsWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae121b1d5f2d968f696190c64828be91adc71da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686619"
---
# <a name="utilassemblestringswithalloc-function"></a><span data-ttu-id="96231-105">UtilAssembleStringsWithAlloc 函式</span><span class="sxs-lookup"><span data-stu-id="96231-105">UtilAssembleStringsWithAlloc function</span></span>

<span data-ttu-id="96231-106">**UtilAssembleStringsWithAlloc** 函式會配置字串，並使用字串資料表所提供的字串將它格式化。</span><span class="sxs-lookup"><span data-stu-id="96231-106">The **UtilAssembleStringsWithAlloc** function allocates a string and formats it using strings provided by the string table.</span></span> <span data-ttu-id="96231-107">此函數會使用 [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) 來建立格式化的字串。</span><span class="sxs-lookup"><span data-stu-id="96231-107">This function uses [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) to create the formatted string.</span></span>

## <a name="syntax"></a><span data-ttu-id="96231-108">語法</span><span class="sxs-lookup"><span data-stu-id="96231-108">Syntax</span></span>


```C++
HRESULT UtilAssembleStringsWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR InputFormat,
  _In_  LPCWSTR InputString,
  _In_  BOOLEAN AdditionalArgument,
  _In_  ULONG   AdditionalValue
);
```



## <a name="parameters"></a><span data-ttu-id="96231-109">參數</span><span class="sxs-lookup"><span data-stu-id="96231-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96231-110">*緩衝區* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="96231-110">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96231-111">類型： \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="96231-111">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="96231-112">將放置新配置之字串的位置。</span><span class="sxs-lookup"><span data-stu-id="96231-112">The location where the newly allocated string will be placed.</span></span> <span data-ttu-id="96231-113">當不再需要字串時，必須使用 [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放它。</span><span class="sxs-lookup"><span data-stu-id="96231-113">When the string is no longer needed, it must be released with [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="96231-114">*BufferMax* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96231-114">*BufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96231-115">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="96231-115">Type: **UINT**</span></span>

<span data-ttu-id="96231-116">*緩衝區* 所配置的字串中允許的最大字元數。</span><span class="sxs-lookup"><span data-stu-id="96231-116">The maximum number of characters allowed in the string allocated by *Buffer*.</span></span> <span data-ttu-id="96231-117">如果產生的格式化字串長度超過指定的字元數，則會被截斷並以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="96231-117">If the resulting formatted string is longer than the number of characters specified, it is truncated and null-terminated.</span></span>

> [!Note]  
> <span data-ttu-id="96231-118">此參數不可以設定為零。</span><span class="sxs-lookup"><span data-stu-id="96231-118">This parameter may not be set to zero.</span></span>

 

</dd> <dt>

<span data-ttu-id="96231-119">*InputFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96231-119">*InputFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96231-120">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="96231-120">Type: **LPCWSTR**</span></span>

<span data-ttu-id="96231-121">字串資料表中的字串資源，代表傳遞給 [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)的格式參數。</span><span class="sxs-lookup"><span data-stu-id="96231-121">String resource out of the string table representing a format parameter passed to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa).</span></span> <span data-ttu-id="96231-122">它是使用 [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)所建立。</span><span class="sxs-lookup"><span data-stu-id="96231-122">It is constructed using [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span></span>

<span data-ttu-id="96231-123">資源字串格式必須指定採用寬字元串的格式參數，或採用不帶正負號的 long 和寬字元串格式參數。</span><span class="sxs-lookup"><span data-stu-id="96231-123">The resource string format must specify either a format parameter taking a wide string, or a format parameter taking an unsigned long and a wide string.</span></span>

</dd> <dt>

<span data-ttu-id="96231-124">*InputString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96231-124">*InputString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96231-125">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="96231-125">Type: **LPCWSTR**</span></span>

<span data-ttu-id="96231-126">字串資料表中的字串資源，代表傳遞給 [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) 的引數，用於取代格式參數中的寬字元串。</span><span class="sxs-lookup"><span data-stu-id="96231-126">String resource out of the string table representing an argument passed to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) in place of the wide string in the format parameter.</span></span> <span data-ttu-id="96231-127">它是使用 [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)所建立。</span><span class="sxs-lookup"><span data-stu-id="96231-127">It is constructed using [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span></span>

</dd> <dt>

<span data-ttu-id="96231-128">*AdditionalArgument* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96231-128">*AdditionalArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96231-129">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="96231-129">Type: **BOOLEAN**</span></span>

<span data-ttu-id="96231-130">如果應將 *AdditionalValue* 作為第一個格式化引數傳遞至 [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)，則為 True;否則 (為 false，而且只會將 *InputString* 所識別的資源字串傳遞) 。</span><span class="sxs-lookup"><span data-stu-id="96231-130">True if *AdditionalValue* should be passed in as the first formatting argument to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); otherwise, false (and only the resource string identified by *InputString* will be passed).</span></span>

</dd> <dt>

<span data-ttu-id="96231-131">*AdditionalValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96231-131">*AdditionalValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96231-132">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="96231-132">Type: **ULONG**</span></span>

<span data-ttu-id="96231-133">當 *AdditionalArgument* 為 true 時，要做為第一個格式化引數傳遞至 [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)的值。</span><span class="sxs-lookup"><span data-stu-id="96231-133">The value to pass as the first formatting argument to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) if *AdditionalArgument* is true.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96231-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="96231-134">Return value</span></span>

<span data-ttu-id="96231-135">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="96231-135">Type: **HRESULT**</span></span>

<span data-ttu-id="96231-136">可能的傳回值包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="96231-136">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="96231-137">傳回碼</span><span class="sxs-lookup"><span data-stu-id="96231-137">Return code</span></span>                                                                                  | <span data-ttu-id="96231-138">Description</span><span class="sxs-lookup"><span data-stu-id="96231-138">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="96231-139"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="96231-139"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="96231-140">作業成功。</span><span class="sxs-lookup"><span data-stu-id="96231-140">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="96231-141"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="96231-141"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="96231-142">未正確提供一或多個參數。</span><span class="sxs-lookup"><span data-stu-id="96231-142">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="96231-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="96231-143">Requirements</span></span>



| <span data-ttu-id="96231-144">需求</span><span class="sxs-lookup"><span data-stu-id="96231-144">Requirement</span></span> | <span data-ttu-id="96231-145">值</span><span class="sxs-lookup"><span data-stu-id="96231-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="96231-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96231-146">Minimum supported client</span></span><br/> | <span data-ttu-id="96231-147">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96231-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="96231-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96231-148">Minimum supported server</span></span><br/> | <span data-ttu-id="96231-149">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96231-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="96231-150">標頭</span><span class="sxs-lookup"><span data-stu-id="96231-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="96231-151"><dt>Ndattributils。h</dt></span><span class="sxs-lookup"><span data-stu-id="96231-151"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96231-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96231-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96231-153">**UtilStringCopyWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="96231-153">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)
</dt> <dt>

[<span data-ttu-id="96231-154">**UtilLoadStringWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="96231-154">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
</dt> <dt>

[<span data-ttu-id="96231-155">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="96231-155">**StringCchPrintf**</span></span>](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)
</dt> <dt>

[<span data-ttu-id="96231-156">**MAKEINTRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="96231-156">**MAKEINTRESOURCE**</span></span>](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
</dt> <dt>

[<span data-ttu-id="96231-157">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="96231-157">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

