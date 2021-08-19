---
title: 如何使用消費者介面自動化使無視窗 ActiveX 控制項可供存取
description: 說明如何使用 Microsoft 消費者介面自動化 \ 32;API，以確保可在) 用戶端應用程式 (的輔助技術可存取無視窗的 Microsoft ActiveX 控制項。
ms.assetid: D584E90D-6537-4F48-8553-0DCA061FAF2A
keywords:
- 無視窗的 ActiveX 控制項，協助工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ef56d5f3a06bbfa21502c791163f2251506a10fda7da9d07ee04941ad39de1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570358"
---
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a>如何使用消費者介面自動化使無視窗 ActiveX 控制項可供存取

說明如何使用 microsoft 消費者介面自動化 API，以確保您的無視窗 Microsoft ActiveX 控制項可供) 用戶端應用程式 (的輔助技術使用。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [ActiveX控制](/windows/desktop/com/activex-controls)
-   [使用者介面自動化](entry-uiauto-win32.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Microsoft Win32 和元件物件模型 (COM) 程式設計
-   無視窗的 ActiveX 控制項
-   消費者介面自動化提供者

## <a name="instructions"></a>指示

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a>步驟1：執行消費者介面自動化提供者介面。

若要讓您的應用程式可供存取，您必須為無視窗 ActiveX 控制項（包括 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)、 [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)、 [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)和 [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents)）執行消費者介面自動化提供者介面。 您應該執行這些介面，就像是針對以視窗為基礎的控制項一樣，除了下列步驟中所述。 如需有關執行 UIA 提供者介面的詳細資訊，請參閱 [消費者介面自動化提供者程式設計人員手冊](uiauto-providerportal.md)。

### <a name="step-2-implement-the-iserviceprovider-interface"></a>步驟2：執行 IServiceProvider 介面。

當用戶端需要無視窗控制項的協助工具資訊時，控制項容器會呼叫您控制項的 **IServiceProvider：： QueryService** 方法，以抓取控制項的 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面指標。

下列範例顯示如何執行 **QueryService** 方法。


```C++
STDMETHODIMP CMyAccessibleUIAControl::QueryService(REFGUID guidService,
        REFIID riid, void **ppvObject)
{  
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL; 
 
    if (guidService == __uuidof(IRawElementProviderSimple))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a>步驟3：執行 IRawElementProviderFragment：：流覽方法。

當您的無視窗控制項的 [**IRawElementProviderFragment：：導覽**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) 方法被呼叫，以流覽至無視窗控制項根提供者的父系或同級時，您的 **流覽** 方法應該會委派給控制項容器的 [**IRawElementProviderWindowlessSite：： GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) 方法。

下列範例示範如何執行 [**流覽**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) 方法。


```C++
STDMETHODIMP CMyAccessibleUIAControl::Navigate(NavigateDirection direction,
     IRawElementProviderFragment **ppRetVal) 
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  
    
    if (direction == NavigateDirection_Parent)  
    {  
        // Query the control container's windowless site 
        // for the parent.
         if (SUCCEEDED(m_pClientSite->QueryInterface(
                IID_PPV_ARGS(&pWindowlessSite))))  
        {  
            hr =  pWindowlessSite->GetAdjacentFragment(direction, ppRetVal);  
        }  
    }  

    else if (direction == NavigateDirection_FirstChild)  
    {  
        // GetFragmentForChild is an application-defined function that 
        // retrieves the first or last child fragment.
        hr =  GetFragmentForChild(FIRST, ppRetVal);  
    }  

    else if (direction == NavigateDirection_LastChild)  
    {  
        hr = GetFragmentForChild(LAST, ppRetVal);  
    }  

    SafeRelease(&pWindowlessSite);
    return S_OK;   
}
```



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a>步驟4：執行 IRawElementProviderFragment：： GetRuntimeId 方法。

當您的無視窗控制項收到其 [**IRawElementProviderFragment：： GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) 方法的呼叫時，控制項必須執行下列動作：

1.  藉由呼叫控制網站的 [**IRawElementProviderWindowlessSite：： GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) 方法，來取得執行時間識別碼首碼。
2.  將整數附加到執行時間識別碼前置詞，以建立控制項的唯一執行時間識別碼。
3.  將執行時間識別碼傳回給呼叫者。

下列範例顯示如何執行 [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) 方法。


```C++
STDMETHODIMP CMyAccessibleUIAControl::GetRuntimeId(SAFEARRAY **ppRetVal)  
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        // Create a safe array to hold runtime ID.
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 1, 3);  
        if (psa == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Retrieve the runtime ID prefix from the control container. The prefix
        // consists of UiaAppendRuntimeId followed by the windowless site ID.
        if (SUCCEEDED(hr))
        {    
            hr = pWindowlessSite->GetRuntimeIdPrefix(&psa);  
        } 

        if (SUCCEEDED(hr))
        {
        // Append this fragment's ID to the retrieved runtime ID prefix.
            long i = 2;
            hr = SafeArrayPutElement(psa, &i, (void*)&m_Id);        
        }

        if (SUCCEEDED(hr))
        {
            *ppRetVal = psa;  
        }
    }

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 MSAA 讓無視窗的 ActiveX 控制項可供存取](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[無視窗 ActiveX 控制項協助工具](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 