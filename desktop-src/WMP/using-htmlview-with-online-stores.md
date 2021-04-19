---
title: 使用 HTMLView 搭配線上商店
description: 使用 HTMLView 搭配線上商店
ms.assetid: 78de7ef3-400c-4411-8ade-35c421805df8
keywords:
- Windows Media Player 線上商店，HTMLView
- 線上商店、HTMLView
- 輸入1個線上商店，HTMLView
- 輸入2個線上商店，HTMLView
- HTMLView，線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d136be4f7866b6911b8b007de7e784d6133c217
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968065"
---
# <a name="using-htmlview-with-online-stores"></a><span data-ttu-id="c8325-108">使用 HTMLView 搭配線上商店</span><span class="sxs-lookup"><span data-stu-id="c8325-108">Using HTMLView with Online Stores</span></span>

<span data-ttu-id="c8325-109">Windows Media Player 會提示使用者顯示 **目前播放** 中 HTMLView 內容的許可權。</span><span class="sxs-lookup"><span data-stu-id="c8325-109">Windows Media Player prompts users for permission to display HTMLView content in **Now Playing**.</span></span> <span data-ttu-id="c8325-110">線上商店可以停用此提示，方法是在 ServiceInfo 檔的 **HTMLView** 元素中指定基底 URL 值。</span><span class="sxs-lookup"><span data-stu-id="c8325-110">Online stores can disable this prompt by specifying a base URL value in the **HTMLView** element of the ServiceInfo document.</span></span> <span data-ttu-id="c8325-111">當 Windows Media Player 開啟播放清單來指定要顯示的 HTMLView 內容時，播放程式會比較目前作用中線上商店的 ServiceInfo 檔中的基底 URL 與 HTMLView 內容的基底 URL。</span><span class="sxs-lookup"><span data-stu-id="c8325-111">When Windows Media Player opens a playlist that specifies HTMLView content to display, the Player compares the base URL from the ServiceInfo document of the current active online store to the base URL of the HTMLView content.</span></span> <span data-ttu-id="c8325-112">如果相符，Windows Media Player 會顯示 HTMLView 內容而不提示使用者。</span><span class="sxs-lookup"><span data-stu-id="c8325-112">If they match, Windows Media Player displays the HTMLView content without prompting the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8325-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8325-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8325-114">**顯示 Windows Media Player 中的網頁**</span><span class="sxs-lookup"><span data-stu-id="c8325-114">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="c8325-115">**HTMLView 元素**</span><span class="sxs-lookup"><span data-stu-id="c8325-115">**HTMLView Element**</span></span>](htmlview-element.md)
</dt> <dt>

[<span data-ttu-id="c8325-116">**Type 1 和 Type 2 線上商店的一般資訊**</span><span class="sxs-lookup"><span data-stu-id="c8325-116">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




