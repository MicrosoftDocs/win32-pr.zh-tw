---
description: 如同筆跡分析總覽中所述，筆墨分析技術會在內部維護以樹狀結構為基礎的檔模型，以包含分析結果和關聯性。
ms.assetid: 33ba9292-3bc7-41ba-a602-e2fc94cd3a57
title: 具有筆跡分析的資料 Proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52717b955625e67f50c20703dd0e84449aa1037f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852183"
---
# <a name="data-proxy-with-ink-analysis"></a><span data-ttu-id="f01df-103">具有筆跡分析的資料 Proxy</span><span class="sxs-lookup"><span data-stu-id="f01df-103">Data Proxy with Ink Analysis</span></span>

<span data-ttu-id="f01df-104">如同 [筆跡分析總覽](ink-analysis-overview.md)中所述，筆墨分析技術會在內部維護以樹狀結構為基礎的檔模型，以包含分析結果和關聯性。</span><span class="sxs-lookup"><span data-stu-id="f01df-104">As mentioned in [Ink Analysis Overview](ink-analysis-overview.md), the ink analysis technology internally maintains a tree-based document model to contain analysis results and relationships.</span></span> <span data-ttu-id="f01df-105">如果您的應用程式已經建立不同的檔存放區，您將需要使用針對不同檔模型之間的 proxy 資料而設計的筆墨分析功能。</span><span class="sxs-lookup"><span data-stu-id="f01df-105">If your application already has an established document store that is different, you will need to make use of the ink analysis features designed to proxy data between disparate document models.</span></span>

## <a name="types-of-data-proxy"></a><span data-ttu-id="f01df-106">資料 Proxy 的類型</span><span class="sxs-lookup"><span data-stu-id="f01df-106">Types of Data Proxy</span></span>

<span data-ttu-id="f01df-107">資料 proxy 功能可讓您的應用程式：</span><span class="sxs-lookup"><span data-stu-id="f01df-107">The data proxy features enable your application to:</span></span>

-   <span data-ttu-id="f01df-108">將分析結果資料整合回現有的檔模型。</span><span class="sxs-lookup"><span data-stu-id="f01df-108">Integrate analysis results data back into an existing document model.</span></span>
-   <span data-ttu-id="f01df-109">將 (或狀態) 的先前結果傳達回 [**InkAnalyzer**](inkanalyzer.md)。</span><span class="sxs-lookup"><span data-stu-id="f01df-109">Communicate previous results (or state) back into the [**InkAnalyzer**](inkanalyzer.md).</span></span>
-   <span data-ttu-id="f01df-110">將非筆墨狀態傳達給 [**InkAnalyzer**](inkanalyzer.md)。</span><span class="sxs-lookup"><span data-stu-id="f01df-110">Communicate non-ink state into the [**InkAnalyzer**](inkanalyzer.md).</span></span>
-   <span data-ttu-id="f01df-111">只會將最小的資料集 () 所需的最小資料集與非筆墨狀態進行通訊，以完成分析作業。</span><span class="sxs-lookup"><span data-stu-id="f01df-111">Communicate only the minimum set of data (both previous and non-ink state) needed to complete the analysis operation.</span></span>
-   <span data-ttu-id="f01df-112">流量分析結果輕鬆更新內部應用程式檔模型。</span><span class="sxs-lookup"><span data-stu-id="f01df-112">Easily update the internal application document model with analysis results.</span></span>

<span data-ttu-id="f01df-113">筆墨分析資料 proxy 有兩種基本方法。</span><span class="sxs-lookup"><span data-stu-id="f01df-113">There are two basic approaches to ink analysis data proxy.</span></span> <span data-ttu-id="f01df-114">這些差異會在檔模型之間進行同步處理的時間和方式的詳細資料中進行版面配置。</span><span class="sxs-lookup"><span data-stu-id="f01df-114">The differences lay in the details of when and how the synchronization between the document models occurs.</span></span> <span data-ttu-id="f01df-115">第一個方法（同步更新）需要在應用程式檔中進行變更時修改筆墨分析檔模型。</span><span class="sxs-lookup"><span data-stu-id="f01df-115">The first approach, synchronous update, requires the modification of the ink analysis document model as changes occur in the application document.</span></span> <span data-ttu-id="f01df-116">第二種方法是隨選更新，只需要將應用程式檔模型變更所影響的資料傳遞給 [**InkAnalyzer**](inkanalyzer.md)。</span><span class="sxs-lookup"><span data-stu-id="f01df-116">The second approach, on-demand update, requires only the data affected by changes to the application document model to be passed to the [**InkAnalyzer**](inkanalyzer.md).</span></span> <span data-ttu-id="f01df-117">也就是說，只有筆跡分析檔模型中的資料，與應用程式檔的修改相同區域中的資料，必須在需要時傳遞給 **InkAnalyzer** 。</span><span class="sxs-lookup"><span data-stu-id="f01df-117">That is, only the data for the parts of the Ink Analysis document model that are in the same area as modifications to the application document need be passed to the **InkAnalyzer** as it needs them.</span></span>

