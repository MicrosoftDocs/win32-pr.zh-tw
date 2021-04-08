---
title: 探索頁面
description: 探索頁面
ms.assetid: deb0cbf9-b7e1-4ce6-8241-b9199129515a
keywords:
- Windows Media Player 線上商店，探索頁面
- 線上商店，探索頁面
- 輸入1個線上商店，探索頁面
- Windows Media Player 程式庫，探索頁面
- 程式庫，探索頁面
- 探索頁面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a349b0e7238aa6d59b56f9035a3c02a5b3ff7b7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681413"
---
# <a name="discovery-pages"></a><span data-ttu-id="2068d-109">探索頁面</span><span class="sxs-lookup"><span data-stu-id="2068d-109">Discovery Pages</span></span>

<span data-ttu-id="2068d-110">如果有效的線上商店是類型1存放區，Windows Media Player 會在其使用者介面中顯示商店的內容。</span><span class="sxs-lookup"><span data-stu-id="2068d-110">If the active online store is a type 1 store, Windows Media Player displays the store's content in its user interface.</span></span> <span data-ttu-id="2068d-111">程式庫樹狀檢視控制項具有線上商店的節點。</span><span class="sxs-lookup"><span data-stu-id="2068d-111">The library tree-view control has a node for the online store.</span></span> <span data-ttu-id="2068d-112">當使用者按一下該節點或其任何子節點時，Windows Media Player 會在詳細資料窗格中顯示線上商店的內容。</span><span class="sxs-lookup"><span data-stu-id="2068d-112">When the user clicks that node or any of its subnodes, Windows Media Player displays content from the online store in the details pane.</span></span>

<span data-ttu-id="2068d-113">當使用者與樹狀檢視控制項或詳細資料窗格中的線上商店內容互動時，Windows Media Player 會顯示線上商店所提供的網頁，稱為 [ *探索] 頁面*。</span><span class="sxs-lookup"><span data-stu-id="2068d-113">As the user interacts with online store content in the tree-view control or in the details pane, Windows Media Player displays webpages, called *discovery pages*, provided by the online store.</span></span> <span data-ttu-id="2068d-114">當使用者流覽線上商店的目錄時，探索頁面會提供音樂的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2068d-114">Discovery pages provide additional information about the music as the user browses the online store's catalog.</span></span> <span data-ttu-id="2068d-115">探索頁面會透過 [外部物件](external-object-for-type-1-online-stores.md)的屬性、方法和事件與 Windows Media Player 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="2068d-115">Discovery pages communicate with Windows Media Player through the properties, methods, and events of the [External object](external-object-for-type-1-online-stores.md).</span></span>

<span data-ttu-id="2068d-116">每當 Windows Media Player 變更線上商店內容的查看時，它會呼叫由線上商店的外掛程式所執行的 [IWMPContentPartner：： GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)，以取得要與新視圖一起顯示之探索頁面的 URL。</span><span class="sxs-lookup"><span data-stu-id="2068d-116">Whenever Windows Media Player changes its view of the online store's content, it calls [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate), implemented by the online store's plug-in, to get the URL of the discovery page to display with the new view.</span></span>

