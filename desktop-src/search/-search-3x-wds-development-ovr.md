---
description: 若要為新檔案格式和資料存放區的內容和屬性編制索引，Microsoft Windows Search 必須使用增益集進行擴充。
ms.assetid: 04ddcd97-c358-44d2-9092-a035436c50c9
title: Windows Search 做為開發平台
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19041ac23c90006cc2f1b2f6146cb20a6b972fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689899"
---
# <a name="windows-search-as-a-development-platform"></a>Windows Search 做為開發平台

若要為新檔案格式和資料存放區的內容和屬性編制索引，Microsoft Windows Search 必須使用增益集進行擴充。

在新檔案格式和資料存放區的協力廠商開發人員之前，您必須先執行下列三項作業，才能讓這些格式和存放區以 Windows 檔案總管的形式出現在查詢結果中：

-   執行 Shell 資料來源，以擴充 Shell 命名空間。
-   公開資料存放區中的專案 (如果它們正在加入新的資料存放區，因為它需要編制索引) 。
-   開發通訊協定處理常式，讓 Windows Search 可以存取用來編制索引的資料。

本主題的組織方式如下：

-   [快速入門](#getting-started)
-   [搜尋開發案例總覽](#overview-of-search-development-scenarios)
    -   [新增資料存放區](#adding-a-new-data-store)
    -   [新增檔案格式](#adding-a-new-file-format)
    -   [使用 Windows Search 結果](#consuming-windows-search-results)
-   [處理常式總覽](#overview-of-handlers)
-   [增益集安裝程式指導方針](#add-in-installer-guidelines)
-   [實施者注意事項](#note-to-implementers)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="getting-started"></a>開始使用

在您開始建立 Windows Search 應用程式之前，請記住，慣用的方法是透過 Shell 資料來源。 Shell 資料來源會擴充 Shell 命名空間，並公開資料存放區中的專案。 然後，您可以使用通訊協定處理常式，利用 Windows Search 系統為數據存放區中的專案編制索引。 建議您藉由實作為 Shell 資料來源來存取 Windows Search 的間接方法，因為它可提供完整 Shell 功能的存取權。 如此一來，即可確保合理的使用者體驗。

如果您希望查詢結果出現在 Windows 檔案總管中，您必須先執行 Shell 資料來源，才能建立通訊協定處理常式來擴充索引。 但是，如果所有查詢都是以程式設計方式 (透過 OLE DB 例如) ，並由應用程式的程式碼（而非 Shell）所解釋，則會優先使用 Shell 命名空間，但不是必要的。

需要有通訊協定處理常式，Windows 才能取得檔案內容的知識，例如資料庫或自訂檔案類型中的專案。 雖然 Windows Search 可以為檔案的名稱和屬性編制索引，但 Windows 並不知道該檔案的內容。 如此一來，就無法在 Windows Shell 中建立索引或公開這類專案。 藉由執行自訂通訊協定處理常式，您可以公開這些專案。 如需您嘗試達成之開發人員案例所識別的處理常式清單，請參閱 [處理常式的總覽](#overview-of-handlers)。

## <a name="overview-of-search-development-scenarios"></a>搜尋開發案例總覽

Windows Search 最常見的開發案例如下：

-   [新增資料存放區](#adding-a-new-data-store)
-   [新增檔案格式](#adding-a-new-file-format)
-   [使用 Windows Search 結果](#consuming-windows-search-results)

### <a name="adding-a-new-data-store"></a>新增資料存放區

只有當您要新增要編制索引的新資料存放區時，才需要適用于 Windows Search 的 Shell 資料存放區。 資料存放區是資料的儲存機制，可使用 Shell 資料來源，以容器的形式公開給 Shell 程式設計模型。 然後，您可以使用通訊協定處理常式，利用 Windows Search 系統為數據存放區中的專案編制索引。 通訊協定處理常式會執行以原生格式存取內容來源的通訊協定。 [**ISearchProtocol**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol)和 [**ISearchProtocol2**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol2)介面是用來執行自訂的通訊協定處理常式，以展開可編制索引的資料來源。 如需建立 Shell 資料來源的詳細資訊，請參閱 [執行基本資料夾物件介面](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))。

### <a name="adding-a-new-file-format"></a>新增檔案格式

如果您加入新的自訂檔案格式，則需要開發篩選處理常式或屬性處理常式，但不能同時進行兩者。 篩選是 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的實作為。 它會開啟特定檔案類型的檔案，並篩選索引子的屬性和文字區塊。 篩選器會與檔案類型相關聯，如副檔名、MIME 類型或類別識別碼所表示 (Clsid) 。 雖然一個篩選器可以處理多個檔案類型，但每個檔案類型只能使用一個篩選準則。

屬性處理常式會將儲存在檔案中的資料轉譯成可辨識的結構化架構，並且可由 Windows 檔案總管、Windows Search 和其他應用程式存取。 這些系統接著可以與屬性處理常式互動，以在檔案之間進行寫入和讀取屬性。 轉譯的資料包含詳細資料檢視、提示、詳細資料窗格、屬性頁等等。 每個屬性處理常式都與特定檔案類型相關聯，該檔案類型是由副檔名所識別。 您需要屬性處理常式來執行下列作業：

-   在 UI 中顯示非索引項目目屬性。
-   支援寫入屬性。

### <a name="consuming-windows-search-results"></a>使用 Windows Search 結果

下列各節將說明數種使用 Windows Search 結果的方式：

-   [查詢資料](#querying-data)
-   [查詢遠端資料存放區 (同盟搜尋) ](#querying-remote-data-stores-federated-search)
-   [編制檔案和專案的索引](#indexing-files-and-items)
-   [編制資料存放區索引](#indexing-a-data-store)
-   [管理索引編制程式](#managing-the-indexing-process)
-   [將 Windows 屬性系統與 Windows Search 應用程式整合](#integrating-the-windows-property-system-with-windows-search-applications)

### <a name="querying-data"></a>查詢資料

在結合的 Windows Search 和 Windows 屬性系統上撰寫應用程式的開發人員，不論應用程式或檔案類型為何，都可以存取檔案和專案。 有兩種方式可讓應用程式存取索引子資料：

-   應用程式會將 Windows Search 結構化查詢語言 (SQL)  (SQL) 查詢傳送給 Windows Search OLE DB 提供者，以直接與 OLE DB 通訊，以取得結果。 您可以手動建立查詢，也可以使用 [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) 介面從搜尋關鍵字產生 SQL，並使用 Advanced Query 語法 (AQS) 。
-   應用程式會透過 Shell 層運作。 Shell 層的優點是它也支援 grep 之類的其他來源。 但缺點是，並非所有索引子功能都可以使用。

另一個選項是使用 search-ms：//和 search://通訊協定，其會執行透過 Windows 檔案總管轉譯的 URL 式搜尋。 此選項可啟用最輕量的開發，但不會將結果或使用者選取範圍從結果檢視傳回給呼叫應用程式。 此外，與其他通訊協定一樣，如果應用程式符合所需的功能集，則協力廠商搜尋應用程式可以接管搜尋 ms：//和 search://通訊協定。 如需查詢的詳細資訊，請參閱 [Windows Search 中的查詢](querying-process--windows-search-.md) 程式，並以程式設計 [方式查詢索引](-search-3x-wds-qryidx-overview.md)。

### <a name="querying-remote-data-stores-federated-search"></a>查詢遠端資料存放區 (同盟搜尋) 

在 Windows 7 和更新版本中，同盟搜尋提供了新的搜尋提供者，可透過 web 伺服器、透過 [OpenSearch](https://github.com/dewitt/opensearch) 通訊協定來查詢遠端資料存放區，並將結果列舉為 RSS 或 Atom XML 摘要。 搜尋連接器是使用搜尋提供者模擬資料夾行為的命名空間連接。 如需有關 Windows 7 中遠端資料存放區之搜尋同盟的詳細資訊，請參閱 [windows 中](-search-federated-search-overview.md)的同盟搜尋。

### <a name="indexing-files-and-items"></a>編制檔案和專案的索引

索引的內容是根據 Windows Search 隨附的增益集所支援的檔案和資料類型，以及檔案系統中資料夾的預設包含和排除規則。 例如，Windows 搜尋中包含的篩選器支援超過200種常見的資料類型，包括 Microsoft Office 檔、Microsoft Outlook 電子郵件 (與 MAPI 通訊協定處理常式) 、純文字檔、HTML 及其他更多。 如需原生支援檔案類型的完整清單，請參閱 [索引中包含的內容](-search-3x-wds-included-in-index.md)。

您可以使用屬性處理常式和篩選來擴充索引，以將新檔案格式的內容和屬性公開給索引及 Windows 檔案總管。 篩選是 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的實作為。 篩選器有兩種：一個與個別專案互動，例如檔案，另一個則與容器（例如資料夾）互動。 篩選準則有多個用途，因為它們支援區塊化資料、文字內容、某些屬性，以及多種語言。

相反地，屬性處理常式具有更明確的用途：若要公開由副檔名識別的特定檔案類型的屬性。 檔案類型的屬性處理常式可以啟用 get 和 set 屬性，也可以列舉與該檔案類型相關聯的屬性。 與篩選準則不同的是，屬性處理常式不支援 chucking 資料或文字內容，而且屬性處理常式無法指出 text 屬性在哪種語言中，除非它們支援寫入屬性。

### <a name="indexing-a-data-store"></a>編制資料存放區索引

您可以使用通訊協定處理常式來擴充索引，以提供專屬資料存放區的存取權。 例如，非檔案系統資料存放區中所包含的檔案和專案 (例如資料庫和電子郵件存放區) 需要通訊協定處理常式才能從 URL 對應至資料流程。 通訊協定處理常式也可以選擇性地判斷要用來從資料流程中解壓縮資訊的正確篩選器。 篩選會列舉資料存放區 Url。 然後使用適當的篩選和/或屬性處理常式來個別編制專案的索引。 如需詳細資訊，請參閱 [擴充索引](-search-3x-wds-extidx-overview.md)。

### <a name="managing-the-indexing-process"></a>管理索引編制程式

應用程式開發人員可以使用各種管理介面來控制 Windows Search 索引的範圍和頻率。 這些介面包括新增和移除索引子掃描變更之目錄的功能、以手動方式通知索引變更資料、檢查索引子的狀態，以及強制重新編制部分或所有資料的索引。 如需詳細資訊，請參閱 [管理索引](-search-3x-wds-mngidx-overview.md)。

### <a name="integrating-the-windows-property-system-with-windows-search-applications"></a>將 Windows 屬性系統與 Windows Search 應用程式整合

Windows 屬性系統是資料定義的可擴充讀取/寫入系統，可提供統一的方式來表示 Shell 專案的中繼資料。 Windows Vista 和更新版本中的 Windows 屬性系統可讓您儲存和取得 Shell 專案的中繼資料。 Shell 專案是任何一段內容，例如檔案、資料夾、電子郵件或連絡人。 屬性是與 Shell 專案相關聯之中繼資料的個別部分。 屬性值會以 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構表示。

許多常見的專案類型（例如相片、音樂、檔、郵件、連絡人和檔案）都包含廣泛的通用屬性清單。 如果沒有任何現有的屬性符合其需求，開發人員也可以將自己的屬性引入平臺。 如需將應用程式與 Windows 屬性系統整合的詳細資訊，請參閱 [開發屬性處理常式](-search-3x-wds-extidx-propertyhandlers.md)。

## <a name="overview-of-handlers"></a>處理常式總覽

處理常式是元件物件模型 (COM) 物件，可提供 Shell 專案的功能。 大部分的 Shell 資料來源都會提供可延伸的系統，以便將處理常式系結至專案。 例如，檔系統資料夾使用關聯系統來查閱特定檔案類型的處理常式。 每個檔案類型都需要特定的處理常式。 Adobe Acrobat .pdf 檔案類型需要一個篩選器處理常式，例如，doc 檔案格式需要另一個篩選處理常式等等。

不同的處理常式有一些共同點。 在 Windows Vista 和更新版本中，所有處理常式都必須使用下列其中一個介面來初始化處理常式： [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)、 [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)或 [**IItinitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)。

下表列出高階開發人員工作、每項工作所需的處理常式類型，並提供有關如何執行每項工作之概念資訊的連結。



| Task                                                                                                                                                            | 處理常式                          | 概念資訊                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 存取檔案的屬性以進行編制索引                                                                                                                 | 屬性處理常式                 | [開發屬性處理常式](-search-3x-wds-extidx-propertyhandlers.md)<br/> [自訂檔案格式的系統定義屬性](-shell-systemdefinedpropertiesforfileformats.md)<br/> |
| 為數據物件新增剪貼簿格式 (專案的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject))  (資料物件用於拖放和複製/貼上案例中。 )  | 資料物件處理常式              | [建立資料處理程式](/previous-versions/windows/desktop/legacy/cc144163(v=vs.85))                                                                                                                                                          |
| 為一般顯示在快捷方式功能表中的專案新增動詞                                                                                         | 快速鍵功能表處理常式            | [建立內容功能表處理常式](../shell/context-menu-handlers.md)<br/> [使用動態動詞自訂快捷方式功能表](../shell/shortcut-menu-using-dynamic-verbs.md)<br/>                         |
| 建立檔案類型與特定圖示的關聯                                                                                                                    | 圖示處理常式                     | [建立圖示處理常式](../shell/how-to-create-icon-handlers.md)                                                                                                                                                          |
| 使用可允許自訂與檔案類型互動的 UI 圖片和控制項來建立屬性工作表                                                          | 屬性工作表處理常式           | [屬性工作表處理常式](/previous-versions/windows/desktop/legacy/cc144106(v=vs.85))                                                                                                                                                    |
| 啟用專案類型以支援拖放和複製/貼上案例                                                                                         | 捨棄處理常式                     | [使用拖放和剪貼簿傳送 Shell 物件](/previous-versions/windows/desktop/legacy/bb776905(v=vs.85))                                                                                                                      |
| 解壓縮文字和檔案屬性的區塊以進行索引                                                                                                  | 篩選處理常式                   | [開發篩選處理常式](-search-ifilter-conceptual.md)                                                                                                                                           |
| 建立新檔案類型的索引                                                                                                                                        | 篩選處理常式，屬性處理常式 | [開發篩選處理常式](-search-ifilter-conceptual.md)<br/> [開發屬性處理常式](-search-3x-wds-extidx-propertyhandlers.md)<br/>                                          |
| 為數據存放區的內容編制索引                                                                                                                           | 通訊協定處理常式                 | [開發通訊協定處理常式](-search-3x-wds-phaddins.md)                                                                                                                                            |
| 在 Windows 檔案總管預覽窗格中預覽 Shell 專案的簡化視圖                                                                             | 預覽處理常式                  | [預覽處理常式](../shell/preview-handlers.md)                                                                                                                                                             |
| 當滑鼠停留在 UI 物件上時提供快顯文字                                                                                                      | 資訊提示處理常式                  | [建立 Shell 擴充處理常式](../shell/handlers.md) (提示自訂)                                                                                                                             |
| 提供靜態影像以表示 Shell 專案                                                                                                              | 縮圖處理常式                | [縮圖處理常式](/previous-versions/windows/desktop/legacy/cc144118(v=vs.85))                                                                                                                                                        |



 

下表列出處理常式的處理常式和介面，以及用來執行每一種處理常式的介面。



| 處理常式                | 介面                                                                                                                                                                                                                                                                                                                                                                |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 捨棄處理常式           | [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)、 [**IDropTargetHelper**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idroptargethelper)、 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)、 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)                                                                                                                                                                                                      |
| 資料物件處理常式    | [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)、 [ **IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)                                                                                                                                                                                                                                                                                                  |
| 篩選處理常式         | [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)<br/>                                                                                                                                                                                                                                                                                                                             |
| 圖示處理常式           | [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)<br/> 選用： [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist)、 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)<br/>                                                                                                                                                                                                                                 |
| 資訊提示處理常式        | [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                                                                                                                                                                                                                                                                                                                                        |
| 預覽處理常式        | [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)                                                                                                                                                                                                                                                                                                                              |
| 屬性處理常式       | [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                                                                                                                                                                                                                                                                                           |
| 通訊協定處理常式       | [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)、 [**ISearchProtocol**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol)、 [**IUrlAccessor**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor)<br/> 選用： [**ISearchProtocol2**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol2)、 [**IUrlAccessor2**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor2)、 [**IUrlAccessor3**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor3)、 [**IUrlAccessor4**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor4)<br/> |
| 屬性工作表處理常式 | [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)、 [ **IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)                                                                                                                                                                                                                                                                              |
| 快速鍵功能表處理常式  | [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)、 [**IExplorerCommand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)、 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)                                                                                                                                                                                                                                          |
| 縮圖處理常式      | [**IThumbnailProvider**](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider)                                                                                                                                                                                                                                                                                                                        |



 

> [!Note]  
> 屬性處理常式有時候會 kown 為元資料處理程式。 Shell 資料來源有時也稱為 Shell 命名空間延伸模組。 檔案類型處理常式有時也稱為 Shell 擴充處理常式或 Shell 延伸模組。

 

如需建立處理常式的詳細資訊，請參閱 [建立 Shell 擴充處理常式](../shell/handlers.md)。 如需屬性的詳細資訊，請參閱 [Windows 屬性系統](../properties/windows-properties-system.md)。

## <a name="add-in-installer-guidelines"></a>增益集安裝程式指導方針

建立增益集安裝程式時，請使用下列指導方針：

-   安裝程式必須使用 EXE 或 MSI 安裝程式。
-   必須提供版本資訊。
-   每個安裝的增益集都必須建立 [ **新增/移除程式** ] 專案。
-   安裝程式必須接管目前增益集所瞭解的特定檔案類型或存放區的所有登錄設定。
-   如果先前的增益集遭到覆寫，安裝程式應通知使用者。
-   如果較新的增益集已覆寫先前的增益集，使用者應該能夠還原先前增益集的功能，並將它再次設為該檔案類型或存放區的預設增益集。

## <a name="note-to-implementers"></a>實施者注意事項

建立篩選器或屬性處理常式之前，開發人員應該考慮下列事項：

-   這些處理常式是載入至您無法控制之進程的同進程擴充，例如篩選背景程式進程、Windows 檔案總管 (grep 搜尋) 以及 Windows Mail) 等協力廠商主機。
-   您必須撰寫穩固的安全程式碼，以處理所建立用來攻擊系統的檔案格式的任意損毀形式。
-   您的增益集不能洩漏會產生主機進程問題的資源。
-   您的增益集不會當機，因為這也會讓主機進程損毀，並減緩篩選進程的速度。
-   因為這些處理常式是在背景系統進程中執行，所以它們必須快速執行，而且必須使用最少的 CPU 和 i/o，才能符合系統的效能需求。

因此，開發人員應該撰寫這些增益集，以建立系統層級程式碼的專業知識。

## <a name="additional-resources"></a>其他資源

-   如需建立 Shell 資料來源的詳細資訊，請參閱 [執行基本資料夾物件介面](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))。
-   對於需要使用 Shell 預設系統資料夾 View 物件 (DefView) 的資料來源，請參閱 [執行資料夾檢視](../lwef/nse-folderview.md)、 [**SHCreateShellFolderView**](/windows/win32/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview) 函式和 [**SFV \_ CREATE**](/windows/win32/api/shlobj_core/ns-shlobj_core-sfv_create) structure。 使用 Shell 預設系統資料夾 View 物件 (DefView) 的資料來源必須執行下列一組介面： [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)、 [**IShellFolder2**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder2)、 [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)、 [**IPersistFolder2**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2)和 (選擇性地) [**IPersistFolder3**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3)。 如果您的 **IShellFolder** 執行不使用 **SHCreateShellFolderView** 來建立 DefView，Shell View 物件可能需要 [**IFolderView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifolderview)。
-   [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) 是 Shell 資料來源取用者的主要介面，稱為 DBFolder。 如需 DBFolder 的詳細資訊，請參閱系結 \_ \_ \_ [**內容字串索引鍵**](../shell/str-constants.md)中的 STR PARSE 與 PROPERTIES 常數的描述。 另請參閱 [關聯陣列](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) 和 [**IPropertySystem：： GetPropertyDescriptionListFromString**](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring)。
-   如需 OLE DB 的詳細資訊，請參閱 [OLE DB 程式設計總覽](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx)。 如需 OLE DB 之 .NET Framework Data Provider 的詳細資訊，請參閱 system.string [命名空間](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) 檔。
-   如需搜尋技術上支援社區的訊息面板，請參閱 MSDN 上的 [Windows：搜尋論壇](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads) （英文）。
-   如需相關的程式碼範例，請參閱 [Windows Search 程式碼範例](-search-samples-ovw.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Search 概觀](-search-3x-wds-overview.md)
</dt> <dt>

[Windows Search 支援的語言](-search-3x-wds-language-support.md)
</dt> <dt>

[搭配 Shell 資料和 Windows Search 使用 Managed 程式碼](-search-3x-wds-managed-code.md)
</dt> <dt>

[Windows Search 開發人員指南](-search-developers-guide-entry-page.md)
</dt> </dl>

 

 
