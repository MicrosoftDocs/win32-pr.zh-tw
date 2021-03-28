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
# <a name="creating-searchable-task-links-for-a-control-panel-item"></a>建立主控台專案的可搜尋工作連結

從 Windows Vista，主控台類別目錄檢視會在每個主控台專案的圖示下提供工作連結，如下所示。

![[系統和維護類別] 頁面上的工作連結](images/controlpaneltasklinks.png)

當使用者在視窗右上角的 [ **搜尋** ] 方塊中輸入文字時，搜尋結果會包含這些工作連結，如下所示搜尋「顯示」一字。

![控制台搜尋結果中的工作連結](images/controlpanelsearchresults.png)

本主題將討論下列內容：

-   [工作連結的最佳作法](#task-link-best-practices)
-   [建立工作 XML 檔案](#creating-a-task-xml-file)
-   [當地語系化工作連結](#localizing-task-links)
-   [關鍵字和搜尋](#keywords-and-searching)
-   [相關主題](#related-topics)

## <a name="task-link-best-practices"></a>工作連結的最佳作法

建議您為主控台專案提供工作連結，以協助使用者搜尋功能。 您也可以將關鍵字新增至工作連結，讓使用者即使不知道工作的標題或詞彙也可以找到它們。

最佳的工作連結有三個用途：

1.  提供主控台專案功能的快捷方式。
2.  提供關鍵字，讓使用者可以使用自己的語言來搜尋。 使用者可能會想要輸入「壓縮」，因為他或她知道技術術語。 使用者可以輸入「DB 太大」或「資料庫 filesize」。 在工作中加入適當的關鍵字，表示使用者可以找到您的主控台專案。
3.  提供有關主控台專案用途的提示。 當使用者看到位於主控台專案圖示下方的連結時，他們可以取得有關主控台專案的使用方式，而不是單獨提供的名稱和圖示的詳細資訊。

工作連結應以終端使用者為主，而不是以技術或功能為主。 例如，「啟用資料庫壓縮」會是不正確的用語，因為這是大部分使用者都不熟悉的技術術語。 「讓我的資料庫檔案變小」是比較好的做法，因為它提及使用者的實際結束目標，而不是取得該機制。 目標不是要 oversimplify，而是要以使用者想要完成的工作來說出工作。

## <a name="creating-a-task-xml-file"></a>建立工作 XML 檔案

工作連結是在 XML 檔案中定義。 本節提供範例 .xml 檔案的詳細資料，該檔案會針對稱為「 **記事本**」的主控台專案定義三個工作連結。 它會定義工作連結的標題、關鍵字和命令列。 它也會說明如何指定哪些工作連結會出現在哪個類別下。 註冊要出現在多個類別目錄中的主控台專案，可以選擇根據分類來顯示不同的連結。 提供各種專案的說明，以及提供的資訊，會以 XML 本身的批註形式提供。


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
> 從 Windows 7 開始，您可以使用標準名稱（而不是它的可執行檔名稱）來識別主控台專案： **<sh：控制台>** 元素可用來取代 **<sh：命令>**。 **<sh：控制台>** 元素也會提供屬性，以指定應該開啟之專案的頁面。 以下顯示 **<sh：控制台>** 元素的範例：

 


```
<sh:controlpanel name="Microsoft.Presentation" page="pageWallpaper"/>
```



## <a name="localizing-task-links"></a>當地語系化工作連結

工作連結標題和關鍵字的文字可以儲存在主控台專案模組的字串資料表中。 在此情況下，XML 檔案中使用的格式會變成：


```
<sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
    <!-- This is a generated GUID, specific to this task link -->
    <sh:name>@myTextResources.dll,-100</sh:name>
    <sh:keywords>@myTextResources.dll,-101</sh:keywords>
    <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
</sh:task>
```



在此範例中，工作名稱的文字會出現在 myTextResources.dll 中的字串資源識別碼100，而關鍵字的文字會出現在字串資源識別碼101中。

## <a name="keywords-and-searching"></a>關鍵字和搜尋

主控台搜尋會根據其名稱以及其關鍵字來尋找工作連結。 它會比對搜尋中的每個單字和名稱和關鍵字中的單字前置詞。 例如，在先前的範例中，查詢字串「cpu」會符合「查看執行中的進程」工作，因為「cpu」是在關鍵字清單中。 查詢字串 "pro" 也會發現結果，因為 "process" 這個字是以該字串開頭。 請注意，查詢只會符合前置詞。 查詢字串 "rocess" 不符合結果，因為該字串（當標題字組 "process" 的一部分）不會開始該文字。

當搜尋查詢包含多個標記時，所有標記都必須符合結果的部分關鍵字或工作標題部分的前置詞。 查詢「cpu 層級」不相符，因為「層級」不在關鍵字組中。 「Cpu 執行」查詢會產生結果，因為「cpu」符合關鍵字，而「執行」是工作標題中「正在執行」文字的前置詞。

主控台不會自動提供拼寫更正或像是複數或斷字等變化。 相符專案也不區分大小寫。 為確保成功的關鍵字清單，建議您自行提供變化，例如與螢幕保護裝置相關的這個工作連結： "螢幕保護裝置; 螢幕保護裝置; 螢幕保護裝置;"

不需要新增單數的「螢幕保護裝置」，因為尋找 "屏保" 的查詢也會發現「螢幕保護裝置」，因為首碼相符。 輸入偶數部分的使用者（例如 "screensa"）仍會在具有 "屏保" 作為關鍵字的工作連結上看到相符項。 若為複數形式變更單字的語言，則必須將使用者可合理輸入的所有表單放入關鍵字中。

就慣例而言，Microsoft 省略了一組關鍵字的小型單字，例如「如何」或「我想要」。 預期大部分的使用者只需要輸入最重要的單字，例如「滑鼠」、「高對比」或「視頻驅動程式」以取得結果。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[主控台專案](control-panel-applications.md)
</dt> <dt>

[使用者體驗指南](user-experience-guidelines.md)
</dt> <dt>

[註冊主控台專案](registering-control-panel-items.md)
</dt> <dt>

[使用 CPLApplet](using-cplapplet.md)
</dt> <dt>

[主控台訊息處理](message-processing.md)
</dt> <dt>

[執行主控台專案](executing-control-panel-items.md)
</dt> <dt>

[擴充系統主控台專案](extending-system-control-panel-items.md)
</dt> <dt>

[指派主控台分類](assigning-control-panel-categories.md)
</dt> <dt>

[在 Windows Vista 下存取安全模式下的主控台](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



