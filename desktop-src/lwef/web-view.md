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
ms.openlocfilehash: 73ebe106bdada4da55eef8891a3c93ee82aba3cc4da9194e1fcd4c7e71bcd4e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745679"
---
# <a name="customizing-a-folders-web-view"></a>自訂資料夾的 Web View

\[只有 Windows XP 或更早版本才支援這項功能。 \]

Web view 是一種功能強大且有彈性的方式，可使用 Windows 檔案總管來顯示 Shell 資料夾內容的相關資訊。

-   [簡介](#introduction)
-   [使用 Web View 範本](#using-the-web-view-template)
    -   [範本主體](#the-template-body)
    -   [範本標頭](#the-template-head)
-   [總結](#summary)

## <a name="introduction"></a>簡介

Windows 提供使用者兩種主要方式來查看和流覽 Shell 命名空間。 最熟悉的是傳統樣式，類似于熟悉的 Windows 檔管理員。 右窗格會以下列五種格式的其中一種來列出目前所選資料夾的內容：大型圖示、小圖示、清單、詳細資料和縮圖。 Windows 的 [檔案管理員] 的主要差異在於左窗格，看起來非常類似 Windows Internet Explorer 的 [Explorer] 欄。 它可以調整大小或移除，而且除了熟悉的檔案系統樹狀目錄（例如搜尋窗格）之外，還可以顯示數個窗格。

> [!Note]  
> 本檔中的資訊不適用於 Windows XP，所討論的技術只適用于舊版的 Windows。

 

下圖顯示傳統樣式的 [印表機] 資料夾。

![印表機資料夾的傳統樣式。](images/webview1.png)

傳統樣式適用于一般檔系統資料夾和檔案。 不過，隨著 Windows 95 的引進，檔案系統已發展成命名空間。 命名空間可讓您建立 *虛擬資料夾*，例如印表機或網路鄰近地區，以代表與一般檔系統資料夾非常不同的資訊類型。

Web 樣式（也稱為 Web view）提供更有彈性且功能更強大的方式來呈現與傳統樣式相關的資訊。 在 Web 視圖中，使用者基本上會使用 Internet Explorer 來查看和流覽命名空間。 Web view 的基本版面配置類似于傳統樣式。 Explorer 列沒有變更。 不過，檔案清單所佔用的區域會變成一般用途的顯示區域，該區域實際上是網頁。 Web view 仍會用來顯示資料夾內容的相關資訊，但在顯示的資訊或方式方面有一些限制。 每個資料夾都可以有自己的網頁視圖，其自訂為符合其特定功能。

下圖顯示 [印表機] 資料夾的 Web 視圖， (先前的傳統樣式) 所示。

![[印表機] 資料夾的預設 web 視圖。](images/webview2.png)

Web 視圖與傳統網頁非常類似，是由 HTML 範本所控制。 撰寫 Web view 範本與撰寫網頁幾乎完全相同，而且在內容和版面配置中提供相同程度的彈性。 Web view 範本可以使用動態 HTML (DHTML) 和腳本來回應事件，例如使用者按一下專案。 它們也可以裝載物件，讓它們可以從資料夾或其內容中取得和顯示資訊。

使用者可以藉由啟動 Windows 檔案總管、按一下 [ **view** ] 功能表上的 [**資料夾選項**]，然後選取此選項： [**在資料夾中啟用 Web 內容**] 來選擇 Web 視圖。 不過，使用者也可以開始 Internet Explorer，並 **按一下 [流覽] 功能表、** 指向 [ **Explorer** 列]，然後按一下 [ **資料夾**]，將瀏覽器指向檔案系統。 在 Web 視圖中，Internet Explorer 和 Windows 檔案總管幾乎沒有任何差異。

在右窗格的左側，印表機網頁視圖會顯示具有資料夾名稱和圖示的橫幅，後面接著資料夾的相關資訊區塊。 一般檔案清單會佔用頁面的右側。

當使用者按一下某個專案時，該專案的詳細資訊就會出現在資訊區塊中。 [印表機] Web 視圖實際上會顯示傳統樣式中所提供的相同資訊，但它會以更容易使用的格式來執行。 但是，Web view 並不只是顯示傳統樣式資訊的不同方式。 例如，您可以在資訊區塊底下顯示有用網站的連結，這是傳統樣式中無法使用的功能。 如果使用者按一下此連結，則會顯示該網站。

上圖所示的 [印表機] Web 視圖類似于傳統樣式，因為基礎 Web view 範本 (htt 檔案) 是以這種方式撰寫的。 例如，不會直接由 Web view 範本產生檔案清單。 它是由 Web view 範本所裝載的 [**WebViewFolderContents**](webviewfoldercontents.md) 物件所建立和顯示。 物件的方法和屬性可讓 Web view 控制其版面配置，並取得特定專案的相關資訊。 橫幅和資訊區塊的內容和配置都是在 Web view 範本中指定。

由於 Web view 支援 DHTML，因此範本也可以用來處理使用者互動。 例如，當使用者按一下其中一個印表機圖示時， **WebViewFolderIcon** 物件就會引發 [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) 事件。 此範本會使用以腳本撰寫的 DHTML 事件處理常式，以抓取要求的資訊並將它顯示在資訊區塊中。

[印表機] 資料夾的這個簡單範例就是使用網頁視圖的唯一方式。 藉由撰寫您自己的範本，如有必要，您可以使用 Web view 來顯示資訊，並以您最有效的方式與使用者互動。 請注意，目前 Web view 範本只會顯示系統定義的虛擬資料夾。 雖然開發人員可以藉由執行命名空間延伸來建立虛擬資料夾，但是它們必須使用 [命名空間](/windows/desktop/shell/nse-works) 延伸模組中所述的技術來顯示它。

## <a name="using-the-web-view-template"></a>使用 Web View 範本

在 Web view 中顯示資料的方式，可以藉由修改資料夾的 Desktop.ini 檔案，以有限的方式自訂。 如需詳細資訊，請參閱 [使用 Desktop.ini自訂資料夾 ](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) 。 更有彈性且功能更強大的自訂 Web 視圖方式，就是建立自訂的 Web view 範本。

Web view 範本會控制在 Web 視圖中顯示的內容，以及如何進行。 它使用標準 HTML、DHTML 和腳本技術來取得和顯示資訊，並與使用者互動。 本節討論如何藉由檢查簡單的範本（htt）來建立 Web 視圖。


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



建立您自己的 Web view 範本的簡單方法，就是使用 htt 並加以修改。 因為它相當有限，所以您也應該查看其他更複雜的範例，以瞭解其他想法。 您可以搜尋系統，找出所有 Web view 範本所使用的 htt 延伸模組。 如果您想要建立資料夾的自訂範本，您應該從預設的 htt 範本開始，此範本通常儲存在 C： \\ Winnt \\ Web 或 c： \\ Windows \\ Web。 請注意，這些檔案會定義為隱藏，因此您可能需要修改 Windows 檔案總管設定才能加以查看。 建立 htt 檔案之後，應該將它標示為唯讀並隱藏。

Web view 範本使用 htt 副檔名，因為它們與傳統 .htm 檔稍有不同。 主要差異在於 htt 檔案中的數個特殊變數，系統會以目前的命名空間值取代這些變數。 % THISDIR% 和% THISDIRPATH% 變數代表目前選取之資料夾的名稱和路徑。 % TEMPLATEDIR% 變數代表儲存 Web 視圖樣式表單的資料夾。

如同大多數的 HTML 範本，htt 檔有兩個基本部分：本文和 head。 範本主體會控制 Web view 的基本版面配置，並載入用來與命名空間進行通訊和顯示資訊的物件。 此標頭包含的腳本和函式可進行工作，例如處理調整大小和取得資料夾中的資訊。 大部分的範本（包括 htt）也包含樣式表單。 一般情況下，最好將樣式表單資訊包含在範本中。 當 Web 視圖與遠端命名空間搭配使用時，不同的樣式表單可能無法正常運作。

### <a name="the-template-body"></a>範本主體

範本的主體會指定 Web view 將呈現的內容。 此外，也會載入用來顯示資訊的物件，以及與命名空間資料夾進行通訊的物件。 Htt 所定義的配置與上一節中的圖所示的版面配置類似。 有三個顯示區域：視圖左邊的橫幅和資訊區塊，以及右邊的檔案清單。

這些區域是樣式表單和 DHTML 所要使用的所有指派識別碼。 如下一節所述，有兩個可能的橫幅，其識別碼為 "橫幅" 和 "MiniBanner"。 資訊區塊區域的識別碼是「資訊」。 檔案清單物件的識別碼是 "FileList"。 區域[版面](#controlling-the-web-view-layout)配置的詳細資料是由樣式表單和 Microsoft JScript 函式[FixSize](#adjusting-the-layout-by-using-the-fixsize-function)所處理，本章節稍後將討論這項功能。

### <a name="the-banner-region"></a>橫幅區域

橫幅位於 Web view 左上角的 [顯示] 的頂端。 一般橫幅會顯示其內容會顯示在右側檔案清單中之資料夾的名稱和圖示。 但是，如果視窗變得太短，則圖示下方可能沒有足夠的空間來顯示資訊。 基於這個理由，htt 也會定義只顯示資料夾名稱的 minibanner。 這兩個橫幅一開始會定義為隱藏。 [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) 會選擇要顯示哪一個，並將其設定為「可見」。

一般 htt 的一般橫幅定義如下：


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



橫幅區段的第一個部分會在其下顯示具有水準規則的標題。 資料表標記是用來控制其位置。 Nowrap 屬性設定為 <TD> 標記以防止自動換行。 系統會將% THISDIRNAME% 取代為目前資料夾的名稱。 為了簡單起見， **WebViewFolderIcon** 物件的識別碼為 "Icon"，接著會載入以解壓縮並顯示資料夾的圖示。

Minibanner 區段類似于一般橫幅。 標題的格式會稍微較高，而且沒有規則。 因為沒有任何圖示，所以未載入 **WebViewFolderIcon** 物件。


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a>資訊區域

橫幅下方的 Web view 部分是用來顯示有關所選取專案的詳細資訊。 如果未選取任何專案，則會顯示預設訊息。 因為 htt 只會顯示單一的文字區塊，所以此區段相當簡單。


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



收集資訊的大部分工作都是由 [資料夾資訊腳本](#retrieving-and-displaying-folder-information) 處理，本章節稍後會討論到。 它會將文字指派給 [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx)來顯示資訊。

您可以藉由修改這些元素或包含其他元素，輕鬆地自訂資訊顯示。 您可以在網頁上使用的任何作業都可以使用。 例如，若要顯示網站的連結，您可以在 htt 中的文字區塊之後，新增錨點元素。


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



### <a name="the-filelist-region"></a>FileList 區域

最後，htt 會載入 FileList 區域的 [**WebViewFolderContents**](webviewfoldercontents.md) 物件。 因為它的識別碼設定為 "FileList"，所以它現在稱為 FileList 物件。


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



在大部分的 Web 視圖中都可以找到 FileList 物件，而且有許多用途。 FileList 會顯示所選資料夾所含專案的清單，其選項和外觀與傳統樣式的檔案清單相同。 選取專案時，FileList 會引發 [SelectionChanged](#retrieving-and-displaying-folder-information) 事件，以通知 Web 視圖。 FileList 也會公開方法和屬性，這些方法和屬性可用來取得個別專案的相關資訊，以及控制其顯示區域的位置和大小。

雖然 FileList 物件非常有用，但它只會傳回標準檔案系統資訊，例如檔案大小或屬性。 若要從 Shell 資料夾取出其他種類的資訊，您必須載入和處理其他物件。 可由網頁裝載的任何物件都可以搭配 Web view 使用。

### <a name="the-template-head"></a>範本標頭

Web view 範本的標頭包含執行大部分實際工作的腳本和功能。 有兩個必要的工作需要處理。 其中一個是 Web view 顯示器的版面配置，需要調整以容納不同的顯示區域。 另一個則是在選取專案時，從資料夾中抓取和顯示資訊。 如同樣式表單一樣，最好在範本中包含所有腳本和函式，而不是以個別的檔案形式加以參考。

### <a name="controlling-the-web-view-layout"></a>控制 Web View 版面配置

web view 的可用區域取決於 web view 視窗的大小，以及 Windows 檔案總管 bar 所佔用的空間。 當視窗或 Windows 檔案總管的橫條調整大小時，這個區域就會變更。 因此，當 Web view 載入時，版面配置必須符合可用的區域，並在調整大小時適當地變更。 在樣式表單中指定了大部分的版面配置。 例如，資訊區域的定義是要佔用 Web view 的最左邊30%。


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



調整 Web 視圖大小時，資訊區域的寬度將會變更，以維持該百分比。 [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) 可管理樣式表單無法處理的版面配置問題。

### <a name="loading-and-initializing-the-web-view"></a>載入和初始化 Web View

當 Web view 載入時，必須調整配置以符合可用的顯示區域。 由於尚未選取任何專案，因此 Web 視圖通常會顯示套用至整個資料夾的一些預設資訊。 若要處理初始化， <BODY> 適用于 Generic 的標記。 htt 會偵測 [onload](/previous-versions//ms531409(v=vs.85)) 事件並呼叫 **Init** 函數。


```
<body scroll=no onload="Init">
                    
```



**Init** 是簡單的 JScript 函數。


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



**Init** 會將 [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) 系結至 [視窗。](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) 此事件會在 Web view 顯示區域變更時呼叫。 然後，它會執行 FixSize 來設定初始配置，並將 L \_ 簡介 \_ 文字指派給資訊區域。 L \_ 簡介 \_ 文字是在 [樣式表單] 區段中定義的簡介文字區塊。


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a>使用 FixSize 函數來調整版面配置

[FixSize](#adjusting-the-layout-by-using-the-fixsize-function)函式是用來指定樣式表單無法處理之版面配置的幾個層面。

有兩個可能的橫幅可供使用，視 Web 視圖的高度而定。


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



Htt 使用高度200圖元作為標準和 minibanners 之間的分隔線。 它會將所選取橫幅的樣式設定為可見，另一個則會隱藏。 此外，它也會設定資訊和 FileList 區域的數個版面配置屬性，使其符合所選橫幅的適當大小。

如果 Web 視圖變得太窄， [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) 會使用顯示區域的全形來顯示 FileList 顯示。


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



Htt 會使用400圖元作為窄和寬顯示器之間的分隔線。 如果 Web view 太窄， [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) 會隱藏資訊區域並修改 FileList [pixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) 屬性，使其填滿橫幅下方的整個區域。

最後幾行的 [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) 會根據上述程式碼的結果調整數個版面配置屬性。 FileList 區域的寬度會進行調整，讓它完全填滿資訊區域未佔用之 Web view 的部分。 資訊區域的高度會調整大小，以符合 Web 視圖的橫幅和底部。


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a>正在抓取和顯示資料夾資訊

當使用者選取專案時，FileList 物件就會引發 [SelectionChanged](#retrieving-and-displaying-folder-information) 事件。 此事件是由 JScript 腳本處理。 為了簡單起見，在 htt 中找到的腳本會假設一次只能選取一個專案。


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



腳本會使用兩個 FileList 屬性， [**FileList. FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)和 [**FileList**](/windows/desktop/shell/shellfolderview-folder) 來取得專案的相關資訊。 **FileList** 會識別選取的專案，並以 **FileList.FocusedItem.Name** 提供的專案名稱。 **FileList** 實際上是 [**資料夾**](../shell/folder.md) 物件的指標。 資料夾物件的 [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) 方法是用來取得專案的剩餘資訊。

所有資訊都會串連成單一文字字串，並以 <BR> 可讀性的標記。 然後將文字指派給 [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx)來顯示文字。

## <a name="summary"></a>摘要

本章概述一些可用來自訂 Windows 檔案總管顯示 Shell 資料夾相關資訊方式的技巧。 建立 Desktop.ini 檔案可讓您進行一些簡單的自訂，例如顯示自訂圖示來取代標準資料夾圖示。 當資料夾出現在 Web view 中時，它的版面配置和顯示是由以 HTML 為基礎的範本控制，以決定要顯示的資訊和方法。 您可以使用標準 HTML、DHTML 和腳本技術來建立自訂範本，以對資料夾的 Web 視圖進行高度的控制。

 

 