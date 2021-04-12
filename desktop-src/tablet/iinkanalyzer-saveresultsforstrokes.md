---
description: 儲存與 IInkAnalyzer 相關聯之指定筆劃的分析結果。
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: 'IInkAnalyzer：： SaveResultsForStrokes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1371b056cf01beba75fdcbd427c526ed29d20c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318447"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a><span data-ttu-id="ce699-103">IInkAnalyzer：： SaveResultsForStrokes 方法</span><span class="sxs-lookup"><span data-stu-id="ce699-103">IInkAnalyzer::SaveResultsForStrokes method</span></span>

<span data-ttu-id="ce699-104">儲存與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯之指定筆劃的分析結果。</span><span class="sxs-lookup"><span data-stu-id="ce699-104">Saves analysis results for the specified strokes associated with an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce699-105">語法</span><span class="sxs-lookup"><span data-stu-id="ce699-105">Syntax</span></span>


```C++
HRESULT SaveResultsForStrokes(
  [in]          ULONG ulStrokeIdsCount,
  [in]          LONG  *plStrokeIds,
  [in, out]     ULONG *pulSerializedDataSize,
  [out, retval] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="ce699-106">參數</span><span class="sxs-lookup"><span data-stu-id="ce699-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce699-107">*ulStrokeIdsCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ce699-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce699-108">**PlStrokeIds** 中的筆觸識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="ce699-108">The number of stroke identifiers in **plStrokeIds**.</span></span>

</dd> <dt>

<span data-ttu-id="ce699-109">*plStrokeIds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ce699-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce699-110">筆觸識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="ce699-110">The array of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="ce699-111">*pulSerializedDataSize* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="ce699-111">*pulSerializedDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce699-112">*PpbSerializedData* 中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ce699-112">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="ce699-113">*ppbSerializedData* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="ce699-113">*ppbSerializedData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ce699-114">序列化分析資料的指標。</span><span class="sxs-lookup"><span data-stu-id="ce699-114">Pointer to the serialized analysis data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce699-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce699-115">Return value</span></span>

<span data-ttu-id="ce699-116">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="ce699-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ce699-117">備註</span><span class="sxs-lookup"><span data-stu-id="ce699-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ce699-118">若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請在 *ppbSerializedData* 上呼叫 CoTaskMemFree。</span><span class="sxs-lookup"><span data-stu-id="ce699-118">To avoid a memory leak, call [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) on \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="ce699-119">這個方法會儲存指定之筆劃的目前分析結果。</span><span class="sxs-lookup"><span data-stu-id="ce699-119">This method saves the current analysis results for the specified strokes.</span></span> <span data-ttu-id="ce699-120">這個方法會儲存包含筆劃的筆墨分葉 [**ICoNtextNode**](icontextnode.md) 物件，以及這些內容節點的所有上階。</span><span class="sxs-lookup"><span data-stu-id="ce699-120">This method saves the ink leaf [**IContextNode**](icontextnode.md) objects containing the strokes and all of the ancestors of those context nodes.</span></span> <span data-ttu-id="ce699-121">這個方法不會儲存任何筆觸資料或分析提示節點。</span><span class="sxs-lookup"><span data-stu-id="ce699-121">This method does not save any stroke data or analysis hint nodes.</span></span> <span data-ttu-id="ce699-122">您的應用程式必須負責同步處理任何分析結果和對應的筆劃資料（如果保存的話）。</span><span class="sxs-lookup"><span data-stu-id="ce699-122">It is the responsibility of your application to synchronize any analysis results and corresponding stroke data, if it persists.</span></span>

<span data-ttu-id="ce699-123">當要儲存的 [**ICoNtextNode**](icontextnode.md) 物件已部分填入時，這個方法會傳回錯誤碼 (請參閱 [**ICoNtextNode：： GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)) 。</span><span class="sxs-lookup"><span data-stu-id="ce699-123">This method returns an error code when an [**IContextNode**](icontextnode.md) object to save is partially populated (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce699-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce699-124">Requirements</span></span>



| <span data-ttu-id="ce699-125">需求</span><span class="sxs-lookup"><span data-stu-id="ce699-125">Requirement</span></span> | <span data-ttu-id="ce699-126">值</span><span class="sxs-lookup"><span data-stu-id="ce699-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce699-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce699-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ce699-128">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce699-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ce699-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce699-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ce699-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="ce699-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ce699-131">標頭</span><span class="sxs-lookup"><span data-stu-id="ce699-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce699-132"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="ce699-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ce699-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ce699-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce699-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce699-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ce699-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce699-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce699-136">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ce699-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ce699-137">**IInkAnalyzer：： LoadResults 方法**</span><span class="sxs-lookup"><span data-stu-id="ce699-137">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="ce699-138">**IInkAnalyzer：： SaveResults 方法**</span><span class="sxs-lookup"><span data-stu-id="ce699-138">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="ce699-139">**IInkAnalyzer：： SaveResultsForNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="ce699-139">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="ce699-140">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="ce699-140">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ce699-141">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="ce699-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

