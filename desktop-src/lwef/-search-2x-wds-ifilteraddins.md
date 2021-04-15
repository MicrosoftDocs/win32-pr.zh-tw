---
title: 開發 IFilter 增益集
description: 您可以使用篩選增益集（可執行 IFilterinterface 的元件）擴充 Microsoft Windows 桌面搜尋 (WDS) ，以包含新的檔案類型。
ms.assetid: 71dd515d-a73e-4e0a-b0da-c8a6209d09fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f846cf2101eefc17b1e92fbd7992529a06fb43
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463100"
---
# <a name="developing-ifilter-add-ins"></a>開發 IFilter 增益集

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。

您可以使用篩選增益集（可執行 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)介面的元件）擴充 Microsoft Windows 桌面搜尋 (WDS) ，以包含新的檔案類型。 篩選準則負責存取和剖析檔案中的資料，以及傳回屬性和值的配對，以及用來編制索引的文字區塊。 在編制索引過程中，WDS 會使用每個檔案或專案的 URL 來呼叫適當的篩選。 篩選準則會先解壓縮對應至 WDS 架構中標示為可抓取之屬性的中繼資料，例如標題、檔案大小和上次修改日期。 然後，它會將專案內容分割成文字區塊。 WDS 會將篩選所傳回的屬性和文字新增至目錄。 WDS 可以為具有已註冊篩選的任何檔案類型編制索引。

