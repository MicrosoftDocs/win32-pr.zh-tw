---
title: 註冊自訂屬性、事件和控制項模式
description: 在可以使用自訂屬性、事件或控制項模式之前，提供者和用戶端都必須在執行時間註冊屬性、事件或控制項模式。
ms.assetid: ae36e404-8432-46ed-930e-b86dd5a88d6d
keywords:
- 消費者介面自動化，自訂屬性
- 消費者介面自動化，事件總覽
- 消費者介面自動化，控制項模式總覽
- 消費者介面自動化，註冊自訂屬性
- 消費者介面自動化，註冊事件
- 消費者介面自動化，註冊控制項模式
- 自訂屬性，註冊
- 事件，註冊
- 控制項模式，註冊
- 註冊，自訂屬性
- 註冊、事件
- 註冊、控制模式
- 控制項模式，自訂
- 控制項模式，執行自訂
- 執行自訂控制項模式
- 自訂控制項模式
- 用戶端包裝函式
- 模式處理常式
- 執行模式處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b157e8f08a2c0be74af6b9f53d3578d1e4d03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023916"
---
# <a name="register-custom-properties-events-and-control-patterns"></a>註冊自訂屬性、事件和控制項模式

在可以使用自訂屬性、事件或控制項模式之前，提供者和用戶端都必須在執行時間註冊屬性、事件或控制項模式。 註冊在應用程式程式中是全域有效的，而且在處理常式關閉或最後一個 Microsoft 消費者介面自動化元素物件 ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 或 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) 發行至進程之前，會保持有效。

Registation 牽涉到傳遞 GUID 給消費者介面自動化，以及有關自訂屬性、事件或控制項模式的詳細資訊。 第二次使用相同的資訊註冊相同的 GUID 將會成功，但嘗試以不同的資訊再次註冊相同的 GUID (例如，不同類型的自訂屬性) 將會失敗。 未來，如果自訂規格已接受並整合到消費者介面自動化 core 中，消費者介面自動化將會驗證自訂的註冊資訊，並使用已註冊的程式碼，而不是「官方」架構的執行，藉此將應用程式相容性問題降至最低。 您無法移除已註冊的屬性、事件或控制項模式。

本主題包含下列幾節：

