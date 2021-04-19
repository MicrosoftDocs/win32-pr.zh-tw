---
description: 本主題說明如何驗證 XPS 檔中的簽章，以及如何驗證與這些簽章相關的憑證。
ms.assetid: fd12abaf-dc0f-4db1-837d-c116627bcc7e
title: 驗證檔簽章和憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47dfee91437f7cc36e754e8c1f97fa89cd2387af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980641"
---
# <a name="verify-document-signatures-and-certificates"></a><span data-ttu-id="67d71-103">驗證檔簽章和憑證</span><span class="sxs-lookup"><span data-stu-id="67d71-103">Verify Document Signatures and Certificates</span></span>

<span data-ttu-id="67d71-104">本主題說明如何驗證 XPS 檔中的簽章，以及如何驗證與這些簽章相關的憑證。</span><span class="sxs-lookup"><span data-stu-id="67d71-104">This topic describes how to verify the signatures in an XPS document and how to verify the certificates that are related to those signatures.</span></span>

<span data-ttu-id="67d71-105">在您的程式中使用下列程式碼範例之前，請閱讀 [一般數位簽章程式設計](basic-digital-signature-programming-tasks.md)工作中的免責聲明。</span><span class="sxs-lookup"><span data-stu-id="67d71-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="67d71-106">下列程式碼範例會檢查 XPS 檔中所找到的數位簽章。</span><span class="sxs-lookup"><span data-stu-id="67d71-106">The following code example checks the digital signatures that are found in an XPS document.</span></span>

<span data-ttu-id="67d71-107">若要檢查 XPS 檔中的簽章，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="67d71-107">To check the signatures in an XPS document, perform the following steps:</span></span>

