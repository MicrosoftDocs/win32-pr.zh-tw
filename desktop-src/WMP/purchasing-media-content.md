---
title: 購買媒體內容
description: 購買媒體內容
ms.assetid: df4a3152-f9e3-4a97-b021-6d5e8de9c184
keywords:
- Windows Media Player 線上商店、購買媒體內容
- 線上商店、購買媒體內容
- 輸入1個線上商店、購買媒體內容
- Windows Media Player 線上商店、媒體內容購買
- 線上商店、媒體內容購買
- 輸入1個線上商店、媒體內容購買
- 媒體內容，購買
- 購買媒體內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e420f1dce607e1c596c48490d10bbe8a2a5a5f61
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932913"
---
# <a name="purchasing-media-content"></a><span data-ttu-id="bce02-111">購買媒體內容</span><span class="sxs-lookup"><span data-stu-id="bce02-111">Purchasing Media Content</span></span>

<span data-ttu-id="bce02-112">當 Windows Media Player 在文件庫樹狀檢視中顯示音樂內容時，使用者介面會包含使用者可以按一下以購買內容的元素。</span><span class="sxs-lookup"><span data-stu-id="bce02-112">When Windows Media Player displays music content in the library tree view, the user interface includes elements that the user can click to buy the content.</span></span> <span data-ttu-id="bce02-113">例如，使用者可能會按一下按鈕來購買個別的歌曲，或購買整個專輯。</span><span class="sxs-lookup"><span data-stu-id="bce02-113">For example, the user might click a button to buy an individual song or to buy an entire album.</span></span>

<span data-ttu-id="bce02-114">如果使用中的線上商店是類型1存放區，Windows Media Player 可以存取線上商店目錄中的追蹤、專輯和清單價格。</span><span class="sxs-lookup"><span data-stu-id="bce02-114">If the active online store is a Type 1 store, Windows Media Player has access to track, album, and list prices in the online store's catalog.</span></span> <span data-ttu-id="bce02-115">目錄中的價格是只有線上商店才能瞭解格式的字串。</span><span class="sxs-lookup"><span data-stu-id="bce02-115">Those prices in the catalog are strings that have a format understood only by the online store.</span></span> <span data-ttu-id="bce02-116">Windows Media Player 不會解讀價格字串;它只會顯示在使用者介面專案中，例如購買按鈕。</span><span class="sxs-lookup"><span data-stu-id="bce02-116">Windows Media Player does not interpret price strings; it merely displays them in user interface elements like Buy buttons.</span></span>

<span data-ttu-id="bce02-117">當 Windows Media Player 設定一組媒體專案的購買專案時，它會呼叫 [IWMPContentPartner：： CanBuySilent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent)，將媒體專案的識別碼和價格傳遞給內容合作夥伴外掛程式。</span><span class="sxs-lookup"><span data-stu-id="bce02-117">When Windows Media Player sets up a purchase for a set of media items, it passes the IDs and prices of the media items to the content partner plug-in by calling [IWMPContentPartner::CanBuySilent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent).</span></span> <span data-ttu-id="bce02-118">屆時，外掛程式可以檢查玩家所提供的價格。</span><span class="sxs-lookup"><span data-stu-id="bce02-118">At that point, the plug-in can inspect the prices provided by the Player.</span></span> <span data-ttu-id="bce02-119">這些是使用者預期支付的價格;也就是播放程式向使用者顯示的價格。</span><span class="sxs-lookup"><span data-stu-id="bce02-119">These are the prices that the user expects to pay; that is, the prices that the Player displayed to the user.</span></span> <span data-ttu-id="bce02-120">根據播放程式所提供的媒體識別碼和價格，外掛程式會計算總價格，並在 *bstrTotalPrice* 參數中返回播放程式。</span><span class="sxs-lookup"><span data-stu-id="bce02-120">Based on the media IDs and prices provided by the Player, the plug-in calculates a total price, which it returns to the Player in the *bstrTotalPrice* parameter.</span></span> <span data-ttu-id="bce02-121">播放程式傳遞給 **CanBuySilent** 的價格會提供外掛程式資訊，但不會商都必須外掛程式以傳回特定的總價。</span><span class="sxs-lookup"><span data-stu-id="bce02-121">The prices that the Player passes to **CanBuySilent** provide the plug-in with information, but they do not obligate the plug-in to return a certain total price.</span></span> <span data-ttu-id="bce02-122">外掛程式可以計算出合適的總價格。</span><span class="sxs-lookup"><span data-stu-id="bce02-122">The plug-in can calculate the total price as it sees fit.</span></span>

