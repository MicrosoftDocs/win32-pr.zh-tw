---
description: 使用 ICertServerPolicy：： SetCertificateProperty 方法來設定憑證的主旨屬性。
ms.assetid: 93e4b05d-0230-4562-8052-4e118fd92057
title: 設定憑證屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33534792e65c95e24125968a61cf6ac1ad27039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973205"
---
# <a name="setting-certificate-properties"></a><span data-ttu-id="d1b88-103">設定憑證屬性</span><span class="sxs-lookup"><span data-stu-id="d1b88-103">Setting Certificate Properties</span></span>

<span data-ttu-id="d1b88-104">使用 [**ICertServerPolicy：： SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) 方法來設定憑證的主旨屬性。</span><span class="sxs-lookup"><span data-stu-id="d1b88-104">Use the [**ICertServerPolicy::SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) method to set the subject properties of a certificate.</span></span> <span data-ttu-id="d1b88-105">主旨屬性是與憑證擁有者或要求憑證的個人相關的屬性。</span><span class="sxs-lookup"><span data-stu-id="d1b88-105">Subject properties are properties related to the owner of the certificate or the individual who requested the certificate.</span></span> <span data-ttu-id="d1b88-106">如需主體屬性的清單，請參閱 [名稱屬性](name-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="d1b88-106">For a list of subject properties, see [Name Properties](name-properties.md).</span></span>

<span data-ttu-id="d1b88-107">您也可以使用 [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) 方法來設定 NotBefore 和 NotAfter 憑證屬性。</span><span class="sxs-lookup"><span data-stu-id="d1b88-107">You can also use the [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) method to set the NotBefore and NotAfter certificate properties.</span></span> <span data-ttu-id="d1b88-108">如需 NotBefore 和 NotAfter 憑證屬性的說明，請參閱 [憑證屬性](certificate-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="d1b88-108">For a description of the NotBefore and NotAfter certificate properties, see [Certificate Properties](certificate-properties.md).</span></span>

<span data-ttu-id="d1b88-109">使用 [**ICertServerPolicy：： SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) 方法可將任何數量的延伸模組加入至憑證。</span><span class="sxs-lookup"><span data-stu-id="d1b88-109">Use the [**ICertServerPolicy::SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) method to add any number of extensions to the certificate.</span></span> <span data-ttu-id="d1b88-110">您可以使用延伸模組，將補充主體或使用方式資訊新增到憑證中。</span><span class="sxs-lookup"><span data-stu-id="d1b88-110">You can use extensions to add supplemental subject or usage information to the certificate.</span></span> <span data-ttu-id="d1b88-111">如需詳細資訊，請參閱 [擴充處理常式](extension-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="d1b88-111">For more information, see [Extension Handlers](extension-handlers.md).</span></span>

<span data-ttu-id="d1b88-112">下列範例會設定憑證的憑證屬性和延伸。</span><span class="sxs-lookup"><span data-stu-id="d1b88-112">The following example sets a certificate property and extension on a certificate.</span></span> <span data-ttu-id="d1b88-113">您可以在 [**ICertPolicy2：： verifyrequest 已**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest)的執行中呼叫 [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty)和 [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension)方法。</span><span class="sxs-lookup"><span data-stu-id="d1b88-113">You call the [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) and [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) methods in your [**ICertPolicy2::VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest) implementation.</span></span> <span data-ttu-id="d1b88-114">此範例不是完整的 **verifyrequest 已** 執行;此範例不會顯示驗證邏輯。</span><span class="sxs-lookup"><span data-stu-id="d1b88-114">The example is not a complete **VerifyRequest** implementation; the example does not show verification logic.</span></span>


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



 

 



