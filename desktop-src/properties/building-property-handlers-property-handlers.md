---
description: 本主題說明如何建立及註冊屬性處理常式，以便與 Windows 屬性系統搭配使用。
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: 初始化屬性處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8eb11bc44217e508313bfb477c65925b44216e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193004"
---
# <a name="initializing-property-handlers"></a>初始化屬性處理常式

本主題說明如何建立及註冊屬性處理常式，以便與 Windows 屬性系統搭配使用。

本主題的組織方式如下：

-   [屬性處理常式](#property-handlers)
-   [開始之前](#before-you-begin)
-   [初始化屬性處理常式](#initializing-property-handlers)
-   [記憶體中屬性儲存區](#in-memory-property-store)
-   [處理 PROPVARIANT-Based 值](#dealing-with-propvariant-based-values)
-   [支援開放中繼資料](#supporting-open-metadata)
-   [全文檢索內容](#full-text-contents)
-   [提供屬性的值](#providing-values-for-properties)
-   [回寫值](#writing-back-values)
-   [執行 IPropertyStoreCapabilities](#implementing-ipropertystorecapabilities)
-   [註冊和散發屬性處理常式](#registering-and-distributing-property-handlers)
-   [相關主題](#related-topics)

## <a name="property-handlers"></a>屬性處理常式

屬性處理常式是屬性系統的重要部分。 索引子會在同進程中叫用它們，以讀取和編制屬性值的索引，而且也會透過 Windows 檔案總管同進程來叫用，以便直接在檔案中讀取和寫入屬性值。 這些處理常式必須經過謹慎撰寫和測試，以避免效能降低或受影響檔案中的資料遺失。 如需會影響屬性處理常式執行之索引子特定考慮的詳細資訊，請參閱 [開發 Windows Search 的屬性處理常式](../search/-search-3x-wds-extidx-propertyhandlers.md)。

本主題將討論以範例 XML 為基礎的檔案格式，以描述具有配方副檔名的配方。 配方副檔名會註冊為其本身的相異檔案格式，而不是依賴較通用的 .xml 檔案格式，其處理常式會使用次要資料流程來儲存屬性。 建議您為您的檔案類型註冊唯一的副檔名。

## <a name="before-you-begin"></a>開始之前

屬性處理常式是為特定檔案格式建立 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 抽象的 COM 物件。 他們讀取 (剖析) ，並以符合其規格的方式寫入此檔案格式。 某些屬性處理常式會根據抽象存取特定檔案格式的 Api 來執行其工作。 在開發檔案格式的屬性處理常式之前，您必須先瞭解檔案格式儲存屬性的方式，以及這些屬性 (名稱和值) 如何對應至屬性存放區抽象。

在規劃您的執行時，請記住，屬性處理常式是在進程（例如 Windows 檔案總管、Windows Search 索引子和使用 Shell 專案程式設計模型的協力廠商應用程式）內容中載入的低層級元件。 因此，屬性處理常式無法在 managed 程式碼中執行，而且應該在 c + + 中執行。 如果您的處理常式使用任何 Api 或服務來執行其工作，您必須確保在載入屬性處理常式的環境 () 中，這些服務可以正常運作。

> [!Note]  
> 屬性處理常式一律會與特定檔案類型相關聯;因此，如果您的檔案格式包含需要自訂屬性處理常式的屬性，您應該一律為每個檔案格式註冊唯一的副檔名。

 

## <a name="initializing-property-handlers"></a>初始化屬性處理常式

在系統使用屬性之前，它會藉由呼叫 [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)的執行來初始化。 屬性處理常式的初始化方式是讓系統將資料流程指派給它，而不是將該指派保留給處理常式的執行。 此初始化方法可確保下列事項：

-   屬性處理常式可以在受限制的程式中執行 (重要的安全性功能) 沒有直接讀取或寫入檔案的存取權限，而是透過資料流程存取其內容。
-   系統可信任以正確地處理檔案 oplock，這是一項重要的可靠性措施。
-   屬性系統會提供自動安全儲存服務，而不需要屬性處理常式執行所需的任何額外功能。 如需資料流程的詳細資訊，請參閱 [寫回值](#writing-back-values) 一節。
-   使用 [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) 會將您的實作為檔案系統詳細資料的摘要。 這可讓處理常式透過替代的儲存體（例如檔案傳輸通訊協定 (FTP) 資料夾或副檔名為 .zip 的壓縮檔）支援初始化。

在某些情況下，不可能使用資料流程進行初始化。 在這些情況下，屬性處理常式可以執行兩個進一步的介面： [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) 和 [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)。 如果屬性處理常式未執行 [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)，它必須選擇不在隔離的進程中執行，如果資料流程有變更，系統索引子預設會將它放在其中。 若要退出宣告這項功能，請設定下列登錄值。

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

不過，最好是執行 [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) 並進行以資料流程為基礎的初始化。 因此，您的屬性處理常式會更安全且更可靠。 停用進程隔離通常僅適用于舊版的屬性處理常式，而任何新的程式碼都應避免 strenuously。

若要詳細檢查屬性處理常式的執行，請查看下列程式碼範例，這是 [**IInitializeWithStream：： Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize)的實作為。 處理常式的初始化方式是透過該檔相關聯的 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 實例的指標載入以 XML 為基礎的配方檔。 接近程式碼範例結尾所使用的 **\_ spDocEle** 變數，在範例中稍早定義為 Msxml2.h：： IXMLDOMElementPtr。

> [!Note]  
> 下列和所有後續的程式碼範例取自 Windows 軟體開發套件 (SDK) 中包含的配方處理常式範例。 .

 


```
HRESULT CRecipePropertyStore::Initialize(IStream *pStream, DWORD grfMode)
{
    HRESULT hr = E_FAIL;
    
    try
    {
        if (!_spStream)
        {
            hr = _spDomDoc.CreateInstance(__uuidof(MSXML2::DOMDocument60));
            
            if (SUCCEEDED(hr))
            {
                if (VARIANT_TRUE == _spDomDoc->load(static_cast<IUnknown *>(pStream)))
                {
                    _spDocEle = _spDomDoc->documentElement;
                }
```



Â 

載入檔本身之後，Windows 檔案總管中顯示的屬性會藉由呼叫受保護的 **\_ microsoft.sqlserver.replication.replicationobject.loadproperties** 方法來載入，如下列程式碼範例所示。 此程式會在下一節中詳細檢查。


```
                if (_spDocEle)
                {
                    hr = _LoadProperties();
    
                    if (SUCCEEDED(hr))
                    {
                        _spStream = pStream;
                    }
                }
                else
                {
                    hr = E_FAIL;  // parse error
                }
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
    }
    
    catch (_com_error &e)
    {
        hr = e.Error();
    }
    
    return hr;
}
```



如果資料流程是唯讀的，但 *grfMode* 參數包含 STGM \_ READWRITE 旗標，則初始化應該會失敗，並傳回 stg. \_ E \_ ACCESSDENIED。 如果沒有這種檢查，Windows 檔案總管會將屬性值顯示為可寫入，即使它們不是，也會導致令人困惑的終端使用者體驗。

屬性處理常式在其存留期內只會初始化一次。 如果要求第二個初始化，則處理常式應該會傳回 `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` 。

## <a name="in-memory-property-store"></a>In-Memory 屬性儲存區

在查看 **\_ microsoft.sqlserver.replication.replicationobject.loadproperties** 的執行之前，您應該瞭解範例中使用的 **SYSTEM.WINDOWS.FORMS.INTEGRATION.PROPERTYMAP.ADD** 陣列，將 XML 檔中的屬性對應至屬性系統中的現有屬性（透過其 PKEY 值）。

您不應該將 XML 檔案中的每個元素和屬性公開為屬性。 相反地，請只選取您認為對其檔組織中的使用者很有用的使用者 (在此案例中，配方) 。 當您開發屬性處理常式時，這是要牢記在心的重要概念：在組織案例中真正有用的資訊，以及屬於檔案詳細資料的資訊，都可以藉由開啟檔案本身來查看。 屬性不會是 XML 檔案的完整複製。


```
PropertyMap c_rgPropertyMap[] =
{
{ L"Recipe/Title", PKEY_Title, 
                   VT_LPWSTR, 
                   NULL, 
                   PKEY_Null },
{ L"Recipe/Comments", PKEY_Comment, 
                      VT_LPWSTR, 
                      NULL, 
                      PKEY_Null },
{ L"Recipe/Background", PKEY_Author, 
                        VT_VECTOR | VT_LPWSTR, 
                        L"Author", 
                        PKEY_Null },
{ L"Recipe/RecipeKeywords", PKEY_Keywords, 
                            VT_VECTOR | VT_LPWSTR, 
                            L"Keyword", 
                            PKEY_KeywordCount },
};
```



以下是 [**IInitializeWithStream：： Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize)所呼叫之 **\_ microsoft.sqlserver.replication.replicationobject.loadproperties** 方法的完整實作為。


```
HRESULT CRecipePropertyStore::_LoadProperties()
{
    HRESULT hr = E_FAIL;    
    
    if (_spCache)
    {
        hr = <mark type="const">S_OK</mark>;
    }
    else
    {
        // Create the in-memory property store.
        hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&_spCache));
    
        if (SUCCEEDED(hr))
        {
            // Cycle through each mapped property.
            for (UINT i = 0; i < ARRAYSIZE(c_rgPropertyMap); ++i)
            {
                _LoadProperty(c_rgPropertyMap[i]);
            }
    
            _LoadExtendedProperties();
            _LoadSearchContent();
        }
    }
    return hr;
}
```



**\_ Microsoft.sqlserver.replication.replicationobject.loadproperties** 方法會呼叫 Shell 協助程式函式 [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) ，為處理的屬性建立記憶體中的屬性存放區 (cache) 。 藉由使用快取，系統會追蹤您的變更。 這可讓您無法追蹤屬性值是否已在快取中變更，但尚未儲存至保存的儲存體。 它也可讓您不必要地保存未變更的屬性值。

**\_ Microsoft.sqlserver.replication.replicationobject.loadproperties** 方法也會在下列程式碼中呼叫 **\_ LoadProperty** ，以針對每個對應的屬性) 一次。 **\_ LoadProperty** 會取得 XML 資料流程中 **system.windows.forms.integration.propertymap.add** 元素所指定的屬性值，並透過呼叫 [**IPropertyStoreCache：： SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate)，將它指派給記憶體中的快取。 \_ **IPropertyStoreCache：： SetValueAndState** 呼叫中的 PSC NORMAL 旗標，表示屬性值自其進入快取以來尚未改變。


```
HRESULT CRecipePropertyStore::_LoadProperty(PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    
    MSXML2::IXMLDOMNodePtr spXmlNode(_spDomDoc->selectSingleNode(map.pszXPath));
    if (spXmlNode)
    {
        PROPVARIANT propvar = { 0 };
        propvar.vt = map.vt;
        
        if (map.vt == (VT_VECTOR | VT_LPWSTR))
        {
            hr = _LoadVectorProperty(spXmlNode, &propvar, map);
        }
        else
        {
            // If there is no value, set to VT_EMPTY to indicate
            // that it is not there. Do not return failure.
            if (spXmlNode->text.length() == 0)
            {
                propvar.vt = VT_EMPTY;
                hr = <mark type="const">S_OK</mark>;
            }
            else
            {
                // SimplePropVariantFromString is a helper function.
                // particular to the sample. It is found in Util.cpp.
                hr = SimplePropVariantFromString(spXmlNode->text, &propvar);
            }
        }
    
        if (S_OK == hr)
        {
            hr = _spCache->SetValueAndState(map.key, &propvar, PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    return hr;
}
```



## <a name="dealing-with-propvariant-based-values"></a>處理 PROPVARIANT-Based 值

在 **\_ LoadProperty** 的執行中，會以 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)的形式提供屬性值。 軟體發展工具組 (SDK) 提供一組 Api，可從 **PROPVARIANT** 類型等基本類型（例如 **PWSTR** 或 **int** ）轉換。 這些 Api 可在 Propvarutil 中找到。

例如，若要將 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 轉換為字串，您可以使用 [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) ，如下所示。


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



若要從字串初始化 PROPVARIANT，您可以使用 [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring)。


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



您可以在範例中所包含的任何配方檔案中看到，每個檔案中都可以有一個以上的關鍵字。 為了因應此情況，屬性系統支援以字串向量表示的多重值字串， (例如 "VT \_ vector \| VT \_ LPWSTR" ) 。 範例中的 **\_ LoadVectorProperty** 方法會使用以向量為基礎的值。


```
HRESULT CRecipePropertyStore::_LoadVectorProperty
                                (MSXML2::IXMLDOMNode *pNodeParent,
                                 PROPVARIANT *ppropvar,
                                 struct PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = pNodeParent->selectNodes(map.pszSubNodeName);
    
    if (spList)
    {
        UINT cElems = spList->length;
        ppropvar->calpwstr.cElems = cElems;
        ppropvar->calpwstr.pElems = (PWSTR*)CoTaskMemAlloc(sizeof(PWSTR)*cElems);
    
        if (ppropvar->calpwstr.pElems)
        {
            for (UINT i = 0; (SUCCEEDED(hr) && i < cElems); ++i)
            {
                hr = SHStrDup(spList->item[i]->text, 
                              &(ppropvar->calpwstr.pElems[i]));
            }
    
            if (SUCCEEDED(hr))
            {
                if (!IsEqualPropertyKey(map.keyCount, PKEY_Null))
                {
                    PROPVARIANT propvarCount = { VT_UI4 };
                    propvarCount.uintVal = cElems;
                    
                    _spCache->SetValueAndState(map.keyCount,
                                               &propvarCount, 
                                               PSC_NORMAL);
                }
            }
            else
            {
                PropVariantClear(ppropvar);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
    
    return hr;
}
```



如果值不存在於檔案中，則不會傳回錯誤。 相反地，請將值設定為 VT \_ 空白，並傳回 **S \_ OK**。 VT \_ 空白表示屬性值不存在。

## <a name="supporting-open-metadata"></a>支援開放中繼資料

這個範例會使用以 XML 為基礎的檔案格式。 例如，您可以擴充其架構，以支援在 developmet 期間不會考慮的屬性。 這個系統稱為「開放中繼資料」。 此範例會在名為 **ExtendedProperties** 的 **配方** 元素底下建立節點，以擴充屬性系統，如下列程式碼範例所示。


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



若要在初始化期間載入保存的擴充屬性，請執行 **\_ LoadExtendedProperties** 方法，如下列程式碼範例所示。


```
HRESULT CRecipePropertyStore::_LoadExtendedProperties()
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = 
                  _spDomDoc->selectNodes(L"Recipe/ExtendedProperties/Property");
    
    if (spList)
    {
        UINT cElems = spList->length;
        
        for (UINT i = 0; i < cElems; ++i)
        {
            MSXML2::IXMLDOMElementPtr spElement;
            
            if (SUCCEEDED(spList->item[i]->QueryInterface(IID_PPV_ARGS(&spElement))))
            {
                PROPERTYKEY key;
                _bstr_t bstrPropName = spElement->getAttribute(L"Name").bstrVal;
    
                if (!!bstrPropName &&
                    (SUCCEEDED(PropertyKeyFromString(bstrPropName, &key))))
                {
                    PROPVARIANT propvar = { 0 };
                    _bstr_t bstrEncodedValue = 
                               spElement->getAttribute(L"EncodedValue").bstrVal;
                   
                    if (!!bstrEncodedValue)
                    {
                        // DeserializePropVariantFromString is a helper function
                        // particular to the sample. It is found in Util.cpp.
                        hr = DeserializePropVariantFromString(bstrEncodedValue, 
                                                              &propvar);
                    }
```



在 Propsys 中宣告的序列化 Api 會用來將 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 類型序列化和還原序列化成資料的 blob，然後使用 Base64 編碼將這些 blob 序列化成可儲存在 XML 中的字串。 這些字串會儲存在 **ExtendedProperties** 元素的 **url-encodedvalue** 屬性中。 下列公用程式方法（在範例的 Util .cpp 檔案中執行）會執行序列化。 首先，呼叫 [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) 函數來執行二進位序列化，如下列程式碼範例所示。


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



接著， [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)函數（在 Wincrypt 中宣告）會執行 Base64 轉換。


```
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        DWORD cchString;
        
        if (CryptBinaryToString((BYTE *)pBlob, 
                                cbBlob,
                                CRYPT_STRING_BASE64, 
                                NULL, 
                                &cchString))
        {
            *pszOut = (PWSTR)CoTaskMemAlloc(sizeof(WCHAR) *cchString);
    
            if (*pszOut)
            {
                if (CryptBinaryToString((BYTE *)pBlob, 
                                         cbBlob,
                                         CRYPT_STRING_BASE64,
                                         *pszOut, 
                                         &cchString))
                {
                    hr = <mark type="const">S_OK</mark>;
                }
                else
                {
                    CoTaskMemFree(*pszOut);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
    }
    
    return <mark type="const">S_OK</mark>;}
```



**DeserializePropVariantFromString** 函式（也可以在 Util 中找到）會反轉作業，並將 XML 檔案中的值還原序列化。

如需開啟中繼資料支援的相關資訊，請參閱 [檔案類型](../shell/fa-file-types.md)中的「支援開放中繼資料的檔案類型」。

## <a name="full-text-contents"></a>Full-Text 內容

屬性處理常式也有助於全文檢索搜尋檔案內容，而且如果檔案格式不太複雜，則可以輕鬆地提供該功能。 另外還有一個更強大的方法，可透過 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面實行提供檔案的完整文字。

下表摘要說明使用 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 或 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)的每種方法各有何好處。



| 功能                                   | IFilter                      | IPropertyStore |
|----------------------------------------------|------------------------------|----------------|
| 允許寫回檔案嗎？                  | 否                           | 是            |
| 提供內容和屬性的混合？      | 是                          | 是            |
| 多 語種？                                | 是                          | 否             |
| MIME/內嵌？                               | 是                          | 否             |
| 文字界限？                             | 句子、段落、章節 | 無           |
| 適用于 SPS/SQL Server 的實作為支援？ | 是                          | 否             |
| 實作                               | Complex                      | 簡單         |



 

在配方處理常式範例中，配方檔案格式沒有任何複雜的需求，因此只會針對全文檢索支援執行 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 。 全文檢索搜尋是針對下列陣列中名為的 XML 節點所執行。


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



屬性系統包含 `System.Search.Contents` (PKEY \_ 搜尋 \_ 內容) 屬性，此屬性是建立來提供全文檢索內容給索引子。 這個屬性的值永遠不會直接顯示在 UI 中;上述陣列中所命名之所有 XML 節點的文字都會串連成單一字串。 然後透過呼叫 [**IPropertyStoreCache：： SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) ，將該字串提供給索引子，作為配方檔案的全文檢索內容，如下列程式碼範例所示。


```
HRESULT CRecipePropertyStore::_LoadSearchContent()
{
    HRESULT hr = S_FALSE;
    _bstr_t bstrContent;
    
    for (UINT i = 0; i < ARRAYSIZE(c_rgszContentXPath); ++i)
    {
        MSXML2::IXMLDOMNodeListPtr spList = 
                                  _spDomDoc->selectNodes(c_rgszContentXPath[i]);
    
        if (spList)
        {
            UINT cElems = spList->length;
            
            for (UINT elt = 0; elt < cElems; ++elt)
            {
                bstrContent += L" ";
                bstrContent += spList->item[elt]->text;
            }
        }
    }
    
    if (bstrContent.length() > 0)
    {
        PROPVARIANT propvar = { VT_LPWSTR };
        hr = SHStrDup(bstrContent, &(propvar.pwszVal));
    
        if (SUCCEEDED(hr))
        {
            hr = _spCache->SetValueAndState(PKEY_Search_Contents, 
                                            &propvar, 
                                            PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    
    return hr;}
```



## <a name="providing-values-for-properties"></a>提供屬性的值

當用來讀取值時，通常會因為下列其中一個原因而叫用屬性處理常式：

-   以列舉所有屬性值。
-   取得特定屬性的值。

若為列舉，則會要求屬性處理常式在編制索引期間或在屬性對話方塊要求屬性顯示于 **另** 一個群組時，列舉其屬性。 編制索引會持續以背景作業的方式來運作。 每當檔案變更時，索引子就會收到通知，並藉由要求屬性處理常式來列舉其屬性來重新建立檔案的索引。 因此，請務必有效率地執行屬性處理常式，並儘快傳回屬性值。 列舉所有具有值的屬性，就像您對任何集合所做的一樣，但不會列舉牽涉到記憶體密集計算的屬性，或是可能使抓取速度變慢的網路要求。

撰寫屬性處理常式時，您通常需要考慮下列兩組屬性。

-   主要屬性：您的檔案類型原本就支援的屬性。 例如，交換影像檔案 (EXIF) 中繼資料的相片屬性處理常式原本就支援 `System.Photo.FNumber` 。
-   擴充屬性：您的檔案類型支援作為開啟中繼資料一部分的屬性。

由於範例會使用記憶體內部快取，因此執行 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 方法只是委派給該快取，如下列程式碼範例所示。


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



如果您選擇不要委派至記憶體中的快取，您必須執行您的方法，以提供下列預期的行為>：

-   [**IPropertyStore：： GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85))：如果沒有屬性，此方法會傳回 **S \_ OK**。
-   [**IPropertyStore：： GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85))：如果 *iProp* 大於或等於 *cProps*，這個方法會傳回 E \_ INVALIDARG，而 *pkey* 參數所指向的結構會填入零。
-   [**IPropertyStore：： GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) 和 [**IPropertyStore：： GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) 會反映屬性處理常式的目前狀態。 如果透過 [**IPropertyStore：： SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))將 [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey)新增至檔案或從中移除，這兩個方法必須反映下次呼叫它們時的變更。
-   [**IPropertyStore：： GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85))：如果要求此方法提供不存在的值，則會傳回 **S \_ OK** ，並將值回報為 VT \_ 空白。

## <a name="writing-back-values"></a>回寫值

當屬性處理常式使用 [**IPropertyStore：： SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))寫入屬性的值時，它不會將值寫入至檔案，直到呼叫 [**IPropertyStore：： Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) 為止。 記憶體內部快取在執行此配置時相當有用。 在範例程式碼中， **IPropertyStore：： SetValue** 執行只會在記憶體內部快取中設定新的值，並將該屬性的狀態設定為 [PSC 已變更] \_ 。


```
HRESULT CRecipePropertyStore::SetValue(REFPROPERTYKEY key, const PROPVARIANT *pPropVar)
    {
    
    HRESULT hr = E_FAIL;
    
    if (IsEqualPropertyKey(key, PKEY_Search_Contents))
    {
        // This property is read-only
        hr = HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED);  
    }
    else
    {
        hr = _spCache->SetValueAndState(key, pPropVar, PSC_DIRTY);
    }
    
    return hr;
}
```



在任何 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 的執行中， [**IPropertyStore：： SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))預期會有下列行為：

-   如果屬性已經存在，則會設定屬性的值。
-   如果屬性不存在，就會加入新的屬性並設定其值。
-   如果屬性值不能以與指定 (相同的精確度來保存，就會因為檔案格式) 的大小限制而截斷，所以會將值設定為最遠，而且 \_ \_ 會傳回截斷的。
-   如果屬性處理常式不支援屬性， `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` 則會傳回。
-   如果有另一個原因是無法設定屬性值（例如，透過存取控制清單鎖定的檔案或缺少許可權） (Acl) ，則 \_ \_ 會傳回 Stg. E ACCESSDENIED。

使用資料流程作為範例的其中一個主要優點是可靠性。 屬性處理常式必須一律考慮在發生重大失敗時，不會讓檔案處於不一致的狀態。 顯然應避免使用者的檔案損毀，最好的方法是使用「寫入時複製」機制。 如果您的屬性處理常式使用資料流程來存取檔案，則會自動取得此行為;系統會將任何變更寫入資料流程，只有在認可作業期間以新的複本取代檔案。

若要覆寫這個行為並手動控制檔案儲存程式，您可以在處理常式的登錄專案中設定 ManualSafeSave 值，以退出宣告安全儲存行為，如下所示。

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

當處理常式指定 ManualSafeSave 值時，用來初始化它的資料流程不是交易式資料流程， (STGM \_ 交易) 。 處理常式本身必須執行安全儲存函式，以確保在儲存作業中斷時檔案不會損毀。 如果處理常式會就地進行寫入，則會寫入至提供的資料流程。 如果處理常式不支援這項功能，則必須使用 [**IDestinationStreamFactory：： GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream)來取出用來寫入檔案更新複本的資料流程。 完成寫入處理常式之後，它應該在原始資料流程上呼叫 [**IPropertyStore：： Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) 來完成作業，並將原始資料流程的內容取代為檔案的新複本。

如果您未使用資料流程初始化處理常式，ManualSafeSave 也是預設情況。 若沒有原始資料流程可接收暫存資料流程的內容，您必須使用 [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) 來執行原始程式檔的不可部分完成取代。

會以產生大於 1 MB 之檔案的方式使用的大型檔案格式應可支援就地寫入屬性的支援;否則，效能行為不符合屬性系統用戶端的期望。 在此案例中，寫入屬性所需的時間應該不會受到檔案大小的影響。

針對非常大型的檔案，例如 1 GB 或更多的影片檔案，則需要不同的解決方案。 如果檔案中沒有足夠的空間可進行就地寫入，則如果保留給就地屬性寫入的空間量已用盡，則處理常式可能會失敗屬性更新。 發生此錯誤的原因是為了避免因 2 GB IO (1 而產生效能不佳的效能，1寫入) 。 因為這可能會造成失敗，所以這些檔案格式應保留足夠的空間供就地屬性寫入之用。

如果檔案的標頭中有足夠的空間來寫入中繼資料，而且寫入該中繼資料並不會導致檔案成長或壓縮，則可以安全地就地寫入。 建議您將 64 KB 作為起點。 就地寫入相當於要求在 [**IPropertyStore：： commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))的實 ManualSafeSave 和呼叫 [**IStream：：**](/windows/win32/api/objidl/nf-objidl-istream-commit) commit 的處理常式，而且效能比寫入時複製的效能更佳。 如果檔案大小因為屬性值變更而變更，則不應嘗試就地寫入，因為發生異常終止時可能會損毀檔案。

> [!Note]  
> 基於效能考慮，我們建議使用 ManualSafeSave 選項搭配使用 100 KB 或更大檔案的屬性處理常式。

 

如下列 [**IPropertyStore：： Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))範例所示，會註冊 ManualSafeSave 的處理常式，以說明「手動安全儲存」選項。 **\_ SaveCacheToDom** 方法會將儲存在記憶體中快取中的屬性值寫入至設定物件。


```
HRESULT CRecipePropertyStore::Commit()
{
    HRESULT hr = E_UNEXPECTED;
    if (_pCache)
    {
        // Check grfMode to ensure writes are allowed.
        hr = STG_E_ACCESSDENIED;
        if (_grfMode & STGM_READWRITE)
        {
            // Save the internal value cache to XML DOM object.
            hr = _SaveCacheToDom();
            if (SUCCEEDED(hr))
            {
                // Reset the output stream.
                LARGE_INTEGER liZero = {};
                hr = _pStream->Seek(liZero, STREAM_SEEK_SET, NULL);
```



接下來，詢問 p 是否支援 [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory)。


```
                        if (SUCCEEDED(hr))
                        {
                            // Write the XML out to the temprorary stream and commit it.
                            VARIANT varStream = {};
                            varStream.vt = VT_UNKNOWN;
                            varStream.punkVal = pStreamCommit;
                            hr = _pDomDoc->save(varStream);
                            if (SUCCEEDED(hr))
                            {
                                hr = pStreamCommit->Commit(STGC_DEFAULT);_
```



接下來，認可原始資料流程，這會以安全的方式將資料寫回原始檔案。


```
                        if (SUCCEEDED(hr))
                                {
                                    // Commit the real output stream.
                                    _pStream->Commit(STGC_DEFAULT);
                                }
                            }

                            pStreamCommit->Release();
                        }

                        pSafeCommit->Release();
                    }
                }
            }
        }
    }
```



然後檢查 **\_ SaveCacheToDom** 的執行。


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



接下來，取得儲存在記憶體中快取中的屬性數目。


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



現在逐一查看屬性，以判斷屬性的值在載入記憶體之後是否已變更。


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



[**IPropertyStoreCache：： >getstate**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate)方法會取得快取中的屬性狀態。 PSC 中途 \_ 旗標是在 [**IPropertyStore：： SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) 實中設定的，會將屬性標示為已變更。


```
        if (SUCCEEDED(hr))
        {
            // check the cache state; only save dirty properties
            PSC_STATE psc;
            hr = _pCache->GetState(key, &psc);
            if (SUCCEEDED(hr) && psc == PSC_DIRTY)
            {
                // get the cached value
                PROPVARIANT propvar = {};
                hr = _pCache->GetValue(key, &propvar); 
```



將屬性對應至 XML 節點，如例如 **\_ rgPropertyMap** 陣列中所指定。


```
if (SUCCEEDED(hr))
                {
                    // save as a native property if the key is in the property map
                    BOOL fIsNativeProperty = FALSE;
                    for (UINT i = 0; i < ARRAYSIZE(g_rgPROPERTYMAP); ++i)
                    {
                        if (IsEqualPropertyKey(key, *g_rgPROPERTYMAP[i].pkey))
                        {
                            fIsNativeProperty = TRUE;
                            hr = _SaveProperty(propvar, g_rgPROPERTYMAP[i]);
                            break;
                        }     
```



如果屬性不在對應中，則為 Windows 檔案總管所設定的新屬性。 因為支援開放中繼資料，請將新的屬性儲存在 XML 的 **ExtendedProperties** 區段中。


```
                    
                    // Otherwise, save as an extended property.
                    if (!fIsNativeProperty)
                    {
                        hr = _SaveExtendedProperty(key, propvar);
                    }

                    PropVariantClear(&propvar);
                }
            }
        }
    }

    return hr;    
```



## <a name="implementing-ipropertystorecapabilities"></a>執行 IPropertyStoreCapabilities

[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) 會通知 shell ui 是否可在 shell ui 中編輯特定屬性。 請務必注意，這只與編輯 UI 中屬性的功能有關，而不是您是否可以在屬性上成功呼叫 [**IPropertyStore：： SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) 。 \_從 [**IPropertyStoreCapabilities：： IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) provokes 傳回值 FALSE 的屬性，可能仍可以透過應用程式進行設定。


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) 會 **傳回 \_ [確定]** ，表示應該允許使用者直接編輯屬性;\_FALSE 表示不應如此。 \_FALSE 可能表示應用程式會負責寫入屬性，而不是使用者。 Shell 會根據呼叫這個方法的結果，適當地停用編輯控制項。 會假設不會執行 [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) 的處理常式會透過支援寫入任何屬性來支援開啟的中繼資料。

如果您要建立處理唯讀屬性的處理常式，則應該將 **Initialize** 方法 ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)、 [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)或 [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) ，以便在 \_ \_ 使用 ACCESSDENIED READWRITE 旗標呼叫時傳回 stg. E STGM \_ 。

