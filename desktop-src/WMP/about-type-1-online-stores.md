---
title: 關於類型1線上商店
description: 關於類型1線上商店
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Windows Media Player 線上商店，請輸入1個線上商店
- 線上商店，請輸入1個線上商店
- 輸入1個線上商店，關於
- Windows Media Player，請輸入1個線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ecd939a03734fed121dcaa22c0d7ae89127476
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106968083"
---
# <a name="about-type-1-online-stores"></a><span data-ttu-id="574aa-107">關於類型1線上商店</span><span class="sxs-lookup"><span data-stu-id="574aa-107">About Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="574aa-108">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="574aa-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="574aa-109">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="574aa-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="574aa-110">Microsoft Windows Media Player 11 支援兩種線上商店：類型1和類型2。</span><span class="sxs-lookup"><span data-stu-id="574aa-110">Microsoft Windows Media Player 11 supports two kinds of online stores: type 1 and type 2.</span></span> <span data-ttu-id="574aa-111">類型1存放區比類型2存放區更深層整合至 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="574aa-111">Type 1 stores are more deeply integrated into Windows Media Player than type 2 stores.</span></span> <span data-ttu-id="574aa-112">Type 1 線上商店提供可下載的音樂類別目錄，讓 Windows Media Player 可以將商店的內容提供給使用者，就像內容是在使用者的本機媒體文件庫中一樣。</span><span class="sxs-lookup"><span data-stu-id="574aa-112">A type 1 online store provides a downloadable music catalog so that Windows Media Player can make the store's content available to the user as if the content were in the user's local media library.</span></span>

