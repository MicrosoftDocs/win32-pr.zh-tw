---
description: 將具有無限區域的新分析提示節點加入至 IInkAnalyzer。
ms.assetid: 4cc592c4-456f-4aa5-9a87-d9427de487f3
title: 'IInkAnalyzer：： CreateAnalysisHint 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 041dc1a60c1eeb18d6896a6a23537ac9ebccd321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318459"
---
# <a name="iinkanalyzercreateanalysishint-method"></a><span data-ttu-id="9e395-103">IInkAnalyzer：： CreateAnalysisHint 方法</span><span class="sxs-lookup"><span data-stu-id="9e395-103">IInkAnalyzer::CreateAnalysisHint method</span></span>

<span data-ttu-id="9e395-104">將具有無限區域的新分析提示節點加入至 [**IInkAnalyzer**](iinkanalyzer.md)。</span><span class="sxs-lookup"><span data-stu-id="9e395-104">Adds a new analysis hint node with an infinite area to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9e395-105">語法</span><span class="sxs-lookup"><span data-stu-id="9e395-105">Syntax</span></span>


```C++
HRESULT CreateAnalysisHint(
  [out] IContextNode **ppAnalysisHint
);
```



## <a name="parameters"></a><span data-ttu-id="9e395-106">參數</span><span class="sxs-lookup"><span data-stu-id="9e395-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e395-107">*ppAnalysisHint* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9e395-107">*ppAnalysisHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e395-108">新的分析提示節點。</span><span class="sxs-lookup"><span data-stu-id="9e395-108">The new analysis hint node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e395-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e395-109">Return value</span></span>

<span data-ttu-id="9e395-110">請參閱 [類別和介面-筆墨分析](classes-and-interfaces---ink-analysis.md) 以取得傳回值的描述。</span><span class="sxs-lookup"><span data-stu-id="9e395-110">See [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md) for a description of the return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e395-111">備註</span><span class="sxs-lookup"><span data-stu-id="9e395-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="9e395-112">若要避免記憶體流失，請在 *ppAnalysisHint* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="9e395-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHint* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="9e395-113">若要為 [**IInkAnalyzer**](iinkanalyzer.md)提供額外的內容資訊，您可以將分析提示加入至筆墨分析器。</span><span class="sxs-lookup"><span data-stu-id="9e395-113">To provide extra context information for the [**IInkAnalyzer**](iinkanalyzer.md), you can add analysis hints to the ink analyzer.</span></span> <span data-ttu-id="9e395-114">分析提示可以改善辨識的精確度。</span><span class="sxs-lookup"><span data-stu-id="9e395-114">Analysis hints can improve recognition accuracy.</span></span> <span data-ttu-id="9e395-115">例如，您可以在表單應用程式中加入欄位的「模擬」和「指南」資訊。</span><span class="sxs-lookup"><span data-stu-id="9e395-115">For example, you can add factoid and guide information for fields in a form application.</span></span>

<span data-ttu-id="9e395-116">這個方法會使用 AnalysisHint 的內容節點類型來建立新的 [**ICoNtextNode**](icontextnode.md) (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 並加入新的提示做為 [**IInkAnalyzer**](iinkanalyzer.md) 物件根節點的子節點 (請參閱 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md) 和 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md)) 。</span><span class="sxs-lookup"><span data-stu-id="9e395-116">This method creates a new [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md)) and adds the new hint as a subnode of the [**IInkAnalyzer**](iinkanalyzer.md) object's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

