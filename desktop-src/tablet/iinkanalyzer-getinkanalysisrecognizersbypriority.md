---
description: 抓取 IInkAnalysisRecognizer 物件的已排序集合。
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: 'IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetInkAnalysisRecognizersByPriority
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d596a8138f8ab16852ce99116eef66372ff2b074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848075"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a><span data-ttu-id="1daf5-103">IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法</span><span class="sxs-lookup"><span data-stu-id="1daf5-103">IInkAnalyzer::GetInkAnalysisRecognizersByPriority method</span></span>

<span data-ttu-id="1daf5-104">抓取 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 物件的已排序集合。</span><span class="sxs-lookup"><span data-stu-id="1daf5-104">Retrieves an ordered collection of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="1daf5-105">語法</span><span class="sxs-lookup"><span data-stu-id="1daf5-105">Syntax</span></span>


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a><span data-ttu-id="1daf5-106">參數</span><span class="sxs-lookup"><span data-stu-id="1daf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1daf5-107">*ppInkAnalysisRecognizers* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1daf5-107">*ppInkAnalysisRecognizers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1daf5-108">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)物件的已排序集合。</span><span class="sxs-lookup"><span data-stu-id="1daf5-108">An ordered collection of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1daf5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="1daf5-109">Return value</span></span>

<span data-ttu-id="1daf5-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="1daf5-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1daf5-111">備註</span><span class="sxs-lookup"><span data-stu-id="1daf5-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="1daf5-112">若要避免記憶體流失，請在 *ppInkAnalysisRecognizers* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="1daf5-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppInkAnalysisRecognizers* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="1daf5-113">此集合中的辨識器順序表示 [**IInkAnalyzer**](iinkanalyzer.md) 評估可用辨識器的順序。</span><span class="sxs-lookup"><span data-stu-id="1daf5-113">The order of the recognizers in this collection indicates the order in which the [**IInkAnalyzer**](iinkanalyzer.md) evaluates the available recognizers.</span></span> <span data-ttu-id="1daf5-114">**IInkAnalyzer** 會使用筆觸的語言作為套用 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)的主要準則。</span><span class="sxs-lookup"><span data-stu-id="1daf5-114">The **IInkAnalyzer** uses the language of the strokes as its primary criterion for applying an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span> <span data-ttu-id="1daf5-115">作為次要準則， **IInkAnalyzer** 會比較分析提示資訊與 **IInkAnalysisRecognizer** 物件的支援功能 (請參閱 [**IInkAnalysisRecognizer：： GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1daf5-115">As a secondary criterion, the **IInkAnalyzer** compares analysis hint information against an **IInkAnalysisRecognizer** object's supported capabilities (see [**IInkAnalysisRecognizer::GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)).</span></span> <span data-ttu-id="1daf5-116">如需有關分析提示的詳細資訊，請參閱 [**IInkAnalyzer：： CreateAnalysisHint 方法**](iinkanalyzer-createanalysishint.md)。</span><span class="sxs-lookup"><span data-stu-id="1daf5-116">For more information about analysis hints, see [**IInkAnalyzer::CreateAnalysisHint Method**](iinkanalyzer-createanalysishint.md).</span></span>

<span data-ttu-id="1daf5-117">如果有一個以上的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 支援語言識別項，則 [**IInkAnalyzer**](iinkanalyzer.md) 會使用「第一個」演算法來選取第一個 **IInkAnalysisRecognizer** 來分析該語言的筆觸。</span><span class="sxs-lookup"><span data-stu-id="1daf5-117">If more than one [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports a language identifier, the [**IInkAnalyzer**](iinkanalyzer.md) uses a "first-fit" algorithm to select the first **IInkAnalysisRecognizer** to analyze strokes of that language.</span></span>

## <a name="requirements"></a><span data-ttu-id="1daf5-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1daf5-118">Requirements</span></span>



| <span data-ttu-id="1daf5-119">需求</span><span class="sxs-lookup"><span data-stu-id="1daf5-119">Requirement</span></span> | <span data-ttu-id="1daf5-120">值</span><span class="sxs-lookup"><span data-stu-id="1daf5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1daf5-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1daf5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1daf5-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1daf5-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1daf5-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1daf5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1daf5-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="1daf5-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1daf5-125">標頭</span><span class="sxs-lookup"><span data-stu-id="1daf5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1daf5-126"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="1daf5-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1daf5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1daf5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1daf5-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1daf5-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1daf5-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1daf5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1daf5-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="1daf5-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="1daf5-131">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="1daf5-131">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="1daf5-132">**IInkAnalyzer：： SetHighestPriorityInkAnalysisRecognizer 方法**</span><span class="sxs-lookup"><span data-stu-id="1daf5-132">**IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer Method**</span></span>](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="1daf5-133">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="1daf5-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

