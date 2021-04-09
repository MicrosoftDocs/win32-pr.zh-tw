---
description: 示範如何要求金鑰保存憑證。
ms.assetid: a09f55c1-fb27-41e7-9a2f-617d2360c02f
title: 要求金鑰保存憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da1f69338ed4a41986700853ef5d46ee08612e8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850535"
---
# <a name="requesting-a-key-archival-certificate"></a><span data-ttu-id="8034b-103">要求金鑰保存憑證</span><span class="sxs-lookup"><span data-stu-id="8034b-103">Requesting a Key Archival Certificate</span></span>

<span data-ttu-id="8034b-104">下列範例顯示如何建立和提交 [*憑證要求*](../secgloss/c-gly.md) ，以及接收產生的金鑰保存憑證。</span><span class="sxs-lookup"><span data-stu-id="8034b-104">The following example shows creating and submitting a [*certificate request*](../secgloss/c-gly.md) and receiving the resulting key archival certificate.</span></span> <span data-ttu-id="8034b-105">若要讓此範例成功，必須設定接收憑證要求 (CA) 的證書 [*頒發機構*](../secgloss/c-gly.md) 單位，以進行金鑰保存。</span><span class="sxs-lookup"><span data-stu-id="8034b-105">For this example to succeed, the [*certification authority*](../secgloss/c-gly.md) (CA) that receives the certificate request must be configured for key archival.</span></span>

<span data-ttu-id="8034b-106">下列步驟說明如何建立並提交憑證要求。</span><span class="sxs-lookup"><span data-stu-id="8034b-106">The following steps describe how to create and submit a certificate request.</span></span>

<span data-ttu-id="8034b-107">**建立並提交憑證要求**</span><span class="sxs-lookup"><span data-stu-id="8034b-107">**To create and submit a certificate request**</span></span>

1.  <span data-ttu-id="8034b-108">使用 [**ICertRequest2：： GetCACertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcacertificate) 方法來取出 CA 的 exchange 憑證。</span><span class="sxs-lookup"><span data-stu-id="8034b-108">Retrieve the CA's exchange certificate using the [**ICertRequest2::GetCACertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcacertificate) method.</span></span>
2.  <span data-ttu-id="8034b-109">使用 [**ICEnroll4：:P rivatekeyarchivecertificate**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-get_privatekeyarchivecertificate) 屬性，指定抓取的 CA exchange 憑證是金鑰保存憑證。</span><span class="sxs-lookup"><span data-stu-id="8034b-109">Specify that the retrieved CA exchange certificate is the key archive certificate using the [**ICEnroll4::PrivateKeyArchiveCertificate**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-get_privatekeyarchivecertificate) property.</span></span>
3.  <span data-ttu-id="8034b-110">使用 [**ICEnroll4：： createRequest**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-createrequest) 方法建立 CMC 憑證要求。</span><span class="sxs-lookup"><span data-stu-id="8034b-110">Create a CMC certificate request using the [**ICEnroll4::createRequest**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-createrequest) method.</span></span>
4.  <span data-ttu-id="8034b-111">使用 [**ICertRequest2：： submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) 方法將憑證要求提交給 CA。</span><span class="sxs-lookup"><span data-stu-id="8034b-111">Submit the certificate request to a CA using the [**ICertRequest2::Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) method.</span></span> <span data-ttu-id="8034b-112">CA 必須設定為支援金鑰保存。</span><span class="sxs-lookup"><span data-stu-id="8034b-112">The CA must be configured to support key archival.</span></span>

<span data-ttu-id="8034b-113">下列步驟說明如何取得已發行的憑證以供金鑰保存之用。</span><span class="sxs-lookup"><span data-stu-id="8034b-113">The following steps describe how to retrieve the issued certificate for key archival purposes.</span></span>

<span data-ttu-id="8034b-114">**取得已發行的憑證以進行金鑰保存用途**</span><span class="sxs-lookup"><span data-stu-id="8034b-114">**To retrieve the issued certificate for key archival purposes**</span></span>

