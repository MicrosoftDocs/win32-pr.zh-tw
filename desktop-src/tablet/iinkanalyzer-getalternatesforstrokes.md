---
description: 使用指定的筆觸識別碼抓取筆劃的分析替代項。
ms.assetid: e8bc198e-de0b-49b7-9120-4298985dfe64
title: 'IInkAnalyzer：： GetAlternatesForStrokes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 115b2cc1be4ba35614ada6fddd9c9fbcdfa76357
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113341"
---
# <a name="iinkanalyzergetalternatesforstrokes-method"></a><span data-ttu-id="ef884-103">IInkAnalyzer：： GetAlternatesForStrokes 方法</span><span class="sxs-lookup"><span data-stu-id="ef884-103">IInkAnalyzer::GetAlternatesForStrokes method</span></span>

<span data-ttu-id="ef884-104">使用指定的筆觸識別碼抓取筆劃的分析替代項。</span><span class="sxs-lookup"><span data-stu-id="ef884-104">Retrieves analysis alternates for the strokes with the specified stroke identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef884-105">語法</span><span class="sxs-lookup"><span data-stu-id="ef884-105">Syntax</span></span>


```C++
HRESULT GetAlternatesForStrokes(
  [in]  ULONG              ulStrokeIdsCount,
  [in]  LONG               *plStrokes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="ef884-106">參數</span><span class="sxs-lookup"><span data-stu-id="ef884-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef884-107">*ulStrokeIdsCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef884-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef884-108">*PlStrokes* 中的筆觸識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="ef884-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="ef884-109">*plStrokes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef884-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef884-110">筆觸識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="ef884-110">The array of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="ef884-111">*ulMaximumAlternates* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef884-111">*ulMaximumAlternates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef884-112">傳回的最大分析替代專案數目。</span><span class="sxs-lookup"><span data-stu-id="ef884-112">The maximum number of analysis alternatives returned.</span></span>

</dd> <dt>

<span data-ttu-id="ef884-113">*ppAlternates* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ef884-113">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef884-114">包含分析替代專案的 [**IAnalysisAlternates**](ianalysisalternates.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="ef884-114">The [**IAnalysisAlternates**](ianalysisalternates.md) object containing the analysis alternatives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef884-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef884-115">Return value</span></span>

<span data-ttu-id="ef884-116">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="ef884-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef884-117">備註</span><span class="sxs-lookup"><span data-stu-id="ef884-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ef884-118">若要避免記憶體流失，請在 ppAlternates 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （ \* 當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="ef884-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="ef884-119">Top [**IAnalysisAlternate**](ianalysisalternate.md) 會傳回為集合的第一個替代。</span><span class="sxs-lookup"><span data-stu-id="ef884-119">The top [**IAnalysisAlternate**](ianalysisalternate.md) is returned as the first alternate of the collection.</span></span>

<span data-ttu-id="ef884-120">指定的筆觸不需要代表檔的相鄰區域。</span><span class="sxs-lookup"><span data-stu-id="ef884-120">The specified strokes do not have to represent adjacent areas of the document.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef884-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef884-121">Requirements</span></span>



| <span data-ttu-id="ef884-122">需求</span><span class="sxs-lookup"><span data-stu-id="ef884-122">Requirement</span></span> | <span data-ttu-id="ef884-123">值</span><span class="sxs-lookup"><span data-stu-id="ef884-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef884-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef884-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ef884-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef884-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ef884-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef884-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ef884-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="ef884-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ef884-128">標頭</span><span class="sxs-lookup"><span data-stu-id="ef884-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef884-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="ef884-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ef884-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ef884-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef884-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef884-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ef884-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef884-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef884-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ef884-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ef884-134">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="ef884-134">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="ef884-135">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="ef884-135">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="ef884-136">**IInkAnalyzer：： GetAlternates 方法**</span><span class="sxs-lookup"><span data-stu-id="ef884-136">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="ef884-137">**IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="ef884-137">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="ef884-138">**IInkAnalyzer：： ModifyTopAlternate 方法**</span><span class="sxs-lookup"><span data-stu-id="ef884-138">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="ef884-139">**IInkAnalyzer：： ModifyTopAlternateWithConfirmation 方法**</span><span class="sxs-lookup"><span data-stu-id="ef884-139">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="ef884-140">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="ef884-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

