---
description: 從 Windows Vista，主控台類別目錄檢視會在每個主控台專案的圖示下提供工作連結，如下所示。
ms.assetid: 54a03536-6fe6-4304-a555-58e5bca128b9
title: 建立主控台專案的可搜尋工作連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b4e98e8a6e07f84e8012b58cefe8e0d249fc069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847795"
---
# <a name="creating-searchable-task-links-for-a-control-panel-item"></a><span data-ttu-id="6973e-103">建立主控台專案的可搜尋工作連結</span><span class="sxs-lookup"><span data-stu-id="6973e-103">Creating Searchable Task Links for a Control Panel Item</span></span>

<span data-ttu-id="6973e-104">從 Windows Vista，主控台類別目錄檢視會在每個主控台專案的圖示下提供工作連結，如下所示。</span><span class="sxs-lookup"><span data-stu-id="6973e-104">As of Windows Vista, the Control Panel category view provides task links beneath each Control Panel item's icon as shown here.</span></span>

![[系統和維護類別] 頁面上的工作連結](images/controlpaneltasklinks.png)

<span data-ttu-id="6973e-106">當使用者在視窗右上角的 [ **搜尋** ] 方塊中輸入文字時，搜尋結果會包含這些工作連結，如下所示搜尋「顯示」一字。</span><span class="sxs-lookup"><span data-stu-id="6973e-106">When a user enters text in the **Search** box in the upper right of the window, the search results include these task links as shown here for a search on the word "display".</span></span>

![控制台搜尋結果中的工作連結](images/controlpanelsearchresults.png)

<span data-ttu-id="6973e-108">本主題將討論下列內容：</span><span class="sxs-lookup"><span data-stu-id="6973e-108">This topic discusses the following:</span></span>

