---
title: 自訂資料夾的 Web View
description: Web view 是一種功能強大且有彈性的方式，可使用 Windows 檔案總管來顯示 Shell 資料夾內容的相關資訊。
ms.assetid: a894df21-bcc6-4760-b7d7-9bf95a0dba7f
keywords:
- Web 視圖
- 傳統樣式
- Web 樣式
- 橫幅
- FileList 區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e364551d461eff6ae17a780bafc0b69182a1f16f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681706"
---
# <a name="customizing-a-folders-web-view"></a><span data-ttu-id="88955-108">自訂資料夾的 Web View</span><span class="sxs-lookup"><span data-stu-id="88955-108">Customizing a Folder's Web View</span></span>

<span data-ttu-id="88955-109">\[只有在 Windows XP 或更早版本才支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="88955-109">\[This feature is supported only under Windows XP or earlier.</span></span> <span data-ttu-id="88955-110">\]</span><span class="sxs-lookup"><span data-stu-id="88955-110">\]</span></span>

<span data-ttu-id="88955-111">Web view 是一種功能強大且有彈性的方式，可使用 Windows 檔案總管來顯示 Shell 資料夾內容的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88955-111">A Web view is a powerful and flexible way to use the Windows Explorer to display information about the contents of a Shell folder.</span></span>

