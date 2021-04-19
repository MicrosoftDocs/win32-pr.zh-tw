---
description: 在 IInkAnalyzer 刪除 ICoNtextNode 物件之前發生。
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: '_IAnalysisProxyEvents：： CoNtextNodeDeleting 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 26488c5657b6d2765534f82b6eacae774adcf561
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106985825"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a><span data-ttu-id="fa487-103">\_IAnalysisProxyEvents：： CoNtextNodeDeleting 事件</span><span class="sxs-lookup"><span data-stu-id="fa487-103">\_IAnalysisProxyEvents::ContextNodeDeleting event</span></span>

<span data-ttu-id="fa487-104">在 [**IInkAnalyzer**](iinkanalyzer.md) 刪除 [**ICoNtextNode**](icontextnode.md) 物件之前發生。</span><span class="sxs-lookup"><span data-stu-id="fa487-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa487-105">語法</span><span class="sxs-lookup"><span data-stu-id="fa487-105">Syntax</span></span>


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a><span data-ttu-id="fa487-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa487-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa487-107">*pInkAnalyzer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa487-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa487-108">刪除 [**ICoNtextNode**](icontextnode.md)物件的 [**IInkAnalyzer**](iinkanalyzer.md)物件。</span><span class="sxs-lookup"><span data-stu-id="fa487-108">The [**IInkAnalyzer**](iinkanalyzer.md) object deleting the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="fa487-109">*pCoNtextNodeToBeDeleted* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa487-109">*pContextNodeToBeDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa487-110">要刪除的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="fa487-110">The [**IContextNode**](icontextnode.md) object to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa487-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa487-111">Return value</span></span>

<span data-ttu-id="fa487-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="fa487-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fa487-113">備註</span><span class="sxs-lookup"><span data-stu-id="fa487-113">Remarks</span></span>

<span data-ttu-id="fa487-114">當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。</span><span class="sxs-lookup"><span data-stu-id="fa487-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="fa487-115">此事件發生于筆墨分析的協調階段，或為了回應刪除 [**ICoNtextNode**](icontextnode.md)的筆墨分析器方法。</span><span class="sxs-lookup"><span data-stu-id="fa487-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that deletes an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="fa487-116">在 [**IInkAnalyzer**](iinkanalyzer.md) 刪除 [**ICoNtextNode**](icontextnode.md)之前， **IInkAnalyzer** 會移除內容節點的所有筆劃，並移除其他內容節點的所有連結。</span><span class="sxs-lookup"><span data-stu-id="fa487-116">Before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md), the **IInkAnalyzer** removes all of the strokes from the context node and removes all of the links to other context nodes.</span></span> <span data-ttu-id="fa487-117">在移除內容節點之前， **IInkAnalyzer** 可能會引發下列事件。</span><span class="sxs-lookup"><span data-stu-id="fa487-117">Before the context node is removed, the **IInkAnalyzer** may raise the following events.</span></span>

-   <span data-ttu-id="fa487-118">[**\_ IAnalysisProxyEvents：： StrokeReparented**](-ianalysisproxyevents-strokereparented.md)事件從 [**ICoNtextNode**](icontextnode.md)移動筆劃時。</span><span class="sxs-lookup"><span data-stu-id="fa487-118">The [**\_IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) event when it moves a stroke from the [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="fa487-119">[**\_ IAnalysisProxyEvents：： CoNtextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)事件會先從 [**ICoNtextNode**](icontextnode.md)移除 [**ICoNtextLink**](icontextlink.md) 。</span><span class="sxs-lookup"><span data-stu-id="fa487-119">The [**\_IAnalysisProxyEvents::ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) event before it removes a [**IContextLink**](icontextlink.md) from the [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="fa487-120">**\_ IAnalysisProxyEvents：： CoNtextNodeDeleting** 事件在移除不再具有子節點的父內容節點之前。</span><span class="sxs-lookup"><span data-stu-id="fa487-120">The **\_IAnalysisProxyEvents::ContextNodeDeleting** event before it removes a parent context node that no longer has child nodes.</span></span>

<span data-ttu-id="fa487-121">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="fa487-121">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa487-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa487-122">Requirements</span></span>



| <span data-ttu-id="fa487-123">需求</span><span class="sxs-lookup"><span data-stu-id="fa487-123">Requirement</span></span> | <span data-ttu-id="fa487-124">值</span><span class="sxs-lookup"><span data-stu-id="fa487-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa487-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa487-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fa487-126">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa487-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fa487-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa487-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fa487-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="fa487-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fa487-129">標頭</span><span class="sxs-lookup"><span data-stu-id="fa487-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa487-130"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="fa487-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fa487-131">DLL</span><span class="sxs-lookup"><span data-stu-id="fa487-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa487-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa487-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fa487-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa487-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa487-134">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="fa487-134">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="fa487-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="fa487-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="fa487-136">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="fa487-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="fa487-137">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="fa487-137">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="fa487-138">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="fa487-138">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="fa487-139">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="fa487-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




