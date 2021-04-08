---
title: Client-Side 設計
description: 伺服器端 HTML 頁面中的腳本會與裝載的線上列印順序 Wizard 用戶端進行通訊。 這項通訊是透過 window 所存取的方法和屬性來完成。
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- 發佈嚮導，用戶端設計
- '[外部]、[發行] 嚮導'
- 發佈嚮導，window. 外部
- 發佈嚮導，設計考慮
- 發佈嚮導，線上列印訂購嚮導
- 線上列印順序 Wizard、用戶端設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f794ee5f576077e0523f9a21101205ec789d4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933215"
---
# <a name="client-side-design"></a><span data-ttu-id="ead52-110">Client-Side 設計</span><span class="sxs-lookup"><span data-stu-id="ead52-110">Client-Side Design</span></span>

<span data-ttu-id="ead52-111">伺服器端 HTML 頁面中的腳本會與裝載的線上列印順序 Wizard 用戶端進行通訊。</span><span class="sxs-lookup"><span data-stu-id="ead52-111">Script in server-side HTML pages communicates with the Online Print Ordering Wizard client in which it is hosted.</span></span> <span data-ttu-id="ead52-112">這項通訊是透過 **window** 所存取的方法和屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="ead52-112">This communication is accomplished through methods and properties accessed by the **window.external** object.</span></span>

<span data-ttu-id="ead52-113">本檔涵蓋下列主題。</span><span class="sxs-lookup"><span data-stu-id="ead52-113">The following topics are covered in this document.</span></span>

