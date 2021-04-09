---
description: 本主題說明如何簽署 XPS 檔。
ms.assetid: fbe64aed-6b07-49de-910c-18be68cb65a2
title: 簽署檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4ad07323a26d21f9010c3fd54c708880b90173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849105"
---
# <a name="sign-a-document"></a>簽署檔

本主題說明如何簽署 XPS 檔。

在您的程式中使用下列程式碼範例之前，請閱讀 [一般數位簽章程式設計](basic-digital-signature-programming-tasks.md)工作中的免責聲明。

若要簽署 XPS 檔，請先將它載入到簽章管理員，如初始化簽章 [管理員](initialize-the-signature-manager.md)中所述。

簽署已載入到簽章管理員的檔：

1.  具現化 [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) 介面。
2.  設定簽署原則。
3.  設定 signature 方法。 簽章方法 URI 字串常數定義于 cryptxml 中。 如需有效簽章方法值的詳細資訊，請參閱 [**IXpsSigningOptions：： SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)。
4.  設定摘要方法。 摘要方法 URI 字串常數定義于 cryptxml 中。 如需有效摘要方法值的詳細資訊，請參閱 [**IXpsSigningOptions：： SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)。
5.  將憑證載入，如 [從檔案載入憑證](load-a-certificate-from-a-file.md)中所述。
6.  確認憑證支援簽章方法，如 [確認憑證支援](verify-a-certificate-supports-a-signature-method.md)簽章方法中所述。
7.  確認系統支援摘要方法，如 [確認系統支援摘要方法](verify-a-certificate-supports-a-digest-method.md)中所述。
8.  如有必要，請在 XPS 檔中內嵌憑證信任鏈的憑證，如檔中的 [內嵌憑證鏈](embedding-certificate-trust-chains-in-a-document.md)中所述。
9.  簽署 XPS 檔。

下列程式碼範例說明如何在程式中使用上述步驟。


```C++
    // this example requires:
    //        cryptxml.h
    // and refers to local methods that are described
    // in other topics

    HRESULT                hr               = S_OK;
    BOOL                   supported        = FALSE;
    BOOL                   succeeded        = FALSE;
    IXpsSigningOptions     *signingOptions  = NULL;
    IXpsSignature          *signature       = NULL;
    PCCERT_CONTEXT         certificate      = NULL;
    
    // Instantiate an IXpsSigningOptions interface.
    hr = signatureManager->CreateSigningOptions (&signingOptions);
    
    if (SUCCEEDED(hr)) {
        // Set the signing policy to indicate the document parts 
        //  to sign.
        hr = signingOptions->SetPolicy (XPS_SIGN_POLICY_CORE_PROPERTIES);
    }

    if (SUCCEEDED(hr)) {
        // Set the digital signature method to use to generate the 
        //    signature hash value. 
        //
        // The signature method used in this example is 
        //    defined in cryptxml.h.
        hr = signingOptions->SetSignatureMethod (
            wszURI_XMLNS_DIGSIG_RSA_SHA1);
    }

    if (SUCCEEDED(hr)) {
        // Set the digest method to use.
        //
        // The digest method used in this example is 
        //    defined in cryptxml.h.
        hr = signingOptions->SetDigestMethod (wszURI_XMLNS_DIGSIG_SHA1);
    }

    if (SUCCEEDED(hr)) {
        // Load a certificate from a certificate file
        hr = LoadCertificateFromFile (signingCertificate, &certificate);
    }

    if (SUCCEEDED(hr)) {
        // Verify the certificate supports the digest method
        supported = SupportsDigestAlgorithm (
            wszURI_XMLNS_DIGSIG_SHA1);
        if (!supported) hr = E_FAIL;
    }

    if (SUCCEEDED(hr)) {
        // Verify the signature method is supported by the certificate
        //  and the system
        supported = SupportsSignatureAlgorithm(
            wszURI_XMLNS_DIGSIG_RSA_SHA1, certificate);
        if (!supported) hr = E_FAIL;
    }

    if (SUCCEEDED(hr)) {
        // Embed the certificate trust chain in the XPS package (optional).
        hr = EmbedCertificateChainInXpsPackage (signingOptions, certificate);
    }

    if (SUCCEEDED(hr)) {
        // Sign the XPS document
        hr = signatureManager->Sign (signingOptions, certificate, &signature);
    }

 //<Free the certificate context
    if (NULL != certificate) CertFreeCertificateContext (certificate);

    if (NULL != signingOptions) signingOptions->Release();
    if (NULL != signature) signature->Release();
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**後續步驟**
</dt> <dt>

[將簽名要求新增至 XPS 檔](add-a-signature-request-to-a-document.md)
</dt> <dt>

[驗證檔簽章](verify-document-signatures.md)
</dt> <dt>

**在本節中使用**
</dt> <dt>

[**CertFreeCertificateCoNtext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**IXpsSignatureManager::CreateSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions)
</dt> <dt>

[**IXpsSignatureManager：： Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign)
</dt> <dt>

[**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

[**IXpsSigningOptions::SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
</dt> <dt>

[**IXpsSigningOptions：： SetPolicy**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy)
</dt> <dt>

[**IXpsSigningOptions::SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
</dt> <dt>

[**XPS \_ 簽署 \_ 原則**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

**詳細資訊**
</dt> <dt>

[密碼編譯 API](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[密碼編譯函式](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[從檔案載入憑證](load-a-certificate-from-a-file.md)
</dt> <dt>

[確認憑證支援簽章方法](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[確認系統支援摘要式方法](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[在檔中內嵌憑證鏈](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[XPS 數位簽章 API 錯誤](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS 檔錯誤](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
