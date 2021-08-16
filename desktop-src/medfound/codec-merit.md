---
description: 編解碼器的優點
ms.assetid: 4ed594a0-2cc2-40d2-9b5c-dee59916fa1b
title: 編解碼器的優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56112942aa8378b2016616d0e090e17eb7225ca27b363c96e37eb7cccb6286e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065119"
---
# <a name="codec-merit"></a>編解碼器的優點

從 Windows 7 開始，您可以為媒體基礎編解碼器指派一個 *「值」* 。 列舉編解碼器時，較高的編解碼器偏好較低的編解碼器。 具有任何慣用值的編解碼器，在沒有指派的業績的情況下優先于編解碼器。 如需編解碼器列舉的詳細資訊，請參閱 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)。

這些值是由 Microsoft 所指派。 目前，只有硬體編解碼器才有資格獲得相關價值。 編解碼器廠商也會發出數位憑證，用來驗證編解碼器的業績值。 若要取得憑證，請傳送電子郵件要求至 wmla@microsoft.com 。 取得憑證的套裝程式括簽署授權，以及提供一組資訊檔給 Microsoft。

編解碼器功能的運作方式如下：

1.  編解碼器廠商會實行下列其中一項：
    -   AVStream 迷你驅動程式。 媒體基礎為 AVStream 驅動程式提供標準的 proxy MFT。 這是建議選項。
    -   媒體基礎轉換 (作為硬體的 proxy 的 MFT) 。 如需詳細資訊，請參閱 [硬體 MFTs](hardware-mfts.md)。
2.  編解碼器的業績值會儲存在登錄中，以供快速查閱。
3.  [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函式會依所需的順序來排序編解碼器。 具有值的編解碼器會出現在本機註冊之編解碼器的清單中 (參閱 [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)) ，但在其他編解碼器之前。
4.  建立 MFT 之後，會使用 [輸出保護管理員](output-protection-manager.md) (OPM) API 來驗證編解碼器的業績。
5.  若為 proxy MFT，編解碼器會實作為 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 介面。 若為 AVStream 驅動程式，編解碼器會實 KSPROPSETID \_ OPMVideoOutput 屬性集。

下圖顯示如何在這兩種情況下進行驗證：

![顯示兩個處理常式的圖表：一個是透過 media foundation proxy mft 和 avstream 驅動程式，另一個則是透過自訂 proxy mft](images/codecmerit.png)

## <a name="custom-proxy-mft"></a>自訂 Proxy MFT

如果您提供硬體編解碼器的 proxy MFT，請依照下列方式執行編解碼器的業績值：

1.  在 MFT 中執行 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 介面。 本主題的下一節會顯示範常式序代碼。
2.  將 [ [MFT \_ 編 \_ 解碼器 \_ ](mft-codec-merit-attribute.md) ] 的 [內容] 屬性新增至登錄，如下所示：

    1.  呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 來建立新的屬性存放區。
    2.  呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) 來設定 [ [MFT \_ 編 \_ 解碼器 \_](mft-codec-merit-attribute.md) ] 的 [內容] 屬性。 屬性的值是編解碼器指派的業績。
    3.  呼叫 [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) 以註冊 MFT。 傳遞 *pAttributes* 參數中的屬性存放區。

