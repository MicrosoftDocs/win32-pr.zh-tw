---
description: 在 IInkAnalyzer 藉由變更其父節點來移動 ICoNtextNode 物件之前發生。
ms.assetid: 91261270-aa7c-4f0a-a790-1b2bf322a3ad
title: '_IAnalysisProxyEvents：： CoNtextNodeReparenting 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeReparenting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 084f971edc5adce0845fc7e1c3ea6ea59a066bb0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106985828"
---
# <a name="_ianalysisproxyeventscontextnodereparenting-event"></a><span data-ttu-id="f4089-103">\_IAnalysisProxyEvents：： CoNtextNodeReparenting 事件</span><span class="sxs-lookup"><span data-stu-id="f4089-103">\_IAnalysisProxyEvents::ContextNodeReparenting event</span></span>

<span data-ttu-id="f4089-104">在 [**IInkAnalyzer**](iinkanalyzer.md) 藉由變更其父節點來移動 [**ICoNtextNode**](icontextnode.md) 物件之前發生。</span><span class="sxs-lookup"><span data-stu-id="f4089-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object by changing its parent node.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4089-105">語法</span><span class="sxs-lookup"><span data-stu-id="f4089-105">Syntax</span></span>


```C++
HRESULT ContextNodeReparenting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pNewParentContextNode,
  [in] IContextNode *pContextNodeToBeReparented
);
```



## <a name="parameters"></a><span data-ttu-id="f4089-106">參數</span><span class="sxs-lookup"><span data-stu-id="f4089-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4089-107">*pInkAnalyzer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f4089-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4089-108">移動 [**ICoNtextNode**](icontextnode.md)物件的 [**IInkAnalyzer**](iinkanalyzer.md)物件。</span><span class="sxs-lookup"><span data-stu-id="f4089-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="f4089-109">*pNewParentCoNtextNode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f4089-109">*pNewParentContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4089-110">新的父 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f4089-110">The new parent [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="f4089-111">*pCoNtextNodeToBeReparented* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f4089-111">*pContextNodeToBeReparented* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4089-112">要移動的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f4089-112">The [**IContextNode**](icontextnode.md) object to be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4089-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4089-113">Return value</span></span>

<span data-ttu-id="f4089-114">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="f4089-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f4089-115">備註</span><span class="sxs-lookup"><span data-stu-id="f4089-115">Remarks</span></span>

<span data-ttu-id="f4089-116">當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。</span><span class="sxs-lookup"><span data-stu-id="f4089-116">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="f4089-117">此事件發生于筆墨分析的協調階段，或為了回應將 [**ICoNtextNode**](icontextnode.md) 從一個子節點集合移至 (另一個子節點的方法，請參閱 [**ICoNtextNode：： GetParentNode**](icontextnode-getparentnode.md) 和 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md)) 。</span><span class="sxs-lookup"><span data-stu-id="f4089-117">This event occurs during the reconcile phase of ink analysis, or in response to a method that moves an [**IContextNode**](icontextnode.md) from one collection of subnodes to another (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span>

<span data-ttu-id="f4089-118">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="f4089-118">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4089-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4089-119">Requirements</span></span>



| <span data-ttu-id="f4089-120">需求</span><span class="sxs-lookup"><span data-stu-id="f4089-120">Requirement</span></span> | <span data-ttu-id="f4089-121">值</span><span class="sxs-lookup"><span data-stu-id="f4089-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4089-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4089-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f4089-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4089-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f4089-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4089-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f4089-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="f4089-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f4089-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f4089-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4089-127"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="f4089-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f4089-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f4089-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4089-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4089-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f4089-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4089-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4089-131">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="f4089-131">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="f4089-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="f4089-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="f4089-133">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="f4089-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f4089-134">**ICoNtextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="f4089-134">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="f4089-135">**ICoNtextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="f4089-135">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="f4089-136">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="f4089-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="f4089-137">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="f4089-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="f4089-138">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="f4089-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




