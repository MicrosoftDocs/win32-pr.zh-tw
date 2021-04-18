---
title: 支援雙重或分派介面
description: 就像分派介面一樣，所有的雙重介面都必須繼承自 IDispatch，以將其所有 IDispatch 函式委派 (GetIDsOfNames、Invoke、GetTypeInfo、GetTypeInfoCount) 回到 (ADSI) 的匯總工具 IDispatch。
ms.assetid: abd0fcfc-f45c-4022-af95-60615be0adcc
ms.tgt_platform: multiple
keywords:
- 支援雙重或分派介面 ADSI
- 延伸 ADSI、雙重或分派介面
- ADSI ADSI，範例程式碼 C/c + +，將 IDispatch 方法委派給匯總工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435a4552b364afbf909d04a759e3713ce69befab
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106968515"
---
# <a name="supporting-dual-or-dispatch-interfaces"></a>支援雙重或分派介面

就像分派介面一樣，所有的雙重介面都必須繼承自 [**idispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)，以將其所有 **IDispatch** 函式委派 ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames)、 [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)、 [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo)、 [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) 回到 (ADSI) 的匯總工具 **IDispatch** 。 為了委派，擴充物件應該查詢匯總工具的 **IDispatch** 、呼叫適當的匯總工具方法，然後在使用之後釋放指標。

如果延伸模組可以是獨立元件，請確認其已匯總。 如果是的話，請將分派函式重新路由傳送至該匯總工具的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ，否則您可以呼叫 **idispatch** 的內部執行，也可以呼叫 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)的執行。

下列程式碼範例示範如何將 [**idispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 呼叫重新路由傳送至匯總工具 **idispatch** 。 這個程式碼範例假設 **m \_ pOuterUnknown** 成員變數已初始化為匯總工具的 **IUnknown** 指標。


```C++
/////////////////////////////////////////////////// 
// Delegating IDispatch Methods to the aggregator
///////////////////////////////////////////////////
STDMETHODIMP MyExtension::GetTypeInfoCount(UINT* pctinfo)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetTypeInfoCount( pctinfo );
        pDisp->Release();
    }
    return hr;
}
 
 
STDMETHODIMP MyExtension::GetTypeInfo(UINT itinfo, LCID lcid, ITypeInfo** pptinfo)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetTypeInfo( itinfo, lcid, pptinfo );
        pDisp->Release();
    }
    
    return hr;
}
 
STDMETHODIMP MyExtension::GetIDsOfNames(REFIID riid, LPOLESTR* rgszNames, UINT cNames, LCID lcid, DISPID* rgdispid)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetIDsOfNames( riid, rgszNames, cNames, lcid, 
                 rgdispid);
        pDisp->Release();
    }
    
    return hr;
 
}
 
STDMETHODIMP MyExtension::Invoke(DISPID dispidMember, REFIID riid,
        LCID lcid, WORD wFlags, DISPPARAMS* pdispparams, VARIANT* 
                pvarResult, EXCEPINFO* pexcepinfo, UINT* puArgErr)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->Invoke( dispidMember, riid, lcid, wFlags, 
                 pdispparams, pvarResult, pexcepinfo, puArgErr);
        pDisp->Release();
    }
    
    return hr;
}
```



強烈建議延伸模組寫入器支援雙重介面，而不是其擴充物件中的分派介面。 雙重介面可讓用戶端擁有更快速的存取權，只要在用戶端中啟用 vtable 存取即可。 如需詳細資訊，請參閱 [ADSI 擴充模型中的晚期繫結與 Vtable 存取](late-binding-vs--vtable-access-in-the-adsi-extension-model.md)。 以目前的模型為基礎，執行雙重介面應該比執行分派介面更為困難。

 

 