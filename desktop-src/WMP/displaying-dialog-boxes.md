---
title: 顯示對話方塊
description: 顯示對話方塊
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Windows Media Player 線上商店，顯示對話方塊
- 線上商店，顯示對話方塊
- 輸入1個線上商店，顯示對話方塊
- Windows Media Player 線上商店，對話方塊
- 線上商店、對話方塊
- 輸入1個線上商店、對話方塊
- 顯示對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebe008a6c3eac872edea497dc9d50da408aa7eb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681412"
---
# <a name="displaying-dialog-boxes"></a><span data-ttu-id="c5af6-110">顯示對話方塊</span><span class="sxs-lookup"><span data-stu-id="c5af6-110">Displaying Dialog Boxes</span></span>

<span data-ttu-id="c5af6-111">線上商店可以透過 Windows Media Player 叫用對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c5af6-111">The online store can invoke dialog boxes through Windows Media Player.</span></span> <span data-ttu-id="c5af6-112">若要這樣做，請從探索頁面腳本程式碼呼叫 [External. showPopup](external-showpopup.md) ，提供代表要顯示之對話方塊的自訂索引值。</span><span class="sxs-lookup"><span data-stu-id="c5af6-112">To do this, call [External.showPopup](external-showpopup.md) from the discovery page script code, providing a custom index value that represents the dialog box to display.</span></span> <span data-ttu-id="c5af6-113">此索引值只對線上商店程式碼具有意義;Windows Media Player 不會解讀此值。</span><span class="sxs-lookup"><span data-stu-id="c5af6-113">This index value has meaning only to the online store code; Windows Media Player does not interpret this value.</span></span> <span data-ttu-id="c5af6-114">Windows Media Player 接著會呼叫 [IWMPContentPartner：： GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)，並傳遞 g \_ SzItemInfo \_ PopupURL 作為 *bstrInfoName* 參數和 *pCoNtext* 參數的索引編號。</span><span class="sxs-lookup"><span data-stu-id="c5af6-114">Windows Media Player then calls [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passing g\_szItemInfo\_PopupURL for the *bstrInfoName* parameter and the index number for the *pContext* parameter.</span></span> <span data-ttu-id="c5af6-115">外掛程式接著會傳回包含要在對話方塊中顯示之網頁 URL 的 **BSTR** ，而播放程式會顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c5af6-115">The plug-in then returns a **BSTR** containing the URL of the webpage to display in the dialog box and the Player shows the dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5af6-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5af6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5af6-117">**類型1線上商店的程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="c5af6-117">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




