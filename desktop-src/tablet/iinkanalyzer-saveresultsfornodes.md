---
description: 儲存與 IInkAnalyzer 相關聯之特定內容節點集合的分析結果。
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: 'IInkAnalyzer：： SaveResultsForNodes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eb628fafb9bf479e6a011137105005e541180aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113328"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a><span data-ttu-id="dac51-103">IInkAnalyzer：： SaveResultsForNodes 方法</span><span class="sxs-lookup"><span data-stu-id="dac51-103">IInkAnalyzer::SaveResultsForNodes method</span></span>

<span data-ttu-id="dac51-104">儲存與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯之特定內容節點集合的分析結果。</span><span class="sxs-lookup"><span data-stu-id="dac51-104">Saves analysis results for a specific context node collection associated with an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dac51-105">語法</span><span class="sxs-lookup"><span data-stu-id="dac51-105">Syntax</span></span>


```C++
HRESULT SaveResultsForNodes(
  [in]      IContextNodes *pContextNodes,
  [in, out] ULONG         *pulSerializedDataSize,
  [out]     BYTE          **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="dac51-106">參數</span><span class="sxs-lookup"><span data-stu-id="dac51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dac51-107">*pCoNtextNodes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dac51-107">*pContextNodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dac51-108">要儲存分析結果的 [**ICoNtextNode**](icontextnode.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="dac51-108">The [**IContextNode**](icontextnode.md) collection for which to save analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="dac51-109">*pulSerializedDataSize* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="dac51-109">*pulSerializedDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dac51-110">*PpbSerializedData* 中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="dac51-110">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="dac51-111">*ppbSerializedData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dac51-111">*ppbSerializedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dac51-112">序列化分析資料的指標。</span><span class="sxs-lookup"><span data-stu-id="dac51-112">Pointer to the serialized analysis data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dac51-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="dac51-113">Return value</span></span>

<span data-ttu-id="dac51-114">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="dac51-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dac51-115">備註</span><span class="sxs-lookup"><span data-stu-id="dac51-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="dac51-116">若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請在 *ppbSerializedData* 上呼叫 CoTaskMemFree。</span><span class="sxs-lookup"><span data-stu-id="dac51-116">To avoid a memory leak, call [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) on \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="dac51-117">這個方法會將 [**ICoNtextNode**](icontextnode.md) 物件的目前分析結果儲存在 *pCoNtextNodes* 中，以及其所有上階和子系內容節點。</span><span class="sxs-lookup"><span data-stu-id="dac51-117">This method saves the current analysis results for the [**IContextNode**](icontextnode.md) objects in *pContextNodes* and all of their ancestor and descendant context nodes.</span></span> <span data-ttu-id="dac51-118">這個方法不會儲存任何筆觸資料。</span><span class="sxs-lookup"><span data-stu-id="dac51-118">This method does not save any stroke data.</span></span> <span data-ttu-id="dac51-119">您的應用程式必須負責同步處理任何分析結果和對應的筆劃資料（如果保存的話）。</span><span class="sxs-lookup"><span data-stu-id="dac51-119">It is the responsibility of your application to synchronize any analysis results and corresponding stroke data, if it persists.</span></span>

<span data-ttu-id="dac51-120">如果要儲存的 [**ICoNtextNode**](icontextnode.md) 物件只部分填入，這個方法會傳回錯誤碼 (請參閱 [**ICoNtextNode：： GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)) 。</span><span class="sxs-lookup"><span data-stu-id="dac51-120">If the [**IContextNode**](icontextnode.md) object to be saved is only partially populated, this method returns an error code (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="dac51-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="dac51-121">Requirements</span></span>



| <span data-ttu-id="dac51-122">需求</span><span class="sxs-lookup"><span data-stu-id="dac51-122">Requirement</span></span> | <span data-ttu-id="dac51-123">值</span><span class="sxs-lookup"><span data-stu-id="dac51-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dac51-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dac51-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dac51-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dac51-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dac51-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dac51-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dac51-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="dac51-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="dac51-128">標頭</span><span class="sxs-lookup"><span data-stu-id="dac51-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dac51-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="dac51-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dac51-130">DLL</span><span class="sxs-lookup"><span data-stu-id="dac51-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dac51-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dac51-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="dac51-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dac51-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac51-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="dac51-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="dac51-134">**IInkAnalyzer：： LoadResults 方法**</span><span class="sxs-lookup"><span data-stu-id="dac51-134">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="dac51-135">**IInkAnalyzer：： SaveResults 方法**</span><span class="sxs-lookup"><span data-stu-id="dac51-135">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="dac51-136">**IInkAnalyzer：： SaveResultsForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="dac51-136">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="dac51-137">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="dac51-137">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="dac51-138">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="dac51-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