某些屬性的 [isInnate](./propdesc-schema-typeinfo.md) 屬性設定為 **true**。 固有屬性具有下列特性：

-   屬性通常會以某種方式計算。 例如， `System.Image.BitDepth` 是從影像本身計算而來。
-   變更屬性不會有任何意義，而不需要變更檔案。 比方說，變更 `System.Image.Dimensions` 並不會調整影像大小，所以允許使用者進行變更並不合理。
-   在某些情況下，系統會自動提供這些屬性。 範例包括 `System.DateModified` 檔案系統所提供的，以及以使用者共用檔案的使用者為基礎的範例 `System.SharedWith` 。

由於這些特性，標記為 *IsInnate* 的屬性只會在 Shell UI 中提供給使用者，以做為唯讀屬性。 如果屬性標示為 *IsInnate*，屬性系統不會將該屬性儲存在屬性處理常式中。 因此，屬性處理常式不需要特殊的程式碼，就能在其實作為中考慮這些屬性。 如果未針對特定屬性明確陳述 *IsInnate* 屬性的值，則預設值為 **false**。

## <a name="registering-and-distributing-property-handlers"></a>註冊和散發屬性處理常式

在實作為屬性處理常式的情況下，必須註冊它以及與處理常式相關聯的副檔名。 如需詳細資訊，請參閱 [註冊和散發屬性處理常式](./prophand-reg-dist.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[瞭解屬性處理常式](./building-property-handlers-properties.md)
</dt> <dt>

[使用種類名稱](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[使用屬性清單](./building-property-handlers-property-lists.md)
</dt> <dt>

[註冊和散發屬性處理常式](./prophand-reg-dist.md)
</dt> <dt>

[屬性處理常式的最佳作法和常見問題](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
