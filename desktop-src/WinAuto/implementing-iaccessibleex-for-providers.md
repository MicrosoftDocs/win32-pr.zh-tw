---
title: 為提供者執行 IAccessibleEx
description: 本節說明如何藉由執行 IAccessibleEx 介面，將 Microsoft 消費者介面自動化提供者功能新增至 Microsoft Active Accessibility 伺服器。
ms.assetid: c03dc552-7919-4a35-8ff2-4cdd822bc0b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9460ccbd243aef390b7ade0deb41626173c927a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968701"
---
# <a name="implementing-iaccessibleex-for-providers"></a>為提供者執行 IAccessibleEx

本節說明如何藉由執行 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 介面，將 Microsoft 消費者介面自動化提供者功能新增至 Microsoft Active Accessibility 伺服器。

在執行 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)之前，請考慮下列需求：

-   基準 Microsoft Active Accessibility 可存取的物件階層必須是乾淨的。 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 無法修正現有可存取物件階層的問題。 在執行 **IAccessibleEx** 之前，必須先在 Microsoft Active Accessibility 的執行中更正任何物件模型結構的問題。
-   [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)的執行必須符合 Microsoft Active Accessibility 規格和消費者介面自動化規格。 您可以使用工具來驗證這兩個規格之下的合規性。 如需詳細資訊，請參閱 [測試控管](testing-tools.md) 和 [消費者介面自動化確認 (UIA 確認) 測試自動化架構](https://www.codeplex.com/UIAutomationVerify/)。

執行 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 需要下列主要步驟：

-   在可存取的物件上執行 **IServiceProvider** ，以便在這個或個別的物件上找到 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 介面。
-   在可存取的物件上執行 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 。
-   為任何 Microsoft Active Accessibility 子專案建立可存取的物件，而這些專案在 Microsoft Active Accessibility 是由父物件上的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面表示 (例如，) 清單專案。 在這些物件上執行 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 。
-   在所有可存取的物件上執行 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 。
-   在可存取的物件上，執行適當的控制項模式介面。

### <a name="implementing-the-iserviceprovider-interface"></a>執行 IServiceProvider 介面

由於控制項的 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 執行可能位於不同的物件中，因此用戶端應用程式無法依賴 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取得這個介面。 相反地，用戶端應該呼叫 **IServiceProvider：： QueryService**。 在這個方法的下列範例中，假設 **IAccessibleEx** 不是在另一個物件上執行;因此，此方法只會對 **QueryInterface** 呼叫。


```C++
           
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }
    *ppvObject = NULL;
    if (guidService == __uuidof(IAccessibleEx))
    {
        return QueryInterface(riid, ppvObject);
    }
    else 
    {
        return E_NOINTERFACE;
    }
};      
```



### <a name="implementing-the-iaccessibleex-interface"></a>執行 IAccessibleEx 介面

在 Microsoft Active Accessibility 中，一律會以 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面和子系識別碼來識別 UI 元素。 **IAccessible** 的單一實例可以代表多個 UI 元素。

由於每個 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 實例都只代表單一 UI 元素，因此每個 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 和子系識別碼組都必須對應至單一 **IAccessibleEx** 實例。 **IAccessibleEx** 包含兩種方法來處理此對應：

-   [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild)：抓取指定之子系的 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 介面。 如果 **IAccessibleEx** 執行無法辨識指定的子識別碼、沒有指定之子系的 **IAccessibleEx** ，或代表子專案，則這個方法會傳回 **Null** 。
-   [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair)：抓取 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)元素的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面和子識別碼。 若為不使用子系識別碼的 **IAccessible** 執行，這個方法會抓取對應的 **IAccessible** 物件，並 CHILDID \_ 本身。

下列範例顯示自訂清單視圖中專案的 [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) 和 [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) 方法的執行。 這些方法可讓消費者介面自動化將 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 和子系識別碼組對應至對應的 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 實例。


