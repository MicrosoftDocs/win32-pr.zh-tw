---
title: 在服務工作窗格之間流覽
description: 在服務工作窗格之間流覽
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Windows Media Player 線上商店，導覽
- 線上商店，導覽
- 輸入2個線上商店，導覽
- Windows Media Player 線上商店、服務工作窗格
- 線上商店、服務工作窗格
- 輸入2個線上商店、服務工作窗格
- Windows Media Player 線上商店、工作窗格
- 線上商店、工作窗格
- 類型2線上商店、工作窗格
- 流覽類型2線上商店
- Windows Media Player，服務工作窗格
- Windows Media Player，工作窗格
- 服務工作窗格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86035215f822c67bb40c528f141422977efc8653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300868"
---
# <a name="navigating-between-service-task-panes"></a><span data-ttu-id="f2953-116">在服務工作窗格之間流覽</span><span class="sxs-lookup"><span data-stu-id="f2953-116">Navigating between Service Task Panes</span></span>

<span data-ttu-id="f2953-117">若要在 Windows Media Player 中的服務工作窗格之間流覽，您可以使用 **NavigateTaskPaneURL** 方法，此方法可透過使用 **external** 物件來使用。</span><span class="sxs-lookup"><span data-stu-id="f2953-117">To navigate between service task panes in Windows Media Player, you use the **NavigateTaskPaneURL** method, which is available by using the **window.external** object.</span></span> <span data-ttu-id="f2953-118">當您使用這個方法時，您可以指定三個參數的值：</span><span class="sxs-lookup"><span data-stu-id="f2953-118">When you use this method, you specify values for three parameters:</span></span>

-   <span data-ttu-id="f2953-119">*bstrKeyName*。</span><span class="sxs-lookup"><span data-stu-id="f2953-119">*bstrKeyName*.</span></span> <span data-ttu-id="f2953-120">這是線上商店的索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="f2953-120">This is the key name of the online store.</span></span> <span data-ttu-id="f2953-121">在線上商店中流覽時，請使用目前商店的金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="f2953-121">When navigating within an online store, use the key name of the current store.</span></span>
-   <span data-ttu-id="f2953-122">*bstrTaskPane*。</span><span class="sxs-lookup"><span data-stu-id="f2953-122">*bstrTaskPane*.</span></span> <span data-ttu-id="f2953-123">這個字串包含您想要流覽之服務工作窗格的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2953-123">This string contains the name of the service task pane to which you want to navigate.</span></span>
-   <span data-ttu-id="f2953-124">*bstrParams*。</span><span class="sxs-lookup"><span data-stu-id="f2953-124">*bstrParams*.</span></span> <span data-ttu-id="f2953-125">這個字串包含您想要附加至您想要流覽之服務工作窗格所裝載網頁 URL 的查詢字串參數。</span><span class="sxs-lookup"><span data-stu-id="f2953-125">This string contains the query string parameters you want to append to the URL for the webpage hosted by the service task pane to which you want to navigate.</span></span>

<span data-ttu-id="f2953-126">流覽是由您建立的網頁管理，稱為 [導覽] 頁面。</span><span class="sxs-lookup"><span data-stu-id="f2953-126">Navigation is managed by a webpage you create, called the navigate page.</span></span> <span data-ttu-id="f2953-127">導覽頁面的 URL 是由 ServiceInfo 檔中的 **導覽** 元素所指定。</span><span class="sxs-lookup"><span data-stu-id="f2953-127">The URL for the navigate page is specified by the **Navigate** element in the ServiceInfo document.</span></span> <span data-ttu-id="f2953-128">當您呼叫 **NavigateTaskPaneURL** 時，Windows Media Player 會開啟 [流覽] 頁面，而不是 **ServiceTask1**、 **ServiceTask2** 或 **ServiceTask3** 元素所指定的網頁。</span><span class="sxs-lookup"><span data-stu-id="f2953-128">When you call **NavigateTaskPaneURL**, Windows Media Player opens the navigate page, not the webpage specified by the **ServiceTask1**, **ServiceTask2**, or **ServiceTask3** elements.</span></span> <span data-ttu-id="f2953-129">它是接收 *bstrParams* 所指定之查詢字串的流覽頁面。</span><span class="sxs-lookup"><span data-stu-id="f2953-129">It is the navigate page that receives the query string specified by *bstrParams*.</span></span> <span data-ttu-id="f2953-130">導覽頁面應該包含規則，這些規則可決定導覽之後，在服務工作窗格中顯示的內容。</span><span class="sxs-lookup"><span data-stu-id="f2953-130">The navigate page should contain the rules that determine which content displays in a service task pane after navigation.</span></span>

<span data-ttu-id="f2953-131">例如，假設您想要讓使用者按一下連結，從 **ServiceTask1** 流覽至 **ServiceTask2**。</span><span class="sxs-lookup"><span data-stu-id="f2953-131">For example, suppose you want users to click a link to navigate from **ServiceTask1** to **ServiceTask2**.</span></span> <span data-ttu-id="f2953-132">您可以使用下列 HTML 來建立連結：</span><span class="sxs-lookup"><span data-stu-id="f2953-132">You could use the following HTML to create the link:</span></span>


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



<span data-ttu-id="f2953-133">當使用者按一下影片連結時，Windows Media Player 切換至 **ServiceTask2** 並開啟 [流覽] 頁面，並將下列查詢字串附加至其 URL。</span><span class="sxs-lookup"><span data-stu-id="f2953-133">When the user clicks the Video link, Windows Media Player switches to **ServiceTask2** and opens the navigate page, appending the following query string to its URL.</span></span>


```C++
?From=Music&To=2

```