<span data-ttu-id="9e395-117">若要將內容資訊加入至提示，請使用 [**ICoNtextNode：： AddPropertyData**](icontextnode-addpropertydata.md) ，並將 *pPropertyDataId* 參數設定為其中一個 [分析提示屬性](analysis-hint-properties.md) 常數。</span><span class="sxs-lookup"><span data-stu-id="9e395-117">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="9e395-118">如果提示指派了一個無限區域（稱為全域提示），則 [**IInkAnalyzer**](iinkanalyzer.md) 會將提示的內容套用至不在另一個提示區域內的所有筆墨。</span><span class="sxs-lookup"><span data-stu-id="9e395-118">If a hint is assigned an infinite area, termed a global hint, the [**IInkAnalyzer**](iinkanalyzer.md) applies the hint's context to all ink that is not within another hint's area.</span></span> <span data-ttu-id="9e395-119">多個提示可能會附加至單一 **IInkAnalyzer**。</span><span class="sxs-lookup"><span data-stu-id="9e395-119">Multiple hints may be attached to a single **IInkAnalyzer**.</span></span> <span data-ttu-id="9e395-120">不過，只有一個全域提示可以附加至單一筆墨分析器，而且沒有任何非全域提示可以重迭。</span><span class="sxs-lookup"><span data-stu-id="9e395-120">However, only one global hint can be attached to a single ink analyzer, and no non-global hints can overlap.</span></span> <span data-ttu-id="9e395-121">如需有關提示可提供之內容資訊類型的詳細資訊，請參閱 [分析提示屬性](analysis-hint-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="9e395-121">For more information about the types of context information that a hint can provide, see [Analysis Hint Properties](analysis-hint-properties.md).</span></span>

<span data-ttu-id="9e395-122">新增分析提示並不會標示提示的區域以進行 reanalysis。</span><span class="sxs-lookup"><span data-stu-id="9e395-122">Adding an analysis hint does not mark the hint's area for reanalysis.</span></span> <span data-ttu-id="9e395-123">若要標記 reanalysis 提示內的區域，請使用 [**IInkAnalyzer：： SetDirtyRegion 方法**](iinkanalyzer-setdirtyregion.md) ，將中途區域設定為目前中途區域和分析提示區域的聯集。</span><span class="sxs-lookup"><span data-stu-id="9e395-123">To mark the area within the hint for reanalysis, use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to set the dirty region to the union of the current dirty region and area of the analysis hint.</span></span>

<span data-ttu-id="9e395-124">使用表單應用程式的提示時，應用程式應該避免在表單中混合文字內容與筆跡。</span><span class="sxs-lookup"><span data-stu-id="9e395-124">When using hints for a form application, the application should avoid mixing text context with ink in the forms.</span></span> <span data-ttu-id="9e395-125">這表示，不應該在分析樹狀結構中建立文字欄位名稱。</span><span class="sxs-lookup"><span data-stu-id="9e395-125">This means for example that text field names should not be created in the analysis tree.</span></span> <span data-ttu-id="9e395-126">提示的目的是要將筆墨與頁面上的區域產生關聯;任何文字內容會干擾這個筆墨與提示關聯。</span><span class="sxs-lookup"><span data-stu-id="9e395-126">Hints are meant to associate the ink to areas on pages; any text context interferes with this ink-to-hint association.</span></span> <span data-ttu-id="9e395-127">分析作業可能會在相同的書寫區域中合併筆跡和文字內容，這會使筆墨無法與提示區域相關聯。</span><span class="sxs-lookup"><span data-stu-id="9e395-127">The analysis operation may merge the ink and the text context in the same writing region which would prevent the ink from being associated with the hint area.</span></span>

<span data-ttu-id="9e395-128">如需筆跡分析的詳細資訊，請參閱 [筆墨分析總覽](ink-analysis-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="9e395-128">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e395-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e395-129">Requirements</span></span>



| <span data-ttu-id="9e395-130">需求</span><span class="sxs-lookup"><span data-stu-id="9e395-130">Requirement</span></span> | <span data-ttu-id="9e395-131">值</span><span class="sxs-lookup"><span data-stu-id="9e395-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e395-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e395-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9e395-133">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e395-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9e395-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e395-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9e395-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="9e395-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9e395-136">標頭</span><span class="sxs-lookup"><span data-stu-id="9e395-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e395-137"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="9e395-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9e395-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9e395-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e395-139"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e395-139"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9e395-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e395-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e395-141">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="9e395-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9e395-142">**ICoNtextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="9e395-142">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="9e395-143">**IInkAnalyzer：:D eleteAnalysisHint 方法**</span><span class="sxs-lookup"><span data-stu-id="9e395-143">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="9e395-144">**IInkAnalyzer：： GetAnalysisHints 方法**</span><span class="sxs-lookup"><span data-stu-id="9e395-144">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="9e395-145">**IInkAnalyzer：： GetAnalysisHintsByName 方法**</span><span class="sxs-lookup"><span data-stu-id="9e395-145">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="9e395-146">分析提示屬性</span><span class="sxs-lookup"><span data-stu-id="9e395-146">Analysis Hint Properties</span></span>](analysis-hint-properties.md)
</dt> <dt>

[<span data-ttu-id="9e395-147">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="9e395-147">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

