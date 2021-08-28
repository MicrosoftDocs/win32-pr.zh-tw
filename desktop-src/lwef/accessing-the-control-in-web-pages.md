---
title: 存取網頁中的控制項
description: 存取網頁中的控制項
ms.assetid: 0c799c60-c81a-44ea-a9e0-1a385208528f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb6476ebdf2d26f1aec12a2f46506b3c4882d06
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882967"
---
# <a name="accessing-the-control-in-web-pages"></a>存取網頁中的控制項

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

若要從網頁存取 Microsoft Agent 服務，請使用 [HTML &lt; 物件 &gt; 標記] <HEAD> 或 &lt; 頁面的 BODY 專案 &gt; ，指定控制項的 Microsoft CLSID (類別識別碼) 。 此外，使用程式碼基底參數來指定 Microsoft 代理程式安裝檔案的位置和其版本號碼。

如果系統上已安裝 Microsoft Internet Explorer (3.02 版或更新版本) ，但尚未安裝 Microsoft 代理程式，且使用者存取的網頁具有具有 &lt; &gt; 代理程式 CLSID 的物件標記，則瀏覽器會自動嘗試從 Microsoft 網站下載代理程式。 然後，系統會詢問使用者是否要繼續進行安裝。 若為其他瀏覽器，請洽詢供應商，以取得 ActiveX 控制項的支援或協力廠商支援的相關資訊。

下列範例說明如何使用程式碼基底參數來 autodownload Microsoft 代理程式的英文版2.0。

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

您也可以從自己的 HTTP 伺服器安裝代理程式，也可以在應用程式的安裝過程中安裝代理程式。 若要支援來自您自己的 HTTP 伺服器的安裝，您必須將 Microsoft 代理程式自行安裝封包 .Exe 檔，並在程式碼基底標記中指定其 URL。

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "https://your server/msagent.exe#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

若要支援從網頁自動下載 Microsoft 代理程式語言元件，請在代理程式控制物件標記之前的頁面上包含語言元件的物件標記：

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID: C348XXXX-A7F8-11D1-AA75-00C04FA34D72"
CODEBASE = "#VERSION=2,0,0,0">
</OBJECT>
```

其中 XXXX 取代為語言識別項。 如需目前支援的語言，請查看 Microsoft 代理程式網站。

-   &lt; &gt; 語言元件的物件標記必須在 &lt; &gt; Microsoft Agent 核心元件的物件標記之前。
-   您可以在相同的用戶端上安裝多個語言。
-   在設定字元的 [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) 之前，我們建議您的腳本確認 [**userLanguage**](https://www.bing.com/search?q=**userLanguage**) 屬性中所提供的瀏覽器地區設定符合所設定的語言。

若要支援代理程式的其他語言版本，您可以使用另一個指定語言元件的物件標記。 不過，請注意，嘗試同時安裝多種語言可能需要使用者重新開機。 您可以使用與代理程式核心元件相同的程式，從代理程式網站取得代理程式語言元件。 標準代理程式散發授權涵蓋了語言元件的散發授權。若要開始使用字元，您必須使用 [**load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) 方法載入該字元。 您可以從使用者的本機儲存體或 HTTP 伺服器載入一個字元。 如需有關載入字元之語法的詳細資訊，請參閱 **Load** 方法。 成功載入該字元之後，您就可以使用 Agent 控制項所公開的方法、屬性和事件來撰寫字元的程式。 您也可以使用程式設計語言和瀏覽器所公開的方法、屬性和事件來撰寫字元的程式;例如，若要對按鈕按一下的反應進行程式設計。 請參閱瀏覽器的檔，以判斷其在腳本模型中所公開的功能。 如需 Microsoft Internet Explorer，請參閱 ActiveX SDK 提供的腳本物件模型。

只有當至少有一個用戶端應用程式具有連線時，代理程式的服務才會保持載入。 這表示當使用者在啟用代理程式的網頁之間移動時，代理程式將會關閉，而且您載入的任何字元將會消失。 若要讓代理程式在頁面之間保持 (的狀態，並讓) 的字元保持可見，請建立另一個在頁面變更之間保持載入的用戶端。 例如，您可以建立 HTML 框架組，並 &lt; &gt; 在父框架中宣告 Agent 的物件標記。 然後，您可以將載入至子框架 () s 的頁面編寫腳本，以呼叫父系的腳本。 或者，您也可以 &lt; &gt; 在載入至子框架的每個頁面上包含物件標記。 在此情況下，請記住，每個頁面都是它自己的用戶端。 您可能需要使用「 [**啟動**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) 」方法來設定當使用者與父系或子頁面互動時，可控制的用戶端。

 

 