-   [註冊自訂屬性和事件](#registering-custom-properties-and-events)
-   [執行自訂控制項模式](#implementing-custom-control-patterns)
    -   [用戶端包裝函式和模式處理常式](#the-client-wrapper-and-the-pattern-handler)
    -   [執行用戶端包裝函式](#implementing-the-client-wrapper)
    -   [執行模式處理常式](#implementing-the-pattern-handler)
    -   [註冊自訂控制項模式](#registering-a-custom-control-pattern)
    -   [自訂控制項模式的範例執行](#example-implementation-of-a-custom-control-pattern)
-   [相關主題](#related-topics)

## <a name="registering-custom-properties-and-events"></a>註冊自訂屬性和事件

註冊自訂屬性或事件，可讓提供者和用戶端取得屬性或事件的識別碼，然後將其傳遞給以識別碼做為參數的各種 API 方法。

若要註冊屬性或事件：

1.  定義自訂屬性或事件的 GUID。
2.  以屬性或事件的相關資訊填入 [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) 或 [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) 結構，包括 GUID 和包含自訂屬性或事件名稱的 nonlocalizable 字串。 自訂屬性也需要指定屬性的資料類型，例如屬性是否保留整數或字串。 資料類型必須是 [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) 列舉所指定的下列其中一種類型。 自訂屬性不支援其他資料類型。
    -   **UIAutomationType \_ Bool**
    -   **UIAutomationType \_ Double**
    -   **UIAutomationType \_ 元素**
    -   **UIAutomationType \_ Int**
    -   **UIAutomationType \_ 點**
    -   **UIAutomationType \_ 字串**
3.  使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數來建立 [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) 物件的實例，並取得物件之 [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) 介面的指標。
4.  呼叫 [**IUIAutomationRegistrar：： RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) 或 [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) 方法，並傳遞 [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) 結構或 [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) 結構的位址。

[**IUIAutomationRegistrar：： RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty)或 [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent)方法會傳回屬性識別碼或事件識別碼，應用程式可以傳遞給採用這類識別碼做為參數的任何消費者介面自動化方法。 例如，您可以將已註冊的屬性識別碼傳遞給 [**IUIAutomationElement：： GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) 方法或 [**IUIAutomation：： CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) 方法。

下列範例示範如何註冊自訂屬性。


```C++
// Declare a variable for holding the custom property ID.
PATTERNID g_MyCustomPropertyID;
// Define a GUID for the custom property.
GUID GUID_MyCustomProperty = { 0x82f383ff, 0x4b4d, 0x40d3, 
    { 0x8e, 0xd2, 0x90, 0xb5, 0x25, 0x8e, 0xaa, 0x19 } };

HRESULT RegisterProperty()
{
    // Fill the structure with the GUID, name, and data type.
    UIAutomationPropertyInfo MyCustomPropertyInfo = 
    {
        GUID_MyCustomProperty,
        L"MyCustomProp",
        UIAutomationType_String
    };

    // Create the registrar object and get the IUIAutomationRegistrar 
    // interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar = NULL;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    // Register the property and retrieve the property ID. 
    HRESULT hr = pUIARegistrar->RegisterProperty(&MyCustomPropertyInfo, &g_MyCustomPropertyID);
    pUIARegistrar->Release();

    return hr;
}
```



[**IUIAutomationRegistrar：： RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty)和 [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent)方法所抓取的屬性和事件識別碼，只在取得它們的應用程式內容中有效，而且只會在應用程式存留期間內有效。 當在相同的應用程式的不同執行時間實例上呼叫時，註冊方法可以針對相同的 GUID 傳回不同的整數值。

沒有任何方法可取消註冊自訂屬性或事件。 相反地，它們會在最後一個消費者介面自動化物件釋放時隱含地取消註冊。

> [!IMPORTANT]
> 如果您的程式碼是 Microsoft Active Accessibility (MSAA) 用戶端，則當您變更自訂屬性的值時，必須呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 函數。

 

## <a name="implementing-custom-control-patterns"></a>執行自訂控制項模式

自訂控制項模式不包含在消費者介面自動化 API 中，但會在執行時間由協力廠商提供。 用戶端和提供者應用程式的開發人員必須一起合作來定義自訂控制項模式，包括控制項模式將支援的方法、屬性和事件。 定義控制項模式之後，用戶端和提供者都必須將支援元件物件模型 (COM) 物件，以及在執行時間註冊控制項模式的程式碼。 自訂控制項模式需要執行兩個 COM 物件：用戶端包裝函式和模式處理常式。

> [!Note]  
> 下列主題中的範例將說明如何執行自訂控制項模式，以複製現有 [值](uiauto-implementingvalue.md) 控制項模式的功能。 這些範例僅供教學之用。 實際的自訂控制項模式應該提供標準消費者介面自動化控制項模式無法使用的功能。

 

### <a name="the-client-wrapper-and-the-pattern-handler"></a>用戶端包裝函式和模式處理常式

用戶端包裝函式會執行 API，用戶端會使用此 API 來取得屬性，並呼叫自訂控制項模式所公開的方法。 API 會實作為 COM 介面，此介面會將所有屬性要求和方法呼叫傳遞給消費者介面自動化 core，然後將要求和呼叫封送處理給提供者。

註冊自訂控制項模式的程式碼必須提供消費者介面自動化可以用來建立用戶端包裝函式物件實例的 class factory。 當自訂控制項模式成功註冊之後，消費者介面自動化會傳回 [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) 介面指標，用戶端會使用此指標將屬性要求和方法呼叫轉送至消費者介面自動化核心。

在提供者端，消費者介面自動化 core 會接受來自用戶端的屬性要求和方法呼叫，並將它們傳遞給模式處理常式物件。 然後，模式處理常式會針對自訂控制項模式，在提供者介面上呼叫適當的方法。

註冊自訂控制項模式的程式碼會建立模式處理常式物件，而且當註冊控制項模式時，會提供具有物件 [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) 介面指標的消費者介面自動化。

下圖顯示用戶端屬性要求或方法呼叫如何從用戶端包裝函式、透過消費者介面自動化核心元件流向模式處理常式，然後再到提供者介面。

![顯示從用戶端包裝函式流向模式處理常式和提供者之流程的圖表](images/custompatternsupport.jpg)

執行用戶端包裝函式和模式處理常式介面的物件必須是無限制執行緒。 此外，消費者介面自動化 core 必須能夠直接呼叫物件，而不需要任何中繼封送處理常式代碼。

### <a name="implementing-the-client-wrapper"></a>執行用戶端包裝函式

用戶端包裝函式是一個物件，此物件會公開用戶端用來要求屬性和呼叫自訂控制項模式所支援之方法的 IXxxPattern 介面。 介面是由每個支援的屬性所組成的一對 "getter" 方法 (get \_ CurrentXxx 和 get \_ CachedXxx 方法) ，以及每個支援的方法都有一個 "呼叫端" 方法。 當物件具現化時，物件的函式會收到 [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) 介面的指標，該介面是由消費者介面自動化 core 所執行。 IXxxPattern 介面的方法會使用 [**IUIAutomationPatternInstance：： GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) 和 [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) 方法，將屬性要求和方法呼叫轉送至消費者介面自動化核心。

下列範例顯示如何針對支援單一屬性的簡單自訂控制項模式，執行用戶端包裝函式物件。 如需更複雜的範例，請參閱 [自訂控制項模式的範例執行](#example-implementation-of-a-custom-control-pattern)。


```C++
// Define the client interface.
interface __declspec(uuid("c78b266d-b2c0-4e9d-863b-e3f74a721d47"))
IMyCustomPattern : public IUnknown
{
    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;
};

// Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IMyCustomPattern
{
    IUIAutomationPatternInstance * _pInstance;
    
public:
    // Get IUIAutomationPatternInstance interface pointer from the
    // UI Automation core.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
        : _pInstance(pInstance)
    {
        _pInstance->AddRef();
    }
    
    ~CMyValuePatternClientWrapper()
    {
        _pInstance->Release();
    }

    // Note: Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, FALSE, UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, TRUE, UIAutomationType_Bool, pIsReadOnly);
    }
};
```



### <a name="implementing-the-pattern-handler"></a>執行模式處理常式

模式處理常式是實 [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) 介面的物件。 這個介面有兩種方法： [**IUIAutomationPatternHandler：： CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) 和 [**分派**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch)。 消費者介面自動化 core 會呼叫 **CreateClientWrapper** 方法，並接收 [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) 介面的指標。 **CreateClientWrapper** 會透過具現化用戶端包裝函式物件，並將 **IUIAutomationPatternInstance** 介面指標傳遞至用戶端包裝函式，來回應。

消費者介面自動化 core 會使用 [**分派**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) 方法，將屬性要求和方法呼叫傳遞給自訂控制項模式的提供者介面。 參數包含提供者介面的指標、要呼叫之屬性 getter 或方法的以零為基底的索引，以及包含要傳遞給提供者之參數的 [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) 結構陣列。 模式處理常式會藉由檢查索引參數來判斷要呼叫的提供者方法來回應，然後呼叫該提供者介面，並傳遞包含在 **UIAutomationParameter** 結構中的參數。

在註冊控制項模式之前，會以註冊自訂控制項模式的相同程式碼來具現化模式處理常式物件。 在註冊時，程式碼必須將模式處理常式物件的 [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) 介面指標傳遞至消費者介面自動化 core。

下列範例示範如何針對支援單一屬性的簡單自訂控制項模式，執行模式處理常式物件。 如需更複雜的範例，請參閱 [自訂控制項模式的範例執行](#example-implementation-of-a-custom-control-pattern)。


```C++
// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
};            

// Index used by IUIAutomationPatternHandler::Dispatch.
const int MyValue_GetIsReadOnly = 0; 
            
// Define the pattern handler class.        
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:
    
    // Put standard IUnknown implementation here.

    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);
        }
        return E_INVALIDARG;
    }
};
```



### <a name="registering-a-custom-control-pattern"></a>註冊自訂控制項模式

在可以使用之前，自訂控制項模式必須由提供者和用戶端註冊。 註冊會提供消費者介面自動化核心與控制項模式的詳細資訊，並提供具有控制項模式識別碼的提供者或用戶端，以及控制項模式所支援之屬性和事件的識別碼。 在提供者端，必須先註冊自訂控制項模式，關聯的控制項才能處理 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息，或同時處理。

註冊自訂控制項模式時，提供者或用戶端會提供下列資訊：

-   自訂控制項模式的 GUID。
-   Nonlocalizable 字串，其中包含自訂控制項模式的名稱。
-   支援自訂控制項模式之提供者介面的 GUID。
-   支援自訂控制項模式之用戶端介面的 GUID。
-   [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo)結構的陣列，描述自訂控制項模式所支援的屬性。 您必須為每個屬性指定 GUID、屬性名稱和資料類型。
-   [**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo)結構的陣列，描述自訂控制項模式所支援的方法。 針對每個方法，結構會包含下列資訊：方法名稱、參數的計數、參數資料類型的清單，以及參數名稱的清單。
-   [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo)結構的陣列，描述自訂控制項模式所引發的事件。 針對每個事件，必須指定 GUID 和事件名稱。
-   將自訂控制項模式提供給用戶端的模式處理常式物件之 [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) 介面的位址。

若要註冊自訂控制項模式，提供者或用戶端程式代碼必須執行下列步驟：

1.  使用上述資訊填入 [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) 結構。
2.  使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數來建立 [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) 物件的實例，並取得物件之 [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) 介面的指標。
3.  呼叫 [**IUIAutomationRegistrar：： RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) 方法，並傳遞 [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) 結構的位址。

[**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern)方法會傳回控制項模式識別碼，以及屬性識別碼和事件識別碼的清單。 應用程式可以將這些識別碼傳遞給採用這類識別碼做為參數的任何消費者介面自動化方法。 例如，您可以將已註冊的模式識別碼傳遞至 [**IUIAutomationElement：： GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) 方法，以取得控制項模式的提供者介面指標。

沒有任何方法可取消註冊自訂控制項模式。 相反地，在釋放最後一個消費者介面自動化物件時，它會隱含地取消註冊。

如需示範如何註冊自訂控制項模式的範例，請參閱下一節。

### <a name="example-implementation-of-a-custom-control-pattern"></a>自訂控制項模式的範例執行

本章節包含範例程式碼，示範如何針對自訂控制項模式執行用戶端包裝函式和模式處理常式物件。 此範例會根據 [值](uiauto-implementingvalue.md) 控制項模式來執行自訂控制項模式。


```C++
// Step 1: Define the public provider and client interfaces using IDL. Interface 
// definitions are in C here to simplify the example.

// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_Value)(BSTR * pValue) = 0;
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Define the client interface.
interface __declspec(uuid("103b8323-b04a-4180-9140-8c1e437713a3"))
IUIAutomationMyValuePattern : public IUnknown
{
    STDMETHOD (get_CurrentValue)(BSTR * pValue) = 0;
    STDMETHOD (get_CachedValue)(BSTR * pValue) = 0;

    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;

    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Enumerate the properties and methods starting from 0, and placing the 
// properties first. 
enum
{
    MyValue_GetValue = 0,
    MyValue_GetIsReadOnly = 1,
    MyValue_SetValue = 2,
    MyValue_Reset = 3,
};

// Step 2: Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IUIAutomationMyValuePattern
{
    IUIAutomationPatternInstance * _pInstance;

public:
    // Get IUIAutomationPatternInstance interface pointer.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
    {
        _pInstance = pInstance;
        _pInstance->AddRef();
    }

    // Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, FALSE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CachedValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, TRUE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, FALSE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, TRUE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP SetValue(LPCWSTR pValue)
    {
        UIAutomationParameter SetValueParams[] = 
                { UIAutomationType_String, &pValue };
        return _pInstance->CallMethod(MyValue_SetValue,  SetValueParams, 
                ARRAYSIZE(SetValueParams));
    }

    STDMETHODIMP Reset()
    {
        return _pInstance->CallMethod(MyValue_Reset, NULL, 0);
    }
};

// Step 3: Implement the pattern handler class.
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:

    // Put standard IUnknown implementation here.
    
    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, 
            UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetValue:
            return ((IMyValueProvider*)pTarget)->get_Value((BSTR*)pParams[0].pData);

        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);

        case MyValue_SetValue:
            return ((IMyValueProvider*)pTarget)->SetValue(*(LPCWSTR*)pParams[0].pData);

        case MyValue_Reset:
            return ((IMyValueProvider*)pTarget)->Reset();
        }
        return E_INVALIDARG;
    }
};

CMyValuePatternHandler g_MyValuePatternHandler;

// Step 4: Declare information about the properties and methods supported
// by the custom control pattern.

// Define GUIDs for the custom control pattern and each of its properties 
// and events.
static const GUID MyValue_Pattern_Guid = { 0xa49aa3c0, 0xe413, 0x4ecf, 
        { 0xa1, 0xc3, 0x37, 0x42, 0xa7, 0x86, 0x67, 0x3f } };
static const GUID MyValue_Value_Property_Guid = { 0xe58f3f67, 0x22c7, 0x44f0, 
        { 0x83, 0x55, 0xd8, 0x76, 0x14, 0xa1, 0x10, 0x81 } };
static const GUID MyValue_IsReadOnly_Property_Guid = { 0x480540f2, 0x9829, 0x4acd, 
        { 0xb8, 0xea, 0x6e, 0x2a, 0xdc, 0xe5, 0x3a, 0xfb } };
static const GUID MyValue_Reset_Event_Guid = { 0x5b80edd3, 0x67f, 0x4a70, 
        { 0xb0, 0x7, 0x4, 0x12, 0x85, 0x11, 0x1, 0x7a } };

// Declare information about the properties, in the same order as the
// previously defined "MyValue_" enumerated type.
UIAutomationPropertyInfo g_MyValueProperties[] = 
{
    // GUID, name, data type.
    { MyValue_Value_Property_Guid, L"MyValuePattern.Value", 
                                                    UIAutomationType_String },
    { MyValue_IsReadOnly_Property_Guid, L"MyValuePattern.IsReadOnly", 
                                                    UIAutomationType_Bool },
};

// Declare information about the event.
UIAutomationEventInfo g_MyValueEvents [] =
{
    { MyValue_Reset_Event_Guid,  L"MyValuePattern.Reset" },
};

// Declare the data type and name of the SetValue method parameter. 
UIAutomationType g_SetValueParamTypes[] = { UIAutomationType_String };
LPCWSTR g_SetValueParamNames[] = {L"pNewValue"};

// Declare information about the methods.
UIAutomationMethodInfo g_MyValueMethods[] =
{
    // Name, focus flag, count of in parameters, count of out parameters, types, parameter names.
    { L"MyValuePattern.SetValue", TRUE, 1, 0, g_SetValueParamTypes, g_SetValueParamNames },
    { L"MyValuePattern.Reset", TRUE, 0, 0, NULL, NULL },
};

// Declare the custom control pattern using the previously defined information.
UIAutomationPatternInfo g_ValuePatternInfo =
{
    MyValue_Pattern_Guid,
    L"MyValuePattern",
    __uuidof(IMyValueProvider),
    __uuidof(IUIAutomationMyValuePattern),
    ARRAYSIZE(g_MyValueProperties), g_MyValueProperties, // properties
    ARRAYSIZE(g_MyValueMethods), g_MyValueMethods,       // methods
    ARRAYSIZE(g_MyValueEvents), g_MyValueEvents,         // events 
    &g_MyValuePatternHandler
};

// Step 5: Register the custom control pattern and retrieve the control pattern and property 
// identifiers.

// Control pattern, property, and event IDs.
PATTERNID  g_MyValue_PatternID;
PROPERTYID g_MyValue_Value_PropertyID;
PROPERTYID g_MyValue_IsReadOnly_PropertyID;
EVENTID    g_MyValueReset_EventID;

// ID used by the client to determine whether the custom control pattern is available.
PROPERTYID g_IsMyValuePatternAvailable_PropertyID;

HRESULT RegisterPattern()
{
    // Create the registrar object and get the IUIAutomationRegistrar interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    PROPERTYID propIDs[2]; // Array for property IDs.

    // Register the control pattern.
    HRESULT hr = pUIARegistrar->RegisterPattern(
        &g_ValuePatternInfo,
        &g_MyValue_PatternID,
        &g_IsMyValuePatternAvailable_PropertyID,
        ARRAYSIZE(propIDs), 
        propIDs,
        1,
        &g_MyValueReset_EventID);
            
    if (hr == S_OK)
    {
        // Copy the property IDs.
        g_MyValue_Value_PropertyID = propIDs[0];
        g_MyValue_IsReadOnly_PropertyID = propIDs[1];
    }

    pUIARegistrar->Release();
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[設計自訂屬性、事件和控制項模式](uiauto-designingcustompropseventpatterns.md)
</dt> <dt>

[UI 自動化屬性概觀](uiauto-propertiesoverview.md)
</dt> <dt>

[UI 自動化事件概觀](uiauto-eventsoverview.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 