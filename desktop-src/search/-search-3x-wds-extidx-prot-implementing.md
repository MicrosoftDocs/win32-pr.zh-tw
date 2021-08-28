---
description: 某些應用程式會將它們的專案儲存在資料庫或自訂檔案類型中。
ms.assetid: 0e2b7b4b-ae87-4092-b924-6191cdf42c9b
title: 瞭解通訊協定處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f466d2d329fda81eee4533dc4444250abc42e0a4e8187d603a290acb277e3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119352248"
---
# <a name="understanding-protocol-handlers"></a>瞭解通訊協定處理常式

某些應用程式會將它們的專案儲存在資料庫或自訂檔案類型中。 雖然 Windows Search 可以為檔案的名稱和屬性編制索引，但 Windows 不知道該檔案的內容。 因此，這類專案無法在 Windows Shell 中進行索引或公開。 藉由建立通訊協定處理常式，您可以讓這些專案可供編制索引。 您也可以為複合檔案格式（例如 .zip 檔案）編制索引。

本主題的組織方式如下：

-   [使用通訊協定處理常式編制資料存放區索引](#indexing-data-stores-with-protocol-handlers)
    -   [Shell 資料存放區](#shell-data-stores)
    -   [通訊協定處理常式](#protocol-handlers)
    -   [篩選和通訊協定處理常式](#filters-and-protocol-handlers)
-   [為複合檔案格式編制索引](#indexing-a-compound-file-format)
-   [相關主題](#related-topics)

## <a name="indexing-data-stores-with-protocol-handlers"></a>使用通訊協定處理常式編制資料存放區索引

當使用者需要搜尋舊版資料庫、電子郵件存放區或 Windows Search 不支援的其他資料結構時，您應該先判斷該資料存放區的通訊協定處理常式是否已存在，是否可能與其他應用程式（例如 SharePoint Server）搭配使用。 若是如此，您可以在系統上安裝該通訊協定處理常式。 Windows搜尋通訊協定處理常式會使用類似 SharePoint Server 的設計規格，而且通常可以交換使用。

如需有關使用 Office SharePoint server 2007 部署搜尋伺服器2008的詳細資訊，請參閱同盟[搜尋 \[ 搜尋伺服器 2008 \] ](/previous-versions/office/bb931109(v=office.14))。

### <a name="shell-data-stores"></a>Shell 資料存放區

在新檔案格式和資料存放區的協力廠商開發人員之前，您可以讓這些格式和存放區出現在 Windows 檔案總管的查詢結果中，開發人員必須執行 Shell 資料來源。 Shell 資料來源是一種元件，用來擴充 Shell 命名空間，並公開資料存放區中的專案。 資料存放區是資料的儲存機制。 資料存放區可公開給 Shell 程式設計模型，作為使用 Shell 資料來源的容器。 您可以使用通訊協定處理常式，利用 Windows Search 系統為數據存放區中的專案編制索引。 通訊協定處理常式會執行以原生格式存取內容來源的通訊協定。 [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)和 [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2)介面是用來執行自訂的通訊協定處理常式，以展開可編制索引的資料來源。

如果您希望查詢結果出現在 Windows 檔案總管中，您必須先執行 Shell 資料來源，才能建立通訊協定處理常式來擴充索引。 但是，如果所有查詢都是以程式設計方式 (透過 OLE DB 例如) ，並以應用程式的程式碼（而非 Shell）來解讀，則不一定需要使用 Shell 命名空間。

> [!Note]  
> Shell 資料來源有時也稱為 Shell 命名空間延伸模組。 處理常式有時也稱為 Shell 擴充或 Shell 擴充處理常式。

 

如果您想要讓使用者從 Windows 檔案總管中查看其搜尋結果，您必須建立通訊協定處理常式，以及下列一或多個增益集：

-   快速鍵功能表處理常式
-   圖示處理常式
-   其他類型的檔處理常式

如需您嘗試達成之開發人員案例所識別的處理常式清單，請參閱 Windows Search 中的「處理常式總覽」[作為開發平臺](-search-3x-wds-development-ovr.md)。 如需建立處理常式的相關資訊，請參閱 [註冊 Shell 擴充](../shell/reg-shell-exts.md)功能、操作 [功能表](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))和 [檔案類型處理常式](../shell/fa-file-extensions.md)。

### <a name="protocol-handlers"></a>通訊協定處理常式

如果資料存放區也是容器 (例如檔系統資料夾) ，您必須執行篩選以列舉容器中的 Url。 如果資料存放區包含 Windows Search 所支援的其中一種200檔案類型以外的資料或檔案類型，您必須執行篩選來存取和編制存放區中專案內容的索引。 Windows搜尋使用通訊協定處理常式和 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)技術，類似于 SharePoint Server 所使用的技術。 如果您已經在要編制索引的系統上安裝特定存放區和檔案類型的篩選器，Windows Search 可能可以使用現有的介面來為此資料編制索引。

如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。 如需篩選處理常式的概念資訊，請參閱 [開發篩選處理常式](-search-ifilter-conceptual.md)。

### <a name="filters-and-protocol-handlers"></a>篩選和通訊協定處理常式

通訊協定處理常式會提供資料存放區的 Windows Search 索引子存取權，讓索引子可以編目資料存放區的節點，並將相關資訊解壓縮至索引。 Windows例如，搜尋會隨附適用于檔案系統存放區的通訊協定處理常式，以及 Microsoft Outlook 資料存放區的某些版本的通訊協定處理常式。 Outlook 電子郵件編制索引時，通訊協定處理常式會編目一組 Outlook 資料夾中的所有訊息，並從每個訊息和附件中解壓縮資訊。 這項資訊會傳遞給索引子，以便包含在 Windows Search 目錄中。

如需目錄管理員和編目範圍管理員 (CSM) 的總覽，請參閱 [使用目錄管理員](-search-3x-wds-mngidx-catalog-manager.md) 並 [使用編目範圍管理員](-search-3x-wds-extidx-csm.md)。

## <a name="indexing-a-compound-file-format"></a>為複合檔案格式編制索引

您可以編制複合檔案格式的索引，以便將檔案中的個別專案當作個別結果來傳回。 複合檔案格式（例如，副檔名為 .zip 的壓縮檔）本質上是資料存放區，因此可視為索引用途。 下列範例會在檔案系統命名空間中顯示 .zip 檔案 (FILE://c:/test/test.zip) 其中同時有子資料夾和個別專案。

``` syntax
Test.zip 

    |-folder1 

    |    |-folder2 

    |           |- FileX.txt 

    |- FileY.doc
```

檔案通訊協定處理常式會在透過監視檔案系統變更記錄檔 FILE://c:/test/test.zip 變更時進行探索，並在檔案變更時叫用針對該檔案 .zip 檔案註冊的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ，但它並不知道 .zip 檔案本身的內部結構。

您必須通知索引子，複合檔案格式是資料存放區。 您必須針對個別專案編制索引，並將其視為唯一的實體來加以取出。 在您執行 Shell 資料來源並執行下列步驟之後，您將會有一個通訊協定處理常式，該處理常式可處理複合檔案格式的資料，並將其公開 (.zip 檔案) 為個別專案。

**若要通知索引子有複合檔案是資料存放區：**

1.  針對有能力系結至來源檔案的 .zip 檔案，使用 [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) 或 [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2)) 來建立通訊協定處理常式 (。 如需詳細資訊，請參閱 [安裝和註冊通訊協定處理常式](-search-3x-wds-ph-install-registration.md)。

    例如，您可以使用 .zip 檔案的轉義路徑作為根資料夾名稱，然後使用類似任何其他檔案格式的階層語法。

    ``` syntax
    .zip:///escapedPathTo.zipFile/.zipfolder/.../.zipfile
    ```

    使用上述適用于 c： testtest.zip 的範例資料 \\ \\ ，唯一的 url 如下所示。 使用這些 Url 時，通訊協定處理常式具有系結至 .zip 檔案所需的資訊，以及列舉包含內部檔案的子 Url，讓 .doc 和 .txt 篩選器可以系結和編制索引。

    ``` syntax
      

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/ 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/FileY.Doc 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2/FileX.txt
    ```

2.  確定您的通訊協定處理常式符合下列兩個條件：
    -   .zip 檔案的根 Url 應該會 \_ \_ 在根 .zip 檔案 Url 的 url 上發出 PKEY 搜尋 IsClosedDirectory ([IsClosedDirectory](../properties/props-system-search-iscloseddirectory.md)) 。 例如，.zip：///FILE：% 2f% 2f% 2fc：% 2ftest% 2ftest.zip/應該發出 IsClosedDirectory = **TRUE**。 這會告知索引子，如果此 URL 上的日期未變更，則不需要處理任何子系 Url。
    -   該 URL 的每個子 URL 都應該 \_ \_ 在根 .zip URL 的子 url 上發出 PKEY 搜尋 IsFullyContained ([IsFullyContained](../properties/props-system-search-isfullycontained.md)) 。 一般來說，在累加式編目結束時，索引子會將所有未抓取的 Url 視為應刪除的專案。 但因為沒有任何變更，所以根 .zip 檔案不應該處理根 Url。 發出這個屬性為 **TRUE** 時，會告知索引子，如果這個 URL 尚未在遞增編目結束時處理，則不應將其刪除。 只有在根項目已變更且未造訪時，才會刪除此專案。

Windows搜尋必須要有通訊協定的起始頁，才能知道要以累加方式編目的 Url，以及找到的 Url 應該被忽略。 但我們無法從每個 .zip 檔案的 URL 開始，因為我們不知道每個 .zip 檔案的所在位置。 因此，.zip 通訊協定處理常式的起始頁 URL 必須能夠列舉所有 .zip 檔案的已轉義路徑根目錄中的所有專案。 這些 .zip 的檔案不一定是在 FILE：命名空間中，而且可能是以附件的形式指向 .zip 檔案的 MAPI 類型 URL，例如。

**若要將根註冊為起始頁：**

1.  將根項目（例如 .zip：///）註冊為起始頁，如此一來，所有 .zip 檔案就會在那裡開始。 在處理根 .zip： URL 時，您的通訊協定處理常式應該透過查詢所有 url 的 Windows Search，以產生要發出的子 url 清單（FileExtension = ".zip"）。
2.  請將這些 Url 取消，以移除斜線並將其傳回做為子 Url。 取得您想要之類型的範例查詢可能看起來如下。

    ``` syntax
    SELECT system.itemurl, System.DateModified FROM SystemIndex 
    WHERE System.FileExtension='.zip' OR System.MimeType='mimetypefor.zip'
    ```

3.  當 Windows Search 定期對您 .zip：//////////////////////////////根 URL .zip 進行累加編目時，您 Windows Search 必須 如果在儲存 .zip 檔案的原生存放區中發現刪除，則不會出現在您的列舉中，而且會移除 .zip 中之樹狀結構的分支。
4.  若要系結至另一個通訊協定處理常式的 .zip 資料，您應該在理想的情況下，流覽該 URL 的 [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) ，以系結至物件的儲存區，而不是假設它一律為檔案。 這樣做可讓您彈性地使用郵件存放區中的附件。
5.  發出每個 .zip 檔案的子 Url 時，您應該使用 PKEY \_ 搜尋 \_ UrlToIndexWithModificationTime ([UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md)) 以傳遞 PKEY \_ DateModified (的實際[](../properties/props-system-datemodified.md)) 檔，讓索引子只會在已變更時才編目 .zip 檔。

若要在建立或修改 .zip Url 之後立即進行編制索引，而不需要等候增量編目來探索其新狀態，您可以自行監視檔案系統，以進行 .zip 檔案變更。 不過，這種方法對其他資料存放區（例如 MAPI）沒有作用。

**若要在建立或修改 .zip url 時進行編制索引：**

1.  針對 .zip 檔案類型建立 (和執行 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面) 的篩選。 如需詳細資訊，請參閱[開發 Windows Search 的屬性處理常式](-search-3x-wds-extidx-propertyhandlers.md)。
2.  每次呼叫您的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 實作為時，都是因為已探索或變更該 URL。 然後，透過 [**IGatherNotifyInline**](/previous-versions/windows/desktop/legacy/bb231470(v=vs.85)) 介面產生適用于來源 url 的 .zip URL 事件。 這樣做可讓您立即告知索引子有新的資料要編制索引，而不需要等候增量編目。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[開發通訊協定處理常式](-search-3x-wds-phaddins.md)
</dt> <dt>

[安裝和註冊通訊協定處理常式](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[通知索引變更](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[新增圖示和快顯功能表](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[程式碼範例：通訊協定處理常式的 Shell 擴充功能](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[安裝和註冊通訊協定處理常式](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[建立通訊協定處理常式的搜尋連接器](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[偵錯工具通訊協定處理常式](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
