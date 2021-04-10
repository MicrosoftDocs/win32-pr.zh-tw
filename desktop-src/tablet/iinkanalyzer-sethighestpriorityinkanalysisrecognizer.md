---
description: 將指定的 IInkAnalysisRecognizer 移至 IInkAnalyzer 物件的筆跡辨識器清單中的第一個位置。
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: 'IInkAnalyzer：： SetHighestPriorityInkAnalysisRecognizer 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetHighestPriorityInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 534b94e4f2964aa81f04e0adac6f45f346c530c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848073"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a><span data-ttu-id="82893-103">IInkAnalyzer：： SetHighestPriorityInkAnalysisRecognizer 方法</span><span class="sxs-lookup"><span data-stu-id="82893-103">IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer method</span></span>

<span data-ttu-id="82893-104">將指定的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 移至 [**IInkAnalyzer**](iinkanalyzer.md) 物件的筆跡辨識器清單中的第一個位置。</span><span class="sxs-lookup"><span data-stu-id="82893-104">Moves the specified [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) to the first position in the [**IInkAnalyzer**](iinkanalyzer.md) object's list of ink recognizers.</span></span>

## <a name="syntax"></a><span data-ttu-id="82893-105">語法</span><span class="sxs-lookup"><span data-stu-id="82893-105">Syntax</span></span>


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a><span data-ttu-id="82893-106">參數</span><span class="sxs-lookup"><span data-stu-id="82893-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82893-107">*pInkAnalysisRecognizer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82893-107">*pInkAnalysisRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82893-108">要放在第一個位置的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 。</span><span class="sxs-lookup"><span data-stu-id="82893-108">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) to place in the first position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82893-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="82893-109">Return value</span></span>

<span data-ttu-id="82893-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="82893-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="82893-111">備註</span><span class="sxs-lookup"><span data-stu-id="82893-111">Remarks</span></span>

<span data-ttu-id="82893-112">若要依優先權順序取得筆跡辨識器的清單，請呼叫 [**IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)。</span><span class="sxs-lookup"><span data-stu-id="82893-112">To get the list of ink recognizers in priority order, call [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).</span></span>

<span data-ttu-id="82893-113">這個方法不會影響 [**IInkAnalyzer**](iinkanalyzer.md)物件的筆墨辨識器清單中其餘 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)物件的順序。</span><span class="sxs-lookup"><span data-stu-id="82893-113">This method does not affect the order of the rest of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md) object's list of ink recognizers.</span></span>

<span data-ttu-id="82893-114">[**IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)所傳回的筆跡辨識器順序，表示 [**IInkAnalyzer**](iinkanalyzer.md)評估可用 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)物件的順序。</span><span class="sxs-lookup"><span data-stu-id="82893-114">The order of the ink recognizers returned by [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indicates the order in which the [**IInkAnalyzer**](iinkanalyzer.md) evaluates the available [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

<span data-ttu-id="82893-115">筆跡辨識器的使用會根據其在清單中的順序進行評估。</span><span class="sxs-lookup"><span data-stu-id="82893-115">Use of the ink recognizers is evaluated based on their order in the list.</span></span>

<span data-ttu-id="82893-116">在筆跡分析期間， [**IInkAnalyzer**](iinkanalyzer.md) 會逐一查看其清單中的筆跡辨識器，直到找到支援筆觸語言和其他屬性的辨識器。</span><span class="sxs-lookup"><span data-stu-id="82893-116">During ink analysis, the [**IInkAnalyzer**](iinkanalyzer.md) iterates through the ink recognizers in its list until it finds a recognizer that supports the language and other properties of the strokes.</span></span> <span data-ttu-id="82893-117">此辨識器會用於這些筆觸的筆跡辨識。</span><span class="sxs-lookup"><span data-stu-id="82893-117">This recognizer is used for ink recognition for those strokes.</span></span>

<span data-ttu-id="82893-118">如果 [**IInkAnalyzer**](iinkanalyzer.md) 在分析期間找不到支援一組筆觸的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) ，則 **IInkAnalyzer** 會產生 [**IAnalysisWarning**](ianalysiswarning.md) ，並顯示警告碼 **AnalysisWarningCode \_ InkAnalysisRecognizerNotInstalled** (請參閱 [**IAnalysisWarning：： GetWarningCode**](ianalysiswarning-getwarningcode.md)) 。</span><span class="sxs-lookup"><span data-stu-id="82893-118">If the [**IInkAnalyzer**](iinkanalyzer.md) does not find an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that supports a set of strokes during analysis, the **IInkAnalyzer** generates an [**IAnalysisWarning**](ianalysiswarning.md) with a warning code of **AnalysisWarningCode\_InkAnalysisRecognizerNotInstalled** (see [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="82893-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="82893-119">Requirements</span></span>



| <span data-ttu-id="82893-120">需求</span><span class="sxs-lookup"><span data-stu-id="82893-120">Requirement</span></span> | <span data-ttu-id="82893-121">值</span><span class="sxs-lookup"><span data-stu-id="82893-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82893-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82893-122">Minimum supported client</span></span><br/> | <span data-ttu-id="82893-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82893-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="82893-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82893-124">Minimum supported server</span></span><br/> | <span data-ttu-id="82893-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="82893-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="82893-126">標頭</span><span class="sxs-lookup"><span data-stu-id="82893-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="82893-127"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="82893-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="82893-128">DLL</span><span class="sxs-lookup"><span data-stu-id="82893-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82893-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82893-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="82893-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82893-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82893-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="82893-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="82893-132">**IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法**</span><span class="sxs-lookup"><span data-stu-id="82893-132">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="82893-133">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="82893-133">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="82893-134">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="82893-134">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="82893-135">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="82893-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




