---
description: 抓取所有筆墨分葉節點。
ms.assetid: 988ae9f9-8fca-4757-8eb0-ae161e5690c9
title: 'IInkAnalyzer：： FindInkLeafNodes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d5ebcfe542ab03f2e3d3a24c29142e41433c9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848080"
---
# <a name="iinkanalyzerfindinkleafnodes-method"></a><span data-ttu-id="d0173-103">IInkAnalyzer：： FindInkLeafNodes 方法</span><span class="sxs-lookup"><span data-stu-id="d0173-103">IInkAnalyzer::FindInkLeafNodes method</span></span>

<span data-ttu-id="d0173-104">抓取所有筆墨分葉節點。</span><span class="sxs-lookup"><span data-stu-id="d0173-104">Retrieves all of the ink leaf nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0173-105">語法</span><span class="sxs-lookup"><span data-stu-id="d0173-105">Syntax</span></span>


```C++
HRESULT FindInkLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="d0173-106">參數</span><span class="sxs-lookup"><span data-stu-id="d0173-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0173-107">*ppCoNtextNodesFound* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d0173-107">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0173-108">[**ICoNtextNodes**](icontextnodes.md)集合的指標，其中包含所有筆墨分葉節點。</span><span class="sxs-lookup"><span data-stu-id="d0173-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all ink leaf nodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0173-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0173-109">Return value</span></span>

<span data-ttu-id="d0173-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="d0173-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0173-111">備註</span><span class="sxs-lookup"><span data-stu-id="d0173-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="d0173-112">若要避免記憶體流失，請在 *ppCoNtextNodesFound* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="d0173-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="d0173-113">分葉節點不包含子節點。</span><span class="sxs-lookup"><span data-stu-id="d0173-113">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="d0173-114">筆墨節點包含筆觸資料。</span><span class="sxs-lookup"><span data-stu-id="d0173-114">Ink nodes contain stroke data.</span></span> <span data-ttu-id="d0173-115">筆墨分葉節點的範例包括 InkWord、InkDrawing 和 InkBullet [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d0173-115">Examples of ink leaf nodes are InkWord, InkDrawing, and InkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="d0173-116">如需詳細資訊，請參閱 [內容節點類型](context-node-types.md)。</span><span class="sxs-lookup"><span data-stu-id="d0173-116">For more information, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0173-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0173-117">Requirements</span></span>



| <span data-ttu-id="d0173-118">需求</span><span class="sxs-lookup"><span data-stu-id="d0173-118">Requirement</span></span> | <span data-ttu-id="d0173-119">值</span><span class="sxs-lookup"><span data-stu-id="d0173-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0173-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0173-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d0173-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0173-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d0173-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0173-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d0173-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="d0173-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d0173-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d0173-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0173-125"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="d0173-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d0173-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d0173-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0173-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0173-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d0173-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0173-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0173-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="d0173-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d0173-130">**IInkAnalyzer：： FindInkLeafNodesForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="d0173-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="d0173-131">**IInkAnalyzer：： FindLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="d0173-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="d0173-132">**IInkAnalyzer：： FindNode 方法**</span><span class="sxs-lookup"><span data-stu-id="d0173-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="d0173-133">**IInkAnalyzer：： FindNodesOfType 方法**</span><span class="sxs-lookup"><span data-stu-id="d0173-133">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="d0173-134">**IInkAnalyzer：： FindNodesOfTypeForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="d0173-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="d0173-135">**IInkAnalyzer：： FindNodesOfTypeInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="d0173-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="d0173-136">**IInkAnalyzer：： FindNodesWithCallBack 方法**</span><span class="sxs-lookup"><span data-stu-id="d0173-136">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="d0173-137">**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="d0173-137">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="d0173-138">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="d0173-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

