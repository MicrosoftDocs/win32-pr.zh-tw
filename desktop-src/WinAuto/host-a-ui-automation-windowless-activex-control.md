---
title: 裝載消費者介面自動化無視窗的 ActiveX 控制項
description: 瞭解如何建立控制項容器，以裝載可執行 Microsoft 消費者介面自動化的無視窗 Microsoft ActiveX 控制項。
ms.assetid: A0F82968-F434-4F5E-8052-CF7CE65DB120
keywords:
- 消費者介面自動化，無視窗的 ActiveX 控制項
- 無視窗的 ActiveX 控制項，消費者介面自動化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77026d923ea6f0d2536cbd6a94966ec858443258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315289"
---
# <a name="host-a-ui-automation-windowless-activex-control"></a>裝載消費者介面自動化無視窗的 ActiveX 控制項

瞭解如何建立控制項容器，以裝載可執行 Microsoft 消費者介面自動化的無視窗 Microsoft ActiveX 控制項。 您可以使用此處所述的步驟，確保在) 用戶端應用程式 (的輔助技術可以存取您控制項容器中裝載的任何消費者介面自動化無視窗控制項。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [ActiveX 控制項](/windows/desktop/com/activex-controls)
-   [使用者介面自動化](entry-uiauto-win32.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Microsoft Win32 和元件物件模型 (COM) 程式設計
-   無視窗的 ActiveX 控制項
-   消費者介面自動化提供者

## <a name="instructions"></a>指示

### <a name="step-1-provide-the-irawelementprovidersimple-interface-on-behalf-of-the-windowless-control"></a>步驟1：代表無視窗控制項提供 IRawElementProviderSimple 介面。

只要系統需要無視窗控制項根目錄的 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 指標，系統就會查詢控制項容器。 為了取得指標，容器會呼叫無視窗控制項的 [**IServiceProvider：： QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) 方法的實作為。

如果控制項容器有消費者介面自動化的執行，則可以將無視窗控制項的 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 指標傳回系統。

如果控制項容器有 Microsoft Active Accessibility 的執行，請呼叫 [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) 函式來取得代表控制項的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標，然後將 **IAccessible** 介面指標傳回系統。

### <a name="step-2-implement-the-irawelementproviderwindowlesssite-interface"></a>步驟2：執行 IRawElementProviderWindowlessSite 介面。

控制項容器會執行 [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) 介面，以啟用以消費者介面自動化為基礎的無視窗控制項，以傳達其協助工具資訊。

1.  執行 [**IRawElementProviderWindowlessSite：： GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix)。

    無視窗的控制項片段必須為自己建立唯一的執行時間識別碼。 若要建立其執行時間識別碼，無視窗的控制項片段會藉由呼叫控制網站的 [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) 方法來抓取前置詞值，然後將相對於無視窗控制項中所有其他片段的唯一整數值附加至前置詞。

    無視窗控制項的控制網站應藉由形成包含常數 **UiaAppendRuntimeId** 的 **SAFEARRAY** ，後面接著網站唯一的整數值，來執行 [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix)方法。

    這個範例會示範如何傳回無視窗控制項的執行時間識別碼前置詞。

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetRuntimeIdPrefix(   
         SAFEARRAY **ppsaPrefix)   
    {   
        if (ppsaPrefix == NULL) 
        {
            return E_INVALIDARG;
        }

        // m_siteIndex is the index of the windowless control's
        // site. It is defined by the control container.
        int rId[] = { UiaAppendRuntimeId, m_siteIndex };
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);  
        if (psa == NULL)
        {
            return E_OUTOFMEMORY;
        }

        for (LONG i = 0; i < 2; i++)
        {
            SafeArrayPutElement(psa, &i, (void*)&(rId[i]));
        }

        *ppsaPrefix = psa;  
        return S_OK;  
    }  
    ```

    

2.  執行 [**IRawElementProviderWindowlessSite：： GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) 方法。

    實消費者介面自動化的控制項必須將指標傳回給控制項的父片段提供者。

    若要傳回片段的父系，執行 [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) 介面的物件必須能夠執行 [**流覽**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) 方法。 由於控制項可能無法在父物件的可存取樹狀結構中判斷其位置，因此對無視窗控制項而言，執行 **導覽** 很困難。 [**IRawElementProviderWindowlessSite：： GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment)方法可讓無視窗控制項查詢其網站中的相鄰片段，然後將該片段傳回給呼叫 **導覽** 的用戶端。

    此範例顯示控制項容器如何抓取無視窗控制項的父片段。

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetAdjacentFragment(
            enum NavigateDirection direction, IRawElementProviderFragment **ppFragment)   
    {
        if (ppFragment == NULL)
        {
            return E_INVALIDARG;
        }
        
        *ppFragment = NULL;
        HRESULT hr = S_OK;

        switch (direction)
        {
            case NavigateDirection_Parent:
                {  
                    IRawElementProviderSimple *pSimple = NULL;

                    // Call an application-defined function to retrieve the
                    // parent provider interface.
                    hr = GetParentProvider(&pSimple);  
                    if (SUCCEEDED(hr))  
                    {  
                        // Get the parent's IRawElementProviderFragment interface.
                        hr = pSimple->QueryInterface(IID_PPV_ARGS(ppFragment));  
                        pSimple->Release();  
                    } 
                }  
                break;  
      
            case NavigateDirection_FirstChild:
            case NavigateDirection_LastChild:
                hr = E_INVALIDARG;
                break;

            // Ignore NavigateDirection_NextSibling and NavigateDirection_PreviousSibling
            // because there are no adjacent fragments.
            default:  
                break;  
        }  
      
        return hr;  
    }   
    ```

    

### <a name="step-3-optional-implement-the-irawelementproviderhostingaccessibles-interface"></a>步驟3：選擇性：執行 IRawElementProviderHostingAccessibles 介面。

如果您的控制項容器有消費者介面自動化提供者實作為協助工具樹狀結構的根，其中包含支援 Microsoft Active Accessibility 的無視窗 ActiveX 控制項，則請執行 [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) 介面。 **IRawElementProviderHostingAccessibles** 介面具有單一方法 [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles)，可抓取您的控制項容器所裝載的所有 Microsoft Active Accessibility 型無視窗 ActiveX 控制項的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何裝載 MSAA 無視窗 ActiveX 控制項](host-an-msaa-windowless-activex-control.md)
</dt> <dt>

[無視窗的 ActiveX 控制項協助工具](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 