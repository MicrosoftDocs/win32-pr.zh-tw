---
description: 設定認證管理員
ms.assetid: a20c2e6c-e9d9-438f-a57a-e3080587c11c
title: 設定認證管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3982d3f99cc0d3eb4aab2a0261f0e6b81cdc8a5abb408fc97834950b82b4206f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057942"
---
# <a name="setting-a-credential-manager"></a>設定認證管理員

提供網路來源認證的應用程式必須執行下列動作：

1.  執行公開 [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) 介面的認證管理員物件。
2.  建立網路來源之前，請先建立新的屬性存放區。
3.  在屬性存放區上設定 [**MFNETSOURCE \_ CREDENTIAL \_ MANAGER**](mfnetsource-credential-manager-property.md) 屬性。 屬性的值是 [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) 介面的指標。
4.  將指向屬性存放區的指標傳遞至來源解析程式，如設定 [媒體來源](configuring-a-media-source.md)中所述。

網路來源會使用認證管理員來取得使用者認證。 如果網路來源需要認證才能存取網路資源，則會呼叫應用程式的 [**IMFNetCredentialManager：： BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) 方法。 此呼叫會啟動非同步要求以取得使用者的認證。 **BeginGetCredentials** 方法可以從認證快取或使用者取得認證。 認證會儲存在 *credential 物件* 中。 當作業完成時，應用程式會叫用回呼介面來通知網路來源。 網路來源會呼叫 [**IMFNetCredentialManager：： EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) 來完成非同步作業。

由於這是非同步作業，因此應用程式必須在作業結束時分派回呼。 如需撰寫非同步方法的逐步指示，請參閱 [撰寫非同步方法](writing-an-asynchronous-method.md)。

下列範例顯示如何在網路來源上設定 [**MFNETSOURCE \_ CREDENTIAL \_ MANAGER**](mfnetsource-credential-manager-property.md) 屬性。


```C++
// Creates a media source from a URL.
//
// Demonstrates how to set a credential manager on the network source.

HRESULT CreateMediaSourceWithCredentialManager(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CCredentialManager *pCredentials = new (std::nothrow) CCredentialManager();

    if (pCredentials == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_CREDENTIAL_MANAGER;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pCredentials->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(key, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pCredentials);

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[網路來源驗證](network-source-authentication.md)
</dt> </dl>

 

 