### <a name="synchronous-update"></a><span data-ttu-id="f01df-118">同步更新</span><span class="sxs-lookup"><span data-stu-id="f01df-118">Synchronous Update</span></span>

<span data-ttu-id="f01df-119">同步更新方法需要在 [**InkAnalyzer**](inkanalyzer.md) 物件的 [**CoNtextNode**](icontextnode.md) 物件集合中，修改 (建立和刪除節點的) ，因為它們會在應用程式檔中發生。</span><span class="sxs-lookup"><span data-stu-id="f01df-119">The synchronous update approach requires the modification (creation and deletion) of nodes in the [**InkAnalyzer**](inkanalyzer.md) object's collection of [**ContextNode**](icontextnode.md) objects as they occur in the application document.</span></span> <span data-ttu-id="f01df-120">例如，每次將文字單字加入至應用程式時，就會在 **InkAnalyzer** 中建立對應的 **TextWord** 樣式 **CoNtextNode** 。</span><span class="sxs-lookup"><span data-stu-id="f01df-120">For example, each time a text word is added to the application, a corresponding **TextWord** styled **ContextNode** is created in the **InkAnalyzer**.</span></span> <span data-ttu-id="f01df-121">如果頁面上文字文字的位置變更，則會同時更新對應 **CoNtextNode** 的位置。</span><span class="sxs-lookup"><span data-stu-id="f01df-121">If the location of the text word on the page changes, then the location of the corresponding **ContextNode** is updated at the same time.</span></span> <span data-ttu-id="f01df-122">這種方法比隨選方法更有效率，因為每個檔變更都牽涉到 **InkAnalyzer** 的更新，即使變更不會影響正在分析的筆跡。</span><span class="sxs-lookup"><span data-stu-id="f01df-122">This method is less efficient in terms of computing resources than the on-demand method because every document change involves an update to the **InkAnalyzer**, even if the change does not affect the ink being analyzed.</span></span>

<span data-ttu-id="f01df-123">下列範例旨在示範同步更新的運作方式。</span><span class="sxs-lookup"><span data-stu-id="f01df-123">The following example is meant to show how synchronous update works.</span></span> <span data-ttu-id="f01df-124">想像一下具有現有檔模型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f01df-124">Imagine an application that has an existing document model.</span></span> <span data-ttu-id="f01df-125">當使用者對檔進行變更（例如新增文字）時，變更會以下列方式處理：</span><span class="sxs-lookup"><span data-stu-id="f01df-125">When the end-user makes a change to the document, such as adding new text, the change is processed as follows:</span></span>

1.  <span data-ttu-id="f01df-126">終端使用者會建立新的資料。</span><span class="sxs-lookup"><span data-stu-id="f01df-126">The end user creates the new data.</span></span>
2.  <span data-ttu-id="f01df-127">應用程式會決定如何處理資料、儲存資料，以及呈現資料。</span><span class="sxs-lookup"><span data-stu-id="f01df-127">The application determines how to process the data, stores it, and renders it.</span></span>
3.  <span data-ttu-id="f01df-128">針對實際用途，下列步驟會同時進行。</span><span class="sxs-lookup"><span data-stu-id="f01df-128">For practical purposes, the following steps take place simultaneously.</span></span>
    1.  <span data-ttu-id="f01df-129">應用程式會將資料放入其檔模型。</span><span class="sxs-lookup"><span data-stu-id="f01df-129">The application places the data into its document model.</span></span>
    2.  <span data-ttu-id="f01df-130">應用程式會建立 [**InkAnalyzer**](inkanalyzer.md) 並加以更新。</span><span class="sxs-lookup"><span data-stu-id="f01df-130">The application creates an [**InkAnalyzer**](inkanalyzer.md) and updates it.</span></span> <span data-ttu-id="f01df-131">這麼做可同時確保 **InkAnalyzer** 一律具有最新的資訊。</span><span class="sxs-lookup"><span data-stu-id="f01df-131">Doing this simultaneously assures that the **InkAnalyzer** always has the most recent information.</span></span>
    3.  <span data-ttu-id="f01df-132">應用程式會在 [**InkAnalyzer**](inkanalyzer.md)上呼叫 [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)來開始分析。</span><span class="sxs-lookup"><span data-stu-id="f01df-132">The application calls [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) on the [**InkAnalyzer**](inkanalyzer.md) to begin analysis.</span></span>
