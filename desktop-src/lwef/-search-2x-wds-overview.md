---
title: Windows 桌面搜尋2。x
description: 使用和開發 Microsoft Windows 桌面搜尋的2.x 版 (WDS) 強烈建議您改用 Windows Search。
ms.assetid: 3d73f850-58b8-4a41-8863-e2914661d4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5131fe700b7b049371625249768b0073d009a87
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968283"
---
# <a name="windows-desktop-search-2x"></a>Windows 桌面搜尋2。x

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。

使用和開發 Microsoft Windows 桌面搜尋的2.x 版 (WDS) 強烈建議您改用 [Windows Search](../search/-search-3x-wds-overview.md)。

WDS 是一種索引服務和平臺，可在不同的資料來源和位置快速搜尋檔案和資料。 WDS 可協助使用者和其他應用程式在其電腦上尋找幾乎任何資訊、電子郵件訊息、行事曆約會、相片、檔等等。 此外，WDS 可以在 Windows 檔案總管環境中，從多個資料來源傳回結果，讓您的使用者可以快速預覽、篩選和操作搜尋結果。

WDS 會在指定的編目範圍內、在本機電腦內指定的位置，以及索引子應編目的共用網路中，編制資料的索引。 此編目範圍可由使用者設定選項、管理 Api 和群組原則來控制，而網路系統管理員可以設定這些選項來控制使用者存取權限和索引設定。 群組原則可以限制對特定網路資源的存取，以及定義要編制索引的資源。

本節包含下列主題：