1.  <span data-ttu-id="67d71-108">將檔載入到簽章管理員，如初始化簽章 [管理員](initialize-the-signature-manager.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="67d71-108">Load the document into a signature manager, as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>
2.  <span data-ttu-id="67d71-109">從數位簽章管理員取得簽章的集合。</span><span class="sxs-lookup"><span data-stu-id="67d71-109">Get the collection of signatures from the digital signature manager.</span></span>
3.  <span data-ttu-id="67d71-110">取得集合中的簽章數目。</span><span class="sxs-lookup"><span data-stu-id="67d71-110">Get the number of signatures in the collection.</span></span>
4.  <span data-ttu-id="67d71-111">針對集合中的每個簽章，呼叫 [**驗證**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) 方法，如下面的程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="67d71-111">For each signature in the collection, call the [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) method as shown in the code example that follows.</span></span>


```C++
HRESULT
VerifyAllDigitalSignaturesAndAuthenticateCertificates(
    IXpsSignatureManager *signatureManager
)
{
    HRESULT                       hr                              = S_OK;
    IXpsSignature                 *signature                      = NULL;
    IXpsSignatureCollection       *signaturesInDocument           = NULL;
    UINT32                        numberOfSignaturesInDocument    = NULL;

    hr = signatureManager->GetSignatures(&signaturesInDocument);
    if (SUCCEEDED(hr)) {
        hr = signaturesInDocument->GetCount(&numberOfSignaturesInDocument);
    }

    if (SUCCEEDED(hr)) {
        // Check each signature in the XPS document that was opened in
        //  the signature manager.
        for (UINT32 index = 0; index < numberOfSignaturesInDocument; index++)
        {
            // Get the signature in the current index of the 
            //  IXpsSignatureCollection object
            hr = signaturesInDocument->GetAt(index, &signature);

            if (SUCCEEDED(hr)) {
                PCCERT_CONTEXT       signingCertificate = NULL;
                XPS_SIGNATURE_STATUS signatureStatus; 

                signatureStatus = XPS_SIGNATURE_STATUS_BROKEN;
                // Verify the signature and authenticate 
                //  its signing certificate
                hr = VerifySignatureAndCertificates (
                        signature,
                        &signingCertificate,
                        &signatureStatus);
                if (FAILED(hr)) {
                    // If a FACILITY_SECURITY error code is returned then 
                    //  the current certificate was not the 
                    //    signing certificate, so continue with 
                    //  the enumeration.
                    if (HRESULT_FACILITY(hr) != FACILITY_SECURITY)
                    {
                        // If the error was not a FACILITY_SECURITY error  
                        //  then exit and return the error
                        break; // out of for loop
                    }
                }
                // release pointers for next loop
                if (NULL != signature) {
                    signature->Release(); 
                    signature = NULL; 
                }
                if (NULL != signingCertificate) {
                    CertFreeCertificateContext (signingCertificate); 
                    signingCertificate = NULL;
                }
            }
        }
    }
    if (NULL != signaturesInDocument) signaturesInDocument->Release();
    
    return hr;
}
```



<span data-ttu-id="67d71-112">若要驗證數位簽章，請先確認簽署憑證所建立的簽章，然後驗證簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="67d71-112">To verify a digital signature, first verify the signature created by the signing certificate, then validate the signing certificate.</span></span> <span data-ttu-id="67d71-113">下列程式碼範例中所使用的驗證方法會將憑證快取在暫時憑證存放區中，而在此範例中，此範例稍後會加以呼叫。</span><span class="sxs-lookup"><span data-stu-id="67d71-113">The validation method used in the following code example caches the certificates in a temporary certificate store, which the Crypto API functions use when they are called later in this example.</span></span>

<span data-ttu-id="67d71-114">若要建立暫時的憑證存放區，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="67d71-114">To create a temporary certificate store, perform the following steps:</span></span>

1.  <span data-ttu-id="67d71-115">建立暫時的憑證存放區，以保存簽章所使用的憑證。</span><span class="sxs-lookup"><span data-stu-id="67d71-115">Create a temporary certificate store to hold the certificates used by the signature.</span></span>
2.  <span data-ttu-id="67d71-116">逐一查看簽章的憑證集，並將每個憑證載入暫存憑證存放區中。</span><span class="sxs-lookup"><span data-stu-id="67d71-116">Iterate through the signature's certificate set, and load each certificate into the temporary certificate store.</span></span>


```C++
HRESULT VerifySignatureAndCertificates (
    IXpsSignature           *signature,
    PCCERT_CONTEXT          *signingCertificate,
    XPS_SIGNATURE_STATUS    *signatureStatus
)
{
    HRESULT                         hr                        = S_OK;
    BOOL                            moreCertificates          = FALSE;
    IOpcCertificateEnumerator       *certificatesInSignature  = NULL;
    
    HCERTSTORE                      signatureCertificateStore = NULL;
    
    // Create a temporary certificate store.  
    signatureCertificateStore = CertOpenStore(
        CERT_STORE_PROV_MEMORY, 
        X509_ASN_ENCODING, 
        NULL, 
        0, 
        NULL);

    // Create a certificate enumerator to store the certificates 
    //  that are associated with the current signature.
    hr = signature->GetCertificateEnumerator(&certificatesInSignature);

    if (SUCCEEDED(hr))
    {
    // We need to call the MoveNext method to initialize the enumerator.
        hr = certificatesInSignature->MoveNext(&moreCertificates);
    }
    if (SUCCEEDED(hr))
    {
        // Iterate through the certificates in the signature, 
        //  and add each one to the temporary certificate store.  
        //  This temporary  certificate store simplifies 
        //  authentication of the signing certificate.
        while (moreCertificates)
        {
            PCCERT_CONTEXT certificate  = NULL;
            hr = certificatesInSignature->GetCurrent(&certificate);
            if (SUCCEEDED(hr))
            {
                // got the next certificate so
                // add the current certificate to the temporary certificate store.
                if (!CertAddCertificateContextToStore(signatureCertificateStore,
                    certificate,
                    CERT_STORE_ADD_REPLACE_EXISTING,
                    NULL))
                {
                    hr = E_FAIL;
                    // ERROR: could not add the certificate to the certificate store
                    break; // out of while loop
                }
                CertFreeCertificateContext (certificate);
            }
            else
            {
                // unable to get the certificate so skip
            }

            // move to next certificate in set
            if (FAILED(hr = certificatesInSignature->MoveNext(&moreCertificates)))
            {
                // ERROR: could not move to the next certificate in the enumerator
                break; // out of while loop
            }
            // moreCertificates == FALSE when the end of the set has been reached.
        }//End while
    }
    if (NULL != certificatesInSignature) certificatesInSignature->Release();

```



<span data-ttu-id="67d71-117">若要驗證用來簽署檔的數位簽章和憑證，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="67d71-117">To verify the digital signature and the certificate used to sign the document, perform the following steps:</span></span>

1.  <span data-ttu-id="67d71-118">逐一查看簽章所用的憑證來尋找簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="67d71-118">Find the signing certificate by iterating through the certificates that are used by the signature.</span></span>
2.  <span data-ttu-id="67d71-119">藉由針對憑證驗證簽章來測試憑證。</span><span class="sxs-lookup"><span data-stu-id="67d71-119">Test the certificate by verifying the signature against the certificate.</span></span> <span data-ttu-id="67d71-120">當 [**驗證**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify)方法傳回 xps 簽章狀態 **\_ \_ \_ 有效** 或 xps 簽章 **\_ \_ 狀態 \_ 可疑** 的 xps 簽章狀態，而且不會傳回 **設備 \_ 安全性** 錯誤時，就會找到簽署憑證。 [**\_ \_**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status)</span><span class="sxs-lookup"><span data-stu-id="67d71-120">The signing certificate is found when the [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) method returns an [**XPS\_SIGNATURE\_STATUS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status) of **XPS\_SIGNATURE\_STATUS\_VALID** or **XPS\_SIGNATURE\_STATUS\_QUESTIONABLE**, and does not return a **FACILITY\_SECURITY** error.</span></span>


```C++
    // Reset the enumerator
    hr = signature->GetCertificateEnumerator(&certificatesInSignature);
    if (SUCCEEDED (hr))
    {
        moreCertificates = FALSE;
        hr = certificatesInSignature->MoveNext(&moreCertificates);
    }
    if (SUCCEEDED(hr))
    {
        // Iterate through the certificates in the signature,
        //  and call the IXpsSignature.Verify() method
        //  on each certificate.  
        // A signature can include an entire certificate chain, and so 
        //  only one of the certificates found in this enumeration 
        //  is the certificate that was used to sign the package. 
        //  The signing certificate is the one to authenticate.  
        // To find the signing certificate,  iterate through 
        //  the certificates in the signature and select the certificate that 
        //  returns an XPS_SIGNATURE_STATUS of XPS_SIGNATURE_STATUS_VALID
        //  or XPS_SIGNATURE_STATUS_QUESTIONABLE and does not return a
        //  FACILITY_SECURITY error.
        XPS_SIGNATURE_STATUS localSignatureStatus;
        localSignatureStatus = XPS_SIGNATURE_STATUS_INCOMPLIANT;
        do
        {
            PCCERT_CONTEXT certificate = NULL;
            DWORD certificateStatus = NULL;

            if (FAILED(hr = certificatesInSignature->GetCurrent(&certificate)))
            {
                // We will skip corrupted certificates
                // free this one and move to the next
                CertFreeCertificateContext (certificate);
                hr = certificatesInSignature->MoveNext(&moreCertificates);
                if (FAILED(hr))
                {
                    // ERROR: could not move to the next 
                    //  certificate in the enumerator
                    break; // out of do loop with failed hr
                }
                // continue with next loop iteration
                continue;
            }
            
            // Verify that the signature conforms to the XPS signing policy.
            hr = signature->Verify(certificate, &localSignatureStatus);
            if (FAILED(hr))
            {
                // If a FACILITY_SECURITY error code is returned, then the
                //  current certificate was not the signing certificate,
                //  so continue to the next certificate.
                if (HRESULT_FACILITY(hr) == FACILITY_SECURITY)
                {
                    // free this one and move to the next
                    CertFreeCertificateContext (certificate);
                    hr = certificatesInSignature->MoveNext(&moreCertificates);
                    if (FAILED(hr))
                    {
                        // ERROR: could not move to the next certificate 
                        //  in the enumerator
                        break; // out of do loop with failed hr
                    }
                    continue;
                }
                // ERROR: An attempt to verify the signature has failed
                break; // out of do loop with failed hr
            }
            // if verification was successful, localSignatureStatus will
            //  contain the status of the signature.
            //
            // do loop continues in next code example
```



<span data-ttu-id="67d71-121">找到簽署憑證後，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="67d71-121">When the signing certificate has been found, perform the following steps:</span></span>

1.  <span data-ttu-id="67d71-122">儲存傳回的簽章狀態。</span><span class="sxs-lookup"><span data-stu-id="67d71-122">Save the returned signature status.</span></span>
2.  <span data-ttu-id="67d71-123">如有必要，請更新本機狀態，以執行後續的憑證測試：</span><span class="sxs-lookup"><span data-stu-id="67d71-123">Update the local status, if necessary, to perform subsequent certificate tests:</span></span>
    1.  <span data-ttu-id="67d71-124">如果簽章狀態為 [成功]，請將本機狀態設定為 [可疑]，以便測試憑證。</span><span class="sxs-lookup"><span data-stu-id="67d71-124">If the signature status is successful, set the local status to questionable in order to test the certificates.</span></span>
    2.  <span data-ttu-id="67d71-125">如果簽章狀態為 incompliant，請將本機狀態保持為 incompliant。</span><span class="sxs-lookup"><span data-stu-id="67d71-125">If the signature status is incompliant, leave the local status as incompliant.</span></span>
    3.  <span data-ttu-id="67d71-126">如果簽章狀態已中斷或不完整，請將本機狀態設定為 [已中斷]。</span><span class="sxs-lookup"><span data-stu-id="67d71-126">If the signature status is broken or incomplete, set the local status to broken.</span></span>

<span data-ttu-id="67d71-127">「Xps 簽章 **\_ \_ 狀態 \_ INCOMPLIANT** 的「簽章狀態」表示未簽署的 xps 檔元件已簽署，或尚未簽署的 xps 檔部分。</span><span class="sxs-lookup"><span data-stu-id="67d71-127">A signature status of **XPS\_SIGNATURE\_STATUS\_INCOMPLIANT** means that parts of the XPS document that should not have been signed were signed, or parts of the XPS document that should have been signed were not.</span></span> <span data-ttu-id="67d71-128">如果 [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) 傳回這個簽章狀態，則不需要進一步檢查簽章。</span><span class="sxs-lookup"><span data-stu-id="67d71-128">If [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) returns this signature status, further checking of the signature will be unnecessary.</span></span>


```C++
            // continuing do loop from previous code example
            *signingCertificate = certificate;
            *signatureStatus = localSignatureStatus;
            
            // note that this test should only downgrade the 
            // signature status, it should not upgrade it.
            switch (localSignatureStatus) {
                case XPS_SIGNATURE_STATUS_VALID:
                case XPS_SIGNATURE_STATUS_QUESTIONABLE:
                    // the signature is valid or questionable so
                    // save the actual status and set the new status
                    // to questionable so the certificates will be checked.
                    localSignatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    break;

                case XPS_SIGNATURE_STATUS_INCOMPLIANT:
                    // the signature is not compliant 
                    break;

                case XPS_SIGNATURE_STATUS_INCOMPLETE:
                case XPS_SIGNATURE_STATUS_BROKEN:
                    // The Windows 7 XPS viewer displays incomplete signatures
                    // and broken signatures as broken.
                    *signatureStatus = XPS_SIGNATURE_STATUS_BROKEN;
                    localSignatureStatus = XPS_SIGNATURE_STATUS_BROKEN;
                    break;

                default:
                    // there should be no other possible status values
                    break;
            }
            // do loop continues in next code example
```



<span data-ttu-id="67d71-129">若要在簽章狀態有效或有疑問時確認憑證信任，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="67d71-129">To verify the certificate trust if the signature status was valid or questionable, perform the following steps:</span></span>

1.  <span data-ttu-id="67d71-130">取得憑證信任狀態。</span><span class="sxs-lookup"><span data-stu-id="67d71-130">Get the certificate trust status.</span></span>
2.  <span data-ttu-id="67d71-131">評估傳回的憑證信任狀態。</span><span class="sxs-lookup"><span data-stu-id="67d71-131">Evaluate the returned certificate trust status.</span></span>
3.  <span data-ttu-id="67d71-132">傳回產生的狀態。</span><span class="sxs-lookup"><span data-stu-id="67d71-132">Return the resulting status.</span></span>

<span data-ttu-id="67d71-133">下一個程式碼範例不會測試每個可能的憑證信任狀態。</span><span class="sxs-lookup"><span data-stu-id="67d71-133">The next code example does not test for every possible certificate trust status.</span></span> <span data-ttu-id="67d71-134">如需可傳回狀態值的其他詳細資料，請參閱憑證 [**\_ 信任 \_ 狀態**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status)。</span><span class="sxs-lookup"><span data-stu-id="67d71-134">For additional details on the status values that can be returned, see [**CERT\_TRUST\_STATUS**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status).</span></span>


```C++
            // continuing do loop from previous code example
            //
            // at this point, localSignatureStatus should be less than or 
            // equal to what it was before the test.

            // Check the certificate to see if it is valid
            if ((localSignatureStatus == XPS_SIGNATURE_STATUS_VALID) || 
                (localSignatureStatus == XPS_SIGNATURE_STATUS_QUESTIONABLE))
            {
                // This call builds the certificate trust chain from the 
                //  supplied certificate.  The certificate chain is used to
                //  authenticate the supplied certificate.
                hr = GetCertificateTrustStatus (
                    *signingCertificate, 
                    &signatureCertificateStore,
                    &certificateStatus);
                if (FAILED(hr))
                {
                    // ERROR: An attempt to authenticate the certificate 
                    //  has failed
                    break; // out of do loop with failed hr
                }

                // The Crypt API returns a status that can contain more than
                //  one status value.
                // statusFlagMask is set to test all bits except for the
                //  CERT_TRUST_REVOCATION_STATUS_UNKNOWN
                //  CERT_TRUST_IS_OFFLINE_REVOCATION
                //  CERT_TRUST_IS_NOT_TIME_VALID
                //  values because, for this test, these are not considered
                //  to be error conditions.
                DWORD statusFlagMask = ~(
                    CERT_TRUST_REVOCATION_STATUS_UNKNOWN | 
                    CERT_TRUST_IS_OFFLINE_REVOCATION | 
                    CERT_TRUST_IS_NOT_TIME_VALID);

                if (CERT_TRUST_NO_ERROR == (certificateStatus & statusFlagMask))
                {
                    // If *signatureStatus is already 
                    //    XPS_SIGNATURE_STATUS_VALID then there is no need to 
                    //    change the status as the certificate status has no 
                    //    certificate trust errors.
                    // If *signatureStatus is already 
                    //  XPS_SIGNATURE_STATUS_QUESTIONABLE then we will not
                    //  upgrade the trust status of the signature just 
                    //  because there is no trust issue with the certificate.
                }
                else
                {
                    // If trust errors were detected with the certificate, 
                    //  then this XPS signature is given a status of 
                    //  XPS_SIGNATURE_STATUS_QUESTIONABLE
                    *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                }

                // Handle additional certificate errors.  
                //  This is not an exhaustive list of possible errors.

                if (certificateStatus & CERT_TRUST_IS_NOT_TIME_VALID)
                {
                    // The XPS Viewer considers signatures with 
                    //  expired certificates as valid.
                }
                if (certificateStatus & CERT_TRUST_IS_PARTIAL_CHAIN)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }

                if (certificateStatus & CERT_TRUST_IS_NOT_SIGNATURE_VALID)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }

                if (certificateStatus & CERT_TRUST_IS_SELF_SIGNED)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }
                
                if (certificateStatus & CERT_TRUST_IS_UNTRUSTED_ROOT)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }
            }//End if

            hr = certificatesInSignature->MoveNext(&moreCertificates);
            if (FAILED(hr))
            {
                // ERROR: could not move to the next 
                //  certificate in the enumerator
                break; // out of do loop with failed hr
            }
        } while((*signatureStatus != XPS_SIGNATURE_STATUS_VALID) && 
                    moreCertificates);
    } // end if successful

    if (NULL != certificatesInSignature) certificatesInSignature->Release();

    return hr;
}
```



<span data-ttu-id="67d71-135">在下一個程式碼範例中，藉由呼叫後面的程式碼範例中所示的方法取得憑證信任狀態。</span><span class="sxs-lookup"><span data-stu-id="67d71-135">In the next code example, the certificate trust status is obtained by calling the method shown in the code example that follows.</span></span>


```C++
HRESULT GetCertificateTrustStatus(
    __in PCCERT_CONTEXT certificate,
    __in HCERTSTORE* certificateStore,
    __out DWORD* certificateStatus
)
{
    HRESULT    hr = S_OK;

    // The certificate chain that will be created from 
    //  the PCCERT_CONTEXT object passed in.  
    PCCERT_CHAIN_CONTEXT    certificateChain =    NULL;

    hr = CreateCertificateChain(
        certificate, 
        *certificateStore, 
        &certificateChain);

    if (SUCCEEDED(hr)) { 
        *certificateStatus = 
            certificateChain->TrustStatus.dwErrorStatus;
    }

    return hr;
}
```



<span data-ttu-id="67d71-136">上述程式碼範例中所使用的憑證鏈，是藉由呼叫下列程式碼範例中所示的方法來建立。</span><span class="sxs-lookup"><span data-stu-id="67d71-136">The certificate chain used in the preceding code example is created by calling the method shown in the following code example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="67d71-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="67d71-137">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="67d71-138">**在本節中使用**</span><span class="sxs-lookup"><span data-stu-id="67d71-138">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="67d71-139">**CERT \_ 鏈 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="67d71-139">**CERT\_CHAIN\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context)
</dt> <dt>

[<span data-ttu-id="67d71-140">**憑證 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="67d71-140">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="67d71-141">**憑證 \_ 信任 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="67d71-141">**CERT\_TRUST\_STATUS**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status)
</dt> <dt>

[<span data-ttu-id="67d71-142">**CertAddCertificateCoNtextToStore**</span><span class="sxs-lookup"><span data-stu-id="67d71-142">**CertAddCertificateContextToStore**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
</dt> <dt>

[<span data-ttu-id="67d71-143">**CertOpenStore**</span><span class="sxs-lookup"><span data-stu-id="67d71-143">**CertOpenStore**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore)
</dt> <dt>

[<span data-ttu-id="67d71-144">**CertGetCertificateChain**</span><span class="sxs-lookup"><span data-stu-id="67d71-144">**CertGetCertificateChain**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[<span data-ttu-id="67d71-145">**IOpcCertificateEnumerator**</span><span class="sxs-lookup"><span data-stu-id="67d71-145">**IOpcCertificateEnumerator**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator)
</dt> <dt>

[<span data-ttu-id="67d71-146">**IOpcCertificateEnumerator::GetCurrent**</span><span class="sxs-lookup"><span data-stu-id="67d71-146">**IOpcCertificateEnumerator::GetCurrent**</span></span>](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-getcurrent)
</dt> <dt>

[<span data-ttu-id="67d71-147">**IOpcCertificateEnumerator：： MoveNext**</span><span class="sxs-lookup"><span data-stu-id="67d71-147">**IOpcCertificateEnumerator::MoveNext**</span></span>](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-movenext)
</dt> <dt>

[<span data-ttu-id="67d71-148">**IXpsSignature**</span><span class="sxs-lookup"><span data-stu-id="67d71-148">**IXpsSignature**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)
</dt> <dt>

[<span data-ttu-id="67d71-149">**IXpsSignature::GetCertificateEnumerator**</span><span class="sxs-lookup"><span data-stu-id="67d71-149">**IXpsSignature::GetCertificateEnumerator**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getcertificateenumerator)
</dt> <dt>

[<span data-ttu-id="67d71-150">**IXpsSignature：： Verify**</span><span class="sxs-lookup"><span data-stu-id="67d71-150">**IXpsSignature::Verify**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify)
</dt> <dt>

[<span data-ttu-id="67d71-151">**IXpsSignatureCollection**</span><span class="sxs-lookup"><span data-stu-id="67d71-151">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)
</dt> <dt>

[<span data-ttu-id="67d71-152">**IXpsSignatureCollection：： GetAt**</span><span class="sxs-lookup"><span data-stu-id="67d71-152">**IXpsSignatureCollection::GetAt**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturecollection-getat)
</dt> <dt>

[<span data-ttu-id="67d71-153">**IXpsSignatureCollection：： GetCount**</span><span class="sxs-lookup"><span data-stu-id="67d71-153">**IXpsSignatureCollection::GetCount**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturecollection-getcount)
</dt> <dt>

[<span data-ttu-id="67d71-154">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="67d71-154">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="67d71-155">**IXpsSignatureManager::GetSignatures**</span><span class="sxs-lookup"><span data-stu-id="67d71-155">**IXpsSignatureManager::GetSignatures**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-getsignatures)
</dt> <dt>

[<span data-ttu-id="67d71-156">**XPS \_ 簽名 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="67d71-156">**XPS\_SIGNATURE\_STATUS**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status)
</dt> <dt>

<span data-ttu-id="67d71-157">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="67d71-157">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="67d71-158">在檔中內嵌憑證鏈</span><span class="sxs-lookup"><span data-stu-id="67d71-158">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[<span data-ttu-id="67d71-159">XPS 數位簽章 API 錯誤</span><span class="sxs-lookup"><span data-stu-id="67d71-159">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="67d71-160">XPS 檔錯誤</span><span class="sxs-lookup"><span data-stu-id="67d71-160">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="67d71-161">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="67d71-161">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
