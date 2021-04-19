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
# <a name="verify-document-signatures-and-certificates"></a>驗證檔簽章和憑證

本主題說明如何驗證 XPS 檔中的簽章，以及如何驗證與這些簽章相關的憑證。

在您的程式中使用下列程式碼範例之前，請閱讀 [一般數位簽章程式設計](basic-digital-signature-programming-tasks.md)工作中的免責聲明。

下列程式碼範例會檢查 XPS 檔中所找到的數位簽章。

若要檢查 XPS 檔中的簽章，請執行下列步驟：

1.  將檔載入到簽章管理員，如初始化簽章 [管理員](initialize-the-signature-manager.md)中所述。
2.  從數位簽章管理員取得簽章的集合。
3.  取得集合中的簽章數目。
4.  針對集合中的每個簽章，呼叫 [**驗證**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) 方法，如下面的程式碼範例所示。


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



若要驗證數位簽章，請先確認簽署憑證所建立的簽章，然後驗證簽署憑證。 下列程式碼範例中所使用的驗證方法會將憑證快取在暫時憑證存放區中，而在此範例中，此範例稍後會加以呼叫。

若要建立暫時的憑證存放區，請執行下列步驟：

1.  建立暫時的憑證存放區，以保存簽章所使用的憑證。
2.  逐一查看簽章的憑證集，並將每個憑證載入暫存憑證存放區中。


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



若要驗證用來簽署檔的數位簽章和憑證，請執行下列步驟：

1.  逐一查看簽章所用的憑證來尋找簽署憑證。
2.  藉由針對憑證驗證簽章來測試憑證。 當 [**驗證**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify)方法傳回 xps 簽章狀態 **\_ \_ \_ 有效** 或 xps 簽章 **\_ \_ 狀態 \_ 可疑** 的 xps 簽章狀態，而且不會傳回 **設備 \_ 安全性** 錯誤時，就會找到簽署憑證。 [**\_ \_**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status)


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



找到簽署憑證後，請執行下列步驟：

1.  儲存傳回的簽章狀態。
2.  如有必要，請更新本機狀態，以執行後續的憑證測試：
    1.  如果簽章狀態為 [成功]，請將本機狀態設定為 [可疑]，以便測試憑證。
    2.  如果簽章狀態為 incompliant，請將本機狀態保持為 incompliant。
    3.  如果簽章狀態已中斷或不完整，請將本機狀態設定為 [已中斷]。

「Xps 簽章 **\_ \_ 狀態 \_ INCOMPLIANT** 的「簽章狀態」表示未簽署的 xps 檔元件已簽署，或尚未簽署的 xps 檔部分。 如果 [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) 傳回這個簽章狀態，則不需要進一步檢查簽章。


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



若要在簽章狀態有效或有疑問時確認憑證信任，請執行下列步驟：

1.  取得憑證信任狀態。
2.  評估傳回的憑證信任狀態。
3.  傳回產生的狀態。

下一個程式碼範例不會測試每個可能的憑證信任狀態。 如需可傳回狀態值的其他詳細資料，請參閱憑證 [**\_ 信任 \_ 狀態**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status)。


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



在下一個程式碼範例中，藉由呼叫後面的程式碼範例中所示的方法取得憑證信任狀態。


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



上述程式碼範例中所使用的憑證鏈，是藉由呼叫下列程式碼範例中所示的方法來建立。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

**在本節中使用**
</dt> <dt>

[**CERT \_ 鏈 \_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context)
</dt> <dt>

[**憑證 \_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**憑證 \_ 信任 \_ 狀態**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status)
</dt> <dt>

[**CertAddCertificateCoNtextToStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
</dt> <dt>

[**CertOpenStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore)
</dt> <dt>

[**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[**IOpcCertificateEnumerator**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator)
</dt> <dt>

[**IOpcCertificateEnumerator::GetCurrent**](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-getcurrent)
</dt> <dt>

[**IOpcCertificateEnumerator：： MoveNext**](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-movenext)
</dt> <dt>

[**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)
</dt> <dt>

[**IXpsSignature::GetCertificateEnumerator**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getcertificateenumerator)
</dt> <dt>

[**IXpsSignature：： Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify)
</dt> <dt>

[**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)
</dt> <dt>

[**IXpsSignatureCollection：： GetAt**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturecollection-getat)
</dt> <dt>

[**IXpsSignatureCollection：： GetCount**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturecollection-getcount)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**IXpsSignatureManager::GetSignatures**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-getsignatures)
</dt> <dt>

[**XPS \_ 簽名 \_ 狀態**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status)
</dt> <dt>

**詳細資訊**
</dt> <dt>

[在檔中內嵌憑證鏈](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[XPS 數位簽章 API 錯誤](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS 檔錯誤](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