<span data-ttu-id="2068d-117">在 Windows Media Player 中，線上商店內容的顯示方式有五項資訊：工作、位置類型、位置識別碼、選取的專案類型，以及選取的專案識別碼。</span><span class="sxs-lookup"><span data-stu-id="2068d-117">The view of online store content in Windows Media Player is characterized by five pieces of information: task, location type, location ID, selected item type, and selected item ID.</span></span> <span data-ttu-id="2068d-118">Windows Media Player *將這* 五個專案提供給工作、*位置*、 *pCoNtext*、 *clickLocation* 和 *pClickCoNtext* 參數中的 **GetTemplate** 方法。</span><span class="sxs-lookup"><span data-stu-id="2068d-118">Windows Media Player supplies those five items to the **GetTemplate** method in the *task*, *location*, *pContext*, *clickLocation*, and *pClickContext* parameters.</span></span> <span data-ttu-id="2068d-119">Windows Media Player 會將這五個專案提供給 **外部** 物件的 *task*、 *libraryLocationType*、 *libraryLocationID*、 *selectedItemType* 和 *selectedItemID* 屬性中的探索頁面使用。</span><span class="sxs-lookup"><span data-stu-id="2068d-119">Windows Media Player makes those five items available to discovery pages in the *task*, *libraryLocationType*, *libraryLocationID*, *selectedItemType*, and *selectedItemID* properties of the **External** object.</span></span> <span data-ttu-id="2068d-120">如需 Windows Media Player 如何指定其線上商店內容之觀點的詳細資訊，請參閱 [位置和選取的專案](location-and-selected-item.md)。</span><span class="sxs-lookup"><span data-stu-id="2068d-120">For more information about how Windows Media Player specifies its view of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="2068d-121">除了讓探索頁面與 Windows Media Player 通訊之外， **外部** 物件也可讓探索頁面與線上商店的外掛程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="2068d-121">In addition to enabling a discovery page to communicate with Windows Media Player, the **External** object enables a discovery page to communicate with the online store's plug-in.</span></span> <span data-ttu-id="2068d-122">發生這種情況時，Windows Media Player 會作為探索頁面與外掛程式之間的橋樑。</span><span class="sxs-lookup"><span data-stu-id="2068d-122">When that happens, Windows Media Player acts as a bridge between the discovery page and the plug-in.</span></span> <span data-ttu-id="2068d-123">例如，[探索] 頁面可以呼叫 [sendMessage](external-sendmessage.md) ，以將自訂訊息傳送至外掛程式。</span><span class="sxs-lookup"><span data-stu-id="2068d-123">For example, the discovery page can call [External.sendMessage](external-sendmessage.md) to send a custom message to the plug-in.</span></span> <span data-ttu-id="2068d-124">Windows Media Player 接收此方法呼叫，然後再呼叫 [IWMPContentPartner：： SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage) ，將訊息傳遞至外掛程式。</span><span class="sxs-lookup"><span data-stu-id="2068d-124">Windows Media Player receives this method call and in turn calls [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage) to pass the message to the plug-in.</span></span> <span data-ttu-id="2068d-125">外掛程式完成訊息的處理之後，就會呼叫 [IWMPContentPartnerCallback：： SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)。</span><span class="sxs-lookup"><span data-stu-id="2068d-125">When the plug-in has finished processing the message, it calls [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete).</span></span> <span data-ttu-id="2068d-126">Windows Media Player 接著會引發 [OnSendMessageComplete](external-onsendmessagecomplete-event.md) 事件，以通知探索頁面。</span><span class="sxs-lookup"><span data-stu-id="2068d-126">Windows Media Player then notifies the discovery page by raising the [External.OnSendMessageComplete](external-onsendmessagecomplete-event.md) event.</span></span>

<span data-ttu-id="2068d-127">**外部** 物件也提供可讓探索頁面與另一個探索頁面通訊的方式。</span><span class="sxs-lookup"><span data-stu-id="2068d-127">The **External** object also provides a way for a discovery page to communicate with another discovery page.</span></span> <span data-ttu-id="2068d-128">當探索頁面上的腳本呼叫 [changeView](external-changeview.md)時，腳本可以在 *ViewParams* 參數中提供字串。</span><span class="sxs-lookup"><span data-stu-id="2068d-128">When script on a discovery page calls [External.changeView](external-changeview.md), the script can supply a string in the *ViewParams* parameter.</span></span> <span data-ttu-id="2068d-129">Windows Media Player 不會解讀 *ViewParams* 字串，但它會將字串提供給 [viewParameters](external-viewparameters.md) 屬性中的下一個 [探索] 頁面。</span><span class="sxs-lookup"><span data-stu-id="2068d-129">Windows Media Player does not interpret the *ViewParams* string, but it makes the string available to the next discovery page in the [External.viewParameters](external-viewparameters.md) property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2068d-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="2068d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2068d-131">**關於類型1線上商店**</span><span class="sxs-lookup"><span data-stu-id="2068d-131">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="2068d-132">**位置和選取的專案**</span><span class="sxs-lookup"><span data-stu-id="2068d-132">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 