3.  應用程式會呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)。 此函式會傳回 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標的陣列，每個符合列舉準則的編解碼器都有一個陣列。
4.  應用程式會呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 來建立 MFT。
5.  [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)方法會呼叫 [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit)函式，以驗證憑證和價值。
6.  [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit)函式會呼叫 [**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) ，並傳送 [**OPM \_ 取得 \_ 編解碼器 \_ 資訊**](opm-get-codec-info.md)狀態要求。 此狀態要求會傳回編解碼器的已指派業績值。 如果這個值與登錄值不符， [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 可能會失敗。

下列程式碼示範如何在您註冊 MFT 時，將 [內容] 值新增至登錄：


```C++
// Shows how to register an MFT with a merit value.

HRESULT RegisterMFTWithMerit()
{
    // The following media types would apply to an H.264 decoder, 
    // and are used here as an example.

    MFT_REGISTER_TYPE_INFO aDecoderInputTypes[] = 
    {
        { MFMediaType_Video, MFVideoFormat_H264 },
    };

    MFT_REGISTER_TYPE_INFO aDecoderOutputTypes[] = 
    {
        { MFMediaType_Video, MFVideoFormat_RGB32 }
    };
    
    // Create an attribute store to hold the merit attribute.
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MFT_CODEC_MERIT_Attribute, 
            DECODER_MERIT   // Use the codec's assigned merit value.
            );
    }

    // Register the decoder for MFTEnum(Ex).
    if (SUCCEEDED(hr))
    {
        hr = MFTRegister(
            CLSID_MPEG1SampleDecoder,                   // CLSID
            MFT_CATEGORY_VIDEO_DECODER,                 // Category
            const_cast<LPWSTR>(SZ_DECODER_NAME),        // Friendly name
            0,                                          // Flags
            ARRAYSIZE(aDecoderInputTypes),              // Number of input types
            aDecoderInputTypes,                         // Input types
            ARRAYSIZE(aDecoderOutputTypes),             // Number of output types
            aDecoderOutputTypes,                        // Output types
            pAttributes                                 // Attributes 
            );
    }

    SafeRelease(&pAttributes);
    return hr;
}
```



### <a name="implementing-iopmvideooutput-for-codec-merit"></a>實施適用于編解碼器的 IOPMVideoOutput

下列程式碼會示範如何針對編解碼器提供執行 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 。 如需 OPM API 的一般討論，請參閱 [輸出保護管理員](output-protection-manager.md)。

> [!Note]  
> 此處所示的程式碼沒有模糊化或其他安全性機制。 其目的是要顯示 OPM 交握和狀態要求的基本執行。

 

此範例假設 *g \_ >testcert.pfx* 是包含編解碼器憑證鏈的位元組陣列，而 *g \_ PrivateKey* 是包含憑證私密金鑰的位元組陣列：


```C++
// Byte array that contains the codec's certificate.

const BYTE g_TestCert[] =
{
    // ... (certificate not shown)
```




```C++
// Byte array that contains the private key from the certificate.

const BYTE g_PrivateKey[] = 
{
    // .... (key not shown)
```



在 [**IOPMVideoOutput：： StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) 方法中，產生交握的亂數字。 將此數位和憑證傳回給呼叫者：


```C++
STDMETHODIMP CodecMerit::StartInitialization(
    OPM_RANDOM_NUMBER *prnRandomNumber,
    BYTE **ppbCertificate,
    ULONG *pulCertificateLength
    )
{
    HRESULT hr = S_OK;

    DWORD cbCertificate = sizeof(g_TestCert);
    const BYTE *pCertificate = g_TestCert;

    // Generate the random number for the OPM handshake.
    hr = BCryptGenRandom(
        NULL,  
        (PUCHAR)&m_RandomNumber, 
        sizeof(m_RandomNumber),
        BCRYPT_USE_SYSTEM_PREFERRED_RNG
        );

    // Allocate the buffer to copy the certificate.
    if (SUCCEEDED(hr))
    {
        *ppbCertificate = (PBYTE)CoTaskMemAlloc(cbCertificate);

        if (*ppbCertificate == NULL) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Copy the certificate and the random number.
    if (SUCCEEDED(hr))
    {
        *pulCertificateLength = cbCertificate;
        CopyMemory(*ppbCertificate, pCertificate, cbCertificate);
        *prnRandomNumber = m_RandomNumber;
    }
    return hr;
}
```



[**IOPMVideoOutput：： FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization)方法會完成 OPM 交握：


```C++
STDMETHODIMP CodecMerit::FinishInitialization(
    const OPM_ENCRYPTED_INITIALIZATION_PARAMETERS *pParameters
    )
{
    HRESULT hr = S_OK;
    BCRYPT_ALG_HANDLE hAlg = NULL;
    BCRYPT_KEY_HANDLE hKey = NULL;
    BCRYPT_OAEP_PADDING_INFO paddingInfo = {0};
    DWORD DecryptedLength = 0;
    PBYTE pbDecryptedParams = NULL;

    // The caller should pass the following structure in
    // pParameters:

    typedef struct {
        GUID  guidCOPPRandom;   // Our random number.
        GUID  guidKDI;          // AES signing key.
        DWORD StatusSeqStart;   // Status sequence number.
        DWORD CommandSeqStart;  // Command sequence number.
    } InitParams;

    paddingInfo.pszAlgId = BCRYPT_SHA512_ALGORITHM;

    //  Decrypt the input using the decoder's private key.

    hr = BCryptOpenAlgorithmProvider(
        &hAlg,
        BCRYPT_RSA_ALGORITHM,
        MS_PRIMITIVE_PROVIDER,
        0
        );

    //  Import the private key.
    if (SUCCEEDED(hr))
    {
        hr = BCryptImportKeyPair(
            hAlg,
            NULL,
            BCRYPT_RSAPRIVATE_BLOB,
            &hKey,
            (PUCHAR)g_PrivateKey, //pbData,
            sizeof(g_PrivateKey), //cbData,
            0
            );
    }

    //  Decrypt the input data.

    if (SUCCEEDED(hr))
    {
        hr = BCryptDecrypt(
            hKey,
            (PBYTE)pParameters,
            OPM_ENCRYPTED_INITIALIZATION_PARAMETERS_SIZE,
            &paddingInfo,
            NULL,
            0,
            NULL,
            0,
            &DecryptedLength,
            BCRYPT_PAD_OAEP
            );
    }

    if (SUCCEEDED(hr))
    {
        pbDecryptedParams = new (std::nothrow) BYTE[DecryptedLength];

        if (pbDecryptedParams == NULL) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    if (SUCCEEDED(hr))
    {
         hr = BCryptDecrypt(
             hKey,
             (PBYTE)pParameters,
             OPM_ENCRYPTED_INITIALIZATION_PARAMETERS_SIZE,
             &paddingInfo,
             NULL,
             0,
             pbDecryptedParams,
             DecryptedLength,
             &DecryptedLength,
             BCRYPT_PAD_OAEP
             );
    }

    if (SUCCEEDED(hr))
    {
        InitParams *Params = (InitParams *)pbDecryptedParams;
        
        //  Check the random number.
        if (0 != memcmp(&m_RandomNumber, &Params->guidCOPPRandom, sizeof(m_RandomNumber)))
        {
            hr = E_ACCESSDENIED;
        } 
        else 
        {
            //  Save the key and the sequence numbers.

            CopyMemory(m_AESKey.abRandomNumber, &Params->guidKDI, sizeof(m_AESKey));
            m_StatusSequenceNumber = Params->StatusSeqStart;
            m_CommandSequenceNumber = Params->CommandSeqStart;
        }
    }

    //  Clean up.

    if (hKey)
    {
        BCryptDestroyKey(hKey);
    }
    if (hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg, 0);
    }
    delete [] pbDecryptedParams;

    return hr;
}
```



在 [**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) 方法中，執行 [**OPM \_ 取得 \_ 編解碼器 \_ 資訊**](opm-get-codec-info.md) 狀態要求。 輸入資料是 [**OPM \_ 取得 \_ 編解碼器 \_ 資訊 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) 結構，其中包含您的 MFT CLSID。 輸出資料是 [**OPM \_ 取得 \_ 編解碼器 \_ 資訊 \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) 結構，其中包含編解碼器的資訊。


```C++
STDMETHODIMP CodecMerit::GetInformation( 
    const OPM_GET_INFO_PARAMETERS *Parameters,
    OPM_REQUESTED_INFORMATION *pRequest
    )
{

    HRESULT hr = S_OK;
    OPM_GET_CODEC_INFO_PARAMETERS *CodecInfoParameters;

    //  Check the MAC.
    OPM_OMAC Tag = { 0 };

    hr = ComputeOMAC(
        m_AESKey, 
        (PBYTE)Parameters + OPM_OMAC_SIZE, 
        sizeof(OPM_GET_INFO_PARAMETERS) - OPM_OMAC_SIZE, 
        &Tag
        );

    if (SUCCEEDED(hr))
    {
        if (0 != memcmp(Tag.abOMAC, &Parameters->omac, OPM_OMAC_SIZE))
        {
            hr = E_ACCESSDENIED;
        }
    }

    // Validate the status sequence number. This must be consecutive
    // from the previous sequence number.

    if (SUCCEEDED(hr))
    {
        if (Parameters->ulSequenceNumber != m_StatusSequenceNumber++)
        {
            hr = E_ACCESSDENIED;
        }
    }

    //  Check the status request.

    if (SUCCEEDED(hr))
    {
        if (Parameters->guidInformation != OPM_GET_CODEC_INFO) 
        {
            hr = E_NOTIMPL;
        }
    }

    //  Check parameters.

    if (SUCCEEDED(hr))
    {
        CodecInfoParameters = (OPM_GET_CODEC_INFO_PARAMETERS *)Parameters->abParameters;

        if (Parameters->cbParametersSize > OPM_GET_INFORMATION_PARAMETERS_SIZE ||
            Parameters->cbParametersSize < sizeof(ULONG) ||
            Parameters->cbParametersSize - sizeof(ULONG) != CodecInfoParameters->cbVerifier
            ) 
        {
            hr = E_INVALIDARG;
        }
    }

    //  The input data should consist of the CLSID of the decoder.

    if (SUCCEEDED(hr))
    {
        CodecInfoParameters = (OPM_GET_CODEC_INFO_PARAMETERS *)Parameters->abParameters;
    
        if (CodecInfoParameters->cbVerifier != sizeof(CLSID) ||
            0 != memcmp(&CLSID_MPEG1SampleDecoder,
                        CodecInfoParameters->Verifier,
                        CodecInfoParameters->cbVerifier)) 
        {
            hr = E_ACCESSDENIED;
        }
    }

    if (SUCCEEDED(hr))
    {
        // Now return the decoder merit to the caller.

        ZeroMemory(pRequest, sizeof(OPM_REQUESTED_INFORMATION));

        OPM_GET_CODEC_INFO_INFORMATION *pInfo = 
            (OPM_GET_CODEC_INFO_INFORMATION *)pRequest->abRequestedInformation;

        pInfo->Merit = DECODER_MERIT;
        pInfo->rnRandomNumber = Parameters->rnRandomNumber;

        pRequest->cbRequestedInformationSize = sizeof(OPM_GET_CODEC_INFO_INFORMATION);

        //  Sign it with the key.

        hr = ComputeOMAC(
            m_AESKey, 
            (PBYTE)pRequest + OPM_OMAC_SIZE, 
            sizeof(OPM_REQUESTED_INFORMATION) - OPM_OMAC_SIZE, 
            &pRequest->omac
            );
    }

    return hr;
}
```



[**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)方法必須使用 OMAC-1 演算法來計算訊息驗證碼 (MAC) ;請參閱 [計算 OMAC-1 值](opm-example-code.md)。

不需要支援任何其他 OPM 狀態要求。

在編解碼器方面，不需要 [**iopmvideooutput：： COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) 和 [**Iopmvideooutput：： Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) 方法，因此這些方法可以傳回 **E \_ >notimpl**。


```C++
STDMETHODIMP CodecMerit::COPPCompatibleGetInformation( 
    const OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
    OPM_REQUESTED_INFORMATION *pRequestedInformation)
{
    return E_NOTIMPL;
}

STDMETHODIMP CodecMerit::Configure( 
    const OPM_CONFIGURE_PARAMETERS *pParameters,
    ULONG ulAdditionalParametersSize,
    const BYTE *pbAdditionalParameters)
{
    return E_NOTIMPL;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> <dt>

[撰寫自訂的 MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 



