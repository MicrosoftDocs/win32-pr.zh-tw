---
title: 偵測播放玩家
description: 偵測播放玩家
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Windows Media Player 線上商店，偵測玩家
- 線上商店，偵測玩家
- 輸入1個線上商店，偵測玩家
- 輸入2個線上商店，偵測玩家
- Windows Media Player 線上商店、播放機偵測
- 線上商店、播放機偵測
- 輸入1個線上商店、播放機偵測
- 輸入2個線上商店、播放機偵測
- 播放機偵測
- 偵測播放玩家
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb919e790b07ccf5d8df587abd63d2344534b16b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932291"
---
# <a name="detecting-the-player"></a><span data-ttu-id="4e8a8-113">偵測播放玩家</span><span class="sxs-lookup"><span data-stu-id="4e8a8-113">Detecting the Player</span></span>

<span data-ttu-id="4e8a8-114">當您為線上商店建立網頁時，您可能會想要讓使用者能夠在網頁瀏覽器或 Windows Media Player 中查看頁面。</span><span class="sxs-lookup"><span data-stu-id="4e8a8-114">When creating a webpage for your online store, you may decide that you want users to be able to view the page in a Web browser or in Windows Media Player.</span></span> <span data-ttu-id="4e8a8-115">您可以使用 ASP 腳本來判斷是否已在播放程式中主控您的網頁。</span><span class="sxs-lookup"><span data-stu-id="4e8a8-115">You can use an ASP script to determine whether your webpage is hosted in the Player.</span></span>

<span data-ttu-id="4e8a8-116">下列範例程式碼會從 URL 查詢字串中抓取 version 參數，以判斷頁面是否裝載于 Windows Media Player 中：</span><span class="sxs-lookup"><span data-stu-id="4e8a8-116">The following example code retrieves the version parameter from the URL query string to determine whether the page is hosted in Windows Media Player:</span></span>


```C++
<%
    Dim sVersion

    sVersion = Trim(Request.QueryString("version")) 
 
    If sVersion = "" Then   
        Response.Write "Not hosted in Windows Media Player"
    Else 
        Response.Write "Hosted in Windows Media Player<BR>"
        Response.Write "Version is " & sVersion
    End If
%>
```



<span data-ttu-id="4e8a8-117">請注意，上述程式碼會假設在 Windows Media Player 中裝載時，查詢字串中有 version 參數。</span><span class="sxs-lookup"><span data-stu-id="4e8a8-117">Note that the preceding code assumes that the version parameter exists in the query string when hosted in Windows Media Player.</span></span> <span data-ttu-id="4e8a8-118">這適用于使用者開啟的頁面，但對於使用 **外部 NavigateTaskPaneURL** 開啟的頁面，可能不是正確的。</span><span class="sxs-lookup"><span data-stu-id="4e8a8-118">This is true for pages opened by the user, but may not be true for pages opened by using **External.NavigateTaskPaneURL**.</span></span> <span data-ttu-id="4e8a8-119">若要在以程式設計方式流覽時存在版本查詢字串，您必須將 version 參數加入至方法呼叫，或以動態方式將版本附加至 ServiceInfo 檔的 **導覽** 元素基底 URL。</span><span class="sxs-lookup"><span data-stu-id="4e8a8-119">For the version query string to exist when navigating programmatically, you must add the version parameter to the method call or dynamically append the version to the base URL of the **Navigate** element of your ServiceInfo document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e8a8-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="4e8a8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e8a8-121">**動態建立 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="4e8a8-121">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="4e8a8-122">**NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="4e8a8-122">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="4e8a8-123">**Type 1 和 Type 2 線上商店的一般資訊**</span><span class="sxs-lookup"><span data-stu-id="4e8a8-123">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




