---
title: 驗證應用程式
description: 驗證應用程式
ms.assetid: 011815fa-d55c-4abc-9ec8-55d754827342
keywords:
- Windows Media 裝置管理員，驗證
- 裝置管理員，驗證
- 程式設計指南，驗證
- 桌面應用程式，驗證
- 建立 Windows Media 裝置管理員應用程式，驗證
- 驗證 (authentication)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7779cdbb874278e6b62517cc2c1983dd2ce8fa1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967483"
---
# <a name="authenticating-the-application"></a>驗證應用程式

您的應用程式必須執行的第一個步驟是驗證。 驗證會驗證應用程式對 Windows Media 裝置管理員的身分識別。 驗證您的應用程式之後，您可以呼叫 **QueryInterface** 來取得根 [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) 介面，此介面可針對其他必要的介面進行查詢，而這些介面本身可以針對所有其他介面進行查詢。 在啟動時，驗證只需要進行一次。

若要驗證您的應用程式，請執行下列步驟：

1.  CoCreate)  (類別識別碼 MediaDevMgr 的 **MediaDevMgr** 物件，並要求 [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) 介面。
2.  建立 [CSecureChannelClient](csecurechannelclient-class.md) 物件來處理驗證。
3.  傳遞您的應用程式金鑰，並將憑證傳送至安全通道物件。 您可以使用下列範例程式碼中所示的虛擬金鑰/憑證來取得 SDK 函數的基本功能。 不過，若要取得完整的功能 (將檔案傳入和移出裝置) 很重要，您必須向 Microsoft 要求金鑰和憑證，如 [開發工具](tools-for-development.md)所述。
4.  將您在步驟1中建立的 **IComponentAuthenticate** 介面傳遞至安全通道物件。
5.  呼叫 [**CSecureChannelClient：：驗證**](/previous-versions/ms983906(v=msdn.10)) 以驗證您的應用程式。
6.  **IWMDeviceManager** 介面的查詢 **IComponentAuthenticate** 。

這些步驟會顯示在下列 c + + 程式碼中。


```C++
HRESULT CWMDMController::Authenticate()
{
    // Use a dummy key/certificate pair to allow basic functionality.
    // An authentic keypair is required for full SDK functionality.
    BYTE abPVK[] = {0x00};
    BYTE abCert[] = {0x00};
    HRESULT hr;
    CComPtr<IComponentAuthenticate> pAuth;

    // Create the WMDM object and acquire 
    // its authentication interface.
    hr = CoCreateInstance(
        __uuidof(MediaDevMgr),
        NULL,
        CLSCTX_INPROC_SERVER,
        __uuidof(IComponentAuthenticate),
        (void**)&pAuth);

    if (FAILED(hr)) return hr;

    // Create the secure channel client class needed to authenticate the application.
    // We'll use a global member variable to hold the secure channel client
    // in case we need to handle encryption, decryption, or MAC verification
    // during this session.
    m_pSAC = new CSecureChannelClient;
    if (m_pSAC == NULL) return E_FAIL;

    // Send the application's transfer certificate and the associated 
    // private key to the secure channel client.
    hr = m_pSAC->SetCertificate(
        SAC_CERT_V1,
        (BYTE *)abCert, sizeof(abCert),
        (BYTE *)abPVK,  sizeof(abPVK));
    if (FAILED(hr)) return hr;
            
    // Send the authentication interface we created to the secure channel 
    // client and authenticate the application with the V1 protocol.
    // (This is the only protocol currently supported.)
    m_pSAC->SetInterface(pAuth);
    hr = m_pSAC->Authenticate(SAC_PROTOCOL_V1);
    if (FAILED(hr)) return hr;

    // Authentication succeeded, so we can use WMDM.
    // Query for the root WMDM interface.
    hr = pAuth->QueryInterface( __uuidof(IWMDeviceManager), (void**)&m_IWMDMDeviceMgr);

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Windows Media 裝置管理員應用程式**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 