```C++
           
HRESULT CListboxAccessibleObject::GetObjectForChild(
    long idChild, IAccessibleEx **ppRetVal)
{ 
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;
    HRESULT hr = ValidateChildId(vChild);
    if (FAILED(hr))
    {
        return E_INVALIDARG;
    }
    // List item accessible objects are stored as an array of
    // pointers; for the purpose of this example it is assumed that 
    // the list contents will not change. Accessible objects are
    // created only when needed.
    if (itemProviders[idChild - 1] == NULL)
    {
        // Create an object that supports UI Automation and
        // IAccessibleEx for the item.
        itemProviders[idChild - 1] = 
          new CListItemAccessibleObject(idChild, 
          g_pListboxControl);
        if (itemProviders[idChild - 1] == NULL)
        {
            return E_OUTOFMEMORY;
        }
    }
    IAccessibleEx* pAccEx = static_cast<IAccessibleEx*>
      (itemProviders[idChild - 1]);
    if (pAccEx != NULL)
    {
      pAccEx->AddRef();
    }
    *ppRetVal = pAccEx;
    return S_OK; 
}

HRESULT CListItemAccessibleObject::GetIAccessiblePair(
    IAccessible **ppAcc, long *pidChild)
{ 
    if (ppAcc == NULL || pidChild == NULL)
    {
        return E_INVALIDARG;   
    }

                CListboxAccessibleObject* pParent = 
        m_control->GetAccessibleObject();

    HRESULT hr = pParent->QueryInterface( 
        __uuidof(IAccessible), (void**)ppAcc);
    if (FAILED(hr))
    {
        *pidChild = 0;
        return E_NOINTERFACE;
    }
    *pidChild = m_childID; 
    return S_OK; 
}
}
```



如果可存取的物件執行不使用子系識別碼，則仍可執行這些方法，如下列程式碼片段所示。


```C++
           

    // This sample implements IAccessibleEx on the same object; it could use a tear-off
    // or inner object instead.
    class MyAccessibleImpl: public IAccessible,
                        public IAccessibleEx,
                        public IRawElementProviderSimple
    {
    public:
    ...
   HRESULT STDMETHODCALLTYPE GetObjectForChild( long idChild, IAccessibleEx **ppRetVal )
    {
        // This implementation does not support child IDs.
        *ppRetVal = NULL;
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE GetIAccessiblePair( IAccessible ** ppAcc, long * pidChild )
    {
        // This implementation assumes that IAccessibleEx is implemented on same object as
        // IAccessible.
        *ppAcc = static_cast<IAccessible *>(this);
        (*ppAcc)->AddRef();
        *pidChild = CHILDID_SELF;
        return S_OK;
    }
```



### <a name="implement-the-irawelementprovidersimple-interface"></a>執行 IRawElementProviderSimple 介面

伺服器會使用 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 來公開消費者介面自動化屬性和控制項模式的相關資訊。 **IRawElementProviderSimple** 包含下列方法：

-   [**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)：這個方法是用來公開控制項模式介面。 它會傳回支援指定控制項模式的物件; 如果不支援控制項模式，則 **為 Null** 。
-   [**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue)：這個方法是用來公開消費者介面自動化屬性值。
-   [**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)：這個方法不適用於 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 的執行。
-   [**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions)：這個方法不適用於 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 的執行。

[**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)伺服器藉由執行 [**IRawElementProviderSimple：： GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)來公開控制項模式。 這個方法會採用指定控制項模式的整數參數。 如果不支援模式，伺服器會傳回 **Null** 。 如果支援控制項模式介面，伺服器會傳回 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ，然後用戶端會呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取得適當的控制項模式。

[**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)伺服器可以藉由實 [**IRawElementProviderSimple：： GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) ，並提供將屬性識別為參數的整數 PROPERTYID，來支援消費者介面自動化屬性 (例如 LabeledBy 和 IsRequiredForForm) 。 這項技術僅適用于不包含在控制項模式介面中的消費者介面自動化屬性。 與控制項模式介面相關聯的屬性會透過控制項模式介面方法來公開。 例如， [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式中的 IsSelected 屬性會使用 [**ISelectionItemProvider：： get \_ IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)來公開。

 

 