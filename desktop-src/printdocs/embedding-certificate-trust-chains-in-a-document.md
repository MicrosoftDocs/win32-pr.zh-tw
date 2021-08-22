---
description: 本主題說明如何將構成憑證鏈的憑證內嵌至 XPS 檔。
ms.assetid: c6aae8ff-2e1e-43de-9105-171e4187d193
title: 在檔中內嵌憑證鏈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23e47b4cd0d140d7200fb8aa01642ea5fbb731e49dcc289f596a054b0accbf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447578"
---
# <a name="embed-certificate-chains-in-a-document"></a>在檔中內嵌憑證鏈

本主題說明如何將構成憑證鏈的憑證內嵌至 XPS 檔。 憑證鏈包含憑證（根憑證除外）所需的所有憑證，以認證憑證所識別的主體。

若要將憑證鏈內嵌至 XPS 檔，請先建立憑證鏈，如下列程式碼範例所示。

程式碼範例中的 **CreateCertificateChain** 方法接受 *certificateStore* 做為參數，也就是 **HCERTSTORE** 值。 如果此值為 **Null**，則會從用戶端電腦的憑證伺服器中取出憑證。 如果此值是憑證存放區的控制碼，則會從 *certificateStore* 所參考的存放區，以及從用戶端電腦的憑證伺服器中取出憑證。


```C++
HRESULT 
CreateCertificateChain (
    __in PCCERT_CONTEXT            certificate,
    __in HCERTSTORE                certificateStore,
    __out PCCERT_CHAIN_CONTEXT* certificateChain
)
{
    HRESULT  hr = S_OK;

    CERT_CHAIN_PARA certificateChainParameters = {0};

    certificateChainParameters.cbSize = sizeof(CERT_CHAIN_PARA);
    certificateChainParameters.RequestedUsage.dwType = USAGE_MATCH_TYPE_AND;

    // CertGetCertificateChain builds a certificate chain that starts 
    //  from the PCCERT_CONTEXT structure provided by the caller.
    //  After the certificate chain has been successfully created, 
    //  then the authenticity of the certificate can be determined 
    //  by examining the errors, if any, that occurred while the chain
    //  was created.
    BOOL successCreatingCertChain = CertGetCertificateChain (
        NULL,
        certificate,
        NULL,
        certificateStore,
        &certificateChainParameters,
        CERT_CHAIN_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT,
        NULL,
        certificateChain);

    if (!successCreatingCertChain)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    return hr;
}
```



下列程式碼範例會從憑證建立憑證鏈，然後將這些憑證新增至 XPS 檔。 請注意， [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) 會建立憑證鏈，其中簽署憑證是第一個，而根憑證是最後一個。 在此範例中，不會新增簽署憑證和根憑證。 簽署憑證將會透過呼叫 [**IXpsSignatureManager：： Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) 方法來新增，這應該是在檔上呼叫的最後一個簽章方法。 簽署檔時，不會新增根憑證，因為當簽章經過驗證時，用戶端電腦的憑證伺服器必須提供根憑證。


```C++
HRESULT
EmbedCertificateChainInXpsPackage (
    __in IXpsSigningOptions *signingOptions,
    __in PCCERT_CONTEXT signingCertificate
)
{
    HRESULT                 hr                           = S_OK;
    PCCERT_CHAIN_CONTEXT    certificateChainContext      = NULL;
    IOpcCertificateSet      *certificateSetToUpdate      = NULL;
    DWORD                   certificateChainContextIndex = 0;

    // Create the entire certificate chain that originates 
    //  from the certificate that is used to sign the XPS document.
    hr = CreateCertificateChain(
        signingCertificate, 
        NULL, 
        &certificateChainContext);

    if (SUCCEEDED(hr))
    {
        // The signing options of an XPS document contain a pointer to 
        //  an IOpcCertificateSet interface that can be retrieved by 
        //  calling the GetCertificateSet method.
        hr = signingOptions->GetCertificateSet(&certificateSetToUpdate);
    }
    if (SUCCEEDED(hr))
    {
        // for each certificate chain context in this certificate...
        for (certificateChainContextIndex = 0; 
             certificateChainContextIndex < certificateChainContext->cChain; 
             certificateChainContextIndex++)
        {
            // inside a certificate chain context, 
            DWORD adjustedSimpleChainStartIndex = 0;
            DWORD adjustedSimpleChainEndIndex = 0;
            DWORD simpleCertChainIndex = 0;
            CERT_SIMPLE_CHAIN  *simpleCertificateChainWithinContext = NULL;

            // get the information about the certificate chain
            //  set the first item in the certificate chain to load
            //  Ignore the first PCCERT_CONTEXT in the first CERT_SIMPLE_CHAIN
            //  because this is the certificate that was used to build
            //  the chain and is already loaded in the document
            if (certificateChainContextIndex == 0)
            {
                adjustedSimpleChainStartIndex = 1;
            }
            else
            {
                adjustedSimpleChainStartIndex = 0;
            }
                    
            //  get the last item in the certificate chain
            simpleCertificateChainWithinContext = 
                certificateChainContext->rgpChain[certificateChainContextIndex];
            adjustedSimpleChainEndIndex = 
                simpleCertificateChainWithinContext->cElement;

            // Ignore the last PCCERT_CONTEXT in the last CERT_SIMPLE_CHAIN
            //  because this is the root certificate that must be retrieved
            //  from the client computer's certificate server.
            if (certificateChainContextIndex == certificateChainContext->cChain - 1)
            {
                if (adjustedSimpleChainEndIndex != 0)
                {
                    adjustedSimpleChainEndIndex = adjustedSimpleChainEndIndex - 1;
                }
            }

            // for each certificate chain in this context...
            for (simpleCertChainIndex = adjustedSimpleChainStartIndex; 
                 simpleCertChainIndex < adjustedSimpleChainEndIndex;
                 simpleCertChainIndex++)
            {
                // Add the certificate to the XPS document.
                PCCERT_CONTEXT certificateToEmbed = 
                    simpleCertificateChainWithinContext->rgpElement[simpleCertChainIndex]->pCertContext;
                if (FAILED(hr = certificateSetToUpdate->Add(certificateToEmbed)))
                {
                    break; // out of for loop with failed hr
                }
            }
        }
    }
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**後續步驟**
</dt> <dt>

[從檔案載入憑證](load-a-certificate-from-a-file.md)
</dt> <dt>

[確認憑證支援簽章方法](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[確認系統支援摘要式方法](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

**在此範例中使用**
</dt> <dt>

[**憑證 \_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[**CRYPT \_ OID \_ 資訊**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

[**IOpcCertificateSet**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset)
</dt> <dt>

[**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

**詳細資訊**
</dt> <dt>

[密碼編譯 API](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[密碼編譯函式](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[數位憑證](/windows/desktop/SecCrypto/digital-certificates)
</dt> <dt>

[憑證鏈](/windows/desktop/SecCrypto/certificate-chains)
</dt> <dt>

[憑證信任驗證](/windows/desktop/SecCrypto/certificate-trust-verification)
</dt> <dt>

[XPS 數位簽章 API 錯誤](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS 檔錯誤](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
