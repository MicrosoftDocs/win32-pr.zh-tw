---
title: 取得電腦憑證範例
description: 取得電腦憑證範例
ms.assetid: 4112e29e-7c86-4825-9798-dd1a81b82083
keywords:
- Windows媒體格式 SDK，電腦憑證
- Windows媒體格式 SDK，憑證
- Windows媒體格式 SDK，範例程式碼
- Windows媒體格式 SDK，程式碼範例
- 數位版權管理 (DRM) ，電腦憑證
- DRM (數位版權管理) ，電腦憑證
- 數位版權管理 (DRM) ，憑證
- DRM (數位版權管理) ，憑證
- 數位版權管理 (DRM) ，範例程式碼
- DRM (數位版權管理) ，範例程式碼
- 數位版權管理 (DRM) ，程式碼範例
- DRM (數位版權管理) ，程式碼範例
- DRM 用戶端擴充 Api，電腦憑證
- 用戶端擴充的 Api，電腦憑證
- DRM 用戶端擴充 Api，憑證
- 用戶端擴充 Api，憑證
- DRM 用戶端擴充 Api，範例程式碼
- 用戶端擴充 Api，範例程式碼
- DRM 用戶端擴充 Api，程式碼範例
- 用戶端擴充 Api，程式碼範例
- 憑證，程式碼範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 855479e90095f204a3ba7abafadcb4a31bbcaeaf7c592221ab0d5906cb1d8b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964007"
---
# <a name="get-machine-certificate-example"></a>取得電腦憑證範例

下列範例顯示如何取出電腦憑證集合：


```C++
HRESULT GetMachineCert( BYTE **ppbCert, DWORD *pcbCert )
{
    HRESULT hr = S_OK;
    IWMDRMProvider *pProvider = NULL;
    IWMDRMSecurity *pSecurity = NULL;
    BYTE rgbVersion[4];

    // Create a provider object.
    hr = WMDRMCreateProvider( &pProvider );
    if( FAILED( hr ) ) goto EXIT;

    // Create a security object from a provider object.
    hr = pProvider->CreateObject( IID_IWMDRMSecurity, (void**) &pSecurity );
    if( FAILED( hr ) ) goto EXIT;

    // Query the security to get the machine certificate.
    hr = pSecurity->GetMachineCertificate( WMDRM_CERTIFICATE_TYPE_V2,
        rgbVersion, ppbCert, pcbCert );

    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_RELEASE( pSecurity );
    SAFE_RELEASE( pProvider );

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DRM 匯入範例**](drm-import-examples.md)
</dt> </dl>

 

 




