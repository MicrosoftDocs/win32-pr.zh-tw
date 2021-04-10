---
description: 取得值，指出 IInkAnalyzer 對 IAnalysisAlternate 精確度的信賴等級。
ms.assetid: ac1c68df-2e0c-4633-b7ee-519482a4d67a
title: 'IAnalysisAlternate：： GetRecognitionConfidence 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognitionConfidence
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eacaf7e5a8feaddcd437e68cf7acfa4fc5a7fc80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690619"
---
# <a name="ianalysisalternategetrecognitionconfidence-method"></a><span data-ttu-id="3f7e4-103">IAnalysisAlternate：： GetRecognitionConfidence 方法</span><span class="sxs-lookup"><span data-stu-id="3f7e4-103">IAnalysisAlternate::GetRecognitionConfidence method</span></span>

<span data-ttu-id="3f7e4-104">取得值，指出 [**IInkAnalyzer**](iinkanalyzer.md) 對 [**IAnalysisAlternate**](ianalysisalternate.md)精確度的信賴等級。</span><span class="sxs-lookup"><span data-stu-id="3f7e4-104">Gets a value that indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3f7e4-105">語法</span><span class="sxs-lookup"><span data-stu-id="3f7e4-105">Syntax</span></span>


```C++
HRESULT GetRecognitionConfidence(
  [out] RecognitionConfidence *pConfidence
);
```



## <a name="parameters"></a><span data-ttu-id="3f7e4-106">參數</span><span class="sxs-lookup"><span data-stu-id="3f7e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f7e4-107">*pConfidence* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3f7e4-107">*pConfidence* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f7e4-108">[**InkRecognitionConfidence 列舉**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence)的指標，指出 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)具有替代辨識之精確度的信賴等級。</span><span class="sxs-lookup"><span data-stu-id="3f7e4-108">A pointer to an [**InkRecognitionConfidence Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) that indicates the level of confidence that the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) has in the accuracy of the recognition alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f7e4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3f7e4-109">Return value</span></span>

<span data-ttu-id="3f7e4-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="3f7e4-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f7e4-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f7e4-111">Requirements</span></span>



| <span data-ttu-id="3f7e4-112">需求</span><span class="sxs-lookup"><span data-stu-id="3f7e4-112">Requirement</span></span> | <span data-ttu-id="3f7e4-113">值</span><span class="sxs-lookup"><span data-stu-id="3f7e4-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f7e4-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f7e4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3f7e4-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f7e4-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3f7e4-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f7e4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3f7e4-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="3f7e4-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3f7e4-118">標頭</span><span class="sxs-lookup"><span data-stu-id="3f7e4-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f7e4-119"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="3f7e4-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3f7e4-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3f7e4-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f7e4-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f7e4-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3f7e4-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f7e4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f7e4-123">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="3f7e4-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="3f7e4-124">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="3f7e4-124">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="3f7e4-125">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="3f7e4-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="3f7e4-126">**RecognitionConfidence**</span><span class="sxs-lookup"><span data-stu-id="3f7e4-126">**RecognitionConfidence**</span></span>](recognitionconfidence.md)
</dt> <dt>

[<span data-ttu-id="3f7e4-127">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="3f7e4-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




