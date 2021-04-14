---
title: 從用戶端使用 IAccessibleEx
description: 本主題說明用戶端如何存取伺服器的 IAccessibleEx 執行，並使用它來取得 UI 元素的消費者介面自動化屬性和控制項模式。
ms.assetid: e057bbe8-5dd7-41fc-a5d5-bcf4c1c6433d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b14b935bd7ed432ea4d378034763635309213f
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "104383250"
---
# <a name="using-iaccessibleex-from-a-client"></a>從用戶端使用 IAccessibleEx

本主題說明用戶端如何存取伺服器的 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 執行，並使用它來取得 UI 元素的消費者介面自動化屬性和控制項模式。

本節中的程式和範例假設已經在同進程中的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 用戶端，以及現有的 Microsoft Active Accessibility 伺服器。 它們也假設用戶端已使用其中一種協助工具架構函數（例如 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)、 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)或 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)）取得 **IAccessible** 物件。

### <a name="obtaining-an-iaccessibleex-interface-from-the-iaccessible-interface"></a>從 IAccessible 介面取得 IAccessibleEx 介面

具有可存取物件之 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的用戶端可以使用它來取得對應的 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 介面，方法是遵循下列步驟：

-   在[](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))具有 IID [](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) \_ \_ Uuidof (IServiceProvider) 的原始 IAccessible 物件上呼叫 QueryInterface。
-   呼叫 **IServiceProvider：： QueryService** 來取得 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)。

### <a name="handling-the-child-id"></a>處理子系識別碼

用戶端必須針對具有 CHILDID 本身以外之子系識別碼的伺服器做好準備 \_ 。 從 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)取得 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)介面之後，用戶端必須呼叫 [**IAccessibleEx：： GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) ，如果子識別碼不是 CHILDID \_ 自我 (表示) 父物件。

下列範例示範如何取得特定 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)物件和子識別碼的 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 。


```C++
   
HRESULT GetIAccessibleExFromIAccessible(IAccessible * pAcc, long idChild, 
                                           IAccessibleEx ** ppaex)
{
    *ppaex = NULL;

    // First, get IServiceProvider from the IAccessible.
    IServiceProvider * pSp = NULL;
    HRESULT hr = pAcc->QueryInterface(IID_IServiceProvider, (void **) & pSp);
    if(FAILED(hr))
        return hr;
    if(pSp == NULL)
        return E_NOINTERFACE;

    // Next, get the IAccessibleEx for the parent object.
    IAccessibleEx * paex = NULL;
    hr = pSp->QueryService(__uuidof(IAccessibleEx), __uuidof(IAccessibleEx),
                                                                 (void **)&paex);
    pSp->Release();
    if(FAILED(hr))
        return hr;
    if(paex == NULL)
        return E_NOINTERFACE;

    // If this is for CHILDID_SELF, we're done. Otherwise, we have a child ID and 
    // can request the object for child.
    if(idChild == CHILDID_SELF)
    {
        *ppaex = paex;
        return S_OK;
    }
    else
    {
        // Get the IAccessibleEx for the specified child.
        IAccessibleEx * paexChild = NULL;
        hr = paex->GetObjectForChild(idChild, &paexChild);
        paex->Release();
        if(FAILED(hr))
            return hr;
        if(paexChild == NULL)
            return E_NOINTERFACE;
        *ppaex = paexChild;
        return S_OK;
    }
}
```



### <a name="obtaining-the-irawelementprovidersimple-interface"></a>取得 IRawElementProviderSimple 介面

如果用戶端有 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 介面，則可以使用 QueryInterface 來取得 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面，如下列範例所示。


```C++
HRESULT GetIRawElementProviderFromIAccessible(IAccessible * pAcc, long idChild,
                                                 IRawElementProviderSimple ** ppEl)
{
    * ppEl = NULL;

    // First, get the IAccessibleEx for the IAccessible and child ID pair.
    IAccessibleEx * paex;
    HRESULT hr = GetIAccessibleExFromIAccessible( pAcc, idChild, &paex );
    if(FAILED(hr))
        return hr;

    // Next, use QueryInterface.
    hr = paex->QueryInterface(__uuidof(IRawElementProviderSimple), (void **)ppEl);
    paex->Release();
    return hr;
}
```



### <a name="retrieving-control-patterns"></a>正在抓取控制項模式

如果用戶端具有 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面的存取權，它可以取出由提供者所執行的控制項模式介面，然後在這些介面上呼叫方法。 下列範例示範如何執行。


