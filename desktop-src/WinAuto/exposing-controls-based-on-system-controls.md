---
title: 根據系統控制項公開控制項
description: 根據系統控制項公開控制項
ms.assetid: 9291b79e-3ed0-4f3c-a610-38215d84f5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09349819cbc8e36d879947fe0cbd0914a1de630171ef70e3b132f58c60c87228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829095"
---
# <a name="exposing-controls-based-on-system-controls"></a>根據系統控制項公開控制項

在嘗試本節所述的技術之前，您應該考慮使用某種形式的動態注釋（直接、值對應或伺服器）。 如需詳細資訊，請參閱 [動態批註 API](dynamic-annotation-api.md)。

在大部分的情況下，Microsoft Active Accessibility 會公開 superclass 或子類別化控制項的相關資訊。 Superclassing 和子類別化可讓應用程式開發人員使用系統控制項的基本功能來建立自訂控制項，並包含應用程式所提供的增強功能。 Superclass 控制項的視窗類別名稱不同于它所依據的系統控制項。 子類別化控制項具有相同的視窗類別名稱。 如需有關 superclassing 和子類別化的詳細資訊，請參閱 Windows 軟體開發套件 (SDK) 檔。

因為 Microsoft Active Accessibility 會公開系統提供之控制項的相關資訊，所以 Microsoft Active Accessibility 會公開修改過的控制項，除非 superclass 或子類別化控制項與基底控制項截然不同。 為了判斷修改過的控制項是否可供存取，應用程式開發人員應該使用 [檢查](inspect-objects.md) 和 [可存取的事件](accessible-event-watcher.md) 監看員之類的公用程式，來比較修改過的控制項與基底控制項的行為。

如果您在使用這些公用程式之後判斷出修改過的控制項無法存取，您就必須將控制項視為任何其他自訂控制項。 控制項必須觸發事件，而應用程式的視窗程式必須提供 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面，讓用戶端應用程式用來取得控制項的相關資訊，以回應 [**WM \_ GETOBJECT**](wm-getobject.md)訊息。

## <a name="createstdaccessibleproxy-and-createstdaccessibleobject"></a>CreateStdAccessibleProxy 和 CreateStdAccessibleObject

如果已修改控制項的所有或大部分 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性與基底控制項相同，請使用 [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) 或 [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) 來簡化控制項 **IAccessible** 介面的執行。

> [!Note]  
> Superclassing 或子類別化可存取的控制項時，請注意 [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) 函式所抓取的物件可能只會執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。 它可能包含其他介面，例如 [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)。 您可能需要包裝這些額外的介面，以保留控制項原始實作所提供的協助工具支援。

 

[**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya)和 [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject)函式會為指定的系統控制項取出 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標。 這些函式的差異在於， **CreateStdAccessibleObject** 會使用從 *hwnd* 參數取得的視窗類別名稱，而 **CreateStdAccessibleProxy** 則會使用其 *szClassName* 參數中所指定的視窗類別名稱。 因此，如果您決定使用這些函式，請使用 **CreateStdAccessibleProxy** 來公開 superclass 控制項的相關資訊，並使用子類別化控制項來執行這兩項功能。

取得系統控制項的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標之後，請在 **IAccessible** 介面的執行中，針對修改過的控制項使用指標。 如果已修改控制項的屬性或方法與基底控制項相同，請使用 **IAccessible** 指標傳回基底控制項所提供的資訊。 如果已修改控制項的屬性與基底控制項不同，請覆寫基底控制項的屬性。

在下列範例中， **CAccCustomButton** 是衍生自 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)的應用程式定義類別。 成員變數 **m \_ PAccDefaultButton** 是 **IAccessible** 介面的指標，該介面是在控制項的初始化程式期間從 [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) 取得的。 在此範例中，自訂控制項的 **role** 屬性與系統控制項的 **role** 屬性相同，因此會傳回基底控制項的 **role** 屬性。 不過， **Description** 屬性與基底控制項的不同，因此會覆寫這個屬性。


```C++
HRESULT CAccCustomButton::Initialize( HWND hWnd, HINSTANCE hInst )
{
.
.
.
    hr = CreateStdAccessibleObject( m_hWnd, 
                                    OBJID_CLIENT, 
                                    IID_IAccessible, 
                                    (void **) &m__pAccDefaultButton );
.
.
.
}

STDMETHODIMP CAccCustomButton::get_accRole( VARIANT varID )
{
    return m_pAccDefaultButton->get_accRole(varID);
}


STDMETHODIMP CAccCustomButton::get_accDescription( VARIANT varChild,
                                                   BSTR* pszDesc )
{
    TCHAR   szString[256];
    OLECHAR wszString[256];

    LoadString( m_hInst, ID_DESCRIPTION, szString, 256 );
    MultiByteToWideChar( CP_ACP, 0, szString, -1, wszString, 256 );
   *pszDesc = SysAllocString( wszString );
   if ( !pszDesc )
       return S_OK;
   else
       return E_OUTOFMEMORY;
}
```



如需有關系統控制項的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法的詳細資訊，請參閱 [附錄 A：支援的消費者介面元素參考](appendix-a--supported-user-interface-elements-reference.md)。

 

 