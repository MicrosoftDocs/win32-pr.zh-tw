---
description: 在 IInkAnalyzer 建立 ICoNtextNode 物件之後發生。
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: '_IAnalysisProxyEvents：： CoNtextNodeCreated 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeCreated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac06a7fc45604e93408b1bb144ee7e884efd351e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103945737"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a><span data-ttu-id="63453-103">\_IAnalysisProxyEvents：： CoNtextNodeCreated 事件</span><span class="sxs-lookup"><span data-stu-id="63453-103">\_IAnalysisProxyEvents::ContextNodeCreated event</span></span>

<span data-ttu-id="63453-104">在 [**IInkAnalyzer**](iinkanalyzer.md) 建立 [**ICoNtextNode**](icontextnode.md) 物件之後發生。</span><span class="sxs-lookup"><span data-stu-id="63453-104">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="63453-105">語法</span><span class="sxs-lookup"><span data-stu-id="63453-105">Syntax</span></span>


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="63453-106">參數</span><span class="sxs-lookup"><span data-stu-id="63453-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63453-107">*pInkAnalyzer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="63453-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63453-108">建立 [**ICoNtextNode**](icontextnode.md)物件的 [**IInkAnalyzer**](iinkanalyzer.md) 。</span><span class="sxs-lookup"><span data-stu-id="63453-108">The [**IInkAnalyzer**](iinkanalyzer.md) creating the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="63453-109">*pCoNtextNodeCreated* \[在\]</span><span class="sxs-lookup"><span data-stu-id="63453-109">*pContextNodeCreated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63453-110">新的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="63453-110">The new [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63453-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="63453-111">Return value</span></span>

<span data-ttu-id="63453-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="63453-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="63453-113">備註</span><span class="sxs-lookup"><span data-stu-id="63453-113">Remarks</span></span>

<span data-ttu-id="63453-114">當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。</span><span class="sxs-lookup"><span data-stu-id="63453-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="63453-115">此事件發生于筆墨分析的協調階段，或為了回應建立 [**ICoNtextNode**](icontextnode.md)的筆墨分析器方法。</span><span class="sxs-lookup"><span data-stu-id="63453-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that creates an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="63453-116">當 [**IInkAnalyzer**](iinkanalyzer.md) 建立 [**ICoNtextNode**](icontextnode.md)時，新的 **ICoNtextNode** 不會包含任何筆觸、不包含其他 **ICoNtextNode** 物件的連結，而且可能不會設定其所有屬性。</span><span class="sxs-lookup"><span data-stu-id="63453-116">When the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md), the new **IContextNode** does not contain any strokes, does not contain links to other **IContextNode** objects, and may not have all of its properties set.</span></span> <span data-ttu-id="63453-117">此外，新的 **ICoNtextNode** 會加入至其父節點的子節點集合結尾 (請參閱 [**ICoNtextNode：： GetParentNode**](icontextnode-getparentnode.md) 和 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md)) 。</span><span class="sxs-lookup"><span data-stu-id="63453-117">Also, the new **IContextNode** is added to the end of its parent node's collection of subnodes (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="63453-118">在這個事件之後， **IInkAnalyzer** 可能會引發下列事件。</span><span class="sxs-lookup"><span data-stu-id="63453-118">After this event, the **IInkAnalyzer** may raise the following events.</span></span>

-   <span data-ttu-id="63453-119">[**\_ IAnalysisProxyEvents：： StrokeReparented**](-ianalysisproxyevents-strokereparented.md)事件將筆劃從某個內容節點移至另一個內容節點時。</span><span class="sxs-lookup"><span data-stu-id="63453-119">The [**\_IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) event when it moves a stroke from one context node to another.</span></span>
-   <span data-ttu-id="63453-120">[**\_ IAnalysisProxyEvents：： CoNtextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)事件將 [**ICoNtextLink**](icontextlink.md)加入 [**ICoNtextNode**](icontextnode.md)時的事件。</span><span class="sxs-lookup"><span data-stu-id="63453-120">The [**\_IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) event when it adds an [**IContextLink**](icontextlink.md) to an [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="63453-121">[**\_ IAnalysisProxyEvents：： CoNtextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)事件，它會在其父節點的子節點集合中變更 [**ICoNtextNode**](icontextnode.md)的順序。</span><span class="sxs-lookup"><span data-stu-id="63453-121">The [**\_IAnalysisProxyEvents::ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) event when it changes the order of an [**IContextNode**](icontextnode.md) within its parent node's collection of subnodes.</span></span>
-   <span data-ttu-id="63453-122">[**IInkAnalyzer**](iinkanalyzer.md)在解析此分析階段的 [**ICoNtextNode**](icontextnode.md)狀態之後，會引發 [**\_ IAnalysisProxyEvents：： CoNtextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md)事件。</span><span class="sxs-lookup"><span data-stu-id="63453-122">The [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) event after it resolves the state of the [**IContextNode**](icontextnode.md) for this analysis phase.</span></span>

<span data-ttu-id="63453-123">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="63453-123">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="63453-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="63453-124">Requirements</span></span>



| <span data-ttu-id="63453-125">需求</span><span class="sxs-lookup"><span data-stu-id="63453-125">Requirement</span></span> | <span data-ttu-id="63453-126">值</span><span class="sxs-lookup"><span data-stu-id="63453-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63453-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63453-127">Minimum supported client</span></span><br/> | <span data-ttu-id="63453-128">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63453-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="63453-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63453-129">Minimum supported server</span></span><br/> | <span data-ttu-id="63453-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="63453-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="63453-131">標頭</span><span class="sxs-lookup"><span data-stu-id="63453-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="63453-132"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="63453-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="63453-133">DLL</span><span class="sxs-lookup"><span data-stu-id="63453-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63453-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63453-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="63453-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63453-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63453-136">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="63453-136">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="63453-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="63453-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="63453-138">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="63453-138">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="63453-139">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="63453-139">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="63453-140">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="63453-140">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="63453-141">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="63453-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




