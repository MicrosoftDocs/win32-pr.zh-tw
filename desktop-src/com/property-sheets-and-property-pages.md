---
title: 屬性工作表和屬性頁
description: 屬性工作表和屬性頁
ms.assetid: 6bcd1c1c-9b66-4422-bb07-67a856b3295d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7991ea650838e9980292257c14d26909e9476f0f35422fa21deab2b0b5ecbbdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104929"
---
# <a name="property-sheets-and-property-pages"></a>屬性工作表和屬性頁

物件的屬性會透過 COM 介面或物件的 **IDispatch** 實作為方法公開給用戶端，讓呼叫這些方法的程式可變更屬性。 屬性頁的 OLE 技術提供方法，根據 Windows 使用者介面標準來建立物件屬性的使用者介面。 因此，這些屬性會公開給終端使用者。 物件的屬性工作表是索引標籤式對話方塊，其中每個索引標籤都對應至特定的屬性頁。 使用屬性頁的 OLE 模型包含下列功能：

-   每個屬性頁都是由執行 [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) 或 [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)的同進程物件所管理。 每一頁都是使用它自己的唯一 CLSID 來識別。
-   物件會藉由執行 [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages)，指定其對屬性頁的支援。 透過這個介面，呼叫端可以取得用來識別物件所支援之特定屬性頁的 Clsid 清單。 如果物件指定屬性頁 CLSID，則物件必須能夠從屬性頁接收屬性變更。
-   任何程式碼 (用戶端或物件) 如果想要顯示物件的屬性工作表，則會傳遞物件的 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 指標 (或陣列（如果有多個物件會受到影響）) 以及 [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) 或 [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect)的分頁 clsid 陣列，以建立索引標籤式對話方塊。
-   屬性框架對話方塊會將每個屬性頁的單一實例具現化，並在每個 CLSID 上使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 。 屬性框架至少取得每個頁面的 [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) 指標。 此外，框架會在每個頁面本身建立一個屬性頁面網站物件。 每個網站會執行 [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) ，並將此指標傳遞至每個頁面。 頁面接著會透過此介面指標與網站通訊。
-   每個頁面也會知道已叫用物件的物件或物件;也就是說，屬性框架會將物件的 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)指標傳遞至每個頁面。 當指示將變更套用至物件時，每個頁面都會查詢適當的介面指標，並以任何想要的方式將新的屬性值傳遞給物件。 這種通訊的發生方式不條文。
-   物件也可以透過 [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) 介面支援每個屬性流覽，讓物件指定在顯示內容頁時應接收初始焦點的屬性，以及指定用戶端在其自己的使用者介面中可顯示的字串和值。

下圖說明這些功能：

![顯示內容表和屬性頁功能的圖表。](images/7ea02938-c2fc-4ad0-a8b1-25222ca890ea.png)

這些介面的定義如下：

``` syntax
interface ISpecifyPropertyPages : IUnknown 
  { 
    HRESULT GetPages([out] CAUUID *pPages); 
  }; 
 
 
interface IPropertyPage : IUnknown 
  { 
    HRESULT SetPageSite([in] IPropertyPageSite *pPageSite); 
    HRESULT Activate([in] HWND hWndParent, [in] LPCRECT prc 
        , [in] BOOL bModal); 
    HRESULT Deactivate(void); 
    HRESULT GetPageInfo([out] PROPPAGEINFO *pPageInfo); 
    HRESULT SetObjects([in] ULONG cObjects 
        , [in, max_is(cObjects)] IUnknown **ppunk); 
    HRESULT Show([in] UINT nCmdShow); 
    HRESULT Move([in] LPCRECT prc); 
    HRESULT IsPageDirty(void); 
    HRESULT Apply(void); 
    HRESULT Help([in] LPCOLESTR pszHelpDir); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
interface IPropertyPageSite : IUnknown 
  { 
    HRESULT OnStatusChange([in] DWORD dwFlags); 
    HRESULT GetLocaleID([out] LCID *pLocaleID); 
    HRESULT GetPageContainer([out] IUnknown **ppUnk); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
```

