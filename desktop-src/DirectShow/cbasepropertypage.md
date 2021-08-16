---
description: CBasePropertyPage 類別是用來執行屬性頁的抽象類別。 如果您要撰寫篩選 (或其他支援屬性頁的物件) ，請使用這個類別。
ms.assetid: 80e77827-ed2f-426e-aa6f-c2aa90031751
title: 'CBasePropertyPage 類別 (Cprop) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ca4bf0789488a8601ae24bd4e43e1af8335fdf97a7864cbfba242b9c99eca8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955010"
---
# <a name="cbasepropertypage-class"></a>CBasePropertyPage 類別

![cbasepropertypage 類別階層](images/cprop01.png)

`CBasePropertyPage`類別是用來執行屬性頁的抽象類別。 如果您要撰寫篩選 (或其他支援屬性頁的物件) ，請使用這個類別。



| 受保護的成員變數                                             | 描述                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bDirty**](cbasepropertypage-m-bdirty.md)                        | 指出是否有任何屬性變更。                                                                             |
| [**m \_ DialogId**](cbasepropertypage-m-dialogid.md)                    | 對話方塊的資源識別碼。                                                                                               |
| [**m \_ Dlg**](cbasepropertypage-m-dlg.md)                              | 對話方塊視窗的控制碼。                                                                                                      |
| [**m \_ hwnd**](cbasepropertypage-m-hwnd.md)                            | 對話方塊視窗的控制碼。                                                                                                      |
| [**m \_ pPageSite**](cbasepropertypage-m-ppagesite.md)                  | 屬性頁網站之 **IPropertyPageSite** 介面的指標。                                                         |
| [**m \_ TitleId**](cbasepropertypage-m-titleid.md)                      | 包含對話方塊標題之字串的資源識別碼。                                                                  |
| 公用方法                                                         | 描述                                                                                                                       |
| [**CBasePropertyPage**](cbasepropertypage-cbasepropertypage.md)       | 函式方法。                                                                                                               |
| [**~ CBasePropertyPage**](cbasepropertypage--cbasepropertypage.md)     | 函式方法。 虛擬。                                                                                                       |
| [**OnActivate**](cbasepropertypage-onactivate.md)                     | 在屬性頁啟用時呼叫。 虛擬。                                                                              |
| [**OnApplyChanges**](cbasepropertypage-onapplychanges.md)             | 當使用者將變更套用至屬性頁時呼叫。 虛擬。                                                               |
| [**OnConnect**](cbasepropertypage-onconnect.md)                       | 提供與屬性頁相關聯之物件的 **IUnknown** 指標。 虛擬。                                        |
| [**OnDeactivate**](cbasepropertypage-ondeactivate.md)                 | 當對話方塊視窗終結時呼叫。 虛擬。                                                                          |
| [**OnDisconnect**](cbasepropertypage-ondisconnect.md)                 | 當屬性頁應該釋放相關聯的物件時呼叫。 虛擬。                                                      |
| [**OnReceiveMessage**](cbasepropertypage-onreceivemessage.md)         | 當對話方塊收到訊息時呼叫。 虛擬。                                                                           |
| IPropertyPage 方法                                                  | 描述                                                                                                                       |
| [**啟用**](cbasepropertypage-activate.md)                         | 建立對話方塊視窗。                                                                                                    |
| [**套用**](cbasepropertypage-apply.md)                               | 將目前的屬性頁值套用至與屬性頁面相關聯的物件                                          |
| [**停用**](cbasepropertypage-deactivate.md)                     | 終結對話方塊視窗。                                                                                                       |
| [**GetPageInfo**](cbasepropertypage-getpageinfo.md)                   | 抓取屬性頁的相關資訊。                                                                                    |
| [**説明**](cbasepropertypage-help.md)                                 | 叫用屬性頁說明。                                                                                                   |
| [**IsPageDirty**](cbasepropertypage-ispagedirty.md)                   | 指出屬性頁面在啟動後，或自最近一次呼叫 **IPropertyPage：： Apply** 之後是否已變更。 |
| [**移動**](cbasepropertypage-move.md)                                 | 放置對話方塊並調整其大小。                                                                                             |
| [**SetObjects**](cbasepropertypage-setobjects.md)                     | 為與屬性頁相關聯的物件提供 **IUnknown** 指標。                                                 |
| [**SetPageSite**](cbasepropertypage-setpagesite.md)                   | 初始化屬性頁。                                                                                                    |
| [**顯示**](cbasepropertypage-show.md)                                 | 顯示或隱藏對話方塊。                                                                                                    |
| [**TranslateAccelerator**](cbasepropertypage-translateaccelerator.md) | 指示屬性頁處理按鍵。                                                                               |



 

## <a name="remarks"></a>備註

屬性頁是 COM 物件，因此您必須為類別識別碼 (CLSID) 產生 GUID，並在 [**CFactoryTemplate**](cfactorytemplate.md) 陣列中提供專案。 如需詳細資訊，請參閱[DirectShow 和 COM](directshow-and-com.md)。 下列範例顯示一般的 class factory 專案：


```
CFactoryTemplate g_Templates[] =
{   
    { 
        L"My Property Page",
        &CLSID_MyPropPage,
        CMyProp::CreateInstance,
        NULL,
        NULL
    },
    /* Also include the template for your filter (not shown). */
};

```



您的篩選準則必須公開 **ISpecifyPropertyPages** 介面。 這個介面包含單一方法 **GetPages**，它會傳回屬性頁的 CLSID。 下列範例顯示如何執行此方法：


```
STDMETHODIMP CMyFilter::GetPages(CAUUID *pPages)
{
    if (!pPages) return E_POINTER;

    pPages->cElems = 1;
    pPages->pElems = reinterpret_cast<GUID*>(CoTaskMemAlloc(sizeof(GUID)));
    if (pPages->pElems == NULL) 
    {
        return E_OUTOFMEMORY;
    }
    *(pPages->pElems) = CLSID_MyPropPage;
    return S_OK;
} 
```



請記得也要覆寫篩選準則的 **NonDelegatingQueryInterface** 方法。 如需詳細資訊，請參閱 [DirectShow 和 COM](directshow-and-com.md)和 [**INonDelegatingUnknown**](inondelegatingunknown.md)。

接下來，將對話方塊建立為專案中的資源，並建立保存對話方塊標題的字串資源。 這兩個資源識別碼都是 **CBasePropertyPage** 函式的參數。 將標題字串保留在資源中，可讓您更輕鬆地將屬性頁當地語系化。

**CBasePropertyPage** 類別提供 **IPropertyPage** 介面的架構。 這個架構會呼叫數個虛擬方法，包括 [**CBasePropertyPage：： OnActivate**](cbasepropertypage-onactivate.md)、 [**CBasePropertyPage：： OnApplyChanges**](cbasepropertypage-onapplychanges.md)等等。 在基類中，這些方法只會傳回 S \_ OK。 您的衍生類別必須覆寫這些虛擬方法的部分或全部。 如需詳細資訊，請參閱個別方法的備註。

如需如何使用這個類別來建立屬性頁的延伸範例，請參閱 [建立篩選屬性頁](creating-a-filter-property-page.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Cprop (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