-   [<span data-ttu-id="6973e-109">工作連結的最佳作法</span><span class="sxs-lookup"><span data-stu-id="6973e-109">Task Link Best Practices</span></span>](#task-link-best-practices)
-   [<span data-ttu-id="6973e-110">建立工作 XML 檔案</span><span class="sxs-lookup"><span data-stu-id="6973e-110">Creating a Task XML File</span></span>](#creating-a-task-xml-file)
-   [<span data-ttu-id="6973e-111">當地語系化工作連結</span><span class="sxs-lookup"><span data-stu-id="6973e-111">Localizing Task Links</span></span>](#localizing-task-links)
-   [<span data-ttu-id="6973e-112">關鍵字和搜尋</span><span class="sxs-lookup"><span data-stu-id="6973e-112">Keywords and Searching</span></span>](#keywords-and-searching)
-   [<span data-ttu-id="6973e-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="6973e-113">Related topics</span></span>](#related-topics)

## <a name="task-link-best-practices"></a><span data-ttu-id="6973e-114">工作連結的最佳作法</span><span class="sxs-lookup"><span data-stu-id="6973e-114">Task Link Best Practices</span></span>

<span data-ttu-id="6973e-115">建議您為主控台專案提供工作連結，以協助使用者搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="6973e-115">It is recommended that you provide task links for your Control Panel items as an aid to users searching for functionality.</span></span> <span data-ttu-id="6973e-116">您也可以將關鍵字新增至工作連結，讓使用者即使不知道工作的標題或詞彙也可以找到它們。</span><span class="sxs-lookup"><span data-stu-id="6973e-116">It is also possible to add keywords to the task links so that a user can find them even without knowing a task's title or terminology.</span></span>

<span data-ttu-id="6973e-117">最佳的工作連結有三個用途：</span><span class="sxs-lookup"><span data-stu-id="6973e-117">The best task links serve three purposes:</span></span>

1.  <span data-ttu-id="6973e-118">提供主控台專案功能的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="6973e-118">Provide a shortcut to the functionality of the Control Panel item.</span></span>
2.  <span data-ttu-id="6973e-119">提供關鍵字，讓使用者可以使用自己的語言來搜尋。</span><span class="sxs-lookup"><span data-stu-id="6973e-119">Provide keywords so that users can search using their own language.</span></span> <span data-ttu-id="6973e-120">使用者可能會想要輸入「壓縮」，因為他或她知道技術術語。</span><span class="sxs-lookup"><span data-stu-id="6973e-120">A user may want to type "compaction" because he or she knows the technical term.</span></span> <span data-ttu-id="6973e-121">使用者可以輸入「DB 太大」或「資料庫 filesize」。</span><span class="sxs-lookup"><span data-stu-id="6973e-121">A user may type "DB too big", or "database filesize".</span></span> <span data-ttu-id="6973e-122">在工作中加入適當的關鍵字，表示使用者可以找到您的主控台專案。</span><span class="sxs-lookup"><span data-stu-id="6973e-122">Adding suitable keywords to the task means that users can find your Control Panel item.</span></span>
3.  <span data-ttu-id="6973e-123">提供有關主控台專案用途的提示。</span><span class="sxs-lookup"><span data-stu-id="6973e-123">Provide hints about what the Control Panel item does.</span></span> <span data-ttu-id="6973e-124">當使用者看到位於主控台專案圖示下方的連結時，他們可以取得有關主控台專案的使用方式，而不是單獨提供的名稱和圖示的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="6973e-124">When a user sees the links beneath a Control Panel item's icon, they can get more information about what the Control Panel item is used for than the name and icon alone can provide.</span></span>

<span data-ttu-id="6973e-125">工作連結應以終端使用者為主，而不是以技術或功能為主。</span><span class="sxs-lookup"><span data-stu-id="6973e-125">Task links should be end-user focused, not technology- or feature-focused.</span></span> <span data-ttu-id="6973e-126">例如，「啟用資料庫壓縮」會是不正確的用語，因為這是大部分使用者都不熟悉的技術術語。</span><span class="sxs-lookup"><span data-stu-id="6973e-126">For example, "Enable database compaction" would be bad wording because it is technical jargon unfamiliar to the majority of users.</span></span> <span data-ttu-id="6973e-127">「讓我的資料庫檔案變小」是比較好的做法，因為它提及使用者的實際結束目標，而不是取得該機制。</span><span class="sxs-lookup"><span data-stu-id="6973e-127">"Make my database file smaller" is better because it mentions the user's actual end goal rather than the mechanism to get there.</span></span> <span data-ttu-id="6973e-128">目標不是要 oversimplify，而是要以使用者想要完成的工作來說出工作。</span><span class="sxs-lookup"><span data-stu-id="6973e-128">The goal is not to oversimplify, but rather to phrase the task in terms of what the user wants to accomplish.</span></span>

## <a name="creating-a-task-xml-file"></a><span data-ttu-id="6973e-129">建立工作 XML 檔案</span><span class="sxs-lookup"><span data-stu-id="6973e-129">Creating a Task XML File</span></span>

<span data-ttu-id="6973e-130">工作連結是在 XML 檔案中定義。</span><span class="sxs-lookup"><span data-stu-id="6973e-130">Task links are defined in an XML file.</span></span> <span data-ttu-id="6973e-131">本節提供範例 .xml 檔案的詳細資料，該檔案會針對稱為「 **記事本**」的主控台專案定義三個工作連結。</span><span class="sxs-lookup"><span data-stu-id="6973e-131">This section provides the details of an example .xml file that defines three task links for a Control Panel item called **Notepad**.</span></span> <span data-ttu-id="6973e-132">它會定義工作連結的標題、關鍵字和命令列。</span><span class="sxs-lookup"><span data-stu-id="6973e-132">It defines titles, keywords, and the command lines for the task links.</span></span> <span data-ttu-id="6973e-133">它也會說明如何指定哪些工作連結會出現在哪個類別下。</span><span class="sxs-lookup"><span data-stu-id="6973e-133">It also illustrates how to specify which task links appear under which category.</span></span> <span data-ttu-id="6973e-134">註冊要出現在多個類別目錄中的主控台專案，可以選擇根據分類來顯示不同的連結。</span><span class="sxs-lookup"><span data-stu-id="6973e-134">A Control Panel item that is registered to appear in more than one category has the option of showing different links depending on the category.</span></span> <span data-ttu-id="6973e-135">提供各種專案的說明，以及提供的資訊，會以 XML 本身的批註形式提供。</span><span class="sxs-lookup"><span data-stu-id="6973e-135">Explanations of the various elements and information provided are given as comments in the XML itself.</span></span>


```
<?xml version="1.0" ?>
<applications xmlns="http://schemas.microsoft.com/windows/cpltasks/v1" 
              xmlns:sh="http://schemas.microsoft.com/windows/tasks/v1">
    
    <!-- Notepad -->
    <application id="{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}"> 
    <!-- This GUID must match the GUID you created for your Control Panel item,
         and registered in namespace -->
    
        <!-- Solitaire -->
        <sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
            <!-- This is a generated GUID, specific to this task link -->
            <sh:name>Play solitaire</sh:name>
            <sh:keywords>solitare;game;cards;ace;diamond;heart;club;single</sh:keywords>
            <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
        </sh:task>

        <!-- Task Manager -->
        <sh:task id="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}" needsElevation="true"> 
            <!-- This is a generated GUID, specific to this task link -->
            <!-- The needsElevation="true" attribute means that the task 
                 appears with a shield icon next to it. Adding this attribute 
                 does not cause the .exe to require elevation - it just adds an 
                 icon to tell users that the command already requires it -->
            <sh:name>See running processes</sh:name>
            <sh:keywords>taskmgr;taskman;running processes;threads;cpu;</sh:keywords>
            <sh:command>taskmgr.exe</sh:command>
        </sh:task>

        <!-- IE -->
        <sh:task id="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}">
            <sh:name>Open Internet Explorer</sh:name>
            <sh:keywords>IE;web;browser;net;Internet;ActiveX;plug-in;plugin</sh:keywords>
            <sh:command>iexplore.exe</sh:command>
        </sh:task>
        
        <!-- Category assignments -->

        <!-- Appearance and Personalization -->
        <category id="1"> 
        <!-- These idref attributes refer to the GUIDs of the tasks defined above. A maximum of five tasks are shown per category. -->
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"/>   
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
        </category>
        
        <!-- Programs -->
        <category id="8"> 
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}">
                <sh:name>Click here to play</sh:name>
                <!-- This overrides the defined text. When the Notepad Control 
                     Panel item appears in the Programs category, it uses the 
                     "Click here to play" text for this Solitaire link, instead 
                     of "Play solitaire". -->
            </sh:task>
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
       </category>
   </application>
</applications>
```



> [!Note]  
> <span data-ttu-id="6973e-136">從 Windows 7 開始，您可以使用標準名稱（而不是它的可執行檔名稱）來識別主控台專案： **<sh：控制台>** 元素可用來取代 **<sh：命令>**。</span><span class="sxs-lookup"><span data-stu-id="6973e-136">As of Windows 7, a Control Panel item can be identified by its canonical name rather than its executable name: the **<sh:controlpanel>** element can be used in place of **<sh:command>**.</span></span> <span data-ttu-id="6973e-137">**<sh：控制台>** 元素也會提供屬性，以指定應該開啟之專案的頁面。</span><span class="sxs-lookup"><span data-stu-id="6973e-137">The **<sh:controlpanel>** element also provides an attribute to specify the page of the item to which it should open.</span></span> <span data-ttu-id="6973e-138">以下顯示 **<sh：控制台>** 元素的範例：</span><span class="sxs-lookup"><span data-stu-id="6973e-138">The following shows an example of the **<sh:controlpanel>** element:</span></span>

 


```
<sh:controlpanel name="Microsoft.Presentation" page="pageWallpaper"/>
```



## <a name="localizing-task-links"></a><span data-ttu-id="6973e-139">當地語系化工作連結</span><span class="sxs-lookup"><span data-stu-id="6973e-139">Localizing Task Links</span></span>

<span data-ttu-id="6973e-140">工作連結標題和關鍵字的文字可以儲存在主控台專案模組的字串資料表中。</span><span class="sxs-lookup"><span data-stu-id="6973e-140">The text for the task links' titles and keywords can be stored in a string table in the Control Panel item's module.</span></span> <span data-ttu-id="6973e-141">在此情況下，XML 檔案中使用的格式會變成：</span><span class="sxs-lookup"><span data-stu-id="6973e-141">In that case, the format used in the XML file becomes:</span></span>


```
<sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
    <!-- This is a generated GUID, specific to this task link -->
    <sh:name>@myTextResources.dll,-100</sh:name>
    <sh:keywords>@myTextResources.dll,-101</sh:keywords>
    <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
</sh:task>
```



<span data-ttu-id="6973e-142">在此範例中，工作名稱的文字會出現在 myTextResources.dll 中的字串資源識別碼100，而關鍵字的文字會出現在字串資源識別碼101中。</span><span class="sxs-lookup"><span data-stu-id="6973e-142">In this example, the text for the task's name appears in string resource ID 100 in myTextResources.dll, and the text for the keywords appears in string resource ID 101.</span></span>

## <a name="keywords-and-searching"></a><span data-ttu-id="6973e-143">關鍵字和搜尋</span><span class="sxs-lookup"><span data-stu-id="6973e-143">Keywords and Searching</span></span>

<span data-ttu-id="6973e-144">主控台搜尋會根據其名稱以及其關鍵字來尋找工作連結。</span><span class="sxs-lookup"><span data-stu-id="6973e-144">The Control Panel search finds task links based on their name and also on their keywords.</span></span> <span data-ttu-id="6973e-145">它會比對搜尋中的每個單字和名稱和關鍵字中的單字前置詞。</span><span class="sxs-lookup"><span data-stu-id="6973e-145">It matches each word in the search with the prefix of words in the name and keywords.</span></span> <span data-ttu-id="6973e-146">例如，在先前的範例中，查詢字串「cpu」會符合「查看執行中的進程」工作，因為「cpu」是在關鍵字清單中。</span><span class="sxs-lookup"><span data-stu-id="6973e-146">For example, the query string "cpu" would match the task "See running processes" in the earlier example because "cpu" is in the keyword list.</span></span> <span data-ttu-id="6973e-147">查詢字串 "pro" 也會發現結果，因為 "process" 這個字是以該字串開頭。</span><span class="sxs-lookup"><span data-stu-id="6973e-147">The query string "pro" would also find that result because the title word "processes" begins with that string.</span></span> <span data-ttu-id="6973e-148">請注意，查詢只會符合前置詞。</span><span class="sxs-lookup"><span data-stu-id="6973e-148">Note that the query only matches prefixes.</span></span> <span data-ttu-id="6973e-149">查詢字串 "rocess" 不符合結果，因為該字串（當標題字組 "process" 的一部分）不會開始該文字。</span><span class="sxs-lookup"><span data-stu-id="6973e-149">The query string "rocess" would not match a result because that string, while part of the title word "process", does not begin that word.</span></span>

<span data-ttu-id="6973e-150">當搜尋查詢包含多個標記時，所有標記都必須符合結果的部分關鍵字或工作標題部分的前置詞。</span><span class="sxs-lookup"><span data-stu-id="6973e-150">When a search query contains multiple tokens, all the tokens must match the prefix of some keyword or part of the task title for a result.</span></span> <span data-ttu-id="6973e-151">查詢「cpu 層級」不相符，因為「層級」不在關鍵字組中。</span><span class="sxs-lookup"><span data-stu-id="6973e-151">The query "cpu level" would not match, because "level" is not in the keyword set.</span></span> <span data-ttu-id="6973e-152">「Cpu 執行」查詢會產生結果，因為「cpu」符合關鍵字，而「執行」是工作標題中「正在執行」文字的前置詞。</span><span class="sxs-lookup"><span data-stu-id="6973e-152">The query "cpu run" would give a result, because "cpu" matches a keyword, and "run" is the prefix of the word "running" in the task's title.</span></span>

<span data-ttu-id="6973e-153">主控台不會自動提供拼寫更正或像是複數或斷字等變化。</span><span class="sxs-lookup"><span data-stu-id="6973e-153">Control Panel does not automatically provide spelling correction or variations such as plurals or hyphenation.</span></span> <span data-ttu-id="6973e-154">相符專案也不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6973e-154">Matches are also case-insensitive.</span></span> <span data-ttu-id="6973e-155">為確保成功的關鍵字清單，建議您自行提供變化，例如與螢幕保護裝置相關的這個工作連結： "螢幕保護裝置; 螢幕保護裝置; 螢幕保護裝置;"</span><span class="sxs-lookup"><span data-stu-id="6973e-155">To ensure a successful keyword list, it is recommended to provide variations yourself, such as for this task link that involves screen savers: "screensavers;screen-savers;screen savers;"</span></span>

<span data-ttu-id="6973e-156">不需要新增單數的「螢幕保護裝置」，因為尋找 "屏保" 的查詢也會發現「螢幕保護裝置」，因為首碼相符。</span><span class="sxs-lookup"><span data-stu-id="6973e-156">There is no need to add the singular "screensaver", because a query that finds "screensavers" will also find "screensaver" due to the prefix match.</span></span> <span data-ttu-id="6973e-157">輸入偶數部分的使用者（例如 "screensa"）仍會在具有 "屏保" 作為關鍵字的工作連結上看到相符項。</span><span class="sxs-lookup"><span data-stu-id="6973e-157">A user typing even part of the word, like "screensa" will still see a match on a task link that has "screensavers" as a keyword.</span></span> <span data-ttu-id="6973e-158">若為複數形式變更單字的語言，則必須將使用者可合理輸入的所有表單放入關鍵字中。</span><span class="sxs-lookup"><span data-stu-id="6973e-158">For languages where plural forms change the word, it is necessary to put all the forms a user could reasonably be expected to type into the keywords.</span></span>

<span data-ttu-id="6973e-159">就慣例而言，Microsoft 省略了一組關鍵字的小型單字，例如「如何」或「我想要」。</span><span class="sxs-lookup"><span data-stu-id="6973e-159">As a convention, Microsoft has omitted small words like "how do I" or "I want to" from the set of keywords.</span></span> <span data-ttu-id="6973e-160">預期大部分的使用者只需要輸入最重要的單字，例如「滑鼠」、「高對比」或「視頻驅動程式」以取得結果。</span><span class="sxs-lookup"><span data-stu-id="6973e-160">The expectation is that most users will simply type the most important words such as "mouse", "high contrast", or "video driver" to get results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6973e-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="6973e-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6973e-162">主控台專案</span><span class="sxs-lookup"><span data-stu-id="6973e-162">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="6973e-163">使用者體驗指南</span><span class="sxs-lookup"><span data-stu-id="6973e-163">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="6973e-164">註冊主控台專案</span><span class="sxs-lookup"><span data-stu-id="6973e-164">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="6973e-165">使用 CPLApplet</span><span class="sxs-lookup"><span data-stu-id="6973e-165">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="6973e-166">主控台訊息處理</span><span class="sxs-lookup"><span data-stu-id="6973e-166">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="6973e-167">執行主控台專案</span><span class="sxs-lookup"><span data-stu-id="6973e-167">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="6973e-168">擴充系統主控台專案</span><span class="sxs-lookup"><span data-stu-id="6973e-168">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="6973e-169">指派主控台分類</span><span class="sxs-lookup"><span data-stu-id="6973e-169">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="6973e-170">在 Windows Vista 下存取安全模式下的主控台</span><span class="sxs-lookup"><span data-stu-id="6973e-170">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