在某些情況下，您不需要撰寫新的篩選準則。 WDS 2.x 包含超過200種專案類型的篩選 (包括 HTML、XML 和原始程式碼檔案等純文字專案) ，並使用與 SharePoint 服務相同的 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)技術。 如果您已針對檔案類型安裝篩選器，WDS 可以使用這些現有的篩選來編制此資料的索引。 此外，WDS 也包含純文字格式之檔案類型的一般篩選。 如果您的檔案類型可以由現有的 SharePoint Services 篩選或純文字篩選器處理，您可以將副檔名和篩選 GUID 新增至登錄，讓 WDS 可以找到並使用它 (如需詳細資訊，請參閱 [註冊篩選增益集](#to-register-a-filter-add-in)) 。

但是，如果您有非純文字和專屬的資料或檔案格式，則撰寫自訂篩選器會是確保 WDS 可以在目錄中編制檔案格式的唯一方法。 檔案類型只能有一個篩選增益集，因此可以覆寫現有的篩選，或針對特定檔案類型覆寫其他篩選器。

本節包含下列主題：

-   [必要的篩選介面](#required-filter-interfaces)
    -   [IFilter 介面](#ifilter-interface)
    -   [IPersistStream](#ipersiststream)
    -   [IPersistFile](#ipersistfile)
    -   [IPersistStorage](#ipersiststorage)
-   [使用篩選器輸出屬性](#outputting-properties-with-filters)
    -   [屬性值](#property-values)
-   [篩選增益集安裝](#filter-add-in-installation)
    -   [註冊所需的 Clsid](#clsids-required-for-registration)
    -   [註冊模型](#registration-model)
    -   [註冊篩選增益集](#to-register-a-filter-add-in)
-   [相關主題](#related-topics)

## <a name="required-filter-interfaces"></a>必要的篩選介面

篩選增益集必須執行 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)介面和下列其中一個介面：

-   [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) -從資料流程載入資料。 這比使用檔案更安全，因為沒有寫入磁片。 IPersistStream 介面是向前相容于 Windows Vista 的慣用方法。
-   [IPersistFile 介面](/windows/win32/api/objidl/nn-objidl-ipersistfile) -從檔案載入資料。 Windows Vista 不支援此介面。
-   [IPersistStorage 介面](/windows/win32/api/objidl/nn-objidl-ipersiststorage) -從 OLE COM 結構化儲存體載入資料。

篩選增益集會使用這些介面來取得專案的內容，並以反復方式將它們傳回至索引，直到到達檔案結尾為止。 篩選增益集應該盡可能健全，以處理損毀的檔案，以及不符合預期輸入格式的檔案。

### <a name="ifilter-interface"></a>IFilter 介面

這是篩選器執行所需的介面。 如需詳細資訊，請參閱 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)介面參考。



| 方法       | 描述                                                                            |
|--------------|----------------------------------------------------------------------------------------|
| Init ()        | 初始化篩選會話。                                                       |
| GetChunk ()    | 將篩選置於第一個或下一個區塊的開頭，並傳回描述項。 |
| GetText ()     | 抓取目前區塊中的文字。                                                 |
| GetValue()   | 從目前的區塊抓取屬性值。                                      |
| BindRegion ()  | 目前保留供內部使用;請勿實行。 這個方法會傳回 E \_ >notimpl。 |



 

### <a name="ipersiststream"></a>IPersistStream

這個介面會從資料流程載入檔案，以比 [IPersistFile 介面](/windows/win32/api/objidl/nn-objidl-ipersistfile) 更安全處理，因為執行 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) 篩選器的內容不需要在磁片上或透過網路開啟任何檔案的許可權。 在存取單一檔案的兩個方法中，這是與 Windows 向前相容的慣用方法。



| 方法       | 描述                                                                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| IsDirty ()     | 檢查是否有變更。 這個方法會傳回 \_ 篩選中的 E >notimpl。                                                                      |
| InitNew ()     | 建立新的存放裝置。 這個方法會傳回 \_ 篩選中的 E >notimpl。                                                                                  |
| 載入 ()        | 從先前儲存物件的資料流來初始化它。                                                                               |
| 儲存 ()        | 將物件儲存至指定的資料流程，並指出物件是否應該重設其中途旗標。 這個方法會傳回 \_ 篩選中的 E >notimpl。 |
| GetSizeMax ()  | 傳回儲存物件所需資料流的大小 (以位元組為單位)。 這個方法會傳回 \_ 篩選中的 E >notimpl。                                      |



 

### <a name="ipersistfile"></a>IPersistFile

此介面會依絕對路徑載入檔案，而且在 Windows Vista 中不支援。



| 方法          | 描述                                                                                                                  |
|-----------------|------------------------------------------------------------------------------------------------------------------------------|
| GetCurFile ()     | 取得與物件相關聯之檔案的目前名稱。 傳回 Load () 中指定的路徑。                          |
| 載入 ()           | 開啟指定的檔案，並從檔案連接初始化物件。 您可以延遲開啟檔案，直到需要為止。 |
| GetClassID ()     | 針對新的檔案類型，傳回 (CLSID) 的類別識別碼。 您應該使用 uuidgen.exe 來產生唯一的 CLSID。           |
| IsDirty ()        | 只需要 \_ 在篩選器中傳回 E >notimpl                                                                                       |
| 儲存 ()           | 只需要 \_ 在篩選器中傳回 E >notimpl                                                                                       |
| SaveCompleted ()  | 只需要 \_ 在篩選器中傳回 E >notimpl                                                                                       |



 

### <a name="ipersiststorage"></a>IPersistStorage

此介面支援結構化儲存體模型，其中每個包含的物件都有它自己的儲存區，它會嵌套在容器的儲存體中。 如同 [IPersistFile 介面](/windows/win32/api/objidl/nn-objidl-ipersistfile)，這個介面會依絕對路徑載入，而且在 Windows Vista 中不受支援。



| 方法            | 描述                                                                                                   |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| IsDirty ()          | 檢查是否有變更。 這個方法會傳回 \_ 篩選中的 E >notimpl。                                 |
| InitNew ()          | 建立新的存放裝置。 這個方法會傳回 \_ 篩選中的 E >notimpl。                                             |
| 載入 ()             | 儲存儲存體。 這個方法會傳回 \_ 篩選中的 E >notimpl。                                                 |
| 儲存 ()             | 傳回儲存物件所需資料流的大小 (以位元組為單位)。 這個方法會傳回 \_ 篩選中的 E >notimpl。 |
| SaveCompleted ()    | 保留供內部使用。 這個方法會傳回 \_ 篩選中的 E >notimpl。                                         |
| HandsOffStorage ()  | 保留供內部使用。 這個方法會傳回 \_ 篩選中的 E >notimpl。                                         |



 

## <a name="outputting-properties-with-filters"></a>使用篩選器輸出屬性

篩選準則的目的是要將檔案的內容和屬性解壓縮，以包含在全文檢索索引中。 WDS 會先呼叫 IPersistFile、IPersistStream 或 IPersistStorage 執行的 Load 方法，然後再叫用 IFilter 執行的 Init 方法。 **GetChunk** 被呼叫來取出文字或屬性值資料的區塊，然後視需要呼叫 **GetText** 或 **GetValue** ，以抓取與區塊相關聯的所有文字或屬性值。 此程式會重複，直到 **GetChunk** 回報檔中沒有其他區塊為止。

**GetChunk** 方法會從要篩選的檔案抓取第一個或下一個邏輯區塊資訊的相關資訊，並將該資訊傳回 \_ 至 STAT 區塊結構，包括單純遞增的區塊識別碼、目前區塊與先前區塊之間的關聯狀態資訊、旗標，指出區塊是否包含文字或值、區塊的地區設定，以及區塊的屬性規格。 屬性規格是由 CLSID 和整數或字串屬性 (識別碼所組成的 [**FULLPROPSPEC**](/windows/desktop/api/filter/ns-filter-fullpropspec) ，例如 D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType) 。 它會識別屬性的類型，而不是屬性值本身。

區塊地區設定識別碼是用來選擇適當的斷詞工具，您必須正確地加以識別。 如果篩選準則無法判斷文字的地區設定，則應該假設預設的系統地區設定，可使用 **GetSystemDefaultLCID** 取得。 如果您控制檔案格式，但目前不包含地區設定資訊，您應該新增使用者功能，以啟用適當的地區設定識別。 使用不相符的斷詞工具可能會導致使用者的查詢體驗不良。

**GetChunk** 只會管理存取區塊，且不會傳回文字或屬性值本身。 相反地，後續呼叫 **GetText** 和 **GetValue** 會取出區塊的主體。 **GetText** 會從目前的區塊文字區塊傳回文字區塊，也就是 Unicode 字串 \_ 。 如果目前的區塊太大，則可能需要一個以上的 **GetText** 方法呼叫。 每次呼叫 **GetText** 方法時，都會抓取緊接在最後一次呼叫 **GetText** 方法的文字後面的文字。 例如，一個呼叫中的最後一個字元可以位於單字的中間，而下一個呼叫中的第一個字元會繼續該字。 搜尋引擎必須處理這種情況。

**GetValue** \_ 會傳回 PROPVARIANT 結構中目前區塊值區塊的屬性值，其可保存各種不同的資料類型。 **GetValue** 必須使用 CoTaskMemAlloc 來配置 PROPVARIANT 結構本身。 **GetValue** 的呼叫端負責釋放 PROPVARIANT 使用 PropVariantClear 所指向的記憶體，以及使用 CoTaskMemFree 釋放結構本身。 如需 PROPVARIANTs 的詳細資訊，請參閱 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 參考。

### <a name="property-values"></a>屬性值

篩選器最少應輸出下列屬性，這些屬性是 WDS 結果檢視器中的預設資料行。



| GUID                                 | PROPSPEC      | 易記名稱  | Description                                                                                                                                     |
|--------------------------------------|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9 | 2             | PrimaryTitle   | 針對此專案顯示的標題。                                                                                                              |
| F29F85E0-4FF9-1068-AB91-08002B27B3D9 | 4             | PrimaryAuthors | 與此專案最相關聯的人員。                                                                                                          |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | PrimaryDate   | PrimaryDate    | 專案的最重要日期，例如收到的電子郵件或修改檔案的日期。                                                               |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | PerceivedType | PerceivedType  | 正在剖析的檔案類型。 必須符合 WDS [感知類型](-search-2x-wds-perceivedtype.md)中所列的其中一個 Windows 桌面搜尋類型。 |



 

若是純文字專案，WDS 會將所有文字和系統定義的屬性（例如檔案大小或副檔名）解壓縮到索引) 的新純文字檔案類型。 其他可傳回至索引的屬性類型包括：

-   針對檔案： author、title、status、關鍵字
-   針對媒體：專輯、內容類型、相機製作、拍攝日期
-   針對通訊：寄件者、收件者、副本、重要性
-   連絡人：職稱、公司電話、公司

上述清單會將所指定之感知類型通用的屬性分組;但是，不論類型為何，都可以使用任何屬性。 例如，公司可以用來做為連絡人的雇主名稱，也可以用來參考與該檔案相關之用戶端的名稱。 其中許多屬性都是用來在 WDS 結果查看中顯示搜尋結果。 例如，檔案的 Title 屬性會顯示為預設結果檢視中的主要資料行。 IFilter 物件應該會輸出與所剖析之專案類型相關的所有屬性。 無法在 WDS 2.x 中新增自訂屬性。 如需可用屬性的完整清單，請參閱 [WDS 架構](-search-2x-wds-schematable.md)。

## <a name="filter-add-in-installation"></a>篩選增益集安裝

安裝篩選牽涉到將 DLL 複製到 Program Files 目錄中的適當位置並加以註冊。 篩選器應執行自我註冊以進行安裝，且應遵循下列指導方針：

-   安裝程式必須使用 EXE 或 MSI 安裝程式。
-   必須提供版本資訊。
-   每個安裝的增益集都必須建立 [ **新增/移除程式** ] 專案。
-   安裝程式必須接管目前增益集所瞭解的特定檔案類型或存放區的所有登錄設定。
-   如果先前的增益集遭到覆寫，安裝程式應通知使用者。
-   如果較新的增益集已覆寫先前的增益集，應該可以還原先前增益集的功能，並將它設為該檔案類型的預設增益集，或重新儲存。

### <a name="clsids-required-for-registration"></a>註冊所需的 Clsid

每個篩選器都有三個相關聯的類別識別碼或 Clsid。 您必須產生一或多個這些 (使用 uuidgen.exe) 註冊篩選增益集。

-   第一個會識別所有篩選準則的持續性處理常式 IID \_ IFilter，也就是 {89BCB740-6119-101A-BCB7-00DD010655AF}。 此 CLSID 對於所有執行 IFilter 的篩選都是常數。
-   第二個 (IID \_ IFilter 金鑰的值) 識別檔案類型的 IFilter 執行。 此索引鍵包含 InprocServer32 值，指定依路徑和執行緒模型的 DLL 名稱。 如果篩選準則位於系統路徑中（例如 system32 目錄），則檔案名即已足夠。 否則，此值應該有完整路徑規格。
-   第三個會識別篩選所處理的檔案類型，並由您的 IPersist 介面上的 GetClassID 方法傳回。

> [!Note]
>
> 在未來的 Microsoft 作業系統版本中，在 system32 目錄中安裝檔案可能會變得更困難，因此建議您將它們安裝在 [Program Files] 底下，並在登錄中包含篩選的完整路徑。 基於安全性理由，在登錄中指定 DLL 的完整路徑也是很謹慎的。 否則，如果您的版本是在版本之前的進程路徑中，則可以載入 DLL 的「特洛伊木馬程式」版本。

 

### <a name="registration-model"></a>註冊模型

當 WDS 可以篩選檔案時，它會在登錄的副檔名下尋找，以決定要載入的篩選。 接著，它會遵循一系列的登錄連結，以下列順序找出篩選 DLL 的名稱：

1.  從位於下列位置的 Clsid：

    **HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ 篩選器覆 \\ 寫 \\ RSApp**

    **HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ 篩選器**

2.  從檔案內容類型：

    **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ MIME \\ 資料庫 \\ 內容類型**

3.  從副檔名 (與 Win32 LoadIFilter API) 相同：

    **HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ 篩選器覆 \\ 寫 \\ RSApp**

    **HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ 篩選器**

    **HKEY \_ 類別 \_ 根 \\ EXTPERSISTENTHANDLER->CLSID->IID \_ IFilter->clsid**

4.  預設位置：

    **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ 篩選器**

### <a name="to-register-a-filter-add-in"></a>註冊篩選增益集

您必須在登錄中總共建立八個專案，以註冊您的篩選增益集，其中：

-   **ext** 是新的檔案名副檔名
-   **Guid \_ 1** 可以是針對此延伸模組產生的任何新 guid
-   **89BCB740-6119-101A-BCB7-00DD010655AF** 是 IFILTER 介面 GUID，也就是所有 IFilter 執行的常數。

1.  使用下列索引鍵和值註冊副檔名的持續性處理常式：

    ```
    HKEY_CLASSES_ROOT\<.ext>\PersistentHandler
       (Default) = {GUID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}
       (Default) = <Persistent Handler Description>
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentAddinsRegistered
       (Default) = (Value Not Set)
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentAddinsRegistered\{89BCB740-6119-101A-BCB7-00DD010655AF}
       (Default) = {CLSID of IFilter implementation}
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentHandler
       (Default) = {GUID_1}
    ```

2.  使用下列索引鍵和值註冊 IFilter 執行：

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}
       (Default) = Extension IFilter Description">
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}\InprocServer32
       (Default) = <DLL Install Path>
       ThreadingModel = Both
    ```

3.  使用下列機碼和值，向 Windows 桌面搜尋登錄 IFilter 執行：

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\RSSearch\ContentIndexCommon\Filters\Extension\<.ext>
       (Default) = {CLSID of IFilter implementation}"
    ```

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> <dt>

[認知類型](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[開發通訊協定處理常式](-search-2x-wds-phaddins.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 