-   [<span data-ttu-id="ead52-114">方法和屬性</span><span class="sxs-lookup"><span data-stu-id="ead52-114">Methods and Properties</span></span>](#methods-and-properties)
-   [<span data-ttu-id="ead52-115">設計考量</span><span class="sxs-lookup"><span data-stu-id="ead52-115">Design Considerations</span></span>](#design-considerations)
-   [<span data-ttu-id="ead52-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="ead52-116">Related topics</span></span>](#related-topics)

## <a name="methods-and-properties"></a><span data-ttu-id="ead52-117">方法和屬性</span><span class="sxs-lookup"><span data-stu-id="ead52-117">Methods and Properties</span></span>

<span data-ttu-id="ead52-118">您可以透過 **window. external** 物件取得下列方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="ead52-118">The following methods and properties are available through the **window.external** object.</span></span>

-   [<span data-ttu-id="ead52-119">**FinalBack**</span><span class="sxs-lookup"><span data-stu-id="ead52-119">**FinalBack**</span></span>](/windows/desktop/shell/iwebwizardhost-finalback)
-   [<span data-ttu-id="ead52-120">**FinalNext**</span><span class="sxs-lookup"><span data-stu-id="ead52-120">**FinalNext**</span></span>](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [<span data-ttu-id="ead52-121">**取消**</span><span class="sxs-lookup"><span data-stu-id="ead52-121">**Cancel**</span></span>](/windows/desktop/shell/iwebwizardhost-cancel)
-   [<span data-ttu-id="ead52-122">**PassportAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="ead52-122">**PassportAuthenticate**</span></span>](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [<span data-ttu-id="ead52-123">**SetHeaderText**</span><span class="sxs-lookup"><span data-stu-id="ead52-123">**SetHeaderText**</span></span>](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [<span data-ttu-id="ead52-124">**SetWizardButtons**</span><span class="sxs-lookup"><span data-stu-id="ead52-124">**SetWizardButtons**</span></span>](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   <span data-ttu-id="ead52-125">[**標題**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ead52-125">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span></span>
-   [<span data-ttu-id="ead52-126">**屬性**</span><span class="sxs-lookup"><span data-stu-id="ead52-126">**Property**</span></span>](/windows/desktop/shell/iwebwizardhost-property)

<span data-ttu-id="ead52-127">伺服器端頁面的腳本會呼叫這些方法，在發行程式期間通知用戶端事件。</span><span class="sxs-lookup"><span data-stu-id="ead52-127">The server-side page's script calls these methods to notify the client of events during the publishing procedure.</span></span> <span data-ttu-id="ead52-128">讓我們看看 [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) 的範例。</span><span class="sxs-lookup"><span data-stu-id="ead52-128">Let's look at [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) as an example.</span></span> <span data-ttu-id="ead52-129">當 wizard 顯示第一個伺服器端的 HTML 網頁時，它會在所裝載的 HTML 網頁前面和之後，事先瞭解 wizard 頁面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ead52-129">When the wizard displays the first server-side HTML page, it does so armed with knowledge of the handles for the wizard pages preceding and following the hosted HTML pages.</span></span> <span data-ttu-id="ead52-130">在我們的範例中，在第一個 HTML 頁面上的使用者，按一下 [上一 **步** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="ead52-130">At this point in our example, the user, sitting at that first HTML page, clicks the **Back** button.</span></span> <span data-ttu-id="ead52-131">Wizard 將此事件的通知傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="ead52-131">The wizard sends a notification of this event to the server.</span></span> <span data-ttu-id="ead52-132">收到此訊息時，伺服器端腳本會參考此事件的 **OnBack** 處理常式，因為這是第一個 HTML 網頁，所以會呼叫 **FinalBack** 方法。</span><span class="sxs-lookup"><span data-stu-id="ead52-132">On receipt of this message, the server-side script refers to its **OnBack** handler for this event, which, as this is the first HTML page, calls the **FinalBack** method.</span></span> <span data-ttu-id="ead52-133">這會讓嚮導先流覽至所顯示的 wizard 頁面，然後再輸入伺服器端 UI。</span><span class="sxs-lookup"><span data-stu-id="ead52-133">This causes the wizard to navigate to the wizard page displayed before entering the server-side UI.</span></span>

<span data-ttu-id="ead52-134">如需這些方法和屬性的完整討論，請參閱 [**WebWizardHost**](/windows/desktop/shell/webwizardhost) 和 [**NewWDEvents**](/windows/desktop/shell/newwdevents) 物件的檔。</span><span class="sxs-lookup"><span data-stu-id="ead52-134">For a complete discussion of these methods and properties, see the documentation for the [**WebWizardHost**](/windows/desktop/shell/webwizardhost) and [**NewWDEvents**](/windows/desktop/shell/newwdevents) objects.</span></span>

## <a name="design-considerations"></a><span data-ttu-id="ead52-135">設計考量</span><span class="sxs-lookup"><span data-stu-id="ead52-135">Design Considerations</span></span>

<span data-ttu-id="ead52-136">HTML 組成每個伺服器端頁面，在 [wizard] 窗格中會正常顯示。</span><span class="sxs-lookup"><span data-stu-id="ead52-136">HTML making up each server-side page is displayed normally in the wizard pane.</span></span> <span data-ttu-id="ead52-137">設計這些頁面時，請記住，無法調整嚮導視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="ead52-137">When designing these pages, bear in mind that a wizard window cannot be resized.</span></span> <span data-ttu-id="ead52-138">因此，頁面應該會經過建立和調整大小，如此一來，就可以避免捲軸捲軸，讓使用者透過 wizard 進行順暢的流覽。</span><span class="sxs-lookup"><span data-stu-id="ead52-138">Pages should therefore be constructed and sized so that scroll bars are avoided whenever possible to provide the user with smooth navigation through the wizard.</span></span>

<span data-ttu-id="ead52-139">每個 HTML 網頁也都必須提供 **OnBack**、 **OnNext** 和 **OnCancel** 事件的處理常式。</span><span class="sxs-lookup"><span data-stu-id="ead52-139">Each HTML page must also provide a handler for **OnBack**, **OnNext**, and **OnCancel** events.</span></span> <span data-ttu-id="ead52-140">**OnNext** 處理常式也會處理 **完成** 事件。</span><span class="sxs-lookup"><span data-stu-id="ead52-140">The **OnNext** handler will also handle the **Finish** event.</span></span> <span data-ttu-id="ead52-141">未執行 **OnBack** 函式的頁面會被視為無效，而且會導致顯示錯誤頁面。</span><span class="sxs-lookup"><span data-stu-id="ead52-141">A page that does not implement an **OnBack** function is considered invalid and will cause an error page to be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ead52-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="ead52-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ead52-143">**WebWizardHost**</span><span class="sxs-lookup"><span data-stu-id="ead52-143">**WebWizardHost**</span></span>](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[<span data-ttu-id="ead52-144">**NewWDEvents**</span><span class="sxs-lookup"><span data-stu-id="ead52-144">**NewWDEvents**</span></span>](/windows/desktop/shell/newwdevents)
</dt> <dt>

[<span data-ttu-id="ead52-145">伺服器端設計</span><span class="sxs-lookup"><span data-stu-id="ead52-145">Server-Side Design</span></span>](pubwiz-server.md)
</dt> </dl>

 

 