1.  <span data-ttu-id="8034b-115">使用 [**ICertRequest2：： GetFullResponseProperty**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getfullresponseproperty) 方法，以取得完整的回應，包括已發行的憑證。</span><span class="sxs-lookup"><span data-stu-id="8034b-115">Retrieve the full response, including the issued certificate, using the [**ICertRequest2::GetFullResponseProperty**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getfullresponseproperty) method.</span></span>
2.  <span data-ttu-id="8034b-116">使用 [**ICEnroll4：： acceptResponse**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-acceptresponse) 方法安裝已發行的憑證。</span><span class="sxs-lookup"><span data-stu-id="8034b-116">Install the issued certificate using the [**ICEnroll4::acceptResponse**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-acceptresponse) method.</span></span>

<span data-ttu-id="8034b-117">下列範例顯示如何建立和提交憑證要求，以及接收產生的金鑰保存憑證。</span><span class="sxs-lookup"><span data-stu-id="8034b-117">The following example shows creating and submitting a certificate request and receiving the resulting key archival certificate.</span></span>


```C++
// Pointer to interface objects.
ICEnroll4 * pEnroll = NULL;
ICertRequest2 * pRequest = NULL;

// BSTR variables.
BSTR    bstrCACert = NULL;
BSTR    bstrDN = NULL;
BSTR    bstrCertAuth = NULL;
BSTR    bstrReq = NULL;
BSTR    bstrDispMsg = NULL;
BSTR    bstrErrorMsg = NULL;

VARIANT varFullResp;

LONG    lDisp =0;
LONG    lRequestID = 0;
LONG    lStatus = 0;

HRESULT    hr;

// Initialize COM.
hr = CoInitializeEx( NULL, COINIT_APARTMENTTHREADED );
if ( FAILED( hr ) )
{
    printf("Failed CoInitializeEx - [%x]\n", hr);
    goto error;
}

// Create an instance of the Certificate Enrollment object.
hr = CoCreateInstance( CLSID_CEnroll,
                       NULL,
                       CLSCTX_INPROC_SERVER,
                       IID_ICEnroll4,
                       (void **)&pEnroll);
if ( FAILED( hr ) )
{
    printf("Failed CoCreateInstance - pEnroll [%x]\n", hr);
    goto error;
}

// Create an instance of the Certificate Request object.
hr = CoCreateInstance( CLSID_CCertRequest,
                       NULL,
                       CLSCTX_INPROC_SERVER,
                       IID_ICertRequest2,
                       (void **)&pRequest);
if ( FAILED( hr ) )
{
    printf("Failed CoCreateInstance - pRequest [%x]\n", hr);
    goto error;
}

// Allocate the BSTR that represents the certification authority.
// Note the use of '\\' to produce a single '\' in C++.
bstrCertAuth = SysAllocString(L"Server\\CertAuth");
if (NULL == bstrCertAuth)
{
    printf("Failed SysAllocString\n");
    goto error;
}

// Retrieve the CA's exchange certificate.
hr = pRequest->GetCACertificate(TRUE,
                                bstrCertAuth,
                                CR_OUT_BASE64HEADER,
                                &bstrCACert);
if (FAILED(hr))
{
    printf("Failed GetCACertificate [%x]\n", hr);
    goto error;
}

// Specify the retrieved certificate 
// as the key archive certificate.
hr = pEnroll->put_PrivateKeyArchiveCertificate(bstrCACert);
if (FAILED(hr))
{
    printf("put_PrivateKeyArchiveCertificate [%x]\n", hr);
    goto error;
}

// Create the data for the request.
// A user interface or database retrieval could
// be used instead of this example's hard-coded text.
bstrDN = SysAllocString(L"CN=UserName"    // common name
                        L",OU=UserUnit"   // org unit
                        L",O=UserOrg"     // org
                        L",L=UserCity"    // locality
                        L",S=WA"          // state
                        L",C=US");        // country/region
if (NULL == bstrDN)
{
    printf("Failed SysAllocString\n");
    goto error;
}

// Create the certificate request.
hr = pEnroll->createRequest( XECR_CMC,
                             bstrDN, 
                             NULL,
                             &bstrReq );
if ( FAILED( hr ) )
{
    printf("Failed createRequest - [%x]\n", hr);
    goto error;
}

// Submit the certificate request.
hr = pRequest->Submit( CR_IN_CMC,
                       bstrReq,
                       NULL,
                       bstrCertAuth,
                       &lDisp );
if ( FAILED( hr ) )
{
    
    printf("Failed Submit - [%x]\n", hr);  
    goto error;
}

// Evaluate the disposition of the submitted request.
switch (lDisp)
{
    case CR_DISP_ISSUED:
           printf("Certificate was issued.\n");
           break;

    case CR_DISP_ISSUED_OUT_OF_BAND:
    case CR_DISP_INCOMPLETE:
    case CR_DISP_ERROR:
    case CR_DISP_DENIED:
    case CR_DISP_UNDER_SUBMISSION:
    case CR_DISP_REVOKED:
            printf("Certificate was not issued: %d\n", lDisp);
            break;

    default:
            printf("Unexpected disposition: %d\n", lDisp);
            goto error;
}

// Retrieve the request ID.
hr = pRequest->GetRequestId(&lRequestID);
if ( FAILED(hr) )
{
    printf("Failed GetRequestId - [%x]\n", hr);  
    goto error;
}
printf("The request ID is %d\n", lRequestID);

if (CR_DISP_ISSUED != lDisp)
{
    // Provide information about why a certificate 
    // was not issued.
    
    // Retrieve the last status.
    hr = pRequest->GetLastStatus(&lStatus);
    if ( FAILED(hr) )
    {
        printf("Failed GetLastStatus - [%x]\n", hr);  
        goto error;
    }

    // Retrieve the disposition message.
    hr = pRequest->GetDispositionMessage(&bstrDispMsg);
    if ( FAILED(hr) )
    {
        printf("Failed GetDispositionMessage - [%x]\n", hr);  
        goto error;
    }

    // Retrieve the error message.
    hr = pRequest->GetErrorMessageText(lStatus,
                                       CR_GEMT_HRESULT_STRING,
                                       &bstrErrorMsg);
    if ( FAILED(hr) )
    {
        printf("Failed GetErrorMessageText - [%x]\n", hr);  
        goto error;
    }
    
    // Display the information and exit.
    printf("Request ID: %d\nDisposition: %S\nError: %S\n",
           lRequestID,
           bstrDispMsg,
           bstrErrorMsg);
    goto error;
}

// Retrieve the full response.
VariantInit(&varFullResp);
hr = pRequest->GetFullResponseProperty( FR_PROP_FULLRESPONSE,
                                        0,
                                        PROPTYPE_BINARY,
                                        CR_OUT_BASE64,
                                        &varFullResp );
if ( FAILED( hr ) )
{
    printf("Failed GetFullResponseProperty - [%x]\n", hr);
    goto error;
}

// Accept the response.
hr = pEnroll->acceptResponse(varFullResp.bstrVal);
if ( FAILED( hr ) )
{
    printf("Failed AcceptResponse - [%x]\n", hr);
    goto error;
}
else
{
    printf("Successfully completed processing\n");
}

error:

// Done processing.
// Clean up object resources.
if ( NULL != pEnroll )
    pEnroll->Release();
if ( NULL != pRequest )
    pRequest->Release();

// Free BSTR variables.
if ( NULL != bstrCACert )
    SysFreeString ( bstrCACert );
if ( NULL != bstrDN )
    SysFreeString ( bstrDN );
if ( NULL != bstrCertAuth )
    SysFreeString ( bstrCertAuth );
if ( NULL != bstrReq )
    SysFreeString ( bstrReq );
if ( NULL != bstrDispMsg )
    SysFreeString ( bstrDispMsg );
if ( NULL != bstrErrorMsg )
    SysFreeString ( bstrErrorMsg );

// Clear VARIANTS.
VariantClear(&varFullResp);

// Free COM resources.
CoUninitialize();

return hr;
```



 

 
