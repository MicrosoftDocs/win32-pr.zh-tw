---
description: 您可以使用設定和記錄 Api 來擴充家長監護。
ms.assetid: f0fc1b11-6de4-48f6-afc9-f05c8812d2bd
title: 家長監護擴充功能總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf609c08a4114d7d96ae600744879bda53ac483d90bcd25def3dd0d5f9e3c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971717"
---
# <a name="parental-controls-extensibility-features-overview"></a>家長監護擴充功能總覽

您可以使用設定和記錄 Api 來擴充家長監護。

-   [記錄-背景](/windows)
-   [記錄延伸](#logging-extensibility)
-   [父控制項面板一般 UI 擴充性連結新增](#parental-controls-panel-general-ui-extensibility-link-addition)
-   [取代網路內容篩選](#web-content-filter-replacement)

## <a name="loggingbackground"></a>記錄-背景

Microsoft 已定義一些標準事件來解決常見的活動：

-   System：家長監護設定變更、帳戶變更、系統時鐘變更、失敗的登入嘗試。
-   使用者：
    -   系統/時間限制：登入時間、登出、應用程式執行嘗試和應用程式執行持續時間 (請參閱) 的附注。
    -   Web 限制：已造訪和封鎖網站，檔案下載嘗試。 Web 瀏覽器和類似瀏覽器的應用程式不需要記錄這些，因為 Web 內容篩選器會執行這項操作。 取代的網頁篩選器需要產生這些事件。
    -   遊戲：遊戲的遊戲和封鎖、遊戲結束 (事件，以及提供) 播放的持續時間。
    -   允許和封鎖特定程式：執行嘗試、關機、受一般應用程式限制封鎖。
    -   立即訊息：轉換初始嘗試、對話聯結嘗試、對話離開、影片/音訊/遊戲/短訊息服務/檔案傳輸/URL 交換功能、連絡人清單變更嘗試。
    -   電子郵件：已接收或接收封鎖、傳送嘗試、連絡人清單變更嘗試。
    -   媒體：媒體已播放並嘗試。

並非所有先前的事件都適合應用程式使用。 帳戶變更、系統時鐘變更，以及登入和登出事件記錄只會由作業系統執行，因此不會公開。

> [!Note]  
> 應用程式專案和結束事件的檢測可在 Windows Vista 中使用，並由家長監護設定以記錄此資料。

 

## <a name="logging-extensibility"></a>記錄延伸

一般自訂事件也會以3個可用的標籤/值來定義，因此 Isv 通常不需要在資訊清單中定義自己的標記/值。 記錄檢視器會辨識並顯示標籤標頭和值（如果使用 (1 到3的欄位數目）) ，而且每個欄位的標題都是使用 WMI API 來註冊。 一般事件檢視器也可以用來查看自訂事件。

如果泛型自訂事件不適合，ISV 可以使用應用程式資訊清單來定義它自己，而且可以使用相同的 WMI API 來註冊最多三個欄位的標頭。

isv 可以選擇定義自己的事件，並透過公用 Windows api，獨立于記錄檢視器中使用它們。 這並沒有完整記錄集中的優點。

## <a name="parental-controls-panel-general-ui-extensibility-link-addition"></a>父控制項面板一般 UI 擴充性連結新增

一般用途的使用者介面擴充性連結是透過 WMI 存取設定來公開，並以名稱資源 DLL 路徑和識別碼、影像 (點陣圖) 路徑、已停用狀態影像 (點陣圖) 路徑、子標題資源 DLL 路徑和識別碼，以及可執行檔路徑規格來建立延伸模組實例。 註冊之後，連結會出現在 [家長監護] 面板的 [更設定] 區域中，然後按一下它將會叫用指定的可執行檔。

可執行檔路徑字串可以選擇性地包含目前使用者的 SID 的標記，以在叫用之前加以取代。 如果可執行檔需要知道 SID，則這可讓連結執行在目前正在查看其中樞頁面的使用者內容中運作。

## <a name="web-content-filter-replacement"></a>取代網路內容篩選

如主題中所述，「家長監護」 [In-Box 限制和使用者介面](parental-controls-in-box-restrictions-and-user-interfaces.md)，可以使用廠商提供的篩選來取代內建的 Web 內容篩選器。 這是透過 WMI 存取設定來執行，以設定擁有篩選的 GUID 和名稱。

一般 UI 擴充性機制可用來公開協力廠商篩選。 這與要出現在最上層家長監護台的 [更設定] 區段中的任何延伸模組所使用的機制相同。 若要在系統層級篩選設定中將相同的 GUID 和適當的名稱資源 DLL 路徑和識別碼設定為額外的步驟，將會隱藏內建的篩選器連結，而協力廠商的專案則會顯示在 [更多設定] 區段的上方。 針對篩選所註冊的名稱將會顯示在 [摘要] 區段中。

重設篩選 GUID 和名稱路徑/識別碼設定，會導致內建的 Web 內容篩選器將本身重新建立為使用中的篩選器，然後再次出現在 Windows 設定] 區段中。

請注意，協力廠商篩選準則不受限於用來插入 Windows 通訊的技術。 篩選器只必須使用擴充性連結來公開其設定，並接受適當的家長監護設定。

 

 