```C++
// Helper function to get a pattern interface from an IAccessible and child ID 
// pair. Gets the IAccessibleEx, then calls GetPatternObject and QueryInterface.
HRESULT GetPatternFromIAccessible(IAccessible * pAcc, long idChild,
                                     PATTERNID patternId, REFIID iid, void ** ppv)
{
    // First, get the IAccesibleEx for this IAccessible and child ID pair.
    IRawElementProviderSimple * pel;
    HRESULT hr = GetIRawElementProviderSimpleFromIAccessible(pAcc, idChild, &pel);
    if(FAILED(hr))
        return hr;
    if(pel == NULL)
        return E_NOINTERFACE;

    // Now get the pattern object.
    IUnknown * pPatternObject = NULL;
    hr = pel->GetPatternProvider(patternId, &pPatternObject);
    pel->Release();
    if(FAILED(hr))
        return hr;
    if(pPatternObject == NULL)
        return E_NOINTERFACE;

    // Finally, use QueryInterface to get the correct interface type.
    hr = pPatternObject->QueryInterface(iid, ppv);
    pPatternObject->Release();
    if(*ppv == NULL)
        return E_NOINTERFACE;
    return hr;
}

HRESULT CallInvokePatternMethod(IAccessible * pAcc, long idChild)
{
    IInvokeProvider * pPattern;
    HRESULT hr = GetPatternFromIAccessible(pAcc, varChild,
                                  UIA_InvokePatternId, __uuidof(IInvokeProvider),
                                  (void **)&pPattern);
    if(FAILED(hr))
        return hr;

    hr = pPattern->Invoke();
    pPattern->Release();
    return hr;
}
```



### <a name="retrieving-property-values"></a>正在抓取屬性值

如果用戶端可以存取 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)，則可以取出屬性值。 下列範例顯示如何取得 AutomationId 和 LabeledBy Microsoft 消費者介面自動化屬性的值。


```C++
#include <initguid.h>
#include <uiautomationcoreapi.h> // Includes the UI Automation property GUID definitions.
#include <uiautomationcoreids.h> // Includes definitions of pattern/property IDs.

// Assume we already have a IRawElementProviderSimple * pEl.

VARIANT varValue;

// Get AutomationId property:
varValue.vt = VT_EMPTY;
HRESULT hr = pEl->GetPropertyValue(UIA_AutomationIdPropertyId, &varValue);
if(SUCCEEDED(hr))
{
    if(varValue.vt == VT_BSTR)
    {
        // AutomationId is varValue.bstrVal.
    }
    VariantClear(&varValue);
}


// Get LabeledBy property:
varValue.vt = VT_EMPTY;
hr = pEl->GetPropertyValue(UIA_LabeledByPropertyId, &varValue);
if(SUCCEEDED(hr))
{
    if(varValue.vt == VT_UNKNOWN || varValue.punkVal != NULL)
    {
        // Use QueryInterface to get IRawElementProviderSimple.
        IRawElementProviderSimple * pElLabel = NULL;
        hr = varValue.punkVal->QueryInterface(__uuidof(IRawElementProviderSimple),
                                              (void**)& pElLabel);
        if (SUCCEEDED(hr))
        {
            if(pElLabel != NULL)
            {
            // Use the pElLabel pointer here.
            pElLabel ->Release();
            }
        }
    }
    VariantClear(&varValue);
}
```



上述範例適用于未與控制項模式相關聯的屬性。 若要存取控制項模式屬性，用戶端必須取得並使用控制項模式介面。

### <a name="retrieving-an-iaccessible-interface-from-an-irawelementprovidersimple-interface"></a>從 IRawElementProviderSimple 介面取出 IAccessible 介面

如果用戶端取得 UI 元素的 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面，用戶端可以使用該介面來取得專案的對應 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。 如果用戶端需要存取專案的 Microsoft Active Accessibility 屬性，這會很有用。

用戶端可以取得 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面做為屬性值 (例如，藉由呼叫 [**IRawElementProviderSimple：： GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) 與 UIA \_ LabeledByPropertyId) ，或做為方法所抓取的專案 (例如，藉由呼叫 [**ISelectionProvider：： GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) 來取出所選元素的 **IRawElementProviderSimple** 介面陣列) 。 取得 **IRawElementProviderSimple** 介面之後，用戶端就可以依照下列步驟，使用它來取得對應的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ：

-   嘗試使用 QueryInterface 來取得 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 介面。
-   如果 QueryInterface 失敗，請在原始取得屬性的 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)實例上呼叫 [**IAccessibleEx：： ConvertReturnedElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) 。
-   在新的 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)實例上呼叫 [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair)方法，以取得 [**IACCESSIBLE**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interfae 和子系識別碼。

下列程式碼片段示範如何從先前取得的 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)介面取得 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面。


```C++
// IRawElementProviderSimple * pVal - an element returned by a property or method
// from another IRawElementProviderSimple.

IAccessible * pAcc = NULL;
long idChild;

// First, try to use QueryInterface to get the IAccessibleEx interface.
IAccessibleEx * pAccEx;
HRESULT hr = pVal->QueryInterface(__uuidof(IAccessibleEx), (void**)&pAccEx);
if (SUCCEEDED(hr)
{
    if (!pAccEx)
    {
        // If QueryInterface fails, and the IRawElementProviderSimple was 
              // obtained as a property or return value from another 
              // IRawElementProviderSimple, pass it to the 
              // IAccessibleEx::ConvertReturnedValue method of the
        // originating element.

        pAccExOrig->ConvertReturnedElement(pVal, &pAccEx);
    }

    if (pAccEx)
    {
        // Call GetIAccessiblePair to get an IAccessible interface and 
              // child ID.
        pAccEx->GetIAccessiblePair(&pAcc, &idChild);
    }

    // Finally, use the IAccessible interface and child ID.
    if (pAcc)
    {
        // Use IAccessible methods to get further information about this UI
              // element, or pass it to existing code that works in terms of 
              // IAccessible.
        ...
    }
}    
```



 

 