-   [<span data-ttu-id="88955-112">簡介</span><span class="sxs-lookup"><span data-stu-id="88955-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="88955-113">使用 Web View 範本</span><span class="sxs-lookup"><span data-stu-id="88955-113">Using the Web View Template</span></span>](#using-the-web-view-template)
    -   [<span data-ttu-id="88955-114">範本主體</span><span class="sxs-lookup"><span data-stu-id="88955-114">The Template Body</span></span>](#the-template-body)
    -   [<span data-ttu-id="88955-115">範本標頭</span><span class="sxs-lookup"><span data-stu-id="88955-115">The Template Head</span></span>](#the-template-head)
-   [<span data-ttu-id="88955-116">總結</span><span class="sxs-lookup"><span data-stu-id="88955-116">Summary</span></span>](#summary)

## <a name="introduction"></a><span data-ttu-id="88955-117">簡介</span><span class="sxs-lookup"><span data-stu-id="88955-117">Introduction</span></span>

<span data-ttu-id="88955-118">Windows 提供使用者兩種主要方式來查看和流覽 Shell 命名空間。</span><span class="sxs-lookup"><span data-stu-id="88955-118">Windows offers users two primary ways to view and navigate the Shell namespace.</span></span> <span data-ttu-id="88955-119">最熟悉的是傳統樣式，類似于熟悉的 Windows 檔案管理員。</span><span class="sxs-lookup"><span data-stu-id="88955-119">The most familiar of these, the Classic style, is similar to the familiar Windows File Manager.</span></span> <span data-ttu-id="88955-120">右窗格會以下列五種格式的其中一種來列出目前所選資料夾的內容：大型圖示、小圖示、清單、詳細資料和縮圖。</span><span class="sxs-lookup"><span data-stu-id="88955-120">The right pane lists the contents of the currently selected folder in one of five formats: Large Icon, Small Icon, List, Details, and Thumbnail.</span></span> <span data-ttu-id="88955-121">與 Windows 檔案管理員的主要差異在於左窗格，看起來非常類似 Windows Internet Explorer 的 [Explorer] 欄。</span><span class="sxs-lookup"><span data-stu-id="88955-121">The major difference from Windows File Manager is the left pane, which looks very similar to the Explorer bar of Windows Internet Explorer.</span></span> <span data-ttu-id="88955-122">它可以調整大小或移除，而且除了熟悉的檔案系統樹狀目錄（例如搜尋窗格）之外，還可以顯示數個窗格。</span><span class="sxs-lookup"><span data-stu-id="88955-122">It can be resized or removed, and it can display several panes in addition to the familiar file system tree, such as a search pane.</span></span>

> [!Note]  
> <span data-ttu-id="88955-123">本檔中的資訊不適用於 Windows XP，所討論的技術只適用于舊版的 Windows。</span><span class="sxs-lookup"><span data-stu-id="88955-123">The information in this document does not apply to Windows XP, the techniques discussed apply only to earlier versions of Windows.</span></span>

 

<span data-ttu-id="88955-124">下圖顯示傳統樣式的 [印表機] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="88955-124">The following illustration shows the Printers folder in Classic style.</span></span>

![印表機資料夾的傳統樣式。](images/webview1.png)

<span data-ttu-id="88955-126">傳統樣式適用于一般檔系統資料夾和檔案。</span><span class="sxs-lookup"><span data-stu-id="88955-126">The Classic style works reasonably well for normal file system folders and files.</span></span> <span data-ttu-id="88955-127">不過，隨著 Windows 95 的推出，檔案系統已發展成命名空間。</span><span class="sxs-lookup"><span data-stu-id="88955-127">However, with the introduction of Windows 95, the file system has evolved into the namespace.</span></span> <span data-ttu-id="88955-128">命名空間可讓您建立 *虛擬資料夾*，例如印表機或網路鄰近地區，以代表與一般檔系統資料夾非常不同的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="88955-128">The namespace allows the creation of *virtual folders*, such as Printers or Network Neighborhood, that can represent very different types of information than a normal file system folder.</span></span>

<span data-ttu-id="88955-129">Web 樣式（也稱為 Web view）提供更有彈性且功能更強大的方式來呈現與傳統樣式相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="88955-129">The Web style, also known as a Web view, offers a more flexible and powerful way of presenting information than Classic style.</span></span> <span data-ttu-id="88955-130">在 Web 視圖中，使用者基本上會使用 Internet Explorer 來查看和流覽命名空間。</span><span class="sxs-lookup"><span data-stu-id="88955-130">In a Web view, the user basically views and navigates the namespace using Internet Explorer.</span></span> <span data-ttu-id="88955-131">Web view 的基本版面配置類似于傳統樣式。</span><span class="sxs-lookup"><span data-stu-id="88955-131">The basic layout of a Web view is similar to Classic style.</span></span> <span data-ttu-id="88955-132">Explorer 列沒有變更。</span><span class="sxs-lookup"><span data-stu-id="88955-132">The Explorer bar is unchanged.</span></span> <span data-ttu-id="88955-133">不過，檔案清單所佔用的區域會變成一般用途的顯示區域，該區域實際上是網頁。</span><span class="sxs-lookup"><span data-stu-id="88955-133">However, the region that was occupied by the file list becomes a general-purpose display area that is effectively a webpage.</span></span> <span data-ttu-id="88955-134">Web view 仍會用來顯示資料夾內容的相關資訊，但在顯示的資訊或方式方面有一些限制。</span><span class="sxs-lookup"><span data-stu-id="88955-134">A Web view is still used to display information about the contents of a folder, but there are few constraints on what information is displayed, or how.</span></span> <span data-ttu-id="88955-135">每個資料夾都可以有自己的網頁視圖，其自訂為符合其特定功能。</span><span class="sxs-lookup"><span data-stu-id="88955-135">Each folder can have its own Web view, customized to suit its particular features.</span></span>

<span data-ttu-id="88955-136">下圖顯示 [印表機] 資料夾的 Web 視圖， (先前的傳統樣式) 所示。</span><span class="sxs-lookup"><span data-stu-id="88955-136">The following illustration shows a Web view of the Printers folder (shown previously in Classic style).</span></span>

![[印表機] 資料夾的預設 web 視圖。](images/webview2.png)

<span data-ttu-id="88955-138">Web 視圖與傳統網頁非常類似，是由 HTML 範本所控制。</span><span class="sxs-lookup"><span data-stu-id="88955-138">Much like conventional webpages, Web views are controlled by an HTML-based template.</span></span> <span data-ttu-id="88955-139">撰寫 Web view 範本與撰寫網頁幾乎完全相同，而且在內容和版面配置中提供相同程度的彈性。</span><span class="sxs-lookup"><span data-stu-id="88955-139">Authoring a Web view template is nearly identical to authoring a webpage and provides the same degree of flexibility in content and layout of information.</span></span> <span data-ttu-id="88955-140">Web view 範本可以使用動態 HTML (DHTML) 和腳本來回應事件，例如使用者按一下專案。</span><span class="sxs-lookup"><span data-stu-id="88955-140">Web view templates can use Dynamic HTML (DHTML) and scripting to respond to events, such as a user clicking an item.</span></span> <span data-ttu-id="88955-141">它們也可以裝載物件，讓它們可以從資料夾或其內容中取得和顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="88955-141">They can also host objects that allow them to obtain and display information from the folder or its contents.</span></span>

<span data-ttu-id="88955-142">使用者可以藉由啟動 Windows 檔案總管、按一下 [ **view** ] 功能表上的 [**資料夾選項**]，然後選取此選項： [**在資料夾中啟用 Web 內容**] 來選擇 Web 視圖。</span><span class="sxs-lookup"><span data-stu-id="88955-142">The user can choose a Web view by starting Windows Explorer, clicking **Folder Options** on the **View** menu, and selecting this option: **Enable Web content in folders**.</span></span> <span data-ttu-id="88955-143">不過，使用者也可以開始 Internet Explorer，並 **按一下 [流覽] 功能表、** 指向 [ **Explorer** 列]，然後按一下 [ **資料夾**]，將瀏覽器指向檔案系統。</span><span class="sxs-lookup"><span data-stu-id="88955-143">However, the user can also start Internet Explorer and point the browser at the file system by clicking the **View** menu, pointing to **Explorer Bar**, and clicking **Folders**.</span></span> <span data-ttu-id="88955-144">在 Web 視圖中，Internet Explorer 和 Windows 檔案總管幾乎沒有任何差異。</span><span class="sxs-lookup"><span data-stu-id="88955-144">In a Web view, there is virtually no difference between Internet Explorer and Windows Explorer.</span></span>

<span data-ttu-id="88955-145">在右窗格的左側，印表機網頁視圖會顯示具有資料夾名稱和圖示的橫幅，後面接著資料夾的相關資訊區塊。</span><span class="sxs-lookup"><span data-stu-id="88955-145">On the left side of the right pane, the Printers Web view displays a banner with the folder's name and icon, followed by a block of information about the folder.</span></span> <span data-ttu-id="88955-146">一般檔案清單會佔用頁面的右側。</span><span class="sxs-lookup"><span data-stu-id="88955-146">The usual file list occupies the right side of the page.</span></span>

<span data-ttu-id="88955-147">當使用者按一下某個專案時，該專案的詳細資訊就會出現在資訊區塊中。</span><span class="sxs-lookup"><span data-stu-id="88955-147">When a user clicks an item, detailed information about the item appears in the information block.</span></span> <span data-ttu-id="88955-148">[印表機] Web 視圖實際上會顯示傳統樣式中所提供的相同資訊，但它會以更容易使用的格式來執行。</span><span class="sxs-lookup"><span data-stu-id="88955-148">The Printers Web view actually displays much the same information that is available in Classic style, but it does so in a more usable format.</span></span> <span data-ttu-id="88955-149">但是，Web view 並不只是顯示傳統樣式資訊的不同方式。</span><span class="sxs-lookup"><span data-stu-id="88955-149">However, a Web view is not simply a different way to display Classic style information.</span></span> <span data-ttu-id="88955-150">例如，您可以在資訊區塊底下顯示有用網站的連結，這是傳統樣式中無法使用的功能。</span><span class="sxs-lookup"><span data-stu-id="88955-150">For example, a link to a useful website can be displayed below the information block, a feature that is not available in Classic style.</span></span> <span data-ttu-id="88955-151">如果使用者按一下此連結，則會顯示該網站。</span><span class="sxs-lookup"><span data-stu-id="88955-151">If the user clicks the link, the site will be displayed.</span></span>

<span data-ttu-id="88955-152">上圖所示的 [印表機] Web 視圖類似于傳統樣式，因為基礎 Web view 範本 (htt 檔案) 是以這種方式撰寫的。</span><span class="sxs-lookup"><span data-stu-id="88955-152">The Printers Web view shown in the preceding illustration is similar to the Classic style, because the underlying Web view template (an .htt file) was written that way.</span></span> <span data-ttu-id="88955-153">例如，不會直接由 Web view 範本產生檔案清單。</span><span class="sxs-lookup"><span data-stu-id="88955-153">The list of files, for instance, is not generated by the Web view template directly.</span></span> <span data-ttu-id="88955-154">它是由 Web view 範本所裝載的 [**WebViewFolderContents**](webviewfoldercontents.md) 物件所建立和顯示。</span><span class="sxs-lookup"><span data-stu-id="88955-154">It is created and displayed by a [**WebViewFolderContents**](webviewfoldercontents.md) object hosted by the Web view template.</span></span> <span data-ttu-id="88955-155">物件的方法和屬性可讓 Web view 控制其版面配置，並取得特定專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88955-155">The object's methods and properties allow the Web view to control its layout and obtain information about particular items.</span></span> <span data-ttu-id="88955-156">橫幅和資訊區塊的內容和配置都是在 Web view 範本中指定。</span><span class="sxs-lookup"><span data-stu-id="88955-156">The content and layout of the banner and information block is specified in the Web view template.</span></span>

<span data-ttu-id="88955-157">由於 Web view 支援 DHTML，因此範本也可以用來處理使用者互動。</span><span class="sxs-lookup"><span data-stu-id="88955-157">Because a Web view supports DHTML, the template can also be used to handle user interaction.</span></span> <span data-ttu-id="88955-158">例如，當使用者按一下其中一個印表機圖示時， **WebViewFolderIcon** 物件就會引發 [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) 事件。</span><span class="sxs-lookup"><span data-stu-id="88955-158">For instance, when a user clicks one of the printer icons, the **WebViewFolderIcon** object fires a [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) event.</span></span> <span data-ttu-id="88955-159">此範本會使用以腳本撰寫的 DHTML 事件處理常式，以抓取要求的資訊並將它顯示在資訊區塊中。</span><span class="sxs-lookup"><span data-stu-id="88955-159">The template uses a DHTML event handler written in script to retrieve the requested information and display it in the information block.</span></span>

<span data-ttu-id="88955-160">[印表機] 資料夾的這個簡單範例就是使用網頁視圖的唯一方式。</span><span class="sxs-lookup"><span data-stu-id="88955-160">This simple example for the Printers folder is by no means the only way to use a Web view.</span></span> <span data-ttu-id="88955-161">藉由撰寫您自己的範本，如有必要，您可以使用 Web view 來顯示資訊，並以您最有效的方式與使用者互動。</span><span class="sxs-lookup"><span data-stu-id="88955-161">By writing your own template and, if necessary, objects, you can use a Web view to display information and interact with the user in whatever way you find most effective.</span></span> <span data-ttu-id="88955-162">請注意，目前 Web view 範本只會顯示系統定義的虛擬資料夾。</span><span class="sxs-lookup"><span data-stu-id="88955-162">Note that, at present, Web view templates only display system-defined virtual folders.</span></span> <span data-ttu-id="88955-163">雖然開發人員可以藉由執行命名空間延伸來建立虛擬資料夾，但是它們必須使用 [命名空間](/windows/desktop/shell/nse-works) 延伸模組中所述的技術來顯示它。</span><span class="sxs-lookup"><span data-stu-id="88955-163">Although developers can create a virtual folder by implementing a namespace extension, they must use the techniques described in [Namespace Extensions](/windows/desktop/shell/nse-works) to display it.</span></span>

## <a name="using-the-web-view-template"></a><span data-ttu-id="88955-164">使用 Web View 範本</span><span class="sxs-lookup"><span data-stu-id="88955-164">Using the Web View Template</span></span>

<span data-ttu-id="88955-165">在 Web view 中顯示資料的方式，可以藉由修改資料夾的 Desktop.ini 檔案，以有限的方式自訂。</span><span class="sxs-lookup"><span data-stu-id="88955-165">The way data is displayed in a Web view can be customized in a limited way by modifying a folder's Desktop.ini file.</span></span> <span data-ttu-id="88955-166">如需詳細資訊，請參閱 [使用 Desktop.ini自訂資料夾 ](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) 。</span><span class="sxs-lookup"><span data-stu-id="88955-166">See [Customizing Folders with Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) for details.</span></span> <span data-ttu-id="88955-167">更有彈性且功能更強大的自訂 Web 視圖方式，就是建立自訂的 Web view 範本。</span><span class="sxs-lookup"><span data-stu-id="88955-167">A much more flexible and powerful way to customize a Web view is to create a custom Web view template.</span></span>

<span data-ttu-id="88955-168">Web view 範本會控制在 Web 視圖中顯示的內容，以及如何進行。</span><span class="sxs-lookup"><span data-stu-id="88955-168">The Web view template controls what is displayed in a Web view and how.</span></span> <span data-ttu-id="88955-169">它使用標準 HTML、DHTML 和腳本技術來取得和顯示資訊，並與使用者互動。</span><span class="sxs-lookup"><span data-stu-id="88955-169">It uses standard HTML, DHTML, and scripting techniques to obtain and display information and interact with the user.</span></span> <span data-ttu-id="88955-170">本節討論如何藉由檢查簡單的範本（htt）來建立 Web 視圖。</span><span class="sxs-lookup"><span data-stu-id="88955-170">This section discusses how to create a Web view by examining a simple template—Generic.htt.</span></span>


```
<html>
    <style>
    <!-- This section defines a variety of styles that can be used
     when displaying the document -->
        body        {font: 8pt/10pt verdana; margin: 0}
        #Banner     {position: absolute; width: 100%; height: 88px; background: URL(res://webvw.dll/folder.gif) no-repeat top left}
        #MiniBanner {position: absolute; width: 100%; height: 32px; background: window}
        #Icon       {position: absolute; left: 11px; top: 12px; width: 64px; height: 64px}
        #FileList   {position: absolute; left: 30%; top: 88px; width: 1px; height: 1px}
        #Info       {position: absolute; top: 88px; width: 30%; background: window; overflow: auto}
        p       {margin-left: 20px; margin-right: 8px}
        p.Title     {font: 16pt/16pt verdana; font-weight: bold; color: #0099FF}
        a:link      {color: #FF6633}
        a:visited   {color: #0099FF}
        a:active    {color: black}
    </style>

    <head>
        <!-- allow references to any resources you might add to the
         folder -->
        <base href="%THISDIRPATH%\">

        <script language="JavaScript">
        
        <!-- This section defines a number of JavaScript utilities -->
            var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br><br>To get information about any of them, click the items icon.<br><br>";
            var L_Multiple_Text = " objects selected.";

            function FixSize() {
            // this function handles layout issues not covered by the style sheet

                var hideTop = 200;
                var hideLeft    = 400;
                var miniHeight  = 32;

                if (200 > document.body.clientHeight) {
                //A short window. Use the minibanner
                    document.all.Banner.style.visibility = "hidden";
                    document.all.MiniBanner.style.visibility = "visible";
                    document.all.FileList.style.top = 32;
                    document.all.Info.style.top = 32;
                }

                else {
                //A normal window. Use the normal banner
                    document.all.Banner.style.visibility = "visible";
                    document.all.MiniBanner.style.visibility = "hidden";
                    document.all.FileList.style.top = (document.all.Banner.offsetHeight - 32) + "px";
                    document.all.Info.style.top = (document.all.Banner.offsetHeight) + "px";
                    document.all.Rule.style.width = (document.body.clientWidth > 84 ? document.body.clientWidth - 84 : 0) + "px";     
                }
                if (400 > document.body.clientWidth) {
                //A narrow window. Hide the Info region and expand the file list region
                    document.all.Info.style.visibility = "hidden";
                    document.all.FileList.style.pixelLeft = 0;
                    document.all.FileList.style.pixelTop = document.all.Info.style.pixelTop;
                }

                else {
                //Normal width
                    document.all.Info.style.visibility = "visible";
                    document.all.FileList.style.pixelLeft = document.all.Info.style.pixelWidth;
                }
                document.all.FileList.style.pixelWidth = document.body.clientWidth - document.all.FileList.style.pixelLeft;
                document.all.FileList.style.pixelHeight = document.body.clientHeight - document.all.FileList.style.pixelTop;
                document.all.Info.style.pixelHeight = document.body.clientHeight - document.all.Info.style.pixelTop;
            }

            function Init() {
                /* Set the initial layout and have FixSize() called whenever the window is resized*/
                window.onresize = FixSize;
                FixSize();
                TextBlock.innerHTML = L_Intro_Text;
            }
        </script>

        <script language="JavaScript" for="FileList" event="SelectionChanged">
            // Updates the TextBlock region when an item is selected
            var data;
            var text;

            // name
            text = "<b>" + FileList.FocusedItem.Name + "</b>";

            // comment
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 3);
            if (data)
                text += "<br>" + data;

            // documents
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 1);
            if (data)
                text += "<br><br>" + FileList.Folder.GetDetailsOf(null, 1) + ": " + data;

            // status
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 2);
            if (data)
                text += "<br><br><b><font color=red>" + data + "</font></b>";

            // tip?
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, -1);
            if (data != "" && data != FileList.FocusedItem.Name)
                text += "<br><br>" + data;

            TextBlock.innerHTML = text;
        </script>
    </head>
<!-- The body of the document controls the actual data display.
 It uses several scripting objects to communicate with the
 namespace folder, and calls on the JavaScript objects defined
 in the header to handle much of the processing -->
    <body scroll=no onload="Init()">

        <!-- The normal banner. This banner displays the folder
         name and icon at the top of the WebView pane. This banner
         is used if the WebView pane is sufficiently large to
         display the icon and still have room for some information -->
        <div id="Banner" style="visibility: hidden">
            <!-- Display the folder name using a table with nowrap
             to prevent word wrapping. Explorer will replace
              %THISDIRNAME% with the current folder name -->
            <table class="clsStd"><tr><td nowrap>
                <p class=Title style="margin-left: 104px; margin-top: 16px">
                %THISDIRNAME% 
            </td></tr></table>
            <!-- this is more efficient than a long graphic, but it has to be adjusted in FixSize() -->
            <hr id="Rule" size=1px color=black style="position: absolute; top: 44px; left: 84px">
            <!-- Load the WebViewFolderIcon object, which extracts the folder's icon -->
            <object id=Icon classid="clsid:e5df9d10-3b52-11d1-83e8-00a0c90dc849">
                <param name="scale" value=200>
            </object>
        </div>

        <!-- The mini banner. This banner is used when the
         WebView pane is too short to display the icon. Instead,
          it displays only the folder name -->
        <div id="MiniBanner" style="visibility: hidden">
            <!-- use a table with nowrap to prevent word wrapping -->
            <table class="clsStd"><tr><td nowrap>
                <p class=Title style="margin-left: 16px; margin-top: 4px">
                %THISDIRNAME%
            </td></tr></table>
        </div>

        <!-- The Info region. This displays the information
         associated with a folder or file. Javascript in the header
         is used to generate the regions contents by by assigning
         a text block to TextBlock.innerHTML -->
        <div id="Info">
            <p style="margin-top: 16px");
            <span id="TextBlock">
            </span>
        </div>
        <!-- end left info panel -->

        <!-- Load the WebViewFolderContents object. This object
         returns information on the contents of the folder that
          can be used in the information display.  -->
        <object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>

    </body>
</html>
            
```



<span data-ttu-id="88955-171">建立您自己的 Web view 範本的簡單方法，就是使用 htt 並加以修改。</span><span class="sxs-lookup"><span data-stu-id="88955-171">A simple way to create your own Web view template is to take Generic.htt and modify it.</span></span> <span data-ttu-id="88955-172">因為它相當有限，所以您也應該查看其他更複雜的範例，以瞭解其他想法。</span><span class="sxs-lookup"><span data-stu-id="88955-172">Because it is rather limited, you should also look at other, more complex examples for additional ideas.</span></span> <span data-ttu-id="88955-173">您可以搜尋系統，找出所有 Web view 範本所使用的 htt 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="88955-173">You can find them by searching your system for the .htt extension used by all Web view templates.</span></span> <span data-ttu-id="88955-174">如果您想要建立資料夾的自訂範本，您應該從預設的 htt 範本開始，這個範本通常儲存在 C： \\ Winnt \\ Web 或 c： \\ Windows \\ Web 中。</span><span class="sxs-lookup"><span data-stu-id="88955-174">If you want to create a custom template for a folder, you should start with the default Folder.htt template, which is usually stored in either C:\\Winnt\\Web or C:\\Windows\\Web.</span></span> <span data-ttu-id="88955-175">請注意，這些檔案會定義為隱藏，因此您可能需要修改 Windows 檔案總管設定才能加以查看。</span><span class="sxs-lookup"><span data-stu-id="88955-175">Note that these files are defined as hidden, so you may need to modify your Windows Explorer settings to view them.</span></span> <span data-ttu-id="88955-176">建立 htt 檔案之後，應該將它標示為唯讀並隱藏。</span><span class="sxs-lookup"><span data-stu-id="88955-176">Once an .htt file is created, it should be marked as read-only and hidden.</span></span>

<span data-ttu-id="88955-177">Web view 範本使用 htt 副檔名，因為它們與傳統 .htm 檔稍有不同。</span><span class="sxs-lookup"><span data-stu-id="88955-177">Web view templates use the .htt extension because they differ slightly from conventional .htm documents.</span></span> <span data-ttu-id="88955-178">主要差異在於 htt 檔案中的數個特殊變數，系統會以目前的命名空間值取代這些變數。</span><span class="sxs-lookup"><span data-stu-id="88955-178">The main difference is several special variables in .htt files that the system replaces with the current namespace values.</span></span> <span data-ttu-id="88955-179">% THISDIR% 和% THISDIRPATH% 變數代表目前選取之資料夾的名稱和路徑。</span><span class="sxs-lookup"><span data-stu-id="88955-179">The %THISDIR% and %THISDIRPATH% variables represent the name and path of the currently selected folder.</span></span> <span data-ttu-id="88955-180">% TEMPLATEDIR% 變數代表儲存 Web 視圖樣式表單的資料夾。</span><span class="sxs-lookup"><span data-stu-id="88955-180">The %TEMPLATEDIR% variable represents the folder where the Web view style sheets are stored.</span></span>

<span data-ttu-id="88955-181">如同大多數的 HTML 範本，htt 檔有兩個基本部分：本文和 head。</span><span class="sxs-lookup"><span data-stu-id="88955-181">Like most HTML templates, .htt files have two basic parts: a body and a head.</span></span> <span data-ttu-id="88955-182">範本主體會控制 Web view 的基本版面配置，並載入用來與命名空間進行通訊和顯示資訊的物件。</span><span class="sxs-lookup"><span data-stu-id="88955-182">The template body controls the basic layout of the Web view and loads the objects used to communicate with the namespace and display information.</span></span> <span data-ttu-id="88955-183">此標頭包含的腳本和函式可進行工作，例如處理調整大小和取得資料夾中的資訊。</span><span class="sxs-lookup"><span data-stu-id="88955-183">The head contains scripts and functions that do tasks such as handling resizing and obtaining information from the folder.</span></span> <span data-ttu-id="88955-184">大部分的範本（包括 htt）也包含樣式表單。</span><span class="sxs-lookup"><span data-stu-id="88955-184">Most templates, including Generic.htt, also include a style sheet.</span></span> <span data-ttu-id="88955-185">一般情況下，最好將樣式表單資訊包含在範本中。</span><span class="sxs-lookup"><span data-stu-id="88955-185">In general, it is better to include the style sheet information in your template.</span></span> <span data-ttu-id="88955-186">當 Web 視圖與遠端命名空間搭配使用時，不同的樣式表單可能無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="88955-186">Separate style sheets may not work properly when a Web view is used with remote namespaces.</span></span>

### <a name="the-template-body"></a><span data-ttu-id="88955-187">範本主體</span><span class="sxs-lookup"><span data-stu-id="88955-187">The Template Body</span></span>

<span data-ttu-id="88955-188">範本的主體會指定 Web view 將呈現的內容。</span><span class="sxs-lookup"><span data-stu-id="88955-188">The body of the template specifies what will be presented by a Web view.</span></span> <span data-ttu-id="88955-189">此外，也會載入用來顯示資訊的物件，以及與命名空間資料夾進行通訊的物件。</span><span class="sxs-lookup"><span data-stu-id="88955-189">It is also where the objects used to display information and communicate with namespace folders are loaded.</span></span> <span data-ttu-id="88955-190">Htt 所定義的配置與上一節中的圖所示的版面配置類似。</span><span class="sxs-lookup"><span data-stu-id="88955-190">The layout defined by Generic.htt is similar to that shown in the illustration in the previous section.</span></span> <span data-ttu-id="88955-191">有三個顯示區域：視圖左邊的橫幅和資訊區塊，以及右邊的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="88955-191">There are three display regions: the banner and information block on the left side of the view, and the file list on the right.</span></span>

<span data-ttu-id="88955-192">這些區域是樣式表單和 DHTML 所要使用的所有指派識別碼。</span><span class="sxs-lookup"><span data-stu-id="88955-192">The regions are all assigned identifiers to be used by the style sheet and DHTML.</span></span> <span data-ttu-id="88955-193">如下一節所述，有兩個可能的橫幅，其識別碼為 "橫幅" 和 "MiniBanner"。</span><span class="sxs-lookup"><span data-stu-id="88955-193">As discussed in the next section, there are two possible banners, with identifiers of "Banner" and "MiniBanner".</span></span> <span data-ttu-id="88955-194">資訊區塊區域的識別碼是「資訊」。</span><span class="sxs-lookup"><span data-stu-id="88955-194">The identifier of the information block's region is "Info".</span></span> <span data-ttu-id="88955-195">檔案清單物件的識別碼是 "FileList"。</span><span class="sxs-lookup"><span data-stu-id="88955-195">The file list object's identifier is "FileList".</span></span> <span data-ttu-id="88955-196">區域 [版面](#controlling-the-web-view-layout) 配置的詳細資料是由樣式表單和 Microsoft JScript 函式 [FixSize](#adjusting-the-layout-by-using-the-fixsize-function)所處理，本章節稍後會討論。</span><span class="sxs-lookup"><span data-stu-id="88955-196">The details of the region's [layout](#controlling-the-web-view-layout) are handled by the style sheet and a Microsoft JScript function, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), which is discussed later in the chapter.</span></span>

### <a name="the-banner-region"></a><span data-ttu-id="88955-197">橫幅區域</span><span class="sxs-lookup"><span data-stu-id="88955-197">The Banner Region</span></span>

<span data-ttu-id="88955-198">橫幅位於 Web view 左上角的 [顯示] 的頂端。</span><span class="sxs-lookup"><span data-stu-id="88955-198">The banner is located at the top of the display, in the upper-left corner of the Web view.</span></span> <span data-ttu-id="88955-199">一般橫幅會顯示其內容會顯示在右側檔案清單中之資料夾的名稱和圖示。</span><span class="sxs-lookup"><span data-stu-id="88955-199">The normal banner displays the name and icon of the folder whose contents are displayed in the file list on the right.</span></span> <span data-ttu-id="88955-200">但是，如果視窗變得太短，則圖示下方可能沒有足夠的空間來顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="88955-200">However, if the window becomes too short, there may be no room below the icon to display information.</span></span> <span data-ttu-id="88955-201">基於這個理由，htt 也會定義只顯示資料夾名稱的 minibanner。</span><span class="sxs-lookup"><span data-stu-id="88955-201">For this reason, Generic.htt also defines a minibanner that only displays the folder name.</span></span> <span data-ttu-id="88955-202">這兩個橫幅一開始會定義為隱藏。</span><span class="sxs-lookup"><span data-stu-id="88955-202">Both banners are initially defined as hidden.</span></span> <span data-ttu-id="88955-203">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) 會選擇要顯示哪一個，並將其設定為「可見」。</span><span class="sxs-lookup"><span data-stu-id="88955-203">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) chooses which one to display and sets it to "visible".</span></span>

<span data-ttu-id="88955-204">一般 htt 的一般橫幅定義如下：</span><span class="sxs-lookup"><span data-stu-id="88955-204">The normal banner for Generic.htt is defined by:</span></span>


```
<div id="Banner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
    <p class=Title style="margin-left: 104px; margin-top: 16px">
        %THISDIRNAME% 
    </td></tr></table>
    <hr id="Rule" size=1px color=black style="position: absolute; top: 44px; left: 84px">
    <object id=Icon classid="clsid:e5df9d10-3b52-11d1-83e8-00a0c90dc849">
        <param name="scale" value=200>
    </object>
</div>
                    
```



<span data-ttu-id="88955-205">橫幅區段的第一個部分會在其下顯示具有水準規則的標題。</span><span class="sxs-lookup"><span data-stu-id="88955-205">The first part of the banner section displays the title with a horizontal rule underneath it.</span></span> <span data-ttu-id="88955-206">資料表標記是用來控制其位置。</span><span class="sxs-lookup"><span data-stu-id="88955-206">Table tags are used to control its position.</span></span> <span data-ttu-id="88955-207">Nowrap 屬性設定為</span><span class="sxs-lookup"><span data-stu-id="88955-207">The nowrap attribute is set for the</span></span> <TD> <span data-ttu-id="88955-208">標記以防止自動換行。</span><span class="sxs-lookup"><span data-stu-id="88955-208">tag to prevent word wrapping.</span></span> <span data-ttu-id="88955-209">系統會將% THISDIRNAME% 取代為目前資料夾的名稱。</span><span class="sxs-lookup"><span data-stu-id="88955-209">The system will replace %THISDIRNAME% with the name of the current folder.</span></span> <span data-ttu-id="88955-210">為了簡單起見， **WebViewFolderIcon** 物件的識別碼為 "Icon"，接著會載入以解壓縮並顯示資料夾的圖示。</span><span class="sxs-lookup"><span data-stu-id="88955-210">A **WebViewFolderIcon** object, with an identifier of "Icon" for simplicity, is then loaded to extract and display the folder's icon.</span></span>

<span data-ttu-id="88955-211">Minibanner 區段類似于一般橫幅。</span><span class="sxs-lookup"><span data-stu-id="88955-211">The minibanner section is similar to the normal banner.</span></span> <span data-ttu-id="88955-212">標題的格式會稍微較高，而且沒有規則。</span><span class="sxs-lookup"><span data-stu-id="88955-212">The format of the title is placed slightly higher and does not have a rule.</span></span> <span data-ttu-id="88955-213">因為沒有任何圖示，所以未載入 **WebViewFolderIcon** 物件。</span><span class="sxs-lookup"><span data-stu-id="88955-213">Because there is no icon, the **WebViewFolderIcon** object is not loaded.</span></span>


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a><span data-ttu-id="88955-214">資訊區域</span><span class="sxs-lookup"><span data-stu-id="88955-214">The Info Region</span></span>

<span data-ttu-id="88955-215">橫幅下方的 Web view 部分是用來顯示有關所選取專案的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="88955-215">The portion of the Web view below the banner is used to present detailed information about the selected item.</span></span> <span data-ttu-id="88955-216">如果未選取任何專案，則會顯示預設訊息。</span><span class="sxs-lookup"><span data-stu-id="88955-216">If no item is selected, a default message is shown.</span></span> <span data-ttu-id="88955-217">因為 htt 只會顯示單一的文字區塊，所以此區段相當簡單。</span><span class="sxs-lookup"><span data-stu-id="88955-217">Because Generic.htt only displays a single block of text, this section is quite simple.</span></span>


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



<span data-ttu-id="88955-218">收集資訊的大部分工作都是由 [資料夾資訊腳本](#retrieving-and-displaying-folder-information) 處理，本章節稍後會討論到。</span><span class="sxs-lookup"><span data-stu-id="88955-218">Most of the work of collecting the information is handled by a [folder information script](#retrieving-and-displaying-folder-information) that is discussed later in the chapter.</span></span> <span data-ttu-id="88955-219">它會將文字指派給 [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx)來顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="88955-219">It displays the information by assigning the text to [TextBlock.innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span></span>

<span data-ttu-id="88955-220">您可以藉由修改這些元素或包含其他元素，輕鬆地自訂資訊顯示。</span><span class="sxs-lookup"><span data-stu-id="88955-220">You can easily customize the information display by modifying these elements or including additional ones.</span></span> <span data-ttu-id="88955-221">您可以在網頁上使用的任何作業都可以使用。</span><span class="sxs-lookup"><span data-stu-id="88955-221">Anything that you can put on a webpage can be used.</span></span> <span data-ttu-id="88955-222">例如，若要顯示網站的連結，您可以在 htt 中的文字區塊之後，新增錨點元素。</span><span class="sxs-lookup"><span data-stu-id="88955-222">For example, to display a link to your website, you can add an anchor element after the text block in Generic.htt.</span></span>


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
        <span>
        <p> Click on <a href="https://your.address"></a>
        </span>
</div>
                    
```



### <a name="the-filelist-region"></a><span data-ttu-id="88955-223">FileList 區域</span><span class="sxs-lookup"><span data-stu-id="88955-223">The FileList Region</span></span>

<span data-ttu-id="88955-224">最後，htt 會載入 FileList 區域的 [**WebViewFolderContents**](webviewfoldercontents.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="88955-224">Finally, Generic.htt loads a [**WebViewFolderContents**](webviewfoldercontents.md) object for the FileList region.</span></span> <span data-ttu-id="88955-225">因為它的識別碼設定為 "FileList"，所以它現在稱為 FileList 物件。</span><span class="sxs-lookup"><span data-stu-id="88955-225">Because its identifier is set to "FileList", it will be referred to as the FileList object from now on.</span></span>


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



<span data-ttu-id="88955-226">在大部分的 Web 視圖中都可以找到 FileList 物件，而且有許多用途。</span><span class="sxs-lookup"><span data-stu-id="88955-226">The FileList object is found in most Web views and serves several purposes.</span></span> <span data-ttu-id="88955-227">FileList 會顯示所選資料夾所含專案的清單，其選項和外觀與傳統樣式的檔案清單相同。</span><span class="sxs-lookup"><span data-stu-id="88955-227">FileList displays the list of items contained by the selected folder with the same options and appearance as the file list in Classic style.</span></span> <span data-ttu-id="88955-228">選取專案時，FileList 會引發 [SelectionChanged](#retrieving-and-displaying-folder-information) 事件，以通知 Web 視圖。</span><span class="sxs-lookup"><span data-stu-id="88955-228">When an item is selected, FileList notifies the Web view by firing a [SelectionChanged](#retrieving-and-displaying-folder-information) event.</span></span> <span data-ttu-id="88955-229">FileList 也會公開方法和屬性，這些方法和屬性可用來取得個別專案的相關資訊，以及控制其顯示區域的位置和大小。</span><span class="sxs-lookup"><span data-stu-id="88955-229">FileList also exposes methods and properties that can be used to retrieve information about individual items and control the position and size of its display area.</span></span>

<span data-ttu-id="88955-230">雖然 FileList 物件非常有用，但它只會傳回標準檔案系統資訊，例如檔案大小或屬性。</span><span class="sxs-lookup"><span data-stu-id="88955-230">Although the FileList object is very useful, it only returns standard file system information, such as file size or attributes.</span></span> <span data-ttu-id="88955-231">若要從 Shell 資料夾取出其他種類的資訊，您必須載入和處理其他物件。</span><span class="sxs-lookup"><span data-stu-id="88955-231">To retrieve other kinds of information from a Shell folder, you will have to load and handle additional objects.</span></span> <span data-ttu-id="88955-232">可由網頁裝載的任何物件都可以搭配 Web view 使用。</span><span class="sxs-lookup"><span data-stu-id="88955-232">Any object that can be hosted by a webpage can be used with a Web view.</span></span>

### <a name="the-template-head"></a><span data-ttu-id="88955-233">範本標頭</span><span class="sxs-lookup"><span data-stu-id="88955-233">The Template Head</span></span>

<span data-ttu-id="88955-234">Web view 範本的標頭包含執行大部分實際工作的腳本和功能。</span><span class="sxs-lookup"><span data-stu-id="88955-234">The head of the Web view template contains the scripts and functions that do most of the actual work.</span></span> <span data-ttu-id="88955-235">有兩個必要的工作需要處理。</span><span class="sxs-lookup"><span data-stu-id="88955-235">There are two essential tasks that need to be handled.</span></span> <span data-ttu-id="88955-236">其中一個是 Web view 顯示器的版面配置，需要調整以容納不同的顯示區域。</span><span class="sxs-lookup"><span data-stu-id="88955-236">One is the layout of the Web view display, which needs to be adjusted to accommodate different display regions.</span></span> <span data-ttu-id="88955-237">另一個則是在選取專案時，從資料夾中抓取和顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="88955-237">The other is retrieving and displaying information from the folder when an item is selected.</span></span> <span data-ttu-id="88955-238">如同樣式表單一樣，最好在範本中包含所有腳本和函式，而不是以個別的檔案形式加以參考。</span><span class="sxs-lookup"><span data-stu-id="88955-238">As with style sheets, it is better to include all scripts and functions in the template instead of referencing them as separate files.</span></span>

### <a name="controlling-the-web-view-layout"></a><span data-ttu-id="88955-239">控制 Web View 版面配置</span><span class="sxs-lookup"><span data-stu-id="88955-239">Controlling the Web View Layout</span></span>

<span data-ttu-id="88955-240">Web view 的可用區域取決於 Web view 視窗的大小，以及 Windows 檔案總管 bar 所佔用的空間。</span><span class="sxs-lookup"><span data-stu-id="88955-240">The area available for a Web view depends on the size of the Web view window and how much of it is taken up by the Windows Explorer bar.</span></span> <span data-ttu-id="88955-241">當視窗或 Windows 檔案總管的橫條調整大小時，這個區域就會變更。</span><span class="sxs-lookup"><span data-stu-id="88955-241">This area will change anytime the window or Windows Explorer bar is resized.</span></span> <span data-ttu-id="88955-242">因此，當 Web view 載入時，版面配置必須符合可用的區域，並在調整大小時適當地變更。</span><span class="sxs-lookup"><span data-stu-id="88955-242">So the layout needs to be matched to the available area when a Web view is loaded and change appropriately when it is resized.</span></span> <span data-ttu-id="88955-243">在樣式表單中指定了大部分的版面配置。</span><span class="sxs-lookup"><span data-stu-id="88955-243">Much of the layout is specified in the style sheet.</span></span> <span data-ttu-id="88955-244">例如，資訊區域的定義是要佔用 Web view 的最左邊30%。</span><span class="sxs-lookup"><span data-stu-id="88955-244">The Info region, for example, is defined to occupy the leftmost 30 percent of the Web view.</span></span>


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



<span data-ttu-id="88955-245">調整 Web 視圖大小時，資訊區域的寬度將會變更，以維持該百分比。</span><span class="sxs-lookup"><span data-stu-id="88955-245">As a Web view is resized, the width of the Info region will change to maintain that percentage.</span></span> <span data-ttu-id="88955-246">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) 可管理樣式表單無法處理的版面配置問題。</span><span class="sxs-lookup"><span data-stu-id="88955-246">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) manages the layout issues that can't be handled by a style sheet.</span></span>

### <a name="loading-and-initializing-the-web-view"></a><span data-ttu-id="88955-247">載入和初始化 Web View</span><span class="sxs-lookup"><span data-stu-id="88955-247">Loading and Initializing the Web View</span></span>

<span data-ttu-id="88955-248">當 Web view 載入時，必須調整配置以符合可用的顯示區域。</span><span class="sxs-lookup"><span data-stu-id="88955-248">When a Web view is loaded, the layout needs to be adjusted to fit the available display area.</span></span> <span data-ttu-id="88955-249">由於尚未選取任何專案，因此 Web 視圖通常會顯示套用至整個資料夾的一些預設資訊。</span><span class="sxs-lookup"><span data-stu-id="88955-249">Because no item has been selected yet, Web views normally display some default information that applies to the whole folder.</span></span> <span data-ttu-id="88955-250">若要處理初始化，</span><span class="sxs-lookup"><span data-stu-id="88955-250">To handle initialization, the</span></span> <BODY> <span data-ttu-id="88955-251">適用于 Generic 的標記。 htt 會偵測 [onload](/previous-versions//ms531409(v=vs.85)) 事件並呼叫 **Init** 函數。</span><span class="sxs-lookup"><span data-stu-id="88955-251">tag for Generic.htt detects the [onload](/previous-versions//ms531409(v=vs.85)) event and calls the **Init** function.</span></span>


```
<body scroll=no onload="Init">
                    
```



<span data-ttu-id="88955-252">**Init** 是簡單的 JScript 函數。</span><span class="sxs-lookup"><span data-stu-id="88955-252">**Init** is a simple JScript function.</span></span>


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



<span data-ttu-id="88955-253">**Init** 會將 [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) 系結至 [視窗。](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) 此事件會在 Web view 顯示區域變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="88955-253">**Init** binds [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) to the [window.onresize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) event so that it will be called whenever the Web view display area changes.</span></span> <span data-ttu-id="88955-254">然後，它會執行 FixSize 來設定初始配置，並將 L \_ 簡介 \_ 文字指派給資訊區域。</span><span class="sxs-lookup"><span data-stu-id="88955-254">It then runs FixSize to set the initial layout and assigns L\_Intro\_Text to the Info region.</span></span> <span data-ttu-id="88955-255">L \_ 簡介 \_ 文字是在 [樣式表單] 區段中定義的簡介文字區塊。</span><span class="sxs-lookup"><span data-stu-id="88955-255">L\_Intro\_Text is a block of introductory text that is defined in the style sheet section.</span></span>


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a><span data-ttu-id="88955-256">使用 FixSize 函數來調整版面配置</span><span class="sxs-lookup"><span data-stu-id="88955-256">Adjusting the Layout by using the FixSize function</span></span>

<span data-ttu-id="88955-257">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function)函式是用來指定樣式表單無法處理之版面配置的幾個層面。</span><span class="sxs-lookup"><span data-stu-id="88955-257">The [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) function is used to specify several aspects of the layout that can't be handled by the style sheet.</span></span>

<span data-ttu-id="88955-258">有兩個可能的橫幅可供使用，視 Web 視圖的高度而定。</span><span class="sxs-lookup"><span data-stu-id="88955-258">There are two possible banners that can be used, depending on the height of the Web view.</span></span>


```
if (200 > document.body.clientHeight) {
    //A short window. Use the minibanner.
    document.all.Banner.style.visibility = "hidden";
    document.all.MiniBanner.style.visibility = "visible";
    document.all.FileList.style.top = 32;
    document.all.Info.style.top = 32;
}
else {
    //A normal window. Use the normal banner.
    document.all.Banner.style.visibility = "visible";
    document.all.MiniBanner.style.visibility = "hidden";
    document.all.FileList.style.top = (document.all.Banner.offsetHeight - 32) + "px";
    document.all.Info.style.top = (document.all.Banner.offsetHeight) + "px";
    document.all.Rule.style.width = (document.body.clientWidth > 84 ?                                    document.body.clientWidth - 84 : 0) + "px";      
}
                    
```



<span data-ttu-id="88955-259">Htt 使用高度200圖元作為標準和 minibanners 之間的分隔線。</span><span class="sxs-lookup"><span data-stu-id="88955-259">Generic.htt uses a height of 200 pixels as the dividing line between normal and minibanners.</span></span> <span data-ttu-id="88955-260">它會將所選取橫幅的樣式設定為可見，另一個則會隱藏。</span><span class="sxs-lookup"><span data-stu-id="88955-260">It sets the style of the selected banner to visible and the other to hidden.</span></span> <span data-ttu-id="88955-261">此外，它也會設定資訊和 FileList 區域的數個版面配置屬性，使其符合所選橫幅的適當大小。</span><span class="sxs-lookup"><span data-stu-id="88955-261">It also sets several layout properties for the Info and FileList regions so that they fit properly with the selected banner.</span></span>

<span data-ttu-id="88955-262">如果 Web 視圖變得太窄， [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) 會使用顯示區域的全形來顯示 FileList 顯示。</span><span class="sxs-lookup"><span data-stu-id="88955-262">If a Web view becomes too narrow, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) uses the full width of the display area for the FileList display.</span></span>


```
if (400 > document.body.clientWidth) {
    //A narrow window. Hide the Info region, and expand the file list region.
    document.all.Info.style.visibility = "hidden";
    document.all.FileList.style.pixelLeft = 0;
    document.all.FileList.style.pixelTop = document.all.Info.style.pixelTop;
}

else {
    //Normal width.
    document.all.Info.style.visibility = "visible";
    document.all.FileList.style.pixelLeft = document.all.Info.style.pixelWidth;
}
                    
```



<span data-ttu-id="88955-263">Htt 會使用400圖元作為窄和寬顯示器之間的分隔線。</span><span class="sxs-lookup"><span data-stu-id="88955-263">Generic.htt uses 400 pixels as the dividing line between narrow and wide displays.</span></span> <span data-ttu-id="88955-264">如果 Web view 太窄， [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) 會隱藏資訊區域並修改 FileList [pixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) 屬性，使其填滿橫幅下方的整個區域。</span><span class="sxs-lookup"><span data-stu-id="88955-264">If the Web view is too narrow, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) hides the Info region and modifies the FileList [pixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) property so that it fills the entire region below the banner.</span></span>

<span data-ttu-id="88955-265">最後幾行的 [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) 會根據上述程式碼的結果調整數個版面配置屬性。</span><span class="sxs-lookup"><span data-stu-id="88955-265">The final few lines of [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) adjust several layout properties based on the results of the preceding code.</span></span> <span data-ttu-id="88955-266">FileList 區域的寬度會進行調整，讓它完全填滿資訊區域未佔用之 Web view 的部分。</span><span class="sxs-lookup"><span data-stu-id="88955-266">The width of the FileList region is adjusted so that it exactly fills the portion of the Web view not occupied by the Info region.</span></span> <span data-ttu-id="88955-267">資訊區域的高度會調整大小，以符合 Web 視圖的橫幅和底部。</span><span class="sxs-lookup"><span data-stu-id="88955-267">The height of the Info region is sized to fit between the banner and the bottom of the Web view.</span></span>


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a><span data-ttu-id="88955-268">正在抓取和顯示資料夾資訊</span><span class="sxs-lookup"><span data-stu-id="88955-268">Retrieving and Displaying Folder Information</span></span>

<span data-ttu-id="88955-269">當使用者選取專案時，FileList 物件就會引發 [SelectionChanged](#retrieving-and-displaying-folder-information) 事件。</span><span class="sxs-lookup"><span data-stu-id="88955-269">When a user selects an item, the FileList object fires a [SelectionChanged](#retrieving-and-displaying-folder-information) event.</span></span> <span data-ttu-id="88955-270">此事件是由 JScript 腳本處理。</span><span class="sxs-lookup"><span data-stu-id="88955-270">This event is handled by a JScript script.</span></span> <span data-ttu-id="88955-271">為了簡單起見，在 htt 中找到的腳本會假設一次只能選取一個專案。</span><span class="sxs-lookup"><span data-stu-id="88955-271">For simplicity, the script found in Generic.htt assumes that only one item can be selected at a time.</span></span>


```
<script language="JavaScript" for="FileList" event="SelectionChanged">
    // Updates the TextBlock region when an item is selected.
    var data;
    var text;

    // Name
    text = "<b>" + FileList.FocusedItem.Name + "</b>";

    // Comment
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 3);
    if (data)
        text += "<br>" + data;

    // Documents
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 1);
    if (data)
        text += "<br><br>" + FileList.Folder.GetDetailsOf(null, 1) + ": " + data;

    // Status
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 2);
    if (data)
        text += "<br><br><b><font color=red>" + data + "</font></b>";

    // Tip 
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, -1);
    if (data != "" && data != FileList.FocusedItem.Name)
        text += "<br><br>" + data;

    TextBlock.innerHTML = text;
