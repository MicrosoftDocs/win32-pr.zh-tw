---
title: 使用 MSAA 讓無視窗的 ActiveX 控制項可供存取
description: 說明如何使用 Microsoft Active Accessibility \ 32;API，以確保在) 用戶端應用程式上，輔助技術 (可以存取無視窗的 Microsoft ActiveX 控制項。
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- ActiveX 控制項，協助工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3a76aa72fadef502a6a4319284ab34fdd5214d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968106"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a>使用 MSAA 讓無視窗的 ActiveX 控制項可供存取

說明如何使用 Microsoft Active Accessibility API，以確保可在) 用戶端應用程式 (輔助技術時，可存取無視窗的 Microsoft ActiveX 控制項。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [ActiveX 控制項](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Microsoft Win32 和元件物件模型 (COM) 程式設計
-   無視窗的 ActiveX 控制項
-   Microsoft Active Accessibility 伺服器

## <a name="instructions"></a>指示

### <a name="step-1-implement-the-iaccessible-interface"></a>步驟1：執行 IAccessible 介面。

若要使無視窗的 ActiveX 控制項可供存取，您必須執行 Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面，就像您對以視窗為基礎的控制項一樣，除了下列步驟中所述。 如需有關執行 **IAccessible** 的詳細資訊，請參閱 [Active Accessibility 伺服器的開發人員指南](developer-s-guide-for-active-accessibility-servers.md)。

### <a name="step-2-implement-the-iserviceprovider-interface"></a>步驟2：執行 IServiceProvider 介面。

當用戶端要求有關無視窗控制項的協助工具資訊時，容器會呼叫您控制項的 [**IServiceProvider：： QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) 方法，以取得 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標。

此範例顯示如何執行 [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) 方法。


```C++
STDMETHODIMP CMyAccessibleMSAAControl::QueryService(REFGUID guidService, 
        REFIID riid, void **ppvObject)
{      
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL;  

    if (guidService == __uuidof(IAccessible))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a>步驟3：將 IAccessible：： get \_ accParent 方法呼叫委派給控制網站的 IAccessibleWindowlessSite：： GetParentAccessible 方法。

當用戶端要求無視窗控制項的父物件時，容器會呼叫您控制項的 [**IAccessible：： get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) 方法。 您的 **get \_ accParent** 實應委派給容器的 [**IAccessibleWindowlessSite：： GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) 方法。

此範例顯示如何執行 [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) 方法。


```C++
HRESULT CMyAccessibleMSAAControl::get_accParent(IDispatch **ppdispParent)  
{  
    if (ppdispParent == NULL)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_FALSE;  
    *ppdispParent = NULL;  

    IAccessibleWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        IAccessible *pParentAcc = NULL;
        if (SUCCEEDED(pWindowlessSite->GetParentAccessible(&pParentAcc)))
        {
            hr = pParentAcc->QueryInterface(IID_PPV_ARGS(ppdispParent));  
        }
    }  

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a>步驟4：取得物件識別碼的範圍，以指派給無視窗控制項中的事件來源。

就像以視窗為基礎的控制項一樣，無視窗的 ActiveX 控制項會呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 函式來通知用戶端有重要的事件。 函數參數包含引發事件之專案的物件識別碼。 無視窗控制項必須使用透過呼叫控制網站的 [**IAccessibleWindowlessSite：： AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) 方法取得的範圍中的值，來指派物件識別碼。

此範例顯示如何從控制項容器取得物件識別碼值的範圍。


```C++
IAccessibleWindowlessSite *pWindowlessSite = NULL;

if (SUCCEEDED(m_pClientSite->QueryInterface(
        IID_PPV_ARGS(&pWindowlessSite))))  
{  
    if (FAILED(pWindowlessSite->AcquireObjectIdRange(100, this, 
            &m_idObjectBase)))  
    {  
        m_idObjectBase = -1;  
    } 
}

SafeRelease(&pWindowlessSite);
```



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a>步驟5：執行 IAccessibleHandler 介面。

當無視窗控制項呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 函式時，控制項會指定引發事件之 UI 專案的物件識別碼，並將控制項容器指定為代表控制項回應 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息的視窗。

如果用戶端應用程式回應事件，控制項容器會收到 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息，其中包含引發事件之 UI 專案的物件識別碼。 控制項容器的回應方式是查詢「擁有」物件識別碼的無視窗控制項，然後呼叫該控制項的 [**IAccessibleHandler：： AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) 方法。 **AccessibleObjectFromID** 方法會傳回 UI 專案的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標，而控制項容器會將指標轉送至用戶端應用程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用消費者介面自動化使無視窗的 ActiveX 控制項可供存取](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[無視窗的 ActiveX 控制項協助工具](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 