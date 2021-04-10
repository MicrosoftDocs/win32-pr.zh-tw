---
title: 執行 WDS 的通訊協定處理常式
description: 建立通訊協定處理常式包括執行 ISearchProtocol 來管理 UrlAccessor 物件、IUrlAccessor 來產生的中繼資料，以及識別資料存放區中專案的適當篩選、IProtocolHandlerSite 來具現化 SearchProtocol 物件，並識別適當的篩選，以及 IFilterto 篩選專屬檔案，或列舉和篩選階層式儲存的檔案。
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a88ca5137b012431fff75bf5975a8b4820121
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092680"
---
# <a name="implementing-a-protocol-handler-for-wds"></a>執行 WDS 的通訊協定處理常式

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。

建立通訊協定處理常式包括執行 [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) 來管理 UrlAccessor 物件、 [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) 來產生的中繼資料，以及識別資料存放區中專案的適當篩選、IProtocolHandlerSite 來具現化 SearchProtocol 物件，以及識別適當的篩選準則，以及使用 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)來篩選專屬檔案，或列舉和篩選階層式儲存的檔案。 通訊協定處理常式必須為多執行緒。

本章節包含下列主題：

-   [Url 上的注意事項](#note-on-urls)
-   [通訊協定處理常式介面](#protocol-handler-interfaces)
-   [適用于容器的 Ifilter](#ifilters-for-containers)
-   [新增通訊協定處理常式選項功能](#adding-protocol-handler-options-functionality)
    -   [ISearchProtocolOptions](#isearchprotocoloptions)
-   [相關主題](#related-topics)

## <a name="note-on-urls"></a>Url 上的注意事項

Windows 桌面搜尋 (WDS) 使用 Url 來唯一識別檔案系統中的專案、類似資料庫的存放區，或在網路上。 定義專案節點的 URL 稱為起始頁;WDS 開始于該起始頁面，並遞迴地編目資料存放區。 一般的 URL 結構如下：

`protocol://host/path/name.extension`

> [!Note]
>
> 當您想要加入新的資料存放區時，必須選取名稱以識別與目前不衝突的名稱。 我們建議採用此命名慣例：公司名稱配置。

 

## <a name="protocol-handler-interfaces"></a>通訊協定處理常式介面

**ISearchProtocol**

[**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol)介面會叫用、初始化和管理 UrlAccessor 物件。 如需有關如何執行 ISearchProtocol 介面的詳細資訊，請參閱 **ISearchProtocol 介面參考**。

**IUrlAccessor**

針對指定的 URL， [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) 介面會產生位置結構和包含專案的相關中繼資料，並將這些專案系結至篩選。 **IUrlAccessor** 物件是由 SearchProtocol 物件具現化並初始化;不過，您也可以執行內部初始化方法，讓您的 **IUrlAccessor** 物件可以執行您的通訊協定處理常式專屬的初始化工作，例如驗證要存取之專案的 URL，或檢查上次修改的時間，以判斷是否必須在目前的編目中處理檔案。

> [!Note]
>
> 系統會忽略目錄的修改時間。 [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor)物件必須列舉子物件，以判斷是否有任何修改或刪除。

 

**UrlAccessor** 物件的大部分設計都取決於結構是階層式或以連結為基礎。 針對階層式資料存放區， **UrlAccessor** 物件必須找到可以列舉其內容的篩選準則。 階層式和連結式通訊協定處理常式之間的另一項差異，是使用 IsDirectory 方法。 在以連結為基礎的通訊協定處理常式中，此方法應該會傳回 \_ FALSE。 階層式通訊協定處理常式必須傳回 \_ 容器的 [確定]。

如需有關如何執行 [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) 介面的進一步指示，請參閱 [**IUrlAccessor 介面**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) 參考。

**IProtocolHandlerSite**

這個介面是用來具現化 **SearchProtocol** 物件，也會為 **UrlAccessor** 物件提供指定類別識別碼 (CLSID) 的適當篩選。

## <a name="ifilters-for-containers"></a>適用于容器的 Ifilter

如果您要執行階層式通訊協定處理常式，您必須執行容器 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)元件，以列舉代表容器或資料夾的 url。 列舉程式是透過 IFilter 介面的 **GetChunk** 和 **GetValue** 方法進行迴圈，此方法會傳回代表容器中每個專案的 url 清單。

首先， **GetChunk** 會傳回具有屬性 set 收集 PROPSET 的 FULLPROSPEC \_ ，以及下列其中一項：

-   PID \_ GTHR \_ DIRLINK、不含上次修改時間之專案的 URL，或
-   PID \_ GTHR \_ DIRLINK \_ WITH \_ TIME、URL 以及上次修改時間

收集 PROPSET 的屬性集 GUID \_ 是0B63E343-9CCC-11D0-BCDB-00805FCCCE04。 PROPSPEC 屬性可以是 PID \_ GTHR \_ DIRLINK = 2 或 pid \_ GTHR \_ DIRLINK \_ ， \_ 時間 = 12 decimal。

\_以時間傳回 PID GTHR \_ DIRLINK \_ \_ 會更有效率，因為索引子可以立即判斷是否需要為專案編制索引，而不需要呼叫 ISearchProtocol->CreateUrlAccessor () 和 IUrlAccessor >GetLastModified () 方法。

然後，如果使用) ，則 **GetValue** 會傳回 URL (和上次修改時間的 PROPVARIANT，如下所示：

-   VT \_ LPWSTR、子專案的 URL，或
-   URL 的向量，後面接著 FILETIME

下列範例程式碼示範如何使用時間來建立適當的 PID \_ GTHR \_ DIRLINK \_ \_ 。

> [!Note]
>
> **此程式碼和資訊是以「原樣」提供，不含任何明示或默示擔保，包括但不限於特定用途的適售性及/或適用性默示擔保。**
>
> 著作權 (C) Microsoft。 著作權所有，並保留一切權利。

 


```
// params are assumed to be valid

HRESULT GetPropVariantForUrlAndTime(PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // allocate the propvariant pointer
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*ppPropValue));
    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // zero init the value

        // now allocate enough memory for 2 nested PropVariants.
        // PID_GTHR_DIRLINK_WITH_TIME is an array of 2 PROPVARIANTs
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // set the container PROPVARIANT that it is a vector of 2 PROPVARIANTS
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // now fill the array of PROPVARIANTS
                // put the pointer to the URL into the vector
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // put the FILETIME into vector
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
>
> 容器 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)元件應該一律列舉所有的子 url，即使子 url 未變更，因為索引子會透過列舉進程偵測刪除。 如果 DIR 連結中的日期輸出 \_ \_ \_ 指出資料尚未變更，則索引子不會更新該 URL 的資料。

 

實體 URL 是 **UrlAccessor** 物件處理的 url。 如果篩選不會發出方便使用的 DisplayUrl，WDS 會在搜尋結果中顯示使用者的實體 URL。 WDS 架構包含兩個屬性，可控制要對終端使用者顯示的內容，如下表所示。



| GUID                                 | PROPSPEC      | Description                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | DisplayFolder | 在搜尋結果中顯示給使用者的資料夾路徑 |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | FolderName    | 父資料夾的顯示名稱                   |



 

如果您的程式碼未發出 DisplayFolder 或資料夾資料夾，則會從 DisplayUrl 計算這些值。 URL 中的正斜線代表存放區或檔案系統內的容器。

## <a name="adding-protocol-handler-options-functionality"></a>新增通訊協定處理常式選項功能

若要讓您的通訊協定處理常式具有預設起始頁 (和專案節點 URL) ，您必須執行 **ISearchProtocolOptions** 介面。 在未來的 WDS 版本中，這個介面會提供 [選項] 對話方塊的勾點，以提供增強的使用者體驗。 此介面提供下列功能：

-   判斷是否符合通訊協定處理常式的需求。 例如，您的通訊協定處理常式存放區可能需要存取指定的應用程式，才能正確地為應用程式的資料編制索引，但應用程式無法使用。
-   識別您的通訊協定處理常式處理專案所需的最低需求。 您可以使用易記的當地語系化描述來表示需求，例如「Microsoft Outlook 2000 或更高版本」。
-   定義通訊協定處理常式預設應處理的 Url。

### <a name="isearchprotocoloptions"></a>ISearchProtocolOptions

下表說明您需要針對 **ISearchProtocolOptions** 介面執行的方法。



| 方法               | 描述                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| CheckRequirements    | 判斷是否符合自訂通訊協定處理常式的最低需求                             |
| GetDefaultCrawlScope | 針對自訂通訊協定處理常式，傳回指定存放區內的預設 Url 清單                   |
| GetRequirements      | 識別自訂通訊協定處理常式之最低需求的使用者易記當地語系化描述 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[通知索引變更](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[使用 Shell 擴充功能新增圖示、預覽和內容功能表](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[安裝和註冊通訊協定處理常式](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 