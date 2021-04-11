---
description: 從 IInkAnalyzer 中移除分析提示。
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: 'IInkAnalyzer：:D eleteAnalysisHint 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.DeleteAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f84f718701abd5bc76b55427aab9df072f758c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113352"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a><span data-ttu-id="69c28-103">IInkAnalyzer：:D eleteAnalysisHint 方法</span><span class="sxs-lookup"><span data-stu-id="69c28-103">IInkAnalyzer::DeleteAnalysisHint method</span></span>

<span data-ttu-id="69c28-104">從 [**IInkAnalyzer**](iinkanalyzer.md)中移除分析提示。</span><span class="sxs-lookup"><span data-stu-id="69c28-104">Removes an analysis hint from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="69c28-105">語法</span><span class="sxs-lookup"><span data-stu-id="69c28-105">Syntax</span></span>


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="69c28-106">參數</span><span class="sxs-lookup"><span data-stu-id="69c28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69c28-107">*pHintToDelete* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69c28-107">*pHintToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69c28-108">來自 [**IInkAnalyzer**](iinkanalyzer.md)的分析提示。</span><span class="sxs-lookup"><span data-stu-id="69c28-108">The analysis hint from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69c28-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="69c28-109">Return value</span></span>

<span data-ttu-id="69c28-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="69c28-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="69c28-111">備註</span><span class="sxs-lookup"><span data-stu-id="69c28-111">Remarks</span></span>

<span data-ttu-id="69c28-112">移除分析提示並不會標示提示的區域以進行 reanalysis。</span><span class="sxs-lookup"><span data-stu-id="69c28-112">Removing an analysis hint does not mark the hint's area for reanalysis.</span></span> <span data-ttu-id="69c28-113">若要標記 reanalysis 提示內的區域，請使用 [**IInkAnalyzer：： SetDirtyRegion 方法**](iinkanalyzer-setdirtyregion.md) ，將中途區域設定為目前中途區域和分析提示區域的聯集。</span><span class="sxs-lookup"><span data-stu-id="69c28-113">To mark the area within the hint for reanalysis, use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to set the dirty region to the union of the current dirty region and area of the analysis hint.</span></span>

<span data-ttu-id="69c28-114">提示已從分析器移除;不過， [**ICoNtextNode**](icontextnode.md) 本身不會被刪除。</span><span class="sxs-lookup"><span data-stu-id="69c28-114">The hint is removed from the analyzer; however, the [**IContextNode**](icontextnode.md) itself is not deleted.</span></span>

<span data-ttu-id="69c28-115">當 *pHintToDelete* 是不是 AnalysisHint 類型的 [**ICoNtextNode**](icontextnode.md) 時，這個方法會傳回錯誤碼 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。</span><span class="sxs-lookup"><span data-stu-id="69c28-115">This method returns an error code when *pHintToDelete* is a [**IContextNode**](icontextnode.md) that is not of type AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="69c28-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="69c28-116">Requirements</span></span>



| <span data-ttu-id="69c28-117">需求</span><span class="sxs-lookup"><span data-stu-id="69c28-117">Requirement</span></span> | <span data-ttu-id="69c28-118">值</span><span class="sxs-lookup"><span data-stu-id="69c28-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69c28-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69c28-119">Minimum supported client</span></span><br/> | <span data-ttu-id="69c28-120">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69c28-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="69c28-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69c28-121">Minimum supported server</span></span><br/> | <span data-ttu-id="69c28-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="69c28-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="69c28-123">標頭</span><span class="sxs-lookup"><span data-stu-id="69c28-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="69c28-124"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="69c28-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="69c28-125">DLL</span><span class="sxs-lookup"><span data-stu-id="69c28-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69c28-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69c28-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="69c28-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69c28-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69c28-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="69c28-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="69c28-129">**IInkAnalyzer：： CreateAnalysisHint 方法**</span><span class="sxs-lookup"><span data-stu-id="69c28-129">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="69c28-130">**IInkAnalyzer：： GetAnalysisHints 方法**</span><span class="sxs-lookup"><span data-stu-id="69c28-130">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="69c28-131">**IInkAnalyzer：： GetAnalysisHintsByName 方法**</span><span class="sxs-lookup"><span data-stu-id="69c28-131">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="69c28-132">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="69c28-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




