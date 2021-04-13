---
description: 包含物件的集合，這些物件會執行 IInkAnalysisRecognizer 介面，以及表示辨識手寫、物件或手勢的能力。
ms.assetid: d9264c9f-bf75-493e-8e41-57ea69955e6b
title: 'IInkAnalysisRecognizers 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ba9bbcd029803e613fb27d351de554c013c02616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318463"
---
# <a name="iinkanalysisrecognizers-interface"></a><span data-ttu-id="d4b71-103">IInkAnalysisRecognizers 介面</span><span class="sxs-lookup"><span data-stu-id="d4b71-103">IInkAnalysisRecognizers interface</span></span>

<span data-ttu-id="d4b71-104">包含物件的集合，這些物件會執行 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 介面，以及表示辨識手寫、物件或手勢的能力。</span><span class="sxs-lookup"><span data-stu-id="d4b71-104">Contains a collection of objects that implement the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) interface and that represent the ability to recognize handwriting, objects, or gestures.</span></span>

## <a name="members"></a><span data-ttu-id="d4b71-105">成員</span><span class="sxs-lookup"><span data-stu-id="d4b71-105">Members</span></span>

<span data-ttu-id="d4b71-106">**IInkAnalysisRecognizers** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="d4b71-106">The **IInkAnalysisRecognizers** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d4b71-107">**IInkAnalysisRecognizers** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d4b71-107">**IInkAnalysisRecognizers** also has these types of members:</span></span>

-   [<span data-ttu-id="d4b71-108">方法</span><span class="sxs-lookup"><span data-stu-id="d4b71-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d4b71-109">方法</span><span class="sxs-lookup"><span data-stu-id="d4b71-109">Methods</span></span>

<span data-ttu-id="d4b71-110">**IInkAnalysisRecognizers** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d4b71-110">The **IInkAnalysisRecognizers** interface has these methods.</span></span>



| <span data-ttu-id="d4b71-111">方法</span><span class="sxs-lookup"><span data-stu-id="d4b71-111">Method</span></span>                                                                               | <span data-ttu-id="d4b71-112">描述</span><span class="sxs-lookup"><span data-stu-id="d4b71-112">Description</span></span>                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4b71-113">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="d4b71-113">**GetCount**</span></span>](iinkanalysisrecognizers-getcount.md)                                 | <span data-ttu-id="d4b71-114">抓取這個集合中的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="d4b71-114">Retrieves the number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span><br/> |
| [<span data-ttu-id="d4b71-115">**GetInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="d4b71-115">**GetInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizers-getinkanalysisrecognizer.md) | <span data-ttu-id="d4b71-116">抓取位於指定之索引處的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 。</span><span class="sxs-lookup"><span data-stu-id="d4b71-116">Retrieves the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="d4b71-117">備註</span><span class="sxs-lookup"><span data-stu-id="d4b71-117">Remarks</span></span>

<span data-ttu-id="d4b71-118">[**IInkAnalyzer**](iinkanalyzer.md)的 [**IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)方法會傳回 **IInkAnalysisRecognizers** 集合，其中包含目前平板電腦上可用的筆墨辨識器。</span><span class="sxs-lookup"><span data-stu-id="d4b71-118">The [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) method of [**IInkAnalyzer**](iinkanalyzer.md) returns an **IInkAnalysisRecognizers** collection containing the ink recognizers available on the current Tablet PC.</span></span>

<span data-ttu-id="d4b71-119">針對語言辨識器， [**IInkAnalysisRecognizer：： GetLanguages**](iinkanalysisrecognizer-getlanguages.md) 方法會傳回非空白的陣列。</span><span class="sxs-lookup"><span data-stu-id="d4b71-119">For a language recognizer, the [**IInkAnalysisRecognizer::GetLanguages**](iinkanalysisrecognizer-getlanguages.md) method returns a non-empty array.</span></span> <span data-ttu-id="d4b71-120">針對筆勢辨識器和物件辨識器， **IInkAnalysisRecognizer：： GetLanguages** 方法會傳回空陣列。</span><span class="sxs-lookup"><span data-stu-id="d4b71-120">For both gesture recognizers and object recognizers, the **IInkAnalysisRecognizer::GetLanguages** method returns an empty array.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4b71-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4b71-121">Requirements</span></span>



| <span data-ttu-id="d4b71-122">需求</span><span class="sxs-lookup"><span data-stu-id="d4b71-122">Requirement</span></span> | <span data-ttu-id="d4b71-123">值</span><span class="sxs-lookup"><span data-stu-id="d4b71-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b71-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4b71-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d4b71-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4b71-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d4b71-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4b71-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d4b71-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="d4b71-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d4b71-128">標頭</span><span class="sxs-lookup"><span data-stu-id="d4b71-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4b71-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="d4b71-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d4b71-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d4b71-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4b71-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4b71-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d4b71-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4b71-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4b71-133">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="d4b71-133">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="d4b71-134">**IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法**</span><span class="sxs-lookup"><span data-stu-id="d4b71-134">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="d4b71-135">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="d4b71-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

