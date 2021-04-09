---
description: 抓取特定識別碼的應用程式特定資料或其他屬性資料。
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: 'ICoNtextNode：： GetPropertyData 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 381d137dd73056a2a6f4c2e9cd3746f9f16c5b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690600"
---
# <a name="icontextnodegetpropertydata-method"></a><span data-ttu-id="b165e-103">ICoNtextNode：： GetPropertyData 方法</span><span class="sxs-lookup"><span data-stu-id="b165e-103">IContextNode::GetPropertyData method</span></span>

<span data-ttu-id="b165e-104">抓取特定識別碼的應用程式特定資料或其他屬性資料。</span><span class="sxs-lookup"><span data-stu-id="b165e-104">Retrieves application-specific data or other property data for the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="b165e-105">語法</span><span class="sxs-lookup"><span data-stu-id="b165e-105">Syntax</span></span>


```C++
HRESULT GetPropertyData(
  [in]      const GUID  *pPropertyDataId,
  [in, out]       ULONG *pulPropertyDataSize,
  [out]           BYTE  **ppbPropertyData
);
```



## <a name="parameters"></a><span data-ttu-id="b165e-106">參數</span><span class="sxs-lookup"><span data-stu-id="b165e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b165e-107">*pPropertyDataId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b165e-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b165e-108">資料的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b165e-108">The identifier for the data.</span></span>

</dd> <dt>

<span data-ttu-id="b165e-109">*pulPropertyDataSize* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b165e-109">*pulPropertyDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b165e-110">資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b165e-110">The size of the data in bytes.</span></span> <span data-ttu-id="b165e-111">未使用傳入的值。</span><span class="sxs-lookup"><span data-stu-id="b165e-111">The value that is passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b165e-112">*ppbPropertyData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b165e-112">*ppbPropertyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b165e-113">8位不帶正負號的整數陣列的指標，其中包含屬性資料。</span><span class="sxs-lookup"><span data-stu-id="b165e-113">A pointer to an 8-bit unsigned integer array that contains the property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b165e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b165e-114">Return value</span></span>

<span data-ttu-id="b165e-115">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="b165e-115">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b165e-116">備註</span><span class="sxs-lookup"><span data-stu-id="b165e-116">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b165e-117">若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *ppbPropertyData* 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b165e-117">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbPropertyData* when you no longer need the information.</span></span>

 

<span data-ttu-id="b165e-118">除了使用 [**ICoNtextNode：： AddPropertyData**](icontextnode-addpropertydata.md)來取得已加入的應用程式特定資料以外，這個方法還會用來抓取 [內容節點屬性](context-node-properties.md) 常數所描述的通用屬性。</span><span class="sxs-lookup"><span data-stu-id="b165e-118">In addition to retrieving application-specific data that was added with [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md), this method is used to retrieve common properties that are described by the [Context Node Properties](context-node-properties.md) constants.</span></span>

<span data-ttu-id="b165e-119">字串類型屬性包括：</span><span class="sxs-lookup"><span data-stu-id="b165e-119">The string-type properties include:</span></span>

-   <span data-ttu-id="b165e-120">GUID \_ CNP \_ RECOGNIZEDSTRING</span><span class="sxs-lookup"><span data-stu-id="b165e-120">GUID\_CNP\_RECOGNIZEDSTRING</span></span>
-   <span data-ttu-id="b165e-121">GUID \_ CNP \_ SHAPENAME</span><span class="sxs-lookup"><span data-stu-id="b165e-121">GUID\_CNP\_SHAPENAME</span></span>
-   <span data-ttu-id="b165e-122">GUID \_ AHP \_ ANALYSISHINTNAME</span><span class="sxs-lookup"><span data-stu-id="b165e-122">GUID\_AHP\_ANALYSISHINTNAME</span></span>
-   <span data-ttu-id="b165e-123">GUID \_ AHP \_ PREFIXTEXT</span><span class="sxs-lookup"><span data-stu-id="b165e-123">GUID\_AHP\_PREFIXTEXT</span></span>
-   <span data-ttu-id="b165e-124">GUID \_ AHP \_ SUFFIXTEXT</span><span class="sxs-lookup"><span data-stu-id="b165e-124">GUID\_AHP\_SUFFIXTEXT</span></span>
-   <span data-ttu-id="b165e-125">GUID \_ AHP 的 \_ 模擬</span><span class="sxs-lookup"><span data-stu-id="b165e-125">GUID\_AHP\_FACTOID</span></span>

