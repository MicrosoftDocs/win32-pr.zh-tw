---
description: 抓取所有分葉節點。
ms.assetid: 5534053c-c5b9-4576-857f-c8af39e821a7
title: 'IInkAnalyzer：： FindLeafNodes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f923afe94c25e45dbcbfe79d554282b69ebec3a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511660"
---
# <a name="iinkanalyzerfindleafnodes-method"></a><span data-ttu-id="a3e2e-103">IInkAnalyzer：： FindLeafNodes 方法</span><span class="sxs-lookup"><span data-stu-id="a3e2e-103">IInkAnalyzer::FindLeafNodes method</span></span>

<span data-ttu-id="a3e2e-104">抓取所有分葉節點。</span><span class="sxs-lookup"><span data-stu-id="a3e2e-104">Retrieves all of the leaf nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e2e-105">語法</span><span class="sxs-lookup"><span data-stu-id="a3e2e-105">Syntax</span></span>


```C++
HRESULT FindLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="a3e2e-106">參數</span><span class="sxs-lookup"><span data-stu-id="a3e2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3e2e-107">*ppCoNtextNodesFound* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a3e2e-107">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e2e-108">[**ICoNtextNodes**](icontextnodes.md)集合的指標，其中包含所有分葉節點。</span><span class="sxs-lookup"><span data-stu-id="a3e2e-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all leaf nodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3e2e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3e2e-109">Return value</span></span>

<span data-ttu-id="a3e2e-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="a3e2e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a3e2e-111">備註</span><span class="sxs-lookup"><span data-stu-id="a3e2e-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a3e2e-112">若要避免記憶體流失，請在 *ppCoNtextNodesFound* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="a3e2e-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="a3e2e-113">分葉節點不包含子節點。</span><span class="sxs-lookup"><span data-stu-id="a3e2e-113">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="a3e2e-114">筆墨分葉節點的範例包括 InkWord、TextWord、Image、InkDrawing 和 InkBullet [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="a3e2e-114">Examples of ink leaf nodes are InkWord, TextWord, Image, InkDrawing, and InkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="a3e2e-115">如需詳細資訊，請參閱 [內容節點類型](context-node-types.md)。</span><span class="sxs-lookup"><span data-stu-id="a3e2e-115">For more information, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3e2e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3e2e-116">Requirements</span></span>



| <span data-ttu-id="a3e2e-117">需求</span><span class="sxs-lookup"><span data-stu-id="a3e2e-117">Requirement</span></span> | <span data-ttu-id="a3e2e-118">值</span><span class="sxs-lookup"><span data-stu-id="a3e2e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e2e-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3e2e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e2e-120">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3e2e-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a3e2e-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3e2e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a3e2e-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="a3e2e-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a3e2e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a3e2e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3e2e-124"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="a3e2e-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a3e2e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a3e2e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3e2e-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3e2e-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a3e2e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3e2e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e2e-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a3e2e-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a3e2e-129">**IInkAnalyzer：： FindInkLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="a3e2e-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="a3e2e-130">**IInkAnalyzer：： FindInkLeafNodesForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="a3e2e-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="a3e2e-131">**IInkAnalyzer：： FindNode 方法**</span><span class="sxs-lookup"><span data-stu-id="a3e2e-131">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="a3e2e-132">**IInkAnalyzer：： FindNodesOfType 方法**</span><span class="sxs-lookup"><span data-stu-id="a3e2e-132">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="a3e2e-133">**IInkAnalyzer：： FindNodesOfTypeForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="a3e2e-133">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="a3e2e-134">**IInkAnalyzer：： FindNodesOfTypeInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="a3e2e-134">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="a3e2e-135">**IInkAnalyzer：： FindNodesWithCallBack 方法**</span><span class="sxs-lookup"><span data-stu-id="a3e2e-135">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="a3e2e-136">**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="a3e2e-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="a3e2e-137">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="a3e2e-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