<span data-ttu-id="574aa-113">類型1線上商店必須提供可實 [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) 介面的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="574aa-113">A type 1 online store must provide a plug-in that implements the [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="574aa-114">當使用者流覽 Windows Media Player 使用者介面時，播放程式會呼叫外掛程式，讓線上商店可以藉由提供顯示在播放程式中的網頁來增強使用者的體驗。</span><span class="sxs-lookup"><span data-stu-id="574aa-114">As the user navigates in the Windows Media Player user interface, the Player calls the plug-in so that the online store can enhance the user's experience by providing webpages that are displayed in the Player.</span></span>

<span data-ttu-id="574aa-115">類型1線上商店的功能，可與類型2存放區區別，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="574aa-115">Features of type 1 online stores that distinguish them from type 2 stores include the following:</span></span>

-   <span data-ttu-id="574aa-116">**便於使用。**</span><span class="sxs-lookup"><span data-stu-id="574aa-116">**Ease of use.**</span></span> <span data-ttu-id="574aa-117">使用者可以使用他們目前用來管理個人文件庫的相同、熟悉的 Windows Media Player 使用者介面，從線上商店瀏覽目錄音樂。</span><span class="sxs-lookup"><span data-stu-id="574aa-117">Users can browse for music from the online store catalog using the same, familiar Windows Media Player user interface that they currently use to manage their personal library.</span></span> <span data-ttu-id="574aa-118">在任何特定時間，使用者都只能在流覽功能中查看單一線上商店目錄。</span><span class="sxs-lookup"><span data-stu-id="574aa-118">Users can view only a single online store catalog in the Browse feature at any particular time.</span></span>
-   <span data-ttu-id="574aa-119">**方便。**</span><span class="sxs-lookup"><span data-stu-id="574aa-119">**Convenience.**</span></span> <span data-ttu-id="574aa-120">使用者無須從流覽功能切換到 Windows Media Player 使用者介面的另一個部分，就可以取樣或購買音樂。</span><span class="sxs-lookup"><span data-stu-id="574aa-120">Users can sample or purchase music without switching from the Browse feature to another part of the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="574aa-121">**豐富的功能。**</span><span class="sxs-lookup"><span data-stu-id="574aa-121">**Rich features.**</span></span> <span data-ttu-id="574aa-122">因為線上商店目錄的儲存方式類似于使用者的程式庫，所以許多 Windows Media Player 程式庫功能都可以套用至目錄。</span><span class="sxs-lookup"><span data-stu-id="574aa-122">Because the online store catalog is stored in a fashion similar to the user's library, many of the Windows Media Player library features can be applied to the catalog.</span></span> <span data-ttu-id="574aa-123">例如，使用者可以使用流覽功能的單字滾輪來篩選線上商店目錄。</span><span class="sxs-lookup"><span data-stu-id="574aa-123">For example, users can use the Browse feature's word wheel to filter the online store catalog.</span></span>

<span data-ttu-id="574aa-124">在線上商店提供者中，提供類型1存放區的優點，而不是類型2存放區的優點包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="574aa-124">For an online store provider, the advantages of providing a type 1 store rather than a type 2 store include the following:</span></span>

-   <span data-ttu-id="574aa-125">Windows Media Player 程式庫樹狀結構中的高度可見自訂節點。</span><span class="sxs-lookup"><span data-stu-id="574aa-125">A highly visible custom node in the Windows Media Player library tree.</span></span>
-   <span data-ttu-id="574aa-126">針對音樂購買所設計的系統。</span><span class="sxs-lookup"><span data-stu-id="574aa-126">A system designed for music purchases.</span></span>
-   <span data-ttu-id="574aa-127">改進玩家流程的連接。</span><span class="sxs-lookup"><span data-stu-id="574aa-127">Improved connections to Player processes.</span></span>
-   <span data-ttu-id="574aa-128">更好、更容易使用的下載管理員。</span><span class="sxs-lookup"><span data-stu-id="574aa-128">A better, easier-to-use download manager.</span></span>
-   <span data-ttu-id="574aa-129">可以在播放 (中的各種功能之間進行流覽，包括) 開啟特定的程式庫樹狀節點。</span><span class="sxs-lookup"><span data-stu-id="574aa-129">The ability to navigate between various features in the Player (including opening specific library tree nodes).</span></span>
-   <span data-ttu-id="574aa-130">訂用帳戶內容的授權到期通知。</span><span class="sxs-lookup"><span data-stu-id="574aa-130">Notifications about license expiration for subscription content.</span></span>
-   <span data-ttu-id="574aa-131">使用連線的便攜音樂播放機的通知。</span><span class="sxs-lookup"><span data-stu-id="574aa-131">Notifications for working with connected portable music players.</span></span>

<span data-ttu-id="574aa-132">下列各節提供類型1線上商店的總覽資訊。</span><span class="sxs-lookup"><span data-stu-id="574aa-132">The following sections provide overview information about type 1 online stores.</span></span>



| <span data-ttu-id="574aa-133">區段</span><span class="sxs-lookup"><span data-stu-id="574aa-133">Section</span></span>                                                                                              | <span data-ttu-id="574aa-134">描述</span><span class="sxs-lookup"><span data-stu-id="574aa-134">Description</span></span>                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="574aa-135">音樂類別目錄</span><span class="sxs-lookup"><span data-stu-id="574aa-135">Music Catalog</span></span>](music-catalog.md)                                                                   | <span data-ttu-id="574aa-136">描述線上商店所提供的音樂目錄。</span><span class="sxs-lookup"><span data-stu-id="574aa-136">Describes the music catalog provided by the online store.</span></span> <span data-ttu-id="574aa-137">說明 Microsoft 所提供的目錄編譯器。</span><span class="sxs-lookup"><span data-stu-id="574aa-137">Describes the catalog compiler provided by Microsoft.</span></span>                                                                     |
| [<span data-ttu-id="574aa-138">內容容器</span><span class="sxs-lookup"><span data-stu-id="574aa-138">Content Containers</span></span>](content-containers.md)                                                         | <span data-ttu-id="574aa-139">描述 ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)) 的內容容器介面，此介面可用來代表要購買或下載的媒體專案集合。</span><span class="sxs-lookup"><span data-stu-id="574aa-139">Describes the content container interface ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), which is used to represent a collection of media items to be purchased or downloaded.</span></span> |
| [<span data-ttu-id="574aa-140">程式庫整合</span><span class="sxs-lookup"><span data-stu-id="574aa-140">Library Integration</span></span>](library-integration.md)                                                       | <span data-ttu-id="574aa-141">描述線上商店的音樂目錄如何整合到播放程式的程式庫視圖中。</span><span class="sxs-lookup"><span data-stu-id="574aa-141">Describes how the online store's music catalog is integrated into the Player's library view.</span></span>                                                                                        |
| [<span data-ttu-id="574aa-142">探索頁面</span><span class="sxs-lookup"><span data-stu-id="574aa-142">Discovery Pages</span></span>](discovery-pages.md)                                                               | <span data-ttu-id="574aa-143">描述線上商店所提供 Windows Media Player 與網頁之間的互動。</span><span class="sxs-lookup"><span data-stu-id="574aa-143">Describes the interaction between Windows Media Player and webpages provided by the online store.</span></span>                                                                                   |
| [<span data-ttu-id="574aa-144">快顯功能表</span><span class="sxs-lookup"><span data-stu-id="574aa-144">Context Menus</span></span>](context-menus.md)                                                                   | <span data-ttu-id="574aa-145">描述當使用者導覽播放程式的使用者介面時，線上商店如何提供內容功能表。</span><span class="sxs-lookup"><span data-stu-id="574aa-145">Describes how the online store can provide context menus as the user navigates the Player's user interface.</span></span>                                                                         |
| [<span data-ttu-id="574aa-146">音訊串流</span><span class="sxs-lookup"><span data-stu-id="574aa-146">Audio Streams</span></span>](audio-streams.md)                                                                   | <span data-ttu-id="574aa-147">描述線上商店如何以串流處理音訊內容的 URL 來提供 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="574aa-147">Describes how the online store provides Windows Media Player with the URL for streaming audio content.</span></span>                                                                              |
| [<span data-ttu-id="574aa-148">類型1線上商店的 ServiceInfo 檔</span><span class="sxs-lookup"><span data-stu-id="574aa-148">ServiceInfo Document for a Type 1 Online Store</span></span>](serviceinfo-document-for-a-type-1-online-store.md) | <span data-ttu-id="574aa-149">描述類型1線上商店所提供的 ServiceInfo XML 檔。</span><span class="sxs-lookup"><span data-stu-id="574aa-149">Describes the ServiceInfo XML document provided by a type 1 online store.</span></span>                                                                                                           |
| [<span data-ttu-id="574aa-150">輸入1線上商店外掛程式</span><span class="sxs-lookup"><span data-stu-id="574aa-150">Type 1 Online Store Plug-in</span></span>](type-1-online-store-plug-in.md)                                       | <span data-ttu-id="574aa-151">描述類型1線上商店必須提供的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="574aa-151">Describes the plug-in that a type 1 online store must provide.</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="574aa-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="574aa-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="574aa-153">**輸入1個線上商店**</span><span class="sxs-lookup"><span data-stu-id="574aa-153">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




