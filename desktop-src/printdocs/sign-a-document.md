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
# <a name="sign-a-document"></a><span data-ttu-id="e34e3-103">簽署檔</span><span class="sxs-lookup"><span data-stu-id="e34e3-103">Sign a Document</span></span>

<span data-ttu-id="e34e3-104">本主題說明如何簽署 XPS 檔。</span><span class="sxs-lookup"><span data-stu-id="e34e3-104">This topic describes how to sign an XPS document.</span></span>

<span data-ttu-id="e34e3-105">在您的程式中使用下列程式碼範例之前，請閱讀 [一般數位簽章程式設計](basic-digital-signature-programming-tasks.md)工作中的免責聲明。</span><span class="sxs-lookup"><span data-stu-id="e34e3-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="e34e3-106">若要簽署 XPS 檔，請先將它載入到簽章管理員，如初始化簽章 [管理員](initialize-the-signature-manager.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="e34e3-106">To sign an XPS document, first load it into a signature manager as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>

<span data-ttu-id="e34e3-107">簽署已載入到簽章管理員的檔：</span><span class="sxs-lookup"><span data-stu-id="e34e3-107">To sign a document that has been loaded into a signature manager:</span></span>

1.  <span data-ttu-id="e34e3-108">具現化 [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) 介面。</span><span class="sxs-lookup"><span data-stu-id="e34e3-108">Instantiate an [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) interface.</span></span>
2.  <span data-ttu-id="e34e3-109">設定簽署原則。</span><span class="sxs-lookup"><span data-stu-id="e34e3-109">Set the signing policy.</span></span>
3.  <span data-ttu-id="e34e3-110">設定 signature 方法。</span><span class="sxs-lookup"><span data-stu-id="e34e3-110">Set the signature method.</span></span> <span data-ttu-id="e34e3-111">簽章方法 URI 字串常數定義于 cryptxml 中。</span><span class="sxs-lookup"><span data-stu-id="e34e3-111">Signature method URI string constants are defined in cryptxml.h.</span></span> <span data-ttu-id="e34e3-112">如需有效簽章方法值的詳細資訊，請參閱 [**IXpsSigningOptions：： SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)。</span><span class="sxs-lookup"><span data-stu-id="e34e3-112">For more information about valid signature method values, see [**IXpsSigningOptions::SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).</span></span>
4.  <span data-ttu-id="e34e3-113">設定摘要方法。</span><span class="sxs-lookup"><span data-stu-id="e34e3-113">Set the digest method.</span></span> <span data-ttu-id="e34e3-114">摘要方法 URI 字串常數定義于 cryptxml 中。</span><span class="sxs-lookup"><span data-stu-id="e34e3-114">Digest method URI string constants are defined in cryptxml.h.</span></span> <span data-ttu-id="e34e3-115">如需有效摘要方法值的詳細資訊，請參閱 [**IXpsSigningOptions：： SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)。</span><span class="sxs-lookup"><span data-stu-id="e34e3-115">For information about valid digest method values, see [**IXpsSigningOptions::SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).</span></span>
5.  <span data-ttu-id="e34e3-116">將憑證載入，如 [從檔案載入憑證](load-a-certificate-from-a-file.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="e34e3-116">Load the certificate as described in [Load a Certificate From a File](load-a-certificate-from-a-file.md).</span></span>
6.  <span data-ttu-id="e34e3-117">確認憑證支援簽章方法，如 [確認憑證支援](verify-a-certificate-supports-a-signature-method.md)簽章方法中所述。</span><span class="sxs-lookup"><span data-stu-id="e34e3-117">Verify that the certificate supports the signature method, as described in [Verify That a Certificate Supports a Signature Method](verify-a-certificate-supports-a-signature-method.md).</span></span>
7.  <span data-ttu-id="e34e3-118">確認系統支援摘要方法，如 [確認系統支援摘要方法](verify-a-certificate-supports-a-digest-method.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="e34e3-118">Verify that the digest method is supported by the system, as described in [Verify the System Supports a Digest Method](verify-a-certificate-supports-a-digest-method.md).</span></span>
8.  <span data-ttu-id="e34e3-119">如有必要，請在 XPS 檔中內嵌憑證信任鏈的憑證，如檔中的 [內嵌憑證鏈](embedding-certificate-trust-chains-in-a-document.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="e34e3-119">If required, embed the certificates of the certificate trust chain in the XPS document as described in [Embed Certificate Chains in a Document](embedding-certificate-trust-chains-in-a-document.md).</span></span>
9.  <span data-ttu-id="e34e3-120">簽署 XPS 檔。</span><span class="sxs-lookup"><span data-stu-id="e34e3-120">Sign the XPS document.</span></span>

<span data-ttu-id="e34e3-121">下列程式碼範例說明如何在程式中使用上述步驟。</span><span class="sxs-lookup"><span data-stu-id="e34e3-121">The following code example illustrates how to use the preceding steps in a program.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e34e3-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="e34e3-122">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e34e3-123">**後續步驟**</span><span class="sxs-lookup"><span data-stu-id="e34e3-123">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="e34e3-124">將簽名要求新增至 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="e34e3-124">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
</dt> <dt>

[<span data-ttu-id="e34e3-125">驗證檔簽章</span><span class="sxs-lookup"><span data-stu-id="e34e3-125">Verify Document Signatures</span></span>](verify-document-signatures.md)
</dt> <dt>

<span data-ttu-id="e34e3-126">**在本節中使用**</span><span class="sxs-lookup"><span data-stu-id="e34e3-126">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="e34e3-127">**CertFreeCertificateCoNtext**</span><span class="sxs-lookup"><span data-stu-id="e34e3-127">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[<span data-ttu-id="e34e3-128">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="e34e3-128">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="e34e3-129">**IXpsSignatureManager::CreateSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="e34e3-129">**IXpsSignatureManager::CreateSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions)
</dt> <dt>

[<span data-ttu-id="e34e3-130">**IXpsSignatureManager：： Sign**</span><span class="sxs-lookup"><span data-stu-id="e34e3-130">**IXpsSignatureManager::Sign**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign)
</dt> <dt>

[<span data-ttu-id="e34e3-131">**IXpsSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="e34e3-131">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

[<span data-ttu-id="e34e3-132">**IXpsSigningOptions::SetDigestMethod**</span><span class="sxs-lookup"><span data-stu-id="e34e3-132">**IXpsSigningOptions::SetDigestMethod**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
</dt> <dt>

[<span data-ttu-id="e34e3-133">**IXpsSigningOptions：： SetPolicy**</span><span class="sxs-lookup"><span data-stu-id="e34e3-133">**IXpsSigningOptions::SetPolicy**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy)
</dt> <dt>

[<span data-ttu-id="e34e3-134">**IXpsSigningOptions::SetSignatureMethod**</span><span class="sxs-lookup"><span data-stu-id="e34e3-134">**IXpsSigningOptions::SetSignatureMethod**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
</dt> <dt>

[<span data-ttu-id="e34e3-135">**XPS \_ 簽署 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="e34e3-135">**XPS\_SIGN\_POLICY**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

<span data-ttu-id="e34e3-136">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="e34e3-136">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="e34e3-137">密碼編譯 API</span><span class="sxs-lookup"><span data-stu-id="e34e3-137">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="e34e3-138">密碼編譯函式</span><span class="sxs-lookup"><span data-stu-id="e34e3-138">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="e34e3-139">從檔案載入憑證</span><span class="sxs-lookup"><span data-stu-id="e34e3-139">Load a Certificate From a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="e34e3-140">確認憑證支援簽章方法</span><span class="sxs-lookup"><span data-stu-id="e34e3-140">Verify a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="e34e3-141">確認系統支援摘要式方法</span><span class="sxs-lookup"><span data-stu-id="e34e3-141">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="e34e3-142">在檔中內嵌憑證鏈</span><span class="sxs-lookup"><span data-stu-id="e34e3-142">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[<span data-ttu-id="e34e3-143">XPS 數位簽章 API 錯誤</span><span class="sxs-lookup"><span data-stu-id="e34e3-143">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="e34e3-144">XPS 檔錯誤</span><span class="sxs-lookup"><span data-stu-id="e34e3-144">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="e34e3-145">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="e34e3-145">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
