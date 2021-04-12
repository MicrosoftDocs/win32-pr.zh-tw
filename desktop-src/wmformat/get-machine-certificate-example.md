---
title: 取得電腦憑證範例
description: 取得電腦憑證範例
ms.assetid: 4112e29e-7c86-4825-9798-dd1a81b82083
keywords:
- Windows Media Format SDK，電腦憑證
- Windows Media Format SDK，憑證
- Windows Media Format SDK，範例程式碼
- Windows Media Format SDK，程式碼範例
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
ms.openlocfilehash: 2e68a8ecbaf3e3c0ba8001a7a2094ab2b4a7e09a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372503"
---
# <a name="get-machine-certificate-example"></a><span data-ttu-id="6444b-124">取得電腦憑證範例</span><span class="sxs-lookup"><span data-stu-id="6444b-124">Get Machine Certificate Example</span></span>

<span data-ttu-id="6444b-125">下列範例顯示如何取出電腦憑證集合：</span><span class="sxs-lookup"><span data-stu-id="6444b-125">The following example shows how to retrieve the machine certificate collection:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6444b-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="6444b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6444b-127">**DRM 匯入範例**</span><span class="sxs-lookup"><span data-stu-id="6444b-127">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