<span data-ttu-id="b165e-126">傳回值為 \**WCHAR \** _。如果您將 \_ *ppbPropertyData* 參數轉換成 \**WCHAR \**_ ，其傳回的長度為 `(length of the string + 1) _ sizeof(WCHAR)` 。</span><span class="sxs-lookup"><span data-stu-id="b165e-126">The return value is \**WCHAR\**_. If you cast the \_*ppbPropertyData* parameter to \**WCHAR\**_ its returned length is `(length of the string + 1) _ sizeof(WCHAR)`.</span></span>

<span data-ttu-id="b165e-127">布林值類型屬性包括：</span><span class="sxs-lookup"><span data-stu-id="b165e-127">The Boolean-type properties include:</span></span>

-   <span data-ttu-id="b165e-128">GUID \_ AHP \_ OVERRIDELANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="b165e-128">GUID\_AHP\_OVERRIDELANGUAGEID</span></span>
-   <span data-ttu-id="b165e-129">GUID \_ AHP \_ COERCETOFACTOID</span><span class="sxs-lookup"><span data-stu-id="b165e-129">GUID\_AHP\_COERCETOFACTOID</span></span>
-   <span data-ttu-id="b165e-130">GUID \_ AHP \_ WORDMODE</span><span class="sxs-lookup"><span data-stu-id="b165e-130">GUID\_AHP\_WORDMODE</span></span>

<span data-ttu-id="b165e-131">傳回值是 **VARIANT \_ BOOL**。</span><span class="sxs-lookup"><span data-stu-id="b165e-131">The return value is **VARIANT\_BOOL**.</span></span> <span data-ttu-id="b165e-132">如果您將 \* *ppbPropertyData* 參數轉換成 \**VARIANT \_ BOOL \** _ 其傳回的長度為 `sizeof(VARIANT_BOOL)` 。</span><span class="sxs-lookup"><span data-stu-id="b165e-132">If you cast the \**ppbPropertyData* parameter to \**VARIANT\_BOOL\** _ its returned length is `sizeof(VARIANT_BOOL)`.</span></span>

<span data-ttu-id="b165e-133">GUID \_ AHP \_ 指南是一個指南型別屬性。</span><span class="sxs-lookup"><span data-stu-id="b165e-133">GUID\_AHP\_GUIDE is a guide-type property.</span></span> <span data-ttu-id="b165e-134">傳回值為 _*InkAnalysisRecognitionGuide \**_。</span><span class="sxs-lookup"><span data-stu-id="b165e-134">The return value is _*InkAnalysisRecognitionGuide\**_.</span></span> <span data-ttu-id="b165e-135">如果您將 \_ *ppbPropertyData* 參數轉換成 \**InkAnalysisRecognitionGuide \** _ 其傳回的長度為 `sizeof(InkAnalysisRecognitionGuide)` 。</span><span class="sxs-lookup"><span data-stu-id="b165e-135">If you cast the \_*ppbPropertyData* parameter to \**InkAnalysisRecognitionGuide\** _ its returned length is `sizeof(InkAnalysisRecognitionGuide)`.</span></span>

<span data-ttu-id="b165e-136">整數類型屬性包括：</span><span class="sxs-lookup"><span data-stu-id="b165e-136">Integer-type properties include:</span></span>

-   <span data-ttu-id="b165e-137">GUID \_ CNP \_ LINENUMBER</span><span class="sxs-lookup"><span data-stu-id="b165e-137">GUID\_CNP\_LINENUMBER</span></span>
-   <span data-ttu-id="b165e-138">GUID \_ CNP \_ POINTSPERINCH</span><span class="sxs-lookup"><span data-stu-id="b165e-138">GUID\_CNP\_POINTSPERINCH</span></span>
-   <span data-ttu-id="b165e-139">GUID \_ CNP \_ CONFIDENCELEVEL</span><span class="sxs-lookup"><span data-stu-id="b165e-139">GUID\_CNP\_CONFIDENCELEVEL</span></span>
-   <span data-ttu-id="b165e-140">GUID \_ CNP \_ 確認</span><span class="sxs-lookup"><span data-stu-id="b165e-140">GUID\_CNP\_CONFIRMATION</span></span>
-   <span data-ttu-id="b165e-141">GUID \_ CNP \_ MAXIMUMSTROKECOUNT</span><span class="sxs-lookup"><span data-stu-id="b165e-141">GUID\_CNP\_MAXIMUMSTROKECOUNT</span></span>
-   <span data-ttu-id="b165e-142">GUID \_ CNP \_ 分割</span><span class="sxs-lookup"><span data-stu-id="b165e-142">GUID\_CNP\_SEGMENTATION</span></span>
-   <span data-ttu-id="b165e-143">GUID \_ CNP \_ ALIGNMENTLEVEL</span><span class="sxs-lookup"><span data-stu-id="b165e-143">GUID\_CNP\_ALIGNMENTLEVEL</span></span>

