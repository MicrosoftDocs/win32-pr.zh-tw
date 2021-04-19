---
description: 安裝通訊協定處理常式牽涉到將 DLL (s) 複製到 Program Files 目錄中的適當位置，然後透過登錄註冊通訊協定處理常式。
ms.assetid: 07c40c0c-2729-462c-ba40-e05ffea2b889
title: " (Windows Search) 安裝和註冊通訊協定處理常式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb30032ef200832446a8a2f37b2ec427ab40b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970146"
---
# <a name="installing-and-registering-protocol-handlers-windows-search"></a> (Windows Search) 安裝和註冊通訊協定處理常式

安裝通訊協定處理常式牽涉到將 DLL (s) 複製到 Program Files 目錄中的適當位置，然後透過登錄註冊通訊協定處理常式。 安裝應用程式也可以新增搜尋根和範圍規則，以定義 Shell 資料來源的預設編目範圍。

本主題的組織方式如下：

-   [關於 Url](#about-urls)
-   [執行通訊協定處理常式介面](#implementing-protocol-handler-interfaces)
    -   [ISearchProtocol 和 ISearchProtocol2](#isearchprotocol-and-isearchprotocol2)
    -   [IUrlAccessor、IUrlAccessor2、IUrlAccessor3 和 IUrlAccessor4](#iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4)
    -   [IProtocolHandlerSite](#iprotocolhandlersite)
-   [執行容器的篩選處理常式](#implementing-filter-handlers-for-containers)
-   [安裝和註冊通訊協定處理常式](#installing-and-registering-a-protocol-handler)
    -   [註冊通訊協定處理常式的指導方針](#guidelines-for-registering-a-protocol-handler)
    -   [註冊通訊協定處理常式](#installing-and-registering-a-protocol-handler)
    -   [註冊通訊協定處理常式的檔案類型處理常式](#registering-the-protocol-handlers-file-type-handler)
-   [確保您的專案已編制索引](#ensuring-that-your-items-are-indexed)
-   [相關主題](#related-topics)

## <a name="about-urls"></a>關於 Url

Windows Search 會使用 Url 來唯一識別 Shell 資料來源階層中的專案。 階層中第一個節點的 URL 稱為 [搜尋根目錄](-search-3x-wds-extidx-csm-searchroots.md);Windows Search 將在搜尋根目錄開始編制索引，要求通訊協定處理常式列舉每個 URL 的子連結。

一般的 URL 結構如下：


```
<protocol>:// [{user SID}/] <localhost>/<path>/[<ItemID>]
```



下表說明 URL 語法。



| 語法           | 描述                                                                                                                                                                                                        |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <protocol> | 識別要為 URL 叫用的通訊協定處理常式。                                                                                                                                                           |
| {使用者 SID}       | 識別用來呼叫通訊協定處理常式的使用者安全性內容。 如果找不到 (SID) 的使用者安全識別碼，則會在系統服務的安全性內容中呼叫通訊協定處理常式。 |
| <path>     | 定義存放區的階層，其中每個正斜線 ( '/' ) 是資料夾名稱之間的分隔符號。                                                                                                            |
| <ItemID>   | 表示用來識別子專案 (的唯一字串，例如) 的檔案名。                                                                                                                            |



 

Windows Search 索引子會從 Url 修剪最後一個斜線。 因此，您無法依賴最後一個斜線來識別目錄，而不是專案。 您的通訊協定處理常式必須能夠處理此 URL 語法。 確定您選取用來識別 Shell 資料來源的通訊協定名稱不會與目前的資料來源發生衝突。 我們建議採用此命名慣例： `companyName.scheme` 。

如需建立 Shell 資料來源的詳細資訊，請參閱 [執行基本資料夾物件介面](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))。

## <a name="implementing-protocol-handler-interfaces"></a>執行通訊協定處理常式介面

建立通訊協定處理常式需要執行下列三個介面：

-   [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) 可管理 UrlAccessor 物件。
-   [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) 可公開屬性，並針對 Shell 資料來源中的專案識別適當的篩選。
-   用來篩選專屬檔案或列舉和篩選以階層方式儲存之檔案的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 。

除了所列的三個強制介面以外，其他介面是選擇性的，而您可以自由地執行任何選用介面最適合用於手邊的工作。

### <a name="isearchprotocol-and-isearchprotocol2"></a>ISearchProtocol 和 ISearchProtocol2

SearchProtocol 介面會初始化並管理您的通訊協定處理常式 UrlAccessor 物件。 [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2)介面是 [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)的選擇性延伸模組，並且包含額外的方法，可指定使用者和專案的詳細資訊。

### <a name="iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4"></a>IUrlAccessor、IUrlAccessor2、IUrlAccessor3 和 IUrlAccessor4

下表描述 [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) 介面。



| 介面                                                 | 描述                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)              | 針對指定的 URL， [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) 介面可讓您存取在 URL 中公開之專案的屬性。 它也可以將這些屬性系結至通訊協定處理常式特定的篩選 (也就是與檔案名相關聯的篩選器，) 。 |
| [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (選用)  | [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2)介面會使用方法來擴充 [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) ，以取得專案的屬性和其顯示 url 的字碼頁，並在 URL 中取得專案類型 (檔或目錄) 。                                    |
| [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (選用)  | [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3)介面會以取得使用者 sid 陣列的方法擴充 [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) ，讓搜尋通訊協定主機可以模擬這些使用者來為專案編制索引。                                                      |
| [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (選用)  | [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4)介面會使用可識別專案內容是否應該編制索引的方法，擴充 [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3)介面的功能。                                                                 |



 

UrlAccessor 物件是由 SearchProtocol 物件具現化並初始化。 [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)介面透過下表所述的方法，提供重要資訊片段的存取權。



| 方法                                                                                        | 描述                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUrlAccessor::GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)                 | 傳回上次修改 URL 的時間。 如果這次比上次索引子處理這個 URL 的時間還新，就會呼叫 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面 (的篩選處理常式，) 呼叫以解壓縮 (可能) 變更該專案的資料。 系統會忽略目錄的修改時間。 |
| [**IUrlAccessor::IsDirectory**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-isdirectory)                         | 識別 URL 是否代表包含子 Url 的資料夾。                                                                                                                                                                                                                                                            |
| [**IUrlAccessor::BindToStream**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtostream)                       | 系結至 [IStream 介面](/windows/win32/api/objidl/nn-objidl-istream) ，表示自訂資料存放區中的檔案資料。                                                                                                                                                                           |
| [**IUrlAccessor::BindToFilter**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtofilter)                       | 系結至通訊協定處理常式特定的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)，可公開專案的屬性。                                                                                                                                                                                                                 |
| [**IUrlAccessor4::ShouldIndexItemContent**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent) | 識別是否應為專案的內容編制索引。                                                                                                                                                                                                                                                                      |



 

### <a name="iprotocolhandlersite"></a>IProtocolHandlerSite

[**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite)介面是用來具現化篩選器處理常式，此處理程式是在隔離的進程中裝載。 針對指定的持續性類別識別碼取得適當的篩選處理常式 (CLSID) 、檔儲存類別或副檔名。 要求主機進程系結至 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 的好處是，主機進程可以管理尋找適當篩選處理常式的程式，以及控制呼叫處理常式的相關安全性。

## <a name="implementing-filter-handlers-for-containers"></a>執行容器的篩選處理常式

如果您要執行階層式通訊協定處理常式，則必須針對列舉子 Url 的容器執行篩選處理常式。 篩選處理常式是 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的實作為。 透過 **ifilter 介面的** [**Ifilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk)和 [**ifilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue)方法，列舉程式是一種迴圈;每個子 URL 都會公開為屬性的值。

[**IFilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) 會傳回容器的屬性。 為了列舉子 Url， **IFilter：： GetChunk** 會傳回下列其中一項：

-   [PKEY \_搜尋 \_ UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))：

    專案的 URL，不含上次修改時間。 [**IFilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 傳回包含子 URL 的 PROPVARIANT。

-   [PKEY \_搜尋 \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md)：

    URL 和上次修改時間。 [**IFilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 傳回 PROPVARIANT，其中包含子 URL 的向量和上次修改時間。

傳回 [PKEY \_ 搜尋 \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) 會更有效率，因為索引子可以立即判斷是否需要為專案編制索引，而不需要呼叫 [**ISearchProtocol：： CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) 和 [**IUrlAccessor：： GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) 方法。

下列範例程式碼示範如何傳回 [PKEY \_ 搜尋 \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) 屬性。

> [!IMPORTANT]
>
> Copyright (c) Microsoft Corporation。 著作權所有，並保留一切權利。

 


```
// Parameters are assumed to be valid

HRESULT GetPropVariantForUrlAndTime
    (PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // Allocate the propvariant pointer.
    size_t const cbAlloc = sizeof(**ppPropValue);
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(cbAlloc));

    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // Zero init the value

        // Now allocate enough memory for 2 nested PropVariants.
        // PKEY_Search_UrlToIndexWithModificationTime is an array of two PROPVARIANTs.
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // Set the container PROPVARIANT to be a vector of two PROPVARIANTS.
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // Now fill the array of PROPVARIANTS.
                // Put the pointer to the URL into the vector.
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // Put the FILETIME into vector.
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]  
> 容器 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 元件應該一律列舉所有的子 url，即使子 url 未變更，因為索引子會透過列舉進程偵測刪除。 如果 [PKEY \_ 搜尋 \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) 中的日期輸出指出資料尚未變更，則索引子不會更新該 URL 的資料。

 

## <a name="installing-and-registering-a-protocol-handler"></a>安裝和註冊通訊協定處理常式

安裝通訊協定處理常式牽涉到將 DLL (s) 複製到 [Program Files] 目錄中的適當位置，然後 (s) 註冊 DLL。 通訊協定處理常式應該執行自我註冊以進行安裝。 安裝應用程式也可以新增搜尋根目錄和範圍規則，以定義 Shell 資料來源的預設編目範圍，以 [確保您的專案會](#ensuring-that-your-items-are-indexed) 在本主題結尾進行索引。

### <a name="guidelines-for-registering-a-protocol-handler"></a>註冊通訊協定處理常式的指導方針

註冊通訊協定處理常式時，您應該遵循下列指導方針：

-   安裝程式必須使用 EXE 或 MSI 安裝程式。
-   必須提供版本資訊。
-   每個安裝的增益集都必須建立 [新增/移除程式] 專案。
-   安裝程式必須接管目前增益集所瞭解的特定檔案類型或存放區的所有登錄設定。
-   如果先前的增益集遭到覆寫，安裝程式應通知使用者。
-   如果較新的增益集覆寫了先前的增益集，就應該能夠還原先前增益集的功能，並使它成為該檔案類型的預設增益集。
-   安裝程式應定義索引子的預設編目範圍，方法是新增搜尋根目錄和使用編目範圍管理員 (CSM) 的範圍規則。

### <a name="registering-a-protocol-handler"></a>註冊通訊協定處理常式

您必須在登錄中建立14個專案，以註冊通訊協定處理常式元件，其中：

-   *Ver \_Ind \_ ProgID* 是通訊協定處理常式執行的獨立 ProgID 版本。
-   *Ver \_Dep \_ ProgID* 是通訊協定處理常式執行的版本相依 ProgID。
-   *Clsid \_ 1* 是通訊協定處理常式執行的 clsid。

**註冊通訊協定處理常式：**

1.  使用下列索引鍵和值註冊版本獨立 ProgID：

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CurVer
             (Default) = <Ver_Dep_ProgID>
    ```

2.  使用下列索引鍵和值註冊版本相依 ProgID：

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

3.  使用下列索引鍵和值註冊通訊協定處理常式的 CLSID：

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          {InprocServer32}
             (Default) = <DLL Install Path>
             Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ProgID>
             (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ShellFolder>
             Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          TypeLib
             (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          VersionIndependentProgID
             (Default) = <Ver_Ind_ProgID>
    ```

4.  向 Windows Search 登錄通訊協定處理常式。 在下列範例中， <Protocol Name> 是通訊協定本身的名稱，例如 file、mapi 等等：

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    在 Windows Vista 之前：

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Desktop Search
                DS
                   Index
                      ProtocolHandlers
                         <Protocol Name>
                            HasRequirements = dword:00000000
                            HasStartPage = dword:00000000
    ```

### <a name="registering-the-protocol-handlers-file-type-handler"></a>註冊通訊協定處理常式的檔案類型處理常式

您必須在登錄中建立兩個專案，以登錄通訊協定處理常式的檔案類型處理常式 (這也稱為 Shell 延伸模組) 。

1.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Desktop
                         NameSpace
                            {CLSID of PH Implementation}
                               (Default) = <Shell Implementation Description>
    ```

2.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Shell Extensions
                         Approved
                            {CLSID of PH Implementation} = <Shell Implementation Description>
    ```

## <a name="ensuring-that-your-items-are-indexed"></a>確保您的專案已編制索引

在您執行通訊協定處理常式之後，您必須指定通訊協定處理常式要編制索引的 Shell 專案。 您可以使用目錄管理員起始重新編制索引 (如需詳細資訊，請參閱 [使用目錄管理員](-search-3x-wds-mngidx-catalog-manager.md)) 。 或者，您也可以使用編目範圍管理員 (CSM) 來設定預設規則，指出您希望索引子進行編目的 Url (如需詳細資訊，請參閱 [使用編目範圍管理員](-search-3x-wds-extidx-csm.md) 和 [管理範圍規則](-search-3x-wds-extidx-csm-scoperules.md)) 。 您也可以新增搜尋根目錄 (如需詳細資訊，請參閱 [管理搜尋根](-search-3x-wds-extidx-csm-searchroots.md)) 。 另一個可用的選項是依照 [WINDOWS SEARCH SDK 範例](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)中的索引編制範例中的程式操作。

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)介面提供的方法會通知容器的搜尋引擎進行編目及/或監看，以及在編目或監看時要包含或排除的容器底下的專案。 在 Windows 7 和更新版本中， [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)會以取得版本的 [**ISearchCrawlScopeManager2：： GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion)方法擴充 **ISearchCrawlScopeManager** ，此方法會通知用戶端 CSM 的狀態是否已變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[瞭解通訊協定處理常式](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[開發通訊協定處理常式](-search-3x-wds-phaddins.md)
</dt> <dt>

[通知索引變更](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[新增圖示和快顯功能表](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[程式碼範例：通訊協定處理常式的 Shell 擴充功能](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[建立通訊協定處理常式的搜尋連接器](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[偵錯工具通訊協定處理常式](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
