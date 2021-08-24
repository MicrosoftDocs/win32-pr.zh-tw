---
description: 使用 ICertServerPolicy：： SetCertificateProperty 方法來設定憑證的主旨屬性。
ms.assetid: 93e4b05d-0230-4562-8052-4e118fd92057
title: 設定憑證屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe131190b10b431427162e628004d8b21053a099015a68184196b7218967222
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117974566"
---
# <a name="setting-certificate-properties"></a>設定憑證屬性

使用 [**ICertServerPolicy：： SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) 方法來設定憑證的主旨屬性。 主旨屬性是與憑證擁有者或要求憑證的個人相關的屬性。 如需主體屬性的清單，請參閱 [名稱屬性](name-properties.md)。

您也可以使用 [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) 方法來設定 NotBefore 和 NotAfter 憑證屬性。 如需 NotBefore 和 NotAfter 憑證屬性的說明，請參閱 [憑證屬性](certificate-properties.md)。

使用 [**ICertServerPolicy：： SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) 方法可將任何數量的延伸模組加入至憑證。 您可以使用延伸模組，將補充主體或使用方式資訊新增到憑證中。 如需詳細資訊，請參閱 [擴充處理常式](extension-handlers.md)。

下列範例會設定憑證的憑證屬性和延伸。 您可以在 [**ICertPolicy2：： verifyrequest 已**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest)的執行中呼叫 [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty)和 [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension)方法。 此範例不是完整的 **verifyrequest 已** 執行;此範例不會顯示驗證邏輯。


```C++
#include <windows.h>
#include <stdio.h>

STDMETHODIMP CCertPolicy::VerifyRequest(
             BSTR const strConfig,
             LONG Context,
             LONG bNewRequest,
             LONG Flags,
             LONG __RPC_FAR *pDisposition)
{
    HRESULT hr = S_OK;
    ICertServerPolicy *pServer = NULL;
    BSTR bstrPropName = NULL;
    VARIANT vPropValue;
    BSTR bstrExtName = NULL;
    VARIANT vExtValue;


    // Retrieve an ICertServerPolicy interface pointer.
    hr = CoCreateInstance( CLSID_CCertServerPolicy,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICertServerPolicy,
                           (void **) &pServer );
    if (FAILED( hr ))
    {
        printf("Failed CoCreateInstance for ICertServerPolicy "
            "- %x\n", hr );
        return hr;
    }

    // Set the context to which this request refers.
    hr = pServer->SetContext(Context);
    if (FAILED( hr ))
    {
        printf("Failed SetContext(%u) - %x\n", Context, hr );
        pServer->Release();
        return hr;
    }

    // Specify the subject property to set on the certificate.
    bstrPropName = SysAllocString(L"Subject.EMail");
    if ( NULL == bstrPropName )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for bstrPropName "
            "(no memory)\n" );
        pServer->Release();
        return hr;
    }

    VariantInit( &vPropValue );
    vPropValue.VT_BSTR;
    vPropValue.bstrVal = SysAllocString(L"someone@example.com");
    if ( NULL == vPropValue.bstrVal )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for vPropValue "
            "(no memory)\n" );
        SysFreeString(bstrPropName);
        pServer->Release();
        return hr;
    }

    // Set the subject property on the certificate.
    hr = pServer->SetCertificateProperty( bstrPropName,
                                          PROPTYPE_STRING,
                                          &vPropValue );
    SysFreeString(bstrPropName);
    VariantClear(&vPropValue);
    if (FAILED(hr))
    {
        printf("Failed SetCertificateProperty - %x\n", hr);
        pServer->Release();
        return hr;
    }

    // Specify the extension property to set on the certificate.
    bstrExtName = SysAllocString(L"2.29.38.4");
    if ( NULL == bstrExtName )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for bstrExtName "
            "(no memory)\n" );
        pServer->Release();
        return hr;
    }

    VariantInit( &vExtValue );
    vExtValue.VT_BSTR;
    vExtValue.bstrVal = SysAllocString
        (L"https://example.microsoft.com");
    if ( NULL == vExtValue.bstrVal )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for vExtValue (no memory)\n" );
        SysFreeString(bstrExtName);
        pServer->Release();
        return hr;
    }

    // Set the extension property on the certificate.
    hr = pServer->SetCertificateExtension( bstrExtName,
                                           PROPTYPE_STRING,
                                           EXTENSION_CRITICAL_FLAG,
                                           &vExtValue );
    SysFreeString(bstrExtName);
    VariantClear(&vExtValue);
    if (FAILED(hr))
    {
        printf("Failed SetCertificateExtension - %x\n", hr);
        pServer->Release();
        return hr;
    }

    pServer->Release();
    return(hr);

}
```



 

 