<span data-ttu-id="b165e-144">傳回值為 _*LONG \**_。</span><span class="sxs-lookup"><span data-stu-id="b165e-144">The return value is _*LONG\**_.</span></span> <span data-ttu-id="b165e-145">如果您將 \_ *ppbPropertyData* 參數轉換成 \**LONG \** _ 其傳回的長度為 `sizeof(LONG)` 。</span><span class="sxs-lookup"><span data-stu-id="b165e-145">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)`.</span></span>

<span data-ttu-id="b165e-146">明細度量-類型屬性包括：</span><span class="sxs-lookup"><span data-stu-id="b165e-146">Line metrics-type properties include:</span></span>

-   <span data-ttu-id="b165e-147">GUID \_ CNP \_ ASCENDERS</span><span class="sxs-lookup"><span data-stu-id="b165e-147">GUID\_CNP\_ASCENDERS</span></span>
-   <span data-ttu-id="b165e-148">GUID \_ CNP \_ 下行</span><span class="sxs-lookup"><span data-stu-id="b165e-148">GUID\_CNP\_DESCENDERS</span></span>
-   <span data-ttu-id="b165e-149">GUID \_ CNP \_ 基準</span><span class="sxs-lookup"><span data-stu-id="b165e-149">GUID\_CNP\_BASELINE</span></span>
-   <span data-ttu-id="b165e-150">GUID \_ CNP \_ 中線</span><span class="sxs-lookup"><span data-stu-id="b165e-150">GUID\_CNP\_MIDLINE</span></span>

<span data-ttu-id="b165e-151">傳回值為 _*LONG \**_。</span><span class="sxs-lookup"><span data-stu-id="b165e-151">The return value is _*LONG\**_.</span></span> <span data-ttu-id="b165e-152">如果您將 \_ *ppbPropertyData* 參數轉換成 \**LONG \** _ 其傳回的長度是，則表示 `sizeof(LONG)_4` 起始點的 (x，y) 值，後面接著 (x，y) 值的結束點。</span><span class="sxs-lookup"><span data-stu-id="b165e-152">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)_4`, signifying the (x, y) values for the starting points followed by the (x, y) values for the ending points.</span></span>

<span data-ttu-id="b165e-153">GUID \_ CNP \_ TEXTRECOGNIZERID 是 **guid** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b165e-153">GUID\_CNP\_TEXTRECOGNIZERID is a **GUID** property.</span></span> <span data-ttu-id="b165e-154">傳回值為 \**GUID \** _。如果您將 \_ *ppbPropertyData* 參數轉換成 \**GUID \**_ ，則其傳回的長度為 `sizeof(GUID)` 。</span><span class="sxs-lookup"><span data-stu-id="b165e-154">The return value is \**GUID\**_. If you cast the \_*ppbPropertyData* parameter to \**GUID\**_ its returned length is `sizeof(GUID)`.</span></span>

