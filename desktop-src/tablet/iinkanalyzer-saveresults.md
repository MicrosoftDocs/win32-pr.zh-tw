---
description: 儲存 IInkAnalyzer 的所有分析結果。
ms.assetid: 538eb781-d831-475b-ba09-271d71f6a6bf
title: 'IInkAnalyzer：： SaveResults 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a07351662512ad3234dfe6847cd8c4300bd035e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318448"
---
# <a name="iinkanalyzersaveresults-method"></a><span data-ttu-id="b483b-103">IInkAnalyzer：： SaveResults 方法</span><span class="sxs-lookup"><span data-stu-id="b483b-103">IInkAnalyzer::SaveResults method</span></span>

<span data-ttu-id="b483b-104">儲存 [**IInkAnalyzer**](iinkanalyzer.md)的所有分析結果。</span><span class="sxs-lookup"><span data-stu-id="b483b-104">Saves all analysis results for an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b483b-105">語法</span><span class="sxs-lookup"><span data-stu-id="b483b-105">Syntax</span></span>


```C++
HRESULT SaveResults(
  [out] ULONG *pulSerializedDataSize,
  [out] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="b483b-106">參數</span><span class="sxs-lookup"><span data-stu-id="b483b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b483b-107">*pulSerializedDataSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b483b-107">*pulSerializedDataSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b483b-108">*PpbSerializedData* 中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b483b-108">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="b483b-109">*ppbSerializedData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b483b-109">*ppbSerializedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b483b-110">包含已儲存分析結果的陣列。</span><span class="sxs-lookup"><span data-stu-id="b483b-110">An array containing the saved analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b483b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b483b-111">Return value</span></span>

<span data-ttu-id="b483b-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="b483b-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b483b-113">備註</span><span class="sxs-lookup"><span data-stu-id="b483b-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b483b-114">若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *ppbSerializedData* 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b483b-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="b483b-115">這個方法會儲存所有目前的分析結果，其中包括目前的分析提示和自訂辨識器節點 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b483b-115">This method saves all the current analysis results, which include current analysis hint and custom recognizer nodes (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="b483b-116">這個方法不會儲存任何筆觸資料。</span><span class="sxs-lookup"><span data-stu-id="b483b-116">This method does not save any stroke data.</span></span> <span data-ttu-id="b483b-117">您的應用程式必須負責同步處理任何分析結果和對應的筆劃（如果它保存資料）。</span><span class="sxs-lookup"><span data-stu-id="b483b-117">It is the responsibility of your application to synchronize any analysis results and corresponding strokes if it persists data.</span></span>

<span data-ttu-id="b483b-118">當要儲存的 [**ICoNtextNode**](icontextnode.md) 物件已部分填入時，這個方法會傳回錯誤碼 (請參閱 [**ICoNtextNode：： GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b483b-118">This method returns an error code when an [**IContextNode**](icontextnode.md) object to save is partially populated (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b483b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b483b-119">Requirements</span></span>



| <span data-ttu-id="b483b-120">需求</span><span class="sxs-lookup"><span data-stu-id="b483b-120">Requirement</span></span> | <span data-ttu-id="b483b-121">值</span><span class="sxs-lookup"><span data-stu-id="b483b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b483b-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b483b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b483b-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b483b-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b483b-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b483b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b483b-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="b483b-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b483b-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b483b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b483b-127"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="b483b-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b483b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b483b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b483b-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b483b-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b483b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b483b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b483b-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b483b-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b483b-132">**IInkAnalyzer：： LoadResults 方法**</span><span class="sxs-lookup"><span data-stu-id="b483b-132">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="b483b-133">**IInkAnalyzer：： SaveResultsForNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="b483b-133">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="b483b-134">**IInkAnalyzer：： SaveResultsForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="b483b-134">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="b483b-135">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="b483b-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b483b-136">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="b483b-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

