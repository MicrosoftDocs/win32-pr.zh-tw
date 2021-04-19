---
description: 指定與 IInkAnalyzer 物件的資料 proxy 步驟相關聯的事件。
ms.assetid: 57fee525-02e2-4721-b6e5-28112d53db2a
title: '_IAnalysisProxyEvents 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b83019cafb6053b9f803c815289d9f9f64d32a5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106992654"
---
# <a name="_ianalysisproxyevents-interface"></a><span data-ttu-id="71666-103">\_IAnalysisProxyEvents 介面</span><span class="sxs-lookup"><span data-stu-id="71666-103">\_IAnalysisProxyEvents interface</span></span>

<span data-ttu-id="71666-104">指定與 [**IInkAnalyzer**](iinkanalyzer.md) 物件的資料 proxy 步驟相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="71666-104">Specifies events associated with the data proxy steps of an [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>

-   [<span data-ttu-id="71666-105">事件</span><span class="sxs-lookup"><span data-stu-id="71666-105">Events</span></span>](/windows)

### <a name="events"></a><span data-ttu-id="71666-106">事件</span><span class="sxs-lookup"><span data-stu-id="71666-106">Events</span></span>

<span data-ttu-id="71666-107">**\_ IAnalysisProxyEvents** 介面具有這些事件。</span><span class="sxs-lookup"><span data-stu-id="71666-107">The **\_IAnalysisProxyEvents** interface has these events.</span></span>



| <span data-ttu-id="71666-108">事件</span><span class="sxs-lookup"><span data-stu-id="71666-108">Event</span></span>                                                                                      | <span data-ttu-id="71666-109">描述</span><span class="sxs-lookup"><span data-stu-id="71666-109">Description</span></span>                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71666-110">**CoNtextNodeCreated**</span><span class="sxs-lookup"><span data-stu-id="71666-110">**ContextNodeCreated**</span></span>](-ianalysisproxyevents-contextnodecreated.md)                     | <span data-ttu-id="71666-111">在 [**IInkAnalyzer**](iinkanalyzer.md) 建立 [**ICoNtextNode**](icontextnode.md) 物件之後發生。</span><span class="sxs-lookup"><span data-stu-id="71666-111">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                                                  |
| [<span data-ttu-id="71666-112">**CoNtextNodeDeleting**</span><span class="sxs-lookup"><span data-stu-id="71666-112">**ContextNodeDeleting**</span></span>](-ianalysisproxyevents-contextnodedeleting.md)                   | <span data-ttu-id="71666-113">在 [**IInkAnalyzer**](iinkanalyzer.md) 刪除 [**ICoNtextNode**](icontextnode.md) 物件之前發生。</span><span class="sxs-lookup"><span data-stu-id="71666-113">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                                                 |
| [<span data-ttu-id="71666-114">**CoNtextNodeLinkAdding**</span><span class="sxs-lookup"><span data-stu-id="71666-114">**ContextNodeLinkAdding**</span></span>](-ianalysisproxyevents-contextnodelinkadding.md)               | <span data-ttu-id="71666-115">在 [**IInkAnalyzer**](iinkanalyzer.md)于兩個 [**ICoNtextNode**](icontextnode.md)物件之間加入 [**ICoNtextLink**](icontextlink.md)物件之前發生。</span><span class="sxs-lookup"><span data-stu-id="71666-115">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) adds an [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>           |
| [<span data-ttu-id="71666-116">**CoNtextNodeLinkDeleting**</span><span class="sxs-lookup"><span data-stu-id="71666-116">**ContextNodeLinkDeleting**</span></span>](-ianalysisproxyevents-contextnodelinkdeleting.md)           | <span data-ttu-id="71666-117">在 [**IInkAnalyzer**](iinkanalyzer.md)刪除兩個 [**ICoNtextNode**](icontextnode.md)物件之間的 [**ICoNtextLink**](icontextlink.md)物件之前發生。</span><span class="sxs-lookup"><span data-stu-id="71666-117">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes a [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>         |
| [<span data-ttu-id="71666-118">**CoNtextNodeMovingToPosition**</span><span class="sxs-lookup"><span data-stu-id="71666-118">**ContextNodeMovingToPosition**</span></span>](-ianalysisproxyevents-contextnodemovingtoposition.md)   | <span data-ttu-id="71666-119">發生于 [**IInkAnalyzer**](iinkanalyzer.md) 將 [**ICoNtextNode**](icontextnode.md) 物件移至其父節點的子節點集合內的新位置之前。</span><span class="sxs-lookup"><span data-stu-id="71666-119">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object to a new position within its parent node's collection of subnodes.</span></span><br/> |
| [<span data-ttu-id="71666-120">**CoNtextNodePropertiesUpdated**</span><span class="sxs-lookup"><span data-stu-id="71666-120">**ContextNodePropertiesUpdated**</span></span>](-ianalysisproxyevents-contextnodepropertiesupdated.md) | <span data-ttu-id="71666-121">在 [**IInkAnalyzer**](iinkanalyzer.md) 更新 [**ICoNtextNode**](icontextnode.md) 物件的一或多個屬性之後發生。</span><span class="sxs-lookup"><span data-stu-id="71666-121">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) updates one or more properties of an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                        |
| [<span data-ttu-id="71666-122">**CoNtextNodeReparenting**</span><span class="sxs-lookup"><span data-stu-id="71666-122">**ContextNodeReparenting**</span></span>](-ianalysisproxyevents-contextnodereparenting.md)             | <span data-ttu-id="71666-123">在 [**IInkAnalyzer**](iinkanalyzer.md) 藉由變更其父節點來移動 [**ICoNtextNode**](icontextnode.md) 物件之前發生。</span><span class="sxs-lookup"><span data-stu-id="71666-123">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object by changing its parent node.</span></span><br/>                                       |
| [<span data-ttu-id="71666-124">**InkAnalyzerStateChanging**</span><span class="sxs-lookup"><span data-stu-id="71666-124">**InkAnalyzerStateChanging**</span></span>](-ianalysisproxyevents-inkanalyzerstatechanging.md)         | <span data-ttu-id="71666-125">發生于 [**IInkAnalyzer**](iinkanalyzer.md) 協調分析結果之前，讓應用程式可以與 **IInkAnalyzer** 同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="71666-125">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) reconciles analysis results so that an application can synchronize data with the **IInkAnalyzer**.</span></span><br/>                      |
| [<span data-ttu-id="71666-126">**PopulateCoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="71666-126">**PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)                   | <span data-ttu-id="71666-127">發生于 [**IInkAnalyzer**](iinkanalyzer.md) 在部分填入的 [**ICoNtextNode**](icontextnode.md) 物件區域內執行分析之前。</span><span class="sxs-lookup"><span data-stu-id="71666-127">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) performs analysis within the region of a partially populated [**IContextNode**](icontextnode.md) object.</span></span><br/>               |
| [<span data-ttu-id="71666-128">**StrokeReparented**</span><span class="sxs-lookup"><span data-stu-id="71666-128">**StrokeReparented**</span></span>](-ianalysisproxyevents-strokereparented.md)                         | <span data-ttu-id="71666-129">當 [**IInkAnalyzer**](iinkanalyzer.md) 將筆劃從一個 [**ICoNtextNode**](icontextnode.md) 物件移動到另一個時，就會發生。</span><span class="sxs-lookup"><span data-stu-id="71666-129">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) moves a stroke from one [**IContextNode**](icontextnode.md) object to another.</span></span><br/>                                           |



 