4.  <span data-ttu-id="f01df-133">如果變更牽涉到筆跡，而 [**InkAnalyzer**](inkanalyzer.md) 決定新的結果，則會引發一連串的事件。</span><span class="sxs-lookup"><span data-stu-id="f01df-133">A series of events is fired if the change involves ink and the [**InkAnalyzer**](inkanalyzer.md) determines new results.</span></span> <span data-ttu-id="f01df-134">針對 **InkAnalyzer** 中 [**CoNtextNode**](icontextnode.md)物件的集合所做的每項變更，會引發一個事件。</span><span class="sxs-lookup"><span data-stu-id="f01df-134">One event is fired for each change made to the collection of [**ContextNode**](icontextnode.md) objects in the **InkAnalyzer**.</span></span> <span data-ttu-id="f01df-135">這些事件包括 [**CoNtextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md)、 [**CoNtextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md)、 [**CoNtextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)、 [**CoNtextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md)、 [**CoNtextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)、 [**CoNtextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)和 [**CoNtextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)。</span><span class="sxs-lookup"><span data-stu-id="f01df-135">These events include [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md), [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md), [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md), [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md), [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md), and [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md).</span></span> <span data-ttu-id="f01df-136">應用程式會處理這些事件，以適當地將分析作業的結果 proxy 回檔模型。</span><span class="sxs-lookup"><span data-stu-id="f01df-136">The application handles these events to proxy the results of the analysis operation back into the document model as appropriate.</span></span>
5.  <span data-ttu-id="f01df-137">應用程式會更新檔的版面配置，從檔模型中提取新的資料。</span><span class="sxs-lookup"><span data-stu-id="f01df-137">The application updates the layout of the document, pulling the new data from the document model.</span></span>
6.  <span data-ttu-id="f01df-138">新的資料會轉譯回給終端使用者。</span><span class="sxs-lookup"><span data-stu-id="f01df-138">The new data is rendered back to the end user.</span></span>

### <a name="on-demand-update"></a><span data-ttu-id="f01df-139">隨選更新</span><span class="sxs-lookup"><span data-stu-id="f01df-139">On-Demand Update</span></span>

<span data-ttu-id="f01df-140">隨選方法只需要針對正在分析之區域中的那些 [**CoNtextNode**](icontextnode.md) 物件傳遞資料。</span><span class="sxs-lookup"><span data-stu-id="f01df-140">The on-demand approach only requires the data to be passed for those [**ContextNode**](icontextnode.md) objects that are in the areas that are being analyzed.</span></span> <span data-ttu-id="f01df-141">所需的 **CoNtextNode** 物件是在叫用分析作業之後，以及在協調結果之前，從應用程式的檔模型中解壓縮。</span><span class="sxs-lookup"><span data-stu-id="f01df-141">The needed **ContextNode** objects are extracted from the application's document model just after the analysis operation is invoked, and again just prior to reconciling the results.</span></span> <span data-ttu-id="f01df-142">比起同步更新更複雜的是，此方法會產生較佳的效能結果。</span><span class="sxs-lookup"><span data-stu-id="f01df-142">While more complicated to implement than synchronous updates, this approach yields better performance results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f01df-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="f01df-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f01df-144">筆墨分析總覽</span><span class="sxs-lookup"><span data-stu-id="f01df-144">Ink Analysis Overview</span></span>](ink-analysis-overview.md)
</dt> <dt>

[<span data-ttu-id="f01df-145">**InkAnalyzer 類別 (c + +)**</span><span class="sxs-lookup"><span data-stu-id="f01df-145">**InkAnalyzer Class (C++)**</span></span>](inkanalyzer.md)
</dt> <dt>

<span data-ttu-id="f01df-146">[**InkAnalyzer**](/previous-versions/ms583671(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="f01df-146">[**Microsoft.Ink.InkAnalyzer**](/previous-versions/ms583671(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="f01df-147">[**CoNtextNode**](/previous-versions/ms551996(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="f01df-147">[**Microsoft.Ink.ContextNode**](/previous-versions/ms551996(v=vs.100))</span></span>
</dt> </dl>

 

 
