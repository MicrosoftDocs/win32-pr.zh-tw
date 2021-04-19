---
description: 指出 IInkAnalyzer 具有辨識結果精確度的信賴等級。
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: 'RecognitionConfidence 列舉 (IACom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognitionConfidence
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: e0358aacf789c391d99c10fc0fea64670dc4710e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987395"
---
# <a name="recognitionconfidence-enumeration"></a><span data-ttu-id="7f29c-103">RecognitionConfidence 列舉</span><span class="sxs-lookup"><span data-stu-id="7f29c-103">RecognitionConfidence enumeration</span></span>

<span data-ttu-id="7f29c-104">指出 [**IInkAnalyzer**](iinkanalyzer.md) 具有辨識結果精確度的信賴等級。</span><span class="sxs-lookup"><span data-stu-id="7f29c-104">Indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the recognition result.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f29c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f29c-105">Syntax</span></span>


```C++
typedef enum RecognitionConfidence { 
  RecognitionConfidence_Strong        = 0,
  RecognitionConfidence_Intermediate  = 1,
  RecognitionConfidence_Poor          = 2,
  RecognitionConfidence_Unknown       = 3
} RecognitionConfidence;
```



## <a name="constants"></a><span data-ttu-id="7f29c-106">常數</span><span class="sxs-lookup"><span data-stu-id="7f29c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7f29c-107"><span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence \_ 強式**</span><span class="sxs-lookup"><span data-stu-id="7f29c-107"><span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence\_Strong**</span></span>
</dt> <dd>

<span data-ttu-id="7f29c-108">在結果或替代方面具有強烈的信賴度。</span><span class="sxs-lookup"><span data-stu-id="7f29c-108">Strong confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="7f29c-109"><span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence \_ 中繼**</span><span class="sxs-lookup"><span data-stu-id="7f29c-109"><span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence\_Intermediate**</span></span>
</dt> <dd>

<span data-ttu-id="7f29c-110">結果或替代中的中繼信賴度。</span><span class="sxs-lookup"><span data-stu-id="7f29c-110">Intermediate confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="7f29c-111"><span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence \_ 不良**</span><span class="sxs-lookup"><span data-stu-id="7f29c-111"><span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence\_Poor**</span></span>
</dt> <dd>

<span data-ttu-id="7f29c-112">結果或替代的信賴度不佳。</span><span class="sxs-lookup"><span data-stu-id="7f29c-112">Poor confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="7f29c-113"><span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="7f29c-113"><span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence\_Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="7f29c-114">產生已辨識文字的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 不支援信賴等級。</span><span class="sxs-lookup"><span data-stu-id="7f29c-114">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that generated the recognized text does not support confidence levels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f29c-115">備註</span><span class="sxs-lookup"><span data-stu-id="7f29c-115">Remarks</span></span>

<span data-ttu-id="7f29c-116">[**IInkAnalyzer**](iinkanalyzer.md)會使用一或多個 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)物件，將手寫轉換成文字。</span><span class="sxs-lookup"><span data-stu-id="7f29c-116">The [**IInkAnalyzer**](iinkanalyzer.md) uses one or more [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects to convert handwriting to text.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f29c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f29c-117">Requirements</span></span>



| <span data-ttu-id="7f29c-118">需求</span><span class="sxs-lookup"><span data-stu-id="7f29c-118">Requirement</span></span> | <span data-ttu-id="7f29c-119">值</span><span class="sxs-lookup"><span data-stu-id="7f29c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f29c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f29c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7f29c-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f29c-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7f29c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f29c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7f29c-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="7f29c-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7f29c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="7f29c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f29c-125"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="7f29c-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f29c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f29c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f29c-127">**IAnalysisAlternate：： GetRecognitionConfidence 方法**</span><span class="sxs-lookup"><span data-stu-id="7f29c-127">**IAnalysisAlternate::GetRecognitionConfidence Method**</span></span>](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[<span data-ttu-id="7f29c-128">**ICoNtextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="7f29c-128">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="7f29c-129">內容節點屬性</span><span class="sxs-lookup"><span data-stu-id="7f29c-129">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="7f29c-130">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="7f29c-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