<span data-ttu-id="f2953-134">From 參數會識別使用者按下連結的頁面，而 To 參數會識別他或她想要流覽的服務工作窗格數目。</span><span class="sxs-lookup"><span data-stu-id="f2953-134">The From parameter identifies the page from which the user clicked the link and the To parameter identifies the number of the service task pane to which he or she wants to navigate.</span></span> <span data-ttu-id="f2953-135"> (請注意，這些參數沒有任何特殊之處。</span><span class="sxs-lookup"><span data-stu-id="f2953-135">(Note that there is nothing special about these parameters.</span></span> <span data-ttu-id="f2953-136">您可以使用任何您想要的參數做為您選擇的任何用途。 ) </span><span class="sxs-lookup"><span data-stu-id="f2953-136">You can use any parameters you like for any purpose you choose.)</span></span>

<span data-ttu-id="f2953-137">例如，下列範例程式碼顯示 ServiceInfo 檔中的 **導覽** 元素：</span><span class="sxs-lookup"><span data-stu-id="f2953-137">For instance, the following example code shows the **Navigate** element in a ServiceInfo document:</span></span>


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



<span data-ttu-id="f2953-138">下列範例顯示產生的 URL （含查詢字串的完整）：</span><span class="sxs-lookup"><span data-stu-id="f2953-138">The resulting URL, complete with query string, is shown in the following example:</span></span>


```C++
https://www.proseware.com/service/html/navigate.asp?From=Music&To=2

```



<span data-ttu-id="f2953-139">下列範例程式碼顯示導覽頁面：</span><span class="sxs-lookup"><span data-stu-id="f2953-139">The following example code shows the navigate page:</span></span>


```C++
<%
    Dim sURL
    Dim sQS
    Dim sTo

    sURL = ""
    sQS = Request.ServerVariables("QUERY_STRING")
    sTo = "" & Request.QueryString("To")
 
    Select Case sTo
       Case "1" sURL = sURL & "Music_Music.asp"
       Case "2" sURL = sURL & "Music_Video.asp"
       Case "3" sURL = sURL & "Music_Radio.asp"
       Case Else sURL = sURL & "Music_Music.asp"
    End Select
     
    sURL = sURL & "?" & sQS

    Response.Redirect(sURL)    
%>

```



<span data-ttu-id="f2953-140">上述程式碼只會建立 URL，並將瀏覽器重新導向至該 URL。</span><span class="sxs-lookup"><span data-stu-id="f2953-140">The preceding code simply creates a URL and redirects the browser to it.</span></span> <span data-ttu-id="f2953-141">首先，程式碼會從 URL 查詢字串和查詢字串本身抓取值。</span><span class="sxs-lookup"><span data-stu-id="f2953-141">First, the code retrieves To values from the URL query string and the query string itself.</span></span> <span data-ttu-id="f2953-142">它會使用 To 參數的值來決定要顯示的頁面。</span><span class="sxs-lookup"><span data-stu-id="f2953-142">It uses the value of the To parameter to determine which page to display.</span></span> <span data-ttu-id="f2953-143">然後，它會將原始查詢字串附加至 URL。</span><span class="sxs-lookup"><span data-stu-id="f2953-143">It then appends the original query string to the URL.</span></span> <span data-ttu-id="f2953-144">最後，它會使用類似下列的 URL 來導覽瀏覽器：</span><span class="sxs-lookup"><span data-stu-id="f2953-144">Finally, it navigates the browser using a URL similar to the following:</span></span>


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



<span data-ttu-id="f2953-145">當您以這種方式執行流覽時，請務必指定 [SelectedTaskPane](external-selectedtaskpane.md) ，以確定已反白顯示正確的工作按鈕。</span><span class="sxs-lookup"><span data-stu-id="f2953-145">Whenever you perform navigation in this manner, be sure to specify [External.SelectedTaskPane](external-selectedtaskpane.md) to ensure that the correct task button is highlighted.</span></span>

-   <span data-ttu-id="f2953-146">**警告** 請小心使用查詢字串參數進行導覽。</span><span class="sxs-lookup"><span data-stu-id="f2953-146">**Warning** Be careful how you use query string parameters for navigation.</span></span>

<span data-ttu-id="f2953-147">任何建立 ASX 播放清單的人都可以提供 HTMLView 網頁。</span><span class="sxs-lookup"><span data-stu-id="f2953-147">HTMLView webpages can be provided by anyone who creates an ASX playlist.</span></span> <span data-ttu-id="f2953-148">這表示惡意網站可使用 **NavigateTaskPaneURL** 將查詢字串值傳遞至您的線上商店。</span><span class="sxs-lookup"><span data-stu-id="f2953-148">This means that malicious websites can pass query string values to your online store using **NavigateTaskPaneURL**.</span></span> <span data-ttu-id="f2953-149">您必須規劃這種可能性，讓您的線上商店保持安全。</span><span class="sxs-lookup"><span data-stu-id="f2953-149">You must plan for this possibility to keep your online store secure.</span></span> <span data-ttu-id="f2953-150">例如，如果您的線上商店只是向使用者顯示查詢字串值，惡意網站可能會顯示未預期的文字。</span><span class="sxs-lookup"><span data-stu-id="f2953-150">For example, if your online store simply displays a query string value to the user, a malicious website could display unexpected text.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2953-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2953-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2953-152">**顯示 Windows Media Player 中的網頁**</span><span class="sxs-lookup"><span data-stu-id="f2953-152">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="f2953-153">**導覽元素**</span><span class="sxs-lookup"><span data-stu-id="f2953-153">**Navigate Element**</span></span>](navigate-element.md)
</dt> <dt>

[<span data-ttu-id="f2953-154">**類型2線上商店的流覽**</span><span class="sxs-lookup"><span data-stu-id="f2953-154">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