</script>
                    
```



<span data-ttu-id="88955-272">腳本會使用兩個 FileList 屬性， [**FileList. FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)和 [**FileList**](/windows/desktop/shell/shellfolderview-folder) 來取得專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88955-272">The script uses two FileList properties, [**FileList.FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)and [**FileList.Folder**](/windows/desktop/shell/shellfolderview-folder) to obtain information about the item.</span></span> <span data-ttu-id="88955-273">**FileList** 會識別選取的專案，並以 **FileList.FocusedItem.Name** 提供的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="88955-273">**FileList.FocusedItem** identifies the selected item, with the item's name given by **FileList.FocusedItem.Name**.</span></span> <span data-ttu-id="88955-274">**FileList** 實際上是 [**資料夾**](../shell/folder.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="88955-274">**FileList.Folder** is actually a pointer to a [**Folder**](../shell/folder.md) object.</span></span> <span data-ttu-id="88955-275">資料夾物件的 [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) 方法是用來取得專案的剩餘資訊。</span><span class="sxs-lookup"><span data-stu-id="88955-275">The Folder object's [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) method is used to retrieve the remaining information about the item.</span></span>

<span data-ttu-id="88955-276">所有資訊都會串連成單一文字字串，並以</span><span class="sxs-lookup"><span data-stu-id="88955-276">All the information is concatenated into a single text string, separated by</span></span> <BR> <span data-ttu-id="88955-277">可讀性的標記。</span><span class="sxs-lookup"><span data-stu-id="88955-277">tags for readability.</span></span> <span data-ttu-id="88955-278">然後將文字指派給 [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx)來顯示文字。</span><span class="sxs-lookup"><span data-stu-id="88955-278">The text is then displayed by assigning it to [TextBlock.innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span></span>

## <a name="summary"></a><span data-ttu-id="88955-279">總結</span><span class="sxs-lookup"><span data-stu-id="88955-279">Summary</span></span>

<span data-ttu-id="88955-280">本章概述一些可用來自訂 Windows 檔案總管顯示 Shell 資料夾相關資訊方式的技巧。</span><span class="sxs-lookup"><span data-stu-id="88955-280">This chapter outlines some of the techniques you can use to customize the way the Windows Explorer displays information about Shell folders.</span></span> <span data-ttu-id="88955-281">建立 Desktop.ini 檔案可讓您進行一些簡單的自訂，例如顯示自訂圖示來取代標準資料夾圖示。</span><span class="sxs-lookup"><span data-stu-id="88955-281">Creating a Desktop.ini file allows you to do some simple customization, such as displaying a custom icon in place of the standard folder icon.</span></span> <span data-ttu-id="88955-282">當資料夾出現在 Web view 中時，它的版面配置和顯示是由以 HTML 為基礎的範本控制，以決定要顯示的資訊和方法。</span><span class="sxs-lookup"><span data-stu-id="88955-282">When a folder appears in a Web view, its layout and display are controlled by an HTML-based template that determines what information is displayed and how.</span></span> <span data-ttu-id="88955-283">您可以使用標準 HTML、DHTML 和腳本技術來建立自訂範本，以對資料夾的 Web 視圖進行高度的控制。</span><span class="sxs-lookup"><span data-stu-id="88955-283">You can exercise a high degree of control over a folder's Web view by using standard HTML, DHTML, and scripting techniques to create a custom template.</span></span>

 

 