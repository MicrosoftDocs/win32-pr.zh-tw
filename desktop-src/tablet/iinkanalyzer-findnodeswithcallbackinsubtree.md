---
description: 抓取符合指定準則的所有 ICoNtextNode 物件，而且是指定之 ICoNtextNode 物件的子系。
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: 'IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBackInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6b4ba64cd9271158d49ddd72270d4e6f25538672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690591"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a><span data-ttu-id="ba98f-103">IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法</span><span class="sxs-lookup"><span data-stu-id="ba98f-103">IInkAnalyzer::FindNodesWithCallBackInSubTree method</span></span>

<span data-ttu-id="ba98f-104">抓取符合指定準則的所有 [**ICoNtextNode**](icontextnode.md) 物件，而且是指定之 **ICoNtextNode** 物件的子系。</span><span class="sxs-lookup"><span data-stu-id="ba98f-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects that match the specified criteria and are descendants of the specified **IContextNode** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba98f-105">語法</span><span class="sxs-lookup"><span data-stu-id="ba98f-105">Syntax</span></span>


```C++
HRESULT FindNodesWithCallBackInSubTree(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [in]  IContextNode             *pContextNodeToSearchFrom,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="ba98f-106">參數</span><span class="sxs-lookup"><span data-stu-id="ba98f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba98f-107">*pCriteria* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ba98f-107">*pCriteria* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba98f-108">用來評估 [**ICoNtextNode**](icontextnode.md)物件是否符合或失敗其指定準則的 [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md)物件。</span><span class="sxs-lookup"><span data-stu-id="ba98f-108">An [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) object that is used to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails its specified criteria.</span></span>

</dd> <dt>

<span data-ttu-id="ba98f-109">*pCoNtextNodeToSearchFrom* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ba98f-109">*pContextNodeToSearchFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba98f-110">要搜尋其子系的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="ba98f-110">The [**IContextNode**](icontextnode.md) object whose descendants are searched.</span></span>

</dd> <dt>

<span data-ttu-id="ba98f-111">*ppCoNtextNodesFound* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ba98f-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba98f-112">[**ICoNtextNodes**](icontextnodes.md)的指標，其中包含符合指定準則的所有節點。</span><span class="sxs-lookup"><span data-stu-id="ba98f-112">A pointer to the [**IContextNodes**](icontextnodes.md) containing all nodes that meet the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba98f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ba98f-113">Return value</span></span>

<span data-ttu-id="ba98f-114">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="ba98f-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ba98f-115">備註</span><span class="sxs-lookup"><span data-stu-id="ba98f-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ba98f-116">若要避免記憶體流失，請在 *ppCoNtextNodesFound* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="ba98f-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="ba98f-117">如果 [**IInkAnalyzer**](iinkanalyzer.md) 未包含 *pCoNtextNodeToSearchFrom* 節點，這個方法會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ba98f-117">If the [**IInkAnalyzer**](iinkanalyzer.md) does not contain the *pContextNodeToSearchFrom* node, this method returns an error code.</span></span>

<span data-ttu-id="ba98f-118">如果 [**IInkAnalyzer**](iinkanalyzer.md) 未包含這類 [**ICoNtextNode**](icontextnode.md)，則會傳回空的 [**ICoNtextNodes**](icontextnodes.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="ba98f-118">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba98f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba98f-119">Requirements</span></span>



| <span data-ttu-id="ba98f-120">需求</span><span class="sxs-lookup"><span data-stu-id="ba98f-120">Requirement</span></span> | <span data-ttu-id="ba98f-121">值</span><span class="sxs-lookup"><span data-stu-id="ba98f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba98f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba98f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ba98f-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba98f-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ba98f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba98f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ba98f-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="ba98f-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ba98f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ba98f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba98f-127"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="ba98f-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ba98f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ba98f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba98f-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba98f-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ba98f-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba98f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba98f-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ba98f-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ba98f-132">**IInkAnalyzer：： FindInkLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="ba98f-132">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="ba98f-133">**IInkAnalyzer：： FindInkLeafNodesForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="ba98f-133">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="ba98f-134">**IInkAnalyzer：： FindLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="ba98f-134">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="ba98f-135">**IInkAnalyzer：： FindNode 方法**</span><span class="sxs-lookup"><span data-stu-id="ba98f-135">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="ba98f-136">**IInkAnalyzer：： FindNodesOfType 方法**</span><span class="sxs-lookup"><span data-stu-id="ba98f-136">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="ba98f-137">**IInkAnalyzer：： FindNodesOfTypeForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="ba98f-137">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="ba98f-138">**IInkAnalyzer：： FindNodesOfTypeInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="ba98f-138">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="ba98f-139">**IInkAnalyzer：： FindNodesWithCallBack 方法**</span><span class="sxs-lookup"><span data-stu-id="ba98f-139">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="ba98f-140">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="ba98f-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

