---
description: 抓取包含指定筆劃的筆墨分葉節點。
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: 'IInkAnalyzer：： FindInkLeafNodesForStrokes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d19bed823f5385533dfc938eb9f6013b4a5640c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848078"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a><span data-ttu-id="2c176-103">IInkAnalyzer：： FindInkLeafNodesForStrokes 方法</span><span class="sxs-lookup"><span data-stu-id="2c176-103">IInkAnalyzer::FindInkLeafNodesForStrokes method</span></span>

<span data-ttu-id="2c176-104">抓取包含指定筆劃的筆墨分葉節點。</span><span class="sxs-lookup"><span data-stu-id="2c176-104">Retrieves the ink leaf nodes that contain the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c176-105">語法</span><span class="sxs-lookup"><span data-stu-id="2c176-105">Syntax</span></span>


```C++
HRESULT FindInkLeafNodesForStrokes(
  [in]  ULONG         ulStrokeIdsCount,
  [in]  LONG          *plStrokeIds,
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="2c176-106">參數</span><span class="sxs-lookup"><span data-stu-id="2c176-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c176-107">*ulStrokeIdsCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c176-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c176-108">傳入的筆觸識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="2c176-108">The number of stroke identifiers passed in.</span></span>

</dd> <dt>

<span data-ttu-id="2c176-109">*plStrokeIds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c176-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c176-110">筆觸識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="2c176-110">An array of the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="2c176-111">*ppCoNtextNodesFound* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2c176-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c176-112">[**ICoNtextNode**](icontextnode.md)物件的集合，其中包含包含 *plStrokeIds* 陣列中識別碼之筆觸的所有筆墨分葉節點。</span><span class="sxs-lookup"><span data-stu-id="2c176-112">The collection of [**IContextNode**](icontextnode.md) objects that contain all the ink leaf nodes that contain the strokes with identifiers in the *plStrokeIds* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c176-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c176-113">Return value</span></span>

<span data-ttu-id="2c176-114">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="2c176-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2c176-115">備註</span><span class="sxs-lookup"><span data-stu-id="2c176-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="2c176-116">若要避免記憶體流失，請在 *ppCoNtextNodesFound* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="2c176-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="2c176-117">分葉節點不包含子節點。</span><span class="sxs-lookup"><span data-stu-id="2c176-117">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="2c176-118">筆墨節點包含筆觸資料。</span><span class="sxs-lookup"><span data-stu-id="2c176-118">Ink nodes contain stroke data.</span></span> <span data-ttu-id="2c176-119">筆墨分葉節點的範例包括 InkWord、InkDrawing、andInkBullet [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="2c176-119">Examples of ink leaf nodes are InkWord, InkDrawing, andInkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="2c176-120">如需詳細資訊，請參閱 [內容節點類型](context-node-types.md)。</span><span class="sxs-lookup"><span data-stu-id="2c176-120">For more information, see [Context Node Types](context-node-types.md).</span></span>

<span data-ttu-id="2c176-121">如果沒有任何節點包含指定的筆觸，則會傳回空的 [**ICoNtextNodes**](icontextnodes.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="2c176-121">If no nodes contain the specified strokes, an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span> <span data-ttu-id="2c176-122">同樣地，如果 *ulStrokeIdsCount* 為零，則會傳回空的 **ICoNtextNodes** 集合。</span><span class="sxs-lookup"><span data-stu-id="2c176-122">Similarly, if *ulStrokeIdsCount* is zero, an empty **IContextNodes** collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c176-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c176-123">Requirements</span></span>



| <span data-ttu-id="2c176-124">需求</span><span class="sxs-lookup"><span data-stu-id="2c176-124">Requirement</span></span> | <span data-ttu-id="2c176-125">值</span><span class="sxs-lookup"><span data-stu-id="2c176-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c176-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c176-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2c176-127">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c176-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2c176-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c176-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2c176-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="2c176-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2c176-130">標頭</span><span class="sxs-lookup"><span data-stu-id="2c176-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c176-131"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="2c176-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2c176-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2c176-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c176-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c176-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2c176-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c176-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c176-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="2c176-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="2c176-136">**IInkAnalyzer：： FindInkLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="2c176-136">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="2c176-137">**IInkAnalyzer：： FindLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="2c176-137">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="2c176-138">**IInkAnalyzer：： FindNode 方法**</span><span class="sxs-lookup"><span data-stu-id="2c176-138">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="2c176-139">**IInkAnalyzer：： FindNodesOfType 方法**</span><span class="sxs-lookup"><span data-stu-id="2c176-139">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="2c176-140">**IInkAnalyzer：： FindNodesOfTypeForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="2c176-140">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="2c176-141">**IInkAnalyzer：： FindNodesOfTypeInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="2c176-141">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="2c176-142">**IInkAnalyzer：： FindNodesWithCallBack 方法**</span><span class="sxs-lookup"><span data-stu-id="2c176-142">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="2c176-143">**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="2c176-143">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="2c176-144">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="2c176-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