## <a name="remarks"></a><span data-ttu-id="71666-130">備註</span><span class="sxs-lookup"><span data-stu-id="71666-130">Remarks</span></span>

<span data-ttu-id="71666-131">當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用這些事件。</span><span class="sxs-lookup"><span data-stu-id="71666-131">Use these events when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="71666-132">如需有關同步處理應用程式資料與 **IInkAnalyzer** 的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="71666-132">For more information about synchronizing your application data with the **IInkAnalyzer**, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71666-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="71666-133">Requirements</span></span>



| <span data-ttu-id="71666-134">需求</span><span class="sxs-lookup"><span data-stu-id="71666-134">Requirement</span></span> | <span data-ttu-id="71666-135">值</span><span class="sxs-lookup"><span data-stu-id="71666-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71666-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71666-136">Minimum supported client</span></span><br/> | <span data-ttu-id="71666-137">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71666-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="71666-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71666-138">Minimum supported server</span></span><br/> | <span data-ttu-id="71666-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="71666-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="71666-140">標頭</span><span class="sxs-lookup"><span data-stu-id="71666-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="71666-141"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="71666-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="71666-142">DLL</span><span class="sxs-lookup"><span data-stu-id="71666-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71666-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71666-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="71666-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71666-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71666-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="71666-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="71666-146">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="71666-146">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="71666-147">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="71666-147">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="71666-148">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="71666-148">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="71666-149">\_IAnalysisEvents</span><span class="sxs-lookup"><span data-stu-id="71666-149">\_IAnalysisEvents</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="71666-150">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="71666-150">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

