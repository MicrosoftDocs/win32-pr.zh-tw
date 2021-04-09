---
title: 存取網頁中的控制項
description: 存取網頁中的控制項
ms.assetid: 0c799c60-c81a-44ea-a9e0-1a385208528f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a965d73f7277b2b4a62c08a949782488f1e4dba4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681830"
---
# <a name="accessing-the-control-in-web-pages"></a><span data-ttu-id="097c2-103">存取網頁中的控制項</span><span class="sxs-lookup"><span data-stu-id="097c2-103">Accessing the Control in Web Pages</span></span>

<span data-ttu-id="097c2-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="097c2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="097c2-105">若要從網頁存取 Microsoft Agent 服務，請 <OBJECT> 使用位於</span><span class="sxs-lookup"><span data-stu-id="097c2-105">To access the Microsoft Agent services from a webpage, use the HTML <OBJECT> tag within the</span></span> <HEAD> <span data-ttu-id="097c2-106">或</span><span class="sxs-lookup"><span data-stu-id="097c2-106">or</span></span> <BODY> <span data-ttu-id="097c2-107">頁面的元素，為控制項指定 Microsoft CLSID (類別識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="097c2-107">element of the page, specifying the Microsoft CLSID (class identifier) for the control.</span></span> <span data-ttu-id="097c2-108">此外，使用程式碼基底參數來指定 Microsoft 代理程式安裝檔案的位置和其版本號碼。</span><span class="sxs-lookup"><span data-stu-id="097c2-108">In addition, use a CODEBASE parameter to specify the location of the Microsoft Agent installation file and its version number.</span></span>

<span data-ttu-id="097c2-109">如果系統上已安裝 Microsoft Internet Explorer (3.02 版或更新版本) ，但尚未安裝 Microsoft 代理程式，且使用者存取的網頁具有 <OBJECT> 代理程式 CLSID 的標記，則瀏覽器會自動嘗試從 Microsoft 網站下載代理程式。</span><span class="sxs-lookup"><span data-stu-id="097c2-109">If Microsoft Internet Explorer (version 3.02 or later) is installed on the system, but Microsoft Agent is not yet installed and the user accesses a webpage that has the <OBJECT> tag with the Agent CLSID, the browser will automatically attempt to download Agent from the Microsoft website.</span></span> <span data-ttu-id="097c2-110">然後，系統會詢問使用者是否要繼續進行安裝。</span><span class="sxs-lookup"><span data-stu-id="097c2-110">Then, the user will be asked whether to proceed with installation.</span></span> <span data-ttu-id="097c2-111">若為其他瀏覽器，請洽詢供應商，以取得其支援或協力廠商支援 ActiveX 控制項的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="097c2-111">For other browsers, contact the supplier for information regarding their support or third-party support for ActiveX controls.</span></span>

<span data-ttu-id="097c2-112">下列範例說明如何使用程式碼基底參數來 autodownload Microsoft 代理程式的英文版2.0。</span><span class="sxs-lookup"><span data-stu-id="097c2-112">The following example illustrates how to use the CODEBASE parameter to autodownload the English language version 2.0 of Microsoft Agent.</span></span>

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

<span data-ttu-id="097c2-113">您也可以從自己的 HTTP 伺服器安裝代理程式，也可以在應用程式的安裝過程中安裝代理程式。</span><span class="sxs-lookup"><span data-stu-id="097c2-113">Agent can also be installed from your own HTTP server or as part of an application's installation process.</span></span> <span data-ttu-id="097c2-114">若要從您自己的 HTTP 伺服器支援安裝，您需要張貼 Microsoft 代理程式自行安裝封包。Exe 檔案，並在程式碼基底標記中指定其 URL。</span><span class="sxs-lookup"><span data-stu-id="097c2-114">To support installation from your own HTTP server, you need to post the Microsoft Agent self-installing cabinet .Exe file and specify its URL in the CODEBASE tag.</span></span>

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "https://your server/msagent.exe#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

<span data-ttu-id="097c2-115">若要支援從網頁自動下載 Microsoft 代理程式語言元件，請在代理程式控制物件標記之前的頁面上包含語言元件的物件標記：</span><span class="sxs-lookup"><span data-stu-id="097c2-115">To support automatic download of a Microsoft Agent language component from a webpage, include the language component's Object tag on the page before the Agent control Object tag:</span></span>

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID: C348XXXX-A7F8-11D1-AA75-00C04FA34D72"
CODEBASE = "#VERSION=2,0,0,0">
</OBJECT>
```

<span data-ttu-id="097c2-116">其中 XXXX 取代為語言識別項。</span><span class="sxs-lookup"><span data-stu-id="097c2-116">where XXXX is replaced with a Language ID.</span></span> <span data-ttu-id="097c2-117">如需目前支援的語言，請查看 Microsoft 代理程式網站。</span><span class="sxs-lookup"><span data-stu-id="097c2-117">For the languages currently supported, check the Microsoft Agent website.</span></span>

-   <span data-ttu-id="097c2-118"><OBJECT>語言元件的標記必須在 <OBJECT> Microsoft Agent 核心元件的標記之前。</span><span class="sxs-lookup"><span data-stu-id="097c2-118">The <OBJECT> tag for a language component must precede the <OBJECT> tag for the Microsoft Agent core component.</span></span>
-   <span data-ttu-id="097c2-119">您可以在相同的用戶端上安裝多個語言。</span><span class="sxs-lookup"><span data-stu-id="097c2-119">Multiple languages can be installed on the same client.</span></span>
-   <span data-ttu-id="097c2-120">在設定字元的 [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) 之前，我們建議您的腳本確認 [**userLanguage**](https://www.bing.com/search?q=**userLanguage**) 屬性中所提供的瀏覽器地區設定符合所設定的語言。</span><span class="sxs-lookup"><span data-stu-id="097c2-120">Before setting the [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) of a character, we recommend that your script verify that the locale of the browser, available in the [**userLanguage**](https://www.bing.com/search?q=**userLanguage**) property, matches the language being set.</span></span>

<span data-ttu-id="097c2-121">若要支援代理程式的其他語言版本，您可以使用另一個指定語言元件的物件標記。</span><span class="sxs-lookup"><span data-stu-id="097c2-121">To support other language versions of Agent, you use another Object tag specifying the language component.</span></span> <span data-ttu-id="097c2-122">不過，請注意，嘗試同時安裝多種語言可能需要使用者重新開機。</span><span class="sxs-lookup"><span data-stu-id="097c2-122">However, be aware that attempting to install multiple languages at the same time may require the user to reboot.</span></span> <span data-ttu-id="097c2-123">您可以使用與代理程式核心元件相同的程式，從代理程式網站取得代理程式語言元件。</span><span class="sxs-lookup"><span data-stu-id="097c2-123">The Agent language components can be obtained from the Agent website using the same procedure as for the Agent core component.</span></span> <span data-ttu-id="097c2-124">標準代理程式散發授權涵蓋了語言元件的散發授權。若要開始使用字元，您必須使用 [**load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) 方法載入該字元。</span><span class="sxs-lookup"><span data-stu-id="097c2-124">Distribution licensing for the language components are covered in the standard Agent distribution license.To begin using a character, you must load the character using the [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) method.</span></span> <span data-ttu-id="097c2-125">您可以從使用者的本機儲存體或 HTTP 伺服器載入一個字元。</span><span class="sxs-lookup"><span data-stu-id="097c2-125">A character can be loaded from the user's local storage or an HTTP server.</span></span> <span data-ttu-id="097c2-126">如需有關載入字元之語法的詳細資訊，請參閱 **Load** 方法。</span><span class="sxs-lookup"><span data-stu-id="097c2-126">For more information about the syntax for loading a character, see the **Load** method.</span></span> <span data-ttu-id="097c2-127">成功載入該字元之後，您就可以使用 Agent 控制項所公開的方法、屬性和事件來撰寫字元的程式。</span><span class="sxs-lookup"><span data-stu-id="097c2-127">Once the character has been successful loaded you can use the methods, properties, and events exposed by the Agent control to program the character.</span></span> <span data-ttu-id="097c2-128">您也可以使用程式設計語言和瀏覽器所公開的方法、屬性和事件來撰寫字元的程式;例如，若要對按鈕按一下的反應進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="097c2-128">You can also use the methods, properties, and events exposed by your programming language and the browser to program the character; for example, to program its reaction to a button click.</span></span> <span data-ttu-id="097c2-129">請參閱瀏覽器的檔，以判斷其在腳本模型中所公開的功能。</span><span class="sxs-lookup"><span data-stu-id="097c2-129">Consult the documentation for your browser to determine what features it exposes in its scripting model.</span></span> <span data-ttu-id="097c2-130">如需 Microsoft Internet Explorer，請參閱 ActiveX SDK 提供的腳本物件模型。</span><span class="sxs-lookup"><span data-stu-id="097c2-130">For Microsoft Internet Explorer, see the Scripting Object Model, which is available in the ActiveX SDK.</span></span>

<span data-ttu-id="097c2-131">只有當至少有一個用戶端應用程式具有連線時，代理程式的服務才會保持載入。</span><span class="sxs-lookup"><span data-stu-id="097c2-131">Agent's services remain loaded only when there is at least one client application with a connection.</span></span> <span data-ttu-id="097c2-132">這表示當使用者在啟用代理程式的網頁之間移動時，代理程式將會關閉，而且您載入的任何字元將會消失。</span><span class="sxs-lookup"><span data-stu-id="097c2-132">This means that when a user moves between Agent-enabled webpages, Agent will shut down and any characters you loaded will disappear.</span></span> <span data-ttu-id="097c2-133">若要讓代理程式在頁面之間保持 (的狀態，並讓) 的字元保持可見，請建立另一個在頁面變更之間保持載入的用戶端。</span><span class="sxs-lookup"><span data-stu-id="097c2-133">To keep Agent running between pages (and thereby keep a character visible), create another client that remains loaded between page changes.</span></span> <span data-ttu-id="097c2-134">例如，您可以建立 HTML 框架組，並 <OBJECT> 在父框架中宣告 Agent 的標記。</span><span class="sxs-lookup"><span data-stu-id="097c2-134">For example, you can create an HTML frameset and declare an <OBJECT> tag for Agent in the parent frame.</span></span> <span data-ttu-id="097c2-135">然後，您可以將載入至子框架 () s 的頁面編寫腳本，以呼叫父系的腳本。</span><span class="sxs-lookup"><span data-stu-id="097c2-135">You can then script the pages you load into the child frame(s), to call into the parent's script.</span></span> <span data-ttu-id="097c2-136">或者，您也可以 <OBJECT> 在載入至子框架的每個頁面上包含一個標記。</span><span class="sxs-lookup"><span data-stu-id="097c2-136">Alternatively, you can also include an <OBJECT> tag on each page you load into the child frame.</span></span> <span data-ttu-id="097c2-137">在此情況下，請記住，每個頁面都是它自己的用戶端。</span><span class="sxs-lookup"><span data-stu-id="097c2-137">In this case, remember that each page will be its own client.</span></span> <span data-ttu-id="097c2-138">您可能需要使用「 [**啟動**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) 」方法來設定當使用者與父系或子頁面互動時，可控制的用戶端。</span><span class="sxs-lookup"><span data-stu-id="097c2-138">You may need to use the [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) method to set which client has control when the user interacts with the parent or child page.</span></span>

 

 