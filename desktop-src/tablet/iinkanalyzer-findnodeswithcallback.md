---
description: 抓取符合指定準則的所有 ICoNtextNode 物件。
ms.assetid: c0ba46f4-a286-454a-8de2-6663fd2dfed6
title: 'IInkAnalyzer：： FindNodesWithCallBack 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b34501e33d637ca65f13e6e2e5ea0a9001b06198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690592"
---
# <a name="iinkanalyzerfindnodeswithcallback-method"></a><span data-ttu-id="dd69d-103">IInkAnalyzer：： FindNodesWithCallBack 方法</span><span class="sxs-lookup"><span data-stu-id="dd69d-103">IInkAnalyzer::FindNodesWithCallBack method</span></span>

<span data-ttu-id="dd69d-104">抓取符合指定準則的所有 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="dd69d-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects that match the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd69d-105">語法</span><span class="sxs-lookup"><span data-stu-id="dd69d-105">Syntax</span></span>


```C++
HRESULT FindNodesWithCallBack(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="dd69d-106">參數</span><span class="sxs-lookup"><span data-stu-id="dd69d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd69d-107">*pCriteria* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dd69d-107">*pCriteria* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd69d-108">用來評估 [**ICoNtextNode**](icontextnode.md)物件是否符合或失敗其指定準則的 [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md)物件。</span><span class="sxs-lookup"><span data-stu-id="dd69d-108">An [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) object that is used to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails its specified criteria.</span></span>

</dd> <dt>

<span data-ttu-id="dd69d-109">*ppCoNtextNodesFound* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dd69d-109">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd69d-110">[**ICoNtextNodes**](icontextnodes.md)集合的指標，其中包含符合指定準則的所有節點。</span><span class="sxs-lookup"><span data-stu-id="dd69d-110">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all nodes that meet the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd69d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="dd69d-111">Return value</span></span>

<span data-ttu-id="dd69d-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="dd69d-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dd69d-113">備註</span><span class="sxs-lookup"><span data-stu-id="dd69d-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="dd69d-114">若要避免記憶體流失，請在 ppCoNtextNodesFound 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （ \* 當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="dd69d-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="dd69d-115">如果 [**IInkAnalyzer**](iinkanalyzer.md) 未包含這類 [**ICoNtextNode**](icontextnode.md)，則會傳回空的 [**ICoNtextNodes**](icontextnodes.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="dd69d-115">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd69d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd69d-116">Requirements</span></span>



| <span data-ttu-id="dd69d-117">需求</span><span class="sxs-lookup"><span data-stu-id="dd69d-117">Requirement</span></span> | <span data-ttu-id="dd69d-118">值</span><span class="sxs-lookup"><span data-stu-id="dd69d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd69d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dd69d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dd69d-120">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd69d-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dd69d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dd69d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dd69d-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="dd69d-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="dd69d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="dd69d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd69d-124"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="dd69d-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dd69d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dd69d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd69d-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd69d-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="dd69d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd69d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd69d-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="dd69d-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="dd69d-129">**IInkAnalyzer：： FindInkLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="dd69d-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="dd69d-130">**IInkAnalyzer：： FindInkLeafNodesForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="dd69d-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="dd69d-131">**IInkAnalyzer：： FindLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="dd69d-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="dd69d-132">**IInkAnalyzer：： FindNode 方法**</span><span class="sxs-lookup"><span data-stu-id="dd69d-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="dd69d-133">**IInkAnalyzer：： FindNodesOfType 方法**</span><span class="sxs-lookup"><span data-stu-id="dd69d-133">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="dd69d-134">**IInkAnalyzer：： FindNodesOfTypeForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="dd69d-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="dd69d-135">**IInkAnalyzer：： FindNodesOfTypeInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="dd69d-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="dd69d-136">**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="dd69d-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="dd69d-137">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="dd69d-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

