---
description: 本主題說明如何將構成憑證鏈的憑證內嵌至 XPS 檔。
ms.assetid: c6aae8ff-2e1e-43de-9105-171e4187d193
title: 在檔中內嵌憑證鏈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee6476e0c187cf1a62915f0a3ab2b7949586baa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976871"
---
# <a name="embed-certificate-chains-in-a-document"></a><span data-ttu-id="8fc66-103">在檔中內嵌憑證鏈</span><span class="sxs-lookup"><span data-stu-id="8fc66-103">Embed Certificate Chains in a Document</span></span>

<span data-ttu-id="8fc66-104">本主題說明如何將構成憑證鏈的憑證內嵌至 XPS 檔。</span><span class="sxs-lookup"><span data-stu-id="8fc66-104">This topic describes how to embed the certificates that make up a certificate chain into an XPS document.</span></span> <span data-ttu-id="8fc66-105">憑證鏈包含憑證（根憑證除外）所需的所有憑證，以認證憑證所識別的主體。</span><span class="sxs-lookup"><span data-stu-id="8fc66-105">A certificate chain consists of all the certificates, except the root certificate, that are needed to certify the subject identified by the end certificate.</span></span>

<span data-ttu-id="8fc66-106">若要將憑證鏈內嵌至 XPS 檔，請先建立憑證鏈，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="8fc66-106">To embed a certificate chain into an XPS document, first create the certificate chain as illustrated in the following code example.</span></span>

<span data-ttu-id="8fc66-107">程式碼範例中的 **CreateCertificateChain** 方法接受 *certificateStore* 做為參數，也就是 **HCERTSTORE** 值。</span><span class="sxs-lookup"><span data-stu-id="8fc66-107">The **CreateCertificateChain** method in the code example accepts *certificateStore* as a parameter, which is an **HCERTSTORE** value.</span></span> <span data-ttu-id="8fc66-108">如果此值為 **Null**，則會從用戶端電腦的憑證伺服器中取出憑證。</span><span class="sxs-lookup"><span data-stu-id="8fc66-108">If this value is **NULL**, the certificates will be retrieved from the client computer's certificate server.</span></span> <span data-ttu-id="8fc66-109">如果此值是憑證存放區的控制碼，則會從 *certificateStore* 所參考的存放區，以及從用戶端電腦的憑證伺服器中取出憑證。</span><span class="sxs-lookup"><span data-stu-id="8fc66-109">If the value is the handle to a certificate store, the certificates will be retrieved from that store referenced by *certificateStore* as well as from the client computer's certificate server.</span></span>


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



<span data-ttu-id="8fc66-110">下列程式碼範例會從憑證建立憑證鏈，然後將這些憑證新增至 XPS 檔。</span><span class="sxs-lookup"><span data-stu-id="8fc66-110">The following code example creates a certificate chain from certificates and then adds these certificates to an XPS document.</span></span> <span data-ttu-id="8fc66-111">請注意， [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) 會建立憑證鏈，其中簽署憑證是第一個，而根憑證是最後一個。</span><span class="sxs-lookup"><span data-stu-id="8fc66-111">Note that [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) creates the certificate chain in which the signing certificate is first and the root certificate is last.</span></span> <span data-ttu-id="8fc66-112">在此範例中，不會新增簽署憑證和根憑證。</span><span class="sxs-lookup"><span data-stu-id="8fc66-112">The signing certificate and the root certificate are not added in this example.</span></span> <span data-ttu-id="8fc66-113">簽署憑證將會透過呼叫 [**IXpsSignatureManager：： Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) 方法來新增，這應該是在檔上呼叫的最後一個簽章方法。</span><span class="sxs-lookup"><span data-stu-id="8fc66-113">The signing certificates will be added with a call to the [**IXpsSignatureManager::Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) method, which should be the last signature method called on the document.</span></span> <span data-ttu-id="8fc66-114">簽署檔時，不會新增根憑證，因為當簽章經過驗證時，用戶端電腦的憑證伺服器必須提供根憑證。</span><span class="sxs-lookup"><span data-stu-id="8fc66-114">The root certificate is not added when the document is signed, because it must be provided by the client computer's certificate server when the signature is validated.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8fc66-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="8fc66-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8fc66-116">**後續步驟**</span><span class="sxs-lookup"><span data-stu-id="8fc66-116">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="8fc66-117">從檔案載入憑證</span><span class="sxs-lookup"><span data-stu-id="8fc66-117">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="8fc66-118">確認憑證支援簽章方法</span><span class="sxs-lookup"><span data-stu-id="8fc66-118">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="8fc66-119">確認系統支援摘要式方法</span><span class="sxs-lookup"><span data-stu-id="8fc66-119">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

<span data-ttu-id="8fc66-120">**在此範例中使用**</span><span class="sxs-lookup"><span data-stu-id="8fc66-120">**Used in This Example**</span></span>
</dt> <dt>

[<span data-ttu-id="8fc66-121">**憑證 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="8fc66-121">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="8fc66-122">**CertGetCertificateChain**</span><span class="sxs-lookup"><span data-stu-id="8fc66-122">**CertGetCertificateChain**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[<span data-ttu-id="8fc66-123">**CRYPT \_ OID \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="8fc66-123">**CRYPT\_OID\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

[<span data-ttu-id="8fc66-124">**IOpcCertificateSet**</span><span class="sxs-lookup"><span data-stu-id="8fc66-124">**IOpcCertificateSet**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset)
</dt> <dt>

[<span data-ttu-id="8fc66-125">**IXpsSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="8fc66-125">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

<span data-ttu-id="8fc66-126">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="8fc66-126">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="8fc66-127">密碼編譯 API</span><span class="sxs-lookup"><span data-stu-id="8fc66-127">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="8fc66-128">密碼編譯函式</span><span class="sxs-lookup"><span data-stu-id="8fc66-128">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="8fc66-129">數位憑證</span><span class="sxs-lookup"><span data-stu-id="8fc66-129">Digital Certificates</span></span>](/windows/desktop/SecCrypto/digital-certificates)
</dt> <dt>

[<span data-ttu-id="8fc66-130">憑證鏈</span><span class="sxs-lookup"><span data-stu-id="8fc66-130">Certificate Chains</span></span>](/windows/desktop/SecCrypto/certificate-chains)
</dt> <dt>

[<span data-ttu-id="8fc66-131">憑證信任驗證</span><span class="sxs-lookup"><span data-stu-id="8fc66-131">Certificate Trust Verification</span></span>](/windows/desktop/SecCrypto/certificate-trust-verification)
</dt> <dt>

[<span data-ttu-id="8fc66-132">XPS 數位簽章 API 錯誤</span><span class="sxs-lookup"><span data-stu-id="8fc66-132">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="8fc66-133">XPS 檔錯誤</span><span class="sxs-lookup"><span data-stu-id="8fc66-133">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="8fc66-134">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="8fc66-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