<span data-ttu-id="bce02-123">除了計算購買的總價格之外， **CanBuySilent** 還會判斷 purchace 是否能以無訊息方式繼續進行;也就是說，不會顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bce02-123">In addition to calculating the total price of a purchase, **CanBuySilent** determines whether the purchace can proceed silently; that is, without displaying a dialog box.</span></span> <span data-ttu-id="bce02-124">如果 **CanBuySilent** 傳回 **True**，Windows Media Player 只會變更 [購買] 按鈕上的文字，以提示使用者確認購買。</span><span class="sxs-lookup"><span data-stu-id="bce02-124">If **CanBuySilent** returns **True**, Windows Media Player simply changes the text on the Buy button to prompt the user to confirm the purchase.</span></span> <span data-ttu-id="bce02-125">如果 **CanBuySilent** 傳回 **False**，Windows Media Player 會顯示一個對話方塊，提示使用者確認購買。</span><span class="sxs-lookup"><span data-stu-id="bce02-125">If **CanBuySilent** returns **False**, Windows Media Player displays a dialog box that prompts the user to confirm the purchase.</span></span> <span data-ttu-id="bce02-126">對話方塊會提供使用者資訊，以摘要列出購買的資訊，例如專輯數量、個別曲目數目，以及外掛程式) 所傳回的總價格 (。</span><span class="sxs-lookup"><span data-stu-id="bce02-126">The dialog box provides the user with information that summarizes the purchase like number of albums, number of individual tracks, and the total price (as returned by the plug-in).</span></span>

<span data-ttu-id="bce02-127">使用者確認購買之後，Player 會撥打 [IWMPContentPartner：：](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)purchase。</span><span class="sxs-lookup"><span data-stu-id="bce02-127">After the user confirms the purchase, the Player calls [IWMPContentPartner::Buy](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy).</span></span> <span data-ttu-id="bce02-128">這個方法呼叫會提供外掛程式與 **CanBuySilent** 相同的內容容器清單。</span><span class="sxs-lookup"><span data-stu-id="bce02-128">This method call provides the plug-in with the same content container list as **CanBuySilent**.</span></span> <span data-ttu-id="bce02-129">**通話時**，Windows Media Player 也會提供 cookie (單純的 **DWORD** 值，也就是可供外掛程式用來識別交易的會話) 唯一的。</span><span class="sxs-lookup"><span data-stu-id="bce02-129">When calling **Buy**, Windows Media Player also provides a cookie (simply a **DWORD** value, unique for the session) that the plug-in can use to identify the transaction.</span></span> <span data-ttu-id="bce02-130">當交易完成時，外掛程式必須呼叫 [IWMPContentPartnerCallback：： BuyComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete)，傳遞 *dwBuyCookie* 參數的原始 cookie 值，以通知播放程式交易已完成。</span><span class="sxs-lookup"><span data-stu-id="bce02-130">When the transaction is completed, the plug-in must call [IWMPContentPartnerCallback::BuyComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete), passing the original cookie value for the *dwBuyCookie* parameter, to notify the Player that the transaction is finished.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bce02-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="bce02-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bce02-132">**類型1線上商店的程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="bce02-132">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