<span data-ttu-id="b165e-155">GUID \_ CNP \_ ROTATEDBOUNDINGBOX 是旋轉周框方塊屬性。</span><span class="sxs-lookup"><span data-stu-id="b165e-155">GUID\_CNP\_ROTATEDBOUNDINGBOX is a rotated bounding box property.</span></span> <span data-ttu-id="b165e-156">傳回值為 _*LONG \**_。</span><span class="sxs-lookup"><span data-stu-id="b165e-156">The return value is _*LONG\**_.</span></span> <span data-ttu-id="b165e-157">如果您將 \_ *ppbPropertyData* 參數轉換成 \**LONG \** _ 其傳回的長度是，表示方塊 `sizeof(LONG)_8` 四個角落的 (x，y) 值。</span><span class="sxs-lookup"><span data-stu-id="b165e-157">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)_8`, signifying the (x, y) values for the four corners of the box.</span></span>

<span data-ttu-id="b165e-158">GUID \_ CNP \_ HOTPOINT 是作用點屬性。</span><span class="sxs-lookup"><span data-stu-id="b165e-158">GUID\_CNP\_HOTPOINT is a hot point property.</span></span> <span data-ttu-id="b165e-159">傳回值為 \**LONG \** _。如果您將 \_ *ppbPropertyData* 參數轉換成 \**LONG \**_ ，其傳回的長度為 `sizeof(LONG)_2` ，表示該點的 (x，y) 值。</span><span class="sxs-lookup"><span data-stu-id="b165e-159">The return value is \**LONG\**_. If you cast the \_*ppbPropertyData* parameter to \**LONG\**_ its returned length is `sizeof(LONG)_2`, signifying the (x, y) values for the point.</span></span>

<span data-ttu-id="b165e-160">GUID \_ AHP \_ 單詞表是一個字組清單屬性。</span><span class="sxs-lookup"><span data-stu-id="b165e-160">GUID\_AHP\_WORDLIST is a word list property.</span></span> <span data-ttu-id="b165e-161">傳回值為 \**WCHAR \** _。如果您將 \_ *ppbPropertyData* 參數轉換成 \**WCHAR \**_ ，其傳回的長度是 `n _ sizeof(WCHAR)` ，其中 `n` 是清單中字串數目的總和，加上每個字串的每個 **Null** 終止字元的字串長度。</span><span class="sxs-lookup"><span data-stu-id="b165e-161">The return value is \**WCHAR\**_. If you cast the \_*ppbPropertyData* parameter to \**WCHAR\**_ its returned length is `n _ sizeof(WCHAR)`, where `n` is the sum of the string lengths of the number of strings in the list plus 1 for each **NULL** termination character for each string.</span></span>

## <a name="examples"></a><span data-ttu-id="b165e-162">範例</span><span class="sxs-lookup"><span data-stu-id="b165e-162">Examples</span></span>

<span data-ttu-id="b165e-163">此範例顯示存取段落內容節點類型之 AlignmentLevel 內容節點屬性的方法。</span><span class="sxs-lookup"><span data-stu-id="b165e-163">This example shows a method that accesses the AlignmentLevel context node property of a Paragraph context node type.</span></span>


```C++
// Checks a paragraph context node's alignment level property.
// Only paragraph type context nodes contain the alignment level property.
HRESULT CMyClass::ExploreParagraphNode(
    IContextNode *pParagraphNode)
{
    // Get the AlignmentLevel property data for the paragraph.
    LONG * alignmentLevel = NULL;
    ULONG ulDataLen = 0;

    HRESULT hr = pParagraphNode->GetPropertyData(
        (const GUID*)&GUID_CNP_ALIGNMENTLEVEL,
        &ulDataLen,
        (BYTE**)&alignmentLevel);

    if( FAILED(hr) ||
        ulDataLen != sizeof(LONG) ||
        alignmentLevel == NULL )
    {
        // Insert code that handles an error here.
    }
    else
    {
        // Insert code that uses the alignment level here.
    }

    // Free the memory allocated for the property data.
    ::CoTaskMemFree(alignmentLevel);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="b165e-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="b165e-164">Requirements</span></span>



| <span data-ttu-id="b165e-165">需求</span><span class="sxs-lookup"><span data-stu-id="b165e-165">Requirement</span></span> | <span data-ttu-id="b165e-166">值</span><span class="sxs-lookup"><span data-stu-id="b165e-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b165e-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b165e-167">Minimum supported client</span></span><br/> | <span data-ttu-id="b165e-168">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b165e-168">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b165e-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b165e-169">Minimum supported server</span></span><br/> | <span data-ttu-id="b165e-170">都不支援</span><span class="sxs-lookup"><span data-stu-id="b165e-170">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b165e-171">標頭</span><span class="sxs-lookup"><span data-stu-id="b165e-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="b165e-172"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="b165e-172"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b165e-173">DLL</span><span class="sxs-lookup"><span data-stu-id="b165e-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b165e-174"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b165e-174"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b165e-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b165e-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b165e-176">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="b165e-176">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b165e-177">**ICoNtextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="b165e-177">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="b165e-178">**ICoNtextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="b165e-178">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="b165e-179">**ICoNtextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="b165e-179">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="b165e-180">**ICoNtextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="b165e-180">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="b165e-181">**ICoNtextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="b165e-181">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="b165e-182">**ICoNtextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="b165e-182">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="b165e-183">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="b165e-183">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

