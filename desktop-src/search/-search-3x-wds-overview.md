---
description: Windows Search 是一種桌面搜尋平臺，具有最常見檔案類型和資料類型的即時搜尋功能，而協力廠商開發人員可以將這些功能延伸到新的檔案類型和資料類型。
ms.assetid: 6da601c6-3742-40ad-99f2-8817f7f642b3
title: Windows Search 概觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee4cde62ce663c47ab4cafac0c74ca220fe6faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847823"
---
# <a name="windows-search-overview"></a>Windows Search 概觀

Windows Search 是一種桌面搜尋平臺，具有最常見檔案類型和資料類型的即時搜尋功能，而協力廠商開發人員可以將這些功能延伸到新的檔案類型和資料類型。

本主題的組織方式如下：

-   [簡介](#introduction)
    -   [Windows Search 服務](#windows-search-service)
    -   [開發平臺](#development-platform)
    -   [消費者介面](#user-interface)
-   [技術性必要條件](#technical-prerequisites)
    -   [SDK 下載和內容](#sdk-download-and-contents)
-   [Windows Search SDK 檔](#windows-search-sdk-documentation)
-   [Windows Search 的歷程記錄](#history-of-windows-search)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

Windows Search 是 Windows 7 和 Windows Vista 的標準元件，預設為啟用。 Windows Search 取代 Windows 桌面搜尋 (WDS) （以 Windows XP 和 Windows Server 2003 的增益集的形式提供）。

Windows Search 是由三個元件所組成：

-   [Windows Search 服務](#windows-search-service) (WSS) 
-   [開發平台](#development-platform)
-   [User Interface](#user-interface) (使用者介面)

### <a name="windows-search-service"></a>Windows Search 服務

WSS 會組織檔集合的已解壓縮功能。 Windows Search 通訊協定可讓用戶端與裝載 WSS 的伺服器通訊，以發出查詢並讓系統管理員管理索引伺服器。 處理檔案時，WSS 會分析一組檔、解壓縮有用的資訊，然後組織解壓縮的資訊，以便有效率地傳回這些檔的屬性來回應查詢。

可以查詢的檔集合包含目錄，也就是 Windows Search 中最高層級的組織單位。 目錄代表一組可以查詢的索引檔。 目錄包含具有文字或值的屬性資料表，以及 (地區設定) 儲存在資料表資料行中的對應位置。 資料表的每個資料列都會對應至目錄範圍中的個別檔，而且資料表的每個資料行都會對應至屬性。 目錄可能包含反向的索引 (，以供快速文字比對) 和屬性快取 (快速抓取屬性值) 。

索引子進程會實作為在 LocalSystem 帳戶中執行的 Windows 服務，而且一律會為所有使用者執行 (即使沒有任何使用者登入) ，也會允許 Windows Search 完成下列作業：

-   維護一個在所有使用者之間共用的索引。
-   維護內容存取的安全性限制。
-   從網路上的用戶端電腦處理遠端查詢。

搜尋服務的設計目的是要在編制索引時保護使用者體驗和系統效能。 下列情況會導致服務重新節流或暫停索引：

-   非搜尋相關進程的高 CPU 使用率。
-   高系統 i/o 速率，包括檔案讀取和寫入、分頁檔案和檔案快取 i/o，以及對應的檔案 i/o。
-   記憶體不足的可用性。
-   電池壽命偏低。
-   儲存索引之磁片磁碟機上的磁碟空間不足。

### <a name="development-platform"></a>開發平台

存取搜尋 Api 和建立 Windows Search 應用程式的慣用方法是透過 Shell 資料來源。 Shell 資料來源是一種元件，用來擴充 Shell 命名空間，並公開資料存放區中的專案。 資料存放區是資料的儲存機制。 資料存放區可公開給 Shell 程式設計模型，作為使用 Shell 資料來源的容器。 您可以使用通訊協定處理常式，利用 Windows Search 系統為數據存放區中的專案編制索引。

例如， [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) 是一個元件，可建立搜尋資料夾資料來源的實例，這是由 shell 所提供的一種「虛擬」資料來源，可對 shell 命名空間中的其他資料來源執行查詢並列舉結果。 它可以藉由使用索引子，或手動列舉和檢查指定範圍中的專案來完成。 此介面可讓您使用可建立和修改搜尋資料夾的方法來設定搜尋的參數。 如果未呼叫這個介面的方法，則會改用預設值。

最好透過 Shell 資料模型來間接存取 Windows Search 功能，因為它可讓您存取 Shell 資料模型層級的完整 Shell 功能。 例如，您可以將搜尋範圍設定為程式庫 (這是 Windows 7 和更新版本中可用的功能) 使用程式庫資料夾做為查詢的範圍。 如果資料夾位於不同的電腦) ，Windows Search 接著會匯總這些位置的搜尋結果（如果這些位置位於不同的索引 (）。 Shell 資料層也會建立更完整的專案屬性視圖，合成某些屬性值。 它也可讓您存取未依 Windows Search 編制索引之資料存放區的搜尋功能。 例如，您可以搜尋通用序列匯流排 (USB) 儲存裝置、使用 MTP 通訊協定的可攜式裝置，或透過可存取這些儲存體系統的 Shell 資料來源檔案傳輸通訊協定 (FTP) 伺服器。 這樣做可確保更好的使用者體驗。

Windows Search 具有屬性值的快取，用於在 Windows Search 服務 (WSS) 中執行。 您可以使用 Windows Search OLE DB 提供者或透過 [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory)（代表搜尋結果和查詢型視圖中的專案），以程式設計方式查詢這些屬性值。 然後，Windows Search 會在建立檔（例如 Word 檔）的索引時，收集並儲存由篩選處理常式或屬性處理常式所發出的屬性。 重建索引時，會捨棄並重建此存放區。

協力廠商開發人員可以建立應用程式，以透過程式設計方式查詢來取用索引中的資料，而且可以在索引中擴充自訂檔案和專案類型的資料，以 Windows Search 來編制索引。 如果您想要在 Windows 檔案總管中顯示查詢結果，您必須先執行 Shell 資料來源，才能建立通訊協定處理常式來擴充索引。 但是，如果所有查詢都是以程式設計方式 (透過 OLE DB 例如) ，並由應用程式的程式碼（而非 Shell）所解釋，則 Shell 命名空間仍是慣用的，但並非必要。

需要有通訊協定處理常式，Windows 才能取得檔案內容的相關資訊，例如資料庫或自訂檔案類型中的專案。 雖然 Windows Search 可以為檔案的名稱和屬性編制索引，但 Windows 沒有檔案內容的相關資訊。 如此一來，就無法在 Windows Shell 中建立索引或公開這類專案。 藉由執行自訂通訊協定處理常式，您可以公開這些專案。 如需您嘗試達成之開發人員案例所識別的處理常式清單，請參閱 Windows Search 中的「處理常式總覽」 [作為開發平臺](-search-3x-wds-development-ovr.md)。

> [!Note]  
> Shell 資料來源有時也稱為 Shell 命名空間延伸模組。 處理常式有時也稱為 Shell 擴充或 Shell 擴充處理常式。

 

### <a name="user-interface"></a>使用者介面

在 Windows Vista 和更新版本中，Windows Search 已整合到所有 Windows 檔案總管的視窗中，以便立即存取搜尋。 這可讓使用者依檔案名、屬性和全文檢索內容，快速搜尋檔案和專案。 也可以進一步篩選結果以精簡搜尋。 以下是 Windows Search 的一些功能：

-   每個視窗中的 [立即搜尋] 方塊可讓您立即篩選目前正在觀看的所有專案。 [立即搜尋] 方塊會出現在 [[開始] 功能表] 中，以搜尋程式或檔案，而且在所有 Windows 檔案總管視窗的右上角，以篩選顯示的結果。 即時搜尋也會整合到一些其他的 Windows 功能（例如 Windows Media Player），以尋找相關的檔案。
-   您可以使用關鍵字標記檔，以依使用者定義的自訂準則將它們分組。 標記是使用者或應用程式所指派的中繼資料專案，可讓您更輕鬆地根據可能不在專案名稱或內容中的關鍵字尋找檔案。 例如，可能會將一組圖片標示為「亞利桑那州假期2009」，以便在之後藉由搜尋任何包含的文字來快速取回。
-   Windows 檔案總管 views 中增強的資料行標頭可讓您以不同的方式排序和分組檔。 例如，您可以根據名稱、修改日期、類型、大小和標記來排序檔案。 檔也可以根據這些屬性來分組，而且每個群組可依需要 (隱藏或顯示) 篩選。
-   您可以根據名稱、修改日期、類型、大小和標記來堆疊檔。 堆疊包括具有指定屬性的所有檔，並位於所選資料夾的任何子資料夾內。
-   您可以在 Windows 檔案總管的 [搜尋] 窗格中按一下 [ **儲存搜尋** ] 按鈕，將搜尋儲存 (稍後) 。 結果會在開啟儲存的搜尋時，根據原始準則進行動態重新擴展。 如需相關指示，請參閱 [儲存您的搜尋結果](https://windows.microsoft.com/windows-vista/Save-your-search-results)。
-   預覽處理常式和縮圖處理常式可讓使用者預覽 Windows 檔案總管中的檔，而不需要開啟建立它們的應用程式。

## <a name="technical-prerequisites"></a>技術性必要條件

開始閱讀 Windows Search SDK 檔之前，您應該先對下列概念有基本瞭解：

-   如何執行 Shell 資料來源。
-   如何執行處理常式。
-   如何使用原生程式碼。

Shell 資料來源是一種元件，用來擴充 Shell 命名空間，並公開資料存放區中的專案。 在過去，Shell 資料來源稱為 Shell 命名空間延伸模組。 處理常式是元件物件模型 (COM) 物件，可提供 Shell 專案的功能。 如需您嘗試達成之開發人員案例所識別的處理常式清單，請參閱 Windows Search 中的「處理常式總覽」 [作為開發平臺](-search-3x-wds-development-ovr.md)。

如需 Windows Search SDK 互通性元件的詳細資訊，以使用 Windows Search 所公開的 COM 物件以及其他使用 managed 程式碼的程式，請參閱 [使用 managed 程式碼搭配 Shell 資料和 Windows Search](-search-3x-wds-managed-code.md)。 不過，請注意，篩選準則、屬性處理常式和通訊協定處理常式必須以機器碼撰寫。 這是因為可能的 common language runtime (CLR) 在中執行多個增益集的進程的版本控制問題。 剛開始使用 c + + 的開發人員可以從 [Visual C++ 開發人員中心](https://msdn.microsoft.com/vstudio//default.aspx) 和 [Windows 開發開始使用](../desktop-programming.md)開始著手。

### <a name="sdk-download-and-contents"></a>SDK 下載和內容

除了符合所列的技術先決條件之外，您還必須下載 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) 以取得 Windows Search 程式庫。 [WINDOWS SEARCH SDK 範例](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)包含實用的程式碼範例和互通性元件，可供使用 managed 程式碼進行開發。 如需使用程式碼範例的詳細資訊，請參閱 [Windows Search 程式碼範例](-search-3x-wds-sampleentry.md)。

## <a name="windows-search-sdk-documentation"></a>Windows Search SDK 檔

Windows Search SDK 檔的內容如下所示：

-   [Windows Search 做為開發平台](-search-3x-wds-development-ovr.md)

    概述 Windows Search 中的主要開發案例。 提供您嘗試達成之開發案例所識別的處理常式清單、增益集安裝程式指導方針，以及執行附注。

-   [Windows Search 開發人員指南](-search-developers-guide-entry-page.md)

    提供 [管理索引](-search-3x-wds-mngidx-overview.md)、以程式設計 [方式查詢索引](-search-3x-wds-qryidx-overview.md)、 [擴充索引](-search-3x-wds-extidx-overview.md)，以及 [擴充語言資源](extending-language-resources-in-windows-search.md)的說明。

-   [Windows Search 參考](-search-reference-entry-page.md)

    記錄下列 Windows Search 介面類別別： [通訊協定處理常式](-search-protocol-handlers-interfaces-entry-page.md)、 [查詢](-search-querying-interfaces-entry-page.md)、編目 [範圍](-search-crawl-scope-interfaces-entry-page.md)、 [資料增益集](-search-data-addins-interfaces-entry-page.md)、 [索引管理](-search-index-mgt-interfaces-entry-page.md)和 [通知](-search-notifications-interfaces-entry-page.md)。 參考檔也包含 [常數和](-search-constants-and-enumerations-entry-page.md)列舉、 [結構](-search-structures-entry-page.md)、 [屬性](-search-3x-wds-propertymappings.md)對應，以及 [已儲存的搜尋檔案格式](-search-savedsearchfileformat.md)。

-   [Windows Search 程式碼範例](-search-samples-ovw.md)

    描述可用的搜尋 API 程式碼範例。

-   [Windows 中的同盟搜尋](-search-federated-search-overview.md)

    描述 Windows 7 對遠端資料存放區之搜尋同盟的支援搜尋同盟，這些技術可讓使用者從 Windows 檔案總管記憶體取遠端資料並與其互動。

-   [相關搜尋技術](-search-3x-wds-sampleentry.md)

    列出與 Windows Search 相關的技術：企業搜尋、SharePoint 企業搜尋和繼承應用程式，例如 Windows Desktop Search 2.x 和 Platform SDK：索引服務。

-   [Windows Search 詞彙](search-glossary.md)

    定義 Windows Search 和 Shell 技術中使用的重要詞彙。

## <a name="history-of-windows-search"></a>Windows Search 的歷程記錄

Windows Search 取代 Windows 桌面搜尋 (WDS) （以 Windows XP 和 Windows Server 2003 的增益集的形式提供）。 WDS 已從舊版 Windows 取代舊版的索引服務，並增強效能、可用性和擴充性。 新的開發平臺支援產生更安全且穩定系統的需求。 雖然新的查詢平臺與 Microsoft Windows 桌面搜尋不相容 (WDS) 2.x，但是針對舊版 WDS 所撰寫的篩選器和通訊協定處理常式可以更新以使用 Windows Search。 Windows Search 也支援新的屬性系統。 如需篩選、屬性處理常式和通訊協定處理常式的詳細資訊，請參閱 [擴充索引](-search-3x-wds-extidx-overview.md)。

Windows Search 內建于 Windows Vista 和更新版本，並可作為 WDS 2.x 的可轉散發套件更新，以支援下列作業系統：

-   32位版本的 Windows XP Service Pack 2 (SP2) 。
-   所有 x64 型版本的 Windows XP。
-   Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本。
-   所有 x64 型版本的 Windows Server 2003。

執行這些作業系統的系統必須安裝 Windows Search，才能執行針對 Windows Search 所撰寫的應用程式。 如需詳細資訊，請參閱 [知識庫文章917013： Windows 桌面搜尋3.01 的說明和 Windows 桌面搜尋3.01 的多語系消費者介面套件](https://support.microsoft.com/kb/917013)。

## <a name="additional-resources"></a>其他資源

-   如需建立 Shell 資料來源的詳細資訊，請參閱 [執行基本資料夾物件介面](/previous-versions//bb776815(v=vs.85))。
-   如需 [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) 和 DB 資料夾資料來源的詳細資訊，請參閱系結 \_ \_ \_ [內容字串索引鍵](../shell/str-constants.md)中的 STR PARSE 與 PROPERTIES 常數的描述。 另請參閱 [關聯陣列](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) 和 [IPropertySystem：： GetPropertyDescriptionListFromString](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring)。
-   如需 OLE DB 的詳細資訊，請參閱 [OLE DB 程式設計總覽](/cpp/data/oledb/ole-db-programming-overview?view=vs-2019)。 如需 OLE DB 之 .NET Framework Data Provider 的詳細資訊，請參閱 system.string [命名空間](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1&preserve-view=true) 檔。
-   如需檔案類型處理常式的總覽 (也稱為 Shell 擴充處理常式和搜尋處理常式) ，請參閱 [Windows Search 作為開發平臺](-search-3x-wds-development-ovr.md)。
-   如需有關搜尋技術的社區支援訊息板，請參閱 [MSDN 論壇： Windows 桌面搜尋開發](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads)。
-   如需相關的程式碼範例，請參閱 [Windows Search 程式碼範例](-search-samples-ovw.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Search 做為開發平台](-search-3x-wds-development-ovr.md)
</dt> <dt>

[Windows Search 支援的語言](-search-3x-wds-language-support.md)
</dt> <dt>

[搭配 Shell 資料和 Windows Search 使用 Managed 程式碼](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
