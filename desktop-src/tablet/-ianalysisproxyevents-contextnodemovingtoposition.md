---
description: 發生于 IInkAnalyzer 將 ICoNtextNode 物件移至其父節點的子節點集合內的新位置之前。
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: '_IAnalysisProxyEvents：： CoNtextNodeMovingToPosition 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeMovingToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 462e7428fb43fd998d769dd152e19f8109b04158
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106991398"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a><span data-ttu-id="69c09-103">\_IAnalysisProxyEvents：： CoNtextNodeMovingToPosition 事件</span><span class="sxs-lookup"><span data-stu-id="69c09-103">\_IAnalysisProxyEvents::ContextNodeMovingToPosition event</span></span>

<span data-ttu-id="69c09-104">發生于 [**IInkAnalyzer**](iinkanalyzer.md) 將 [**ICoNtextNode**](icontextnode.md) 物件移至其父節點的子節點集合內的新位置之前。</span><span class="sxs-lookup"><span data-stu-id="69c09-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object to a new position within its parent node's collection of subnodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="69c09-105">語法</span><span class="sxs-lookup"><span data-stu-id="69c09-105">Syntax</span></span>


```C++
HRESULT ContextNodeMovingToPosition(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pISubNodeToMove,
  [in] IContextNode *pParentContextNode,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a><span data-ttu-id="69c09-106">參數</span><span class="sxs-lookup"><span data-stu-id="69c09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69c09-107">*pInkAnalyzer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69c09-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69c09-108">移動 [**ICoNtextNode**](icontextnode.md)物件的 [**IInkAnalyzer**](iinkanalyzer.md)物件。</span><span class="sxs-lookup"><span data-stu-id="69c09-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="69c09-109">*pISubNodeToMove* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69c09-109">*pISubNodeToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69c09-110">要移動的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="69c09-110">The [**IContextNode**](icontextnode.md) object to move.</span></span>

</dd> <dt>

<span data-ttu-id="69c09-111">*pParentCoNtextNode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69c09-111">*pParentContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69c09-112">*PISubNodeToMove* 的父 [**ICoNtextNode**](icontextnode.md)物件。</span><span class="sxs-lookup"><span data-stu-id="69c09-112">The parent [**IContextNode**](icontextnode.md) object of *pISubNodeToMove*.</span></span>

</dd> <dt>

<span data-ttu-id="69c09-113">*ulNewIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69c09-113">*ulNewIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69c09-114">*PISubNodeToMove* 在其父節點的子節點集合中的新位置。</span><span class="sxs-lookup"><span data-stu-id="69c09-114">The new location of *pISubNodeToMove* in its parent node's collection of subnodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69c09-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="69c09-115">Return value</span></span>

<span data-ttu-id="69c09-116">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="69c09-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="69c09-117">備註</span><span class="sxs-lookup"><span data-stu-id="69c09-117">Remarks</span></span>

<span data-ttu-id="69c09-118">當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。</span><span class="sxs-lookup"><span data-stu-id="69c09-118">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="69c09-119">此事件發生于筆墨分析的協調階段，或為了回應在其父節點的子節點集合中移動 [**ICoNtextNode**](icontextnode.md) 的筆墨分析器方法 (參閱 [**ICoNtextNode：： GetParentNode**](icontextnode-getparentnode.md) 和 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md)) 。</span><span class="sxs-lookup"><span data-stu-id="69c09-119">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that moves an [**IContextNode**](icontextnode.md) within its parent node's collection of subnodes (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span>

<span data-ttu-id="69c09-120">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="69c09-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69c09-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="69c09-121">Requirements</span></span>



| <span data-ttu-id="69c09-122">需求</span><span class="sxs-lookup"><span data-stu-id="69c09-122">Requirement</span></span> | <span data-ttu-id="69c09-123">值</span><span class="sxs-lookup"><span data-stu-id="69c09-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69c09-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69c09-124">Minimum supported client</span></span><br/> | <span data-ttu-id="69c09-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69c09-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="69c09-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69c09-126">Minimum supported server</span></span><br/> | <span data-ttu-id="69c09-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="69c09-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="69c09-128">標頭</span><span class="sxs-lookup"><span data-stu-id="69c09-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="69c09-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="69c09-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="69c09-130">DLL</span><span class="sxs-lookup"><span data-stu-id="69c09-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69c09-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69c09-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="69c09-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69c09-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69c09-133">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="69c09-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="69c09-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="69c09-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="69c09-135">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="69c09-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="69c09-136">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="69c09-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="69c09-137">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="69c09-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="69c09-138">**ICoNtextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="69c09-138">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="69c09-139">**ICoNtextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="69c09-139">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="69c09-140">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="69c09-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