[**ISpecifyPropertyPages：： GetPages**](/windows/desktop/api/OCIdl/nf-ocidl-ispecifypropertypages-getpages)方法會傳回 (GUID) 值的計數陣列，其中每一個都描述物件所要顯示之屬性頁的 CLSID。 使用 [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) 或 [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect) 叫用屬性工作表的人員會將此陣列傳遞給函數。 請注意，如果呼叫端想要顯示多個物件的屬性頁，它只能將所有物件之 CLSID 清單的交集傳遞給這些函數。 換句話說，呼叫端必須只叫用所有物件通用的屬性頁。

此外，呼叫端也會將受影響物件的 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 指標傳遞給 API 函式。 這兩個 API 函式都會建立一個屬性框架對話方塊，並使用其所載入之每個頁面的 [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) 來具現化頁面網站。 透過這個介面，屬性頁可以：

-   透過 [**GetLocaleID**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getlocaleid)，在屬性工作表中取出目前使用的語言。
-   要求框架透過 [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-translateaccelerator)處理按鍵。
-   透過 [**OnStatusChange**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-onstatuschange)通知頁面中有變更的畫面格。
-   透過 [**GetPageContainer**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getpagecontainer)取得框架本身的介面指標，雖然目前沒有針對此框架定義的介面，但此函式一律會傳回 E \_ >notimpl。

屬性框架會將每個屬性頁物件具現化，並取得每個頁面的 [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) 介面。 透過這個介面，框架會通知頁面網站 ([**SetPageSite**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setpagesite)) 、 [**) 的**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-getpageinfo) 頁面維度和 (字串，將介面指標傳遞給受影響的物件 ([**SetObjects**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setobjects)) 、告知頁面建立和終結其控制項的時機 ([**啟動**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-activate) 和 [**停用**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-deactivate)) 、指示頁面顯示或重新放置其本身 ([**顯示**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-show) 和 [**移動**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-move)) 、指示頁面將其目前的值套用到受影響的 [**物件 (套用) 、**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-apply) 在頁面的變更狀態 ([**IsPageDirty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-ispagedirty)) 、叫用 [說明 [**] ([**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-help) 說明]) ，以及將按鍵傳送至頁面 ([**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-translateaccelerator)) 。

物件也可以支援每個屬性的流覽，其提供：

1.  透過 [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) 和) [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2) 的方式 (，以指定在第一次顯示內容表時，應在哪個屬性頁面上取得初始焦點
2.  一種方法， (物件的 [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)) 來指定預先定義的值，以及可在用戶端的屬性使用者介面中顯示的對應描述性字串。

物件可以選擇支援 (2) ，而不支援 (1) ，例如，當物件沒有屬性工作表時。

[**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)和 [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)介面的定義如下：

``` syntax
interface IPerPropertyBrowsing : IUnknown 
  { 
    HRESULT GetDisplayString([in] DISPID dispID, [out] BSTR *pbstr); 
    HRESULT MapPropertyToPage([in] DISPID dispID, [out] CLSID *pclsid); 
    HRESULT GetPredefinedStrings([in] DISPID dispID, [out] CALPOLESTR *pcaStringsOut, [out] CADWORD *pcaCookiesOut); 
    HRESULT GetPredefinedValue([in] DISPID dispID, [in] DWORD dwCookie, [out] VARIANT *pvarOut); 
  } 
 
interface IPropertyPage2 : IPropertyPage 
  { 
    HRESULT EditProperty([in] DISPID dispID); 
  } 
 
```

為了指定其對這類功能的支援，此物件會執行 [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)。 透過這個介面，呼叫端可以要求完成流覽所需的資訊，例如預先定義的字串 ([**GetPredefinedStrings**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings)) 和值 ([**GetPredefinedValue**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue)) 以及指定屬性 ([**GetDisplayString**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getdisplaystring)) 的顯示字串。

此外，用戶端可以取得屬性頁的 CLSID，讓使用者能夠編輯以 DISPID ([**MapPropertyToPage**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-mappropertytopage)) 識別的指定屬性。 接著，用戶端會指示屬性框架先將 CLSID 和 DISPID 傳遞給 [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect)，以啟動該頁面。 畫面格會先啟用該頁面，並透過 [**IPropertyPage2：： EditProperty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage2-editproperty)將 DISPID 傳遞到頁面。 然後頁面會將焦點設定為該屬性的編輯欄位。 如此一來，用戶端就可以從自己的使用者介面中的屬性名稱跳到可操作該屬性的屬性頁。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[屬性頁和屬性工作表](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