-   [概觀](#windows-desktop-search-2x)
    -   [關於 WDS 索引子](#about-the-wds-indexer)
    -   [關於 WDS 類別目錄](#about-the-wds-catalog)
    -   [關於搜尋引擎和結果](#about-the-search-engine-and-results)
-   [使用 WDS 進行開發](#developing-with-wds)
    -   [使用增益集將資料加入至索引](#adding-data-to-the-index-with-add-ins)
    -   [查詢索引](#querying-the-index)
-   [相容性需求](#compatibility-requirements)
    -   [系統需求](#system-requirements)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

### <a name="about-the-wds-indexer"></a>關於 WDS 索引子

第一次安裝時，索引子會編目我的檔資料夾、Microsoft Outlook 和 Microsoft Outlook Express 電子郵件資料夾中最常見的使用者面向檔案，以及群組原則中指定的位置。 使用者也可以指定新的檔案和位置，讓索引子包含 (，或將) 排除在後續的爬網中。 每個包含的位置都是以 URL 識別，而索引子會從該 URL 開始，並以遞迴方式逐一查看任何子資料夾或位置，直到所有專案都已編制索引為止。 範圍是一組 Url。 自訂應用程式可使用管理 Api 來定義其編目範圍、一組指向通訊協定內路徑的 Url，例如 `file://` 針對磁片磁碟機上的資料夾或 `mapi:// ` OUTLOOK 等 MAPI 電子郵件存放區。 WDS 會使用通訊協定處理常式來存取資料存放區和篩選器，以剖析和編制專案文字和屬性的索引。 然後，此資料會儲存在目錄中。

### <a name="about-the-wds-catalog"></a>關於 WDS 類別目錄

WDS 目錄是從指定的電子郵件、本機磁片磁碟機、網路資源和其他本機資料存放區中的專案收集的文字和屬性的索引。 目錄的內容是以 WDS 設定的選項和規則為基礎、以 WDS 平臺為基礎的應用程式、使用者喜好設定和群組原則。 針對每個編制索引的專案，都有超過200的可用屬性，例如建立日期、大小和特定類型的屬性 ( 「寄件者」) 的電子郵件訊息。 如需這些屬性的清單，請參閱 WDS [架構參考](-search-2x-wds-schematable.md)。

### <a name="about-the-search-engine-and-results"></a>關於搜尋引擎和結果

在 WDS 桌面或 Windows 檔案總管中，使用者可以搜尋索引項目的全文檢索內容和屬性中繼資料。 您也可以從命令列、網頁或自訂應用程式起始相同種類的搜尋。 WDS 搜尋引擎會尋找符合搜尋條件的專案，並將其傳回為 Microsoft ActiveX Data Objects (ADO) 結果集。 WDS 會顯示符合搜尋條件的專案，並可呈現專案的豐富預覽。 您可以建立應用程式來攔截搜尋查詢、執行搜尋，以及/或顯示結果集。

## <a name="developing-with-wds"></a>使用 WDS 進行開發

WDS 有兩種主要類型的整合：將資料新增至索引，以及查詢索引的內容，以抓取符合搜尋準則的記錄。

### <a name="adding-data-to-the-index-with-add-ins"></a>使用 Add-Ins 將資料新增至索引

基本上有兩種類型的資料來源：檔案系統存放區和非檔案系統存放區。 我的檔中的一組檔案是簡單的檔案系統存放區。 WDS 可以搜尋儲存在這類檔案系統中的檔案中的資訊（如果它可以找到檔案類型的篩選器）。 如果您為該檔案類型提供 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)介面的執行，您可以啟用 WDS 來為新的專屬檔案類型編制索引。

非檔案系統存放區（例如資料庫）需要通訊協定處理常式，才能讓 WDS 在資料存放區中流覽和編制資料的索引。 例如，如果您的郵件客戶程式會將收到的電子郵件清單儲存在自己的檔案 (例如 Outlook) 中的 PST 檔案，您可以提供通訊協定處理常式來為每個個別電子郵件編制索引並進行搜尋。 如果資料存放區為階層式，您也必須執行 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)介面，以列舉存放區中的專案。 若要獲得更好的使用者體驗，您可以執行 Shell 擴充功能，以從結果檢視內提供內容功能表和圖示。

目前，WDS 包含超過200種專案類型的篩選 (包括 HTML、XML 和原始程式碼檔案等純文字專案) ，並使用與 SharePoint 服務相同的 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)和通訊協定處理常式技術。 如果您已安裝適用于專屬檔案類型的篩選器，WDS 可以使用現有的篩選介面來為此資料編制索引。

### <a name="querying-the-index"></a>查詢索引

WDS 根據任何可用的架構值，從索引提供自訂結果集的資料。 結果會以 ADO 記錄集的形式傳回。 有四種方式可將 WDS 查詢併入應用程式，每個都提供各種層級的自訂和穩定性。

-   ISearchDesktop 介面-此介面中的 Api 是用來以程式設計方式呼叫 WDS，方法是指定查詢字串、要傳回的資料行清單、類似結構化查詢語言 (SQL)  (SQL) WHERE 子句的範圍限制，以及要排序依據的資料行名稱。 這些 Api 適用于原生和 managed 程式碼。
-   WDS ActiveX 控制項-此控制項會繪製 WDS 搜尋介面，以及管理搜尋和顯示結果。 這個方法比使用 Api 更簡單，但較不具彈性。 若要在 Microsoft Visual Studio 應用程式中使用這個控制項，請從 [**工具**] 功能表移至 [**選擇工具箱專案**] 對話方塊，然後從 [ **COM 元件**] 索引標籤將 [Windows 桌面搜尋-結果檢視器] 新增至 [**工具箱**]。然後，將控制項新增至您想要包含該控制項的表單。 WDS ActiveX 控制項僅與 Windows XP 上的 WDS 2.x 和3.x 相容。
-   命令列參數-應用程式可以呼叫具有各種參數的 WDS 可執行檔，以搜尋和顯示結果。 這會開啟 WDS 視窗，其中顯示結果。 這是將搜尋新增至應用程式的最簡單方式，但不會傳回給呼叫的應用程式任何有關使用者在 WDS 視窗中執行之工作的資訊。
-   WDS 瀏覽器協助程式物件 (BHO) -同樣地，網頁可以使用 BHO 將查詢傳送至 WDS 或已註冊的搜尋應用程式。 針對 WDS 網域安全清單驗證網頁 URL 之後，WDS 會執行查詢並使用標準搜尋介面顯示結果，或將查詢傳遞至已註冊的搜尋應用程式。

使用者可以使用 [先進的查詢語法](-search-2x-wds-aqsreference.md) ，藉由控制搜尋範圍和將搜尋參數與布林運算子結合，來更強大且地查詢目錄。 例如，使用者可以使用類似以下的查詢，從 John 搜尋電子郵件中包含「專案排程」或「專案計劃」的附件： `from:John isattachment:true "project schedule" OR "project plan"` 。

## <a name="compatibility-requirements"></a>相容性需求

WDS 2.6.5 僅適用于 Windows 2000、Windows Server 2003 和 Windows XP。 WDS 是 Microsoft 免費提供的下載，可供個人和企業使用。 您必須先安裝此應用程式，並將其用於為 WDS 2.6.5 建立的應用程式，才能為使用者帳戶編制索引。

### <a name="system-requirements"></a>系統需求

使用 Windows 桌面搜尋需要下列各項：

-   Windows Internet Explorer 或更新版本。
-   若要在目錄中包含您的電子郵件訊息，您必須有 Microsoft Microsoft Outlook 2000 或更新版本，或 Microsoft Outlook Express 6.0 或更新版本。
-   您需要 Office XP 或更新版本，才能在結果檢視中進行 Microsoft Microsoft Office 檔的完整預覽。
-   最小 Pentium 500 MHz 處理器 (1 GHz 建議的) 。
-   Windows XP、Windows 2000 SP4 或更新版本，或 Windows Server 2003 Service Pack 1。
-   最少 128 MB 的 RAM (256 MB 的建議) 。
-   建議使用 500 MB 的可用硬碟空間。 索引的大小取決於您已編制索引的內容數量。
-   建議使用 1024 x 768 螢幕解析度。

## <a name="related-topics"></a>[相關主題]

1.  查詢索引

    -   [透過 ISearchDesktop 以程式設計方式呼叫 WDS () ](-search-2x-wds-callingwdsprogrammatically.md)
    -   [從 Web Pages 呼叫 WDS](-search-2x-wds-browserhelpobject.md)
    -   [從命令列呼叫 WDS](-search-2x-wds-fromcommandline.md)

2.  [擴充索引 (總覽) ](-search-2x-wds-extendingtheindex.md)

    -   [開發 IFilter 增益集](-search-2x-wds-ifilteraddins.md)
    -   [開發通訊協定處理常式](-search-2x-wds-phaddins.md)

3.  一般參考

    -   [WDS 架構](-search-2x-wds-schematable.md)
    -   [進階查詢語法](-search-2x-wds-aqsreference.md)
    -   [WDS 感知類型](-search-2x-wds-perceivedtype.md)

 

 