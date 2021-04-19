---
description: 管理影片編輯專案
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: 管理影片編輯專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491cfcb9a6e94874d2cae43567b61666bbd43cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970879"
---
# <a name="managing-video-editing-projects"></a><span data-ttu-id="a296b-103">管理影片編輯專案</span><span class="sxs-lookup"><span data-stu-id="a296b-103">Managing Video Editing Projects</span></span>

<span data-ttu-id="a296b-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a296b-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="a296b-105">下列秘訣可協助您管理 [DirectShow 編輯服務](directshow-editing-services.md)中的專案。</span><span class="sxs-lookup"><span data-stu-id="a296b-105">The following tips will help you to manage projects in [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="a296b-106">變更至時間軸</span><span class="sxs-lookup"><span data-stu-id="a296b-106">Changes to the Timeline</span></span>

-   <span data-ttu-id="a296b-107">如果您在建立篩選圖形之後變更時間軸，請再次呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 來重建前端。</span><span class="sxs-lookup"><span data-stu-id="a296b-107">If you change the timeline after you build the filter graph, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) again to rebuild the front end.</span></span> <span data-ttu-id="a296b-108">這通常不會影響圖形的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="a296b-108">Usually, this does not affect the rest of the graph.</span></span> <span data-ttu-id="a296b-109">不過，有時候轉譯引擎必須先刪除整個圖形，才能重建前端。</span><span class="sxs-lookup"><span data-stu-id="a296b-109">Occasionally, however, the render engine needs to delete the entire graph before it rebuilds the front end.</span></span> <span data-ttu-id="a296b-110"> (例如，如果您新增或移除群組，就會發生這種情況。 ) **ConnectFrontEnd** 方法會傳回 S \_ 警告 \_ OUTPUTRESET，表示它刪除了圖形。</span><span class="sxs-lookup"><span data-stu-id="a296b-110">(For example, this happens if you add or remove a group.) The **ConnectFrontEnd** method returns S\_WARN\_OUTPUTRESET to signal that it deleted the graph.</span></span> <span data-ttu-id="a296b-111">如果發生這種情況，您的應用程式必須重建圖形的呈現區段。</span><span class="sxs-lookup"><span data-stu-id="a296b-111">If this happens, your application must rebuild the rendering section of the graph.</span></span>
-   <span data-ttu-id="a296b-112">若要從時間軸完全移除所有物件，請呼叫 [**IAMTimeline：： ClearAllGroups**](iamtimeline-clearallgroups.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a296b-112">To remove all objects completely from the timeline, call the [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md) method.</span></span>

<span data-ttu-id="a296b-113">**清除**</span><span class="sxs-lookup"><span data-stu-id="a296b-113">**Cleanup**</span></span>

-   <span data-ttu-id="a296b-114">當您完成使用轉譯引擎時，請呼叫 [**IRenderEngine：： ScrapIt**](irenderengine-scrapit.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a296b-114">When you are finished using a render engine, call the [**IRenderEngine::ScrapIt**](irenderengine-scrapit.md) method.</span></span> <span data-ttu-id="a296b-115">就像任何 COM 物件一樣，當您使用完介面指標時，請務必釋放每個介面指標。</span><span class="sxs-lookup"><span data-stu-id="a296b-115">As with any COM object, be sure to release every interface pointer when you are finished using it.</span></span>
-   <span data-ttu-id="a296b-116">轉譯引擎不會在時間軸上保留參考計數。</span><span class="sxs-lookup"><span data-stu-id="a296b-116">The render engine does not keep a reference count on the timeline.</span></span> <span data-ttu-id="a296b-117">請勿在使用完成之前釋出時程表，而且一律先在轉譯引擎上呼叫 **ScrapIt** 。</span><span class="sxs-lookup"><span data-stu-id="a296b-117">Do not release the timeline before you are done using it, and always call **ScrapIt** on the render engine first.</span></span>
-   <span data-ttu-id="a296b-118">如果您釋出時間軸的所有參考，請勿使用該時間軸中的任何物件，即使您持有它們的參考計數也一樣。</span><span class="sxs-lookup"><span data-stu-id="a296b-118">If you release all references to a timeline, do not use any of the objects in that timeline, even if you are holding reference counts on them.</span></span>

<span data-ttu-id="a296b-119">**多個時間軸實例**</span><span class="sxs-lookup"><span data-stu-id="a296b-119">**Multiple Timeline Instances**</span></span>

-   <span data-ttu-id="a296b-120">請勿在時間軸之間移動時間軸物件。</span><span class="sxs-lookup"><span data-stu-id="a296b-120">Do not move timeline objects between timelines.</span></span> <span data-ttu-id="a296b-121">時間軸中的每個物件都必須由該時間軸建立。</span><span class="sxs-lookup"><span data-stu-id="a296b-121">Every object in a timeline must be created by that timeline.</span></span> <span data-ttu-id="a296b-122">時間軸會保存內部快取，其中包含它所建立之物件的相關資訊;移動時間軸物件可能會中斷快取。</span><span class="sxs-lookup"><span data-stu-id="a296b-122">The timeline holds an internal cache with information about the objects that it creates; moving timeline objects can disrupt the cache.</span></span>
-   <span data-ttu-id="a296b-123">絕對不要使用具有一個以上時間軸的相同轉譯引擎實例。</span><span class="sxs-lookup"><span data-stu-id="a296b-123">Never use the same instance of a render engine with more than one timeline.</span></span> <span data-ttu-id="a296b-124">轉譯引擎會保留快取，內含時間軸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a296b-124">The render engine holds a cache with information about the timeline.</span></span> <span data-ttu-id="a296b-125">多個時間軸會中斷快取，並導致無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="a296b-125">Multiple timelines will disrupt the cache and cause unpredictable results.</span></span> <span data-ttu-id="a296b-126">如果您需要兩個作用中的時間軸，請為每個時間軸建立個別的轉譯引擎實例。</span><span class="sxs-lookup"><span data-stu-id="a296b-126">If you need two active timelines, make separate instances of render engines for each timeline.</span></span>
-   <span data-ttu-id="a296b-127">時間軸可以使用一個以上的轉譯引擎，但不能同時使用。</span><span class="sxs-lookup"><span data-stu-id="a296b-127">A timeline can use more than one render engine, but not at the same time.</span></span> <span data-ttu-id="a296b-128">使用其他轉譯引擎之前，請先刪除舊的轉譯引擎。</span><span class="sxs-lookup"><span data-stu-id="a296b-128">Delete the old render engine before using another render engine.</span></span> <span data-ttu-id="a296b-129"> (當您從使用基本轉譯引擎進行預覽時，通常會發生這種情況，以供寫入檔案的智慧型轉譯引擎。 ) </span><span class="sxs-lookup"><span data-stu-id="a296b-129">(You would typically do this when you switch from using the basic render engine for preview to the smart render engine for file writing.)</span></span>

<span data-ttu-id="a296b-130">**持續性**</span><span class="sxs-lookup"><span data-stu-id="a296b-130">**Persistence**</span></span>

-   <span data-ttu-id="a296b-131">當您將專案儲存至 XML 檔案時，篩選圖形不會持續。</span><span class="sxs-lookup"><span data-stu-id="a296b-131">The filter graph is not persistent when you save the project to an XML file.</span></span> <span data-ttu-id="a296b-132">因此，您會遺失與 smart recompression、壓縮格式或壓縮參數相關的任何資訊。</span><span class="sxs-lookup"><span data-stu-id="a296b-132">Therefore, you lose any information relating to smart recompression, compression format, or compression parameters.</span></span> <span data-ttu-id="a296b-133">在載入專案之後，應用程式會由應用程式還原這些參數。</span><span class="sxs-lookup"><span data-stu-id="a296b-133">It is up to the application to restore these parameters after it loads a project.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a296b-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="a296b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a296b-135">使用 DirectShow 編輯服務</span><span class="sxs-lookup"><span data-stu-id="a296b-135">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



