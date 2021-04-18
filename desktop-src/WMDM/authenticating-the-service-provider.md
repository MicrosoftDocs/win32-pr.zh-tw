---
title: 驗證服務提供者
description: 驗證服務提供者
ms.assetid: e48a8a7c-0277-4f0c-bad2-5bc9d0286da8
keywords:
- Windows Media 裝置管理員，驗證
- 裝置管理員，驗證
- 程式設計指南，驗證
- 服務提供者，驗證
- 建立服務提供者，驗證
- 驗證 (authentication)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271bf5594e4adaede01bb8e3795780f8f5c5177a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106964983"
---
# <a name="authenticating-the-service-provider"></a>驗證服務提供者

若要從 Windows Media 裝置管理員存取，服務提供者必須繼承和執行 [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) 介面。

若要驗證本身，服務提供者會執行下列步驟：

1.  在具現化時，它會建立新的全域 [CSecureChannelServer](csecurechannelserver-class.md) 物件，並從其金鑰檔設定憑證和金鑰值。
2.  它會藉由直接將參數傳遞至其全域 CSecureChannelServer 成員，來實 [**IComponentAuthenticate：： SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) 和 [**IComponentAuthenticate：： SACGetProtocols**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) 方法。
3.  在處理任何已執行的 Windows Media 裝置管理員方法之前，服務提供者必須藉由呼叫 CSecureChannelServer：： fIsAuthenticated 來驗證呼叫端的驗證，如果呼叫端未通過驗證，則會失敗。

下列 c + + 範例會顯示這些步驟。

**建立 CSecureChannelServer 物件**


```C++
CMyServiceProvider::CMyServiceProvider()
{
    HRESULT hr = S_OK;

    // Create the persistent SAC object.
    g_pSAC = new CSecureChannelServer();

    // Set the SAC certificate.
    if (g_pSAC)
    {
        hr = g_pSAC->SetCertificate(
             SAC_CERT_V1,
            (BYTE*)abCert, sizeof(abCert), // SP's certificate.
            (BYTE*)abPVK, sizeof(abPVK)    // SP's key.
        );
    }   
    if (FAILED(hr)) return hr;

    //... Perform other class initialization here ...

    return hr;
}
```



**執行 IComponentAuthenticate 方法**


```C++
STDMETHODIMP CMDServiceProvider::SACAuth(
    DWORD   dwProtocolID,
    DWORD   dwPass,
    BYTE   *pbDataIn,
    DWORD   dwDataInLen,
    BYTE  **ppbDataOut,
    DWORD  *pdwDataOutLen)
{
    HRESULT hr = S_OK;

    // Verify that the global CSecureChannelServer member still exists.
    if (!g_pSAC)
        return E_FAIL;

    // Just pass the call to the global SAC member.
    hr = g_pSAC->SACAuth(
        dwProtocolID,
        dwPass,
        pbDataIn, dwDataInLen,
        ppbDataOut, pdwDataOutLen
    );
    return hr;
}

STDMETHODIMP CMDServiceProvider::SACGetProtocols(
    DWORD **ppdwProtocols,
    DWORD  *pdwProtocolCount)
{
    HRESULT hr = E_FAIL;

    if (!g_pSAC)
        return hr;

    hr = g_pSAC->SACGetProtocols(
        ppdwProtocols,
        pdwProtocolCount
    );
    return hr;
}
```



**驗證呼叫者的驗證**

下列程式碼範例顯示服務提供者在其 **IMDServiceProvider** 介面的實作為過程中檢查呼叫端的驗證。


```C++
STDMETHODIMP CMyServiceProvider::GetDeviceCount(DWORD * pdwCount)
{
    HRESULT hr = S_OK;
    if (!g_pSAC)
        return E_FAIL;

    if (!(g_pSAC->fIsAuthenticated()))
        return WMDM_E_NOTCERTIFIED;

    *pdwCount = m_DeviceCount;

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立服務提供者**](creating-a-service-provider.md)
</dt> </dl>

 

 




