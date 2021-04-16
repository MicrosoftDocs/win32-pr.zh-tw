---
description: 編解碼器的優點
ms.assetid: 4ed594a0-2cc2-40d2-9b5c-dee59916fa1b
title: 編解碼器的優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ecd177c3c32084a030ce75c15cecd5d4c04fc3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567802"
---
# <a name="codec-merit"></a><span data-ttu-id="652ac-103">編解碼器的優點</span><span class="sxs-lookup"><span data-stu-id="652ac-103">Codec Merit</span></span>

<span data-ttu-id="652ac-104">從 Windows 7 開始，您可以為媒體基礎的編解碼器指派一個 *「值」* 。</span><span class="sxs-lookup"><span data-stu-id="652ac-104">Starting in Windows 7, a Media Foundation codec can be assigned a *merit* value.</span></span> <span data-ttu-id="652ac-105">列舉編解碼器時，較高的編解碼器偏好較低的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="652ac-105">When codecs are enumerated, codecs with higher merit are preferred over codecs with lower merit.</span></span> <span data-ttu-id="652ac-106">具有任何慣用值的編解碼器，在沒有指派的業績的情況下優先于編解碼器。</span><span class="sxs-lookup"><span data-stu-id="652ac-106">Codecs with any merit value are preferred over codecs without an assigned merit.</span></span> <span data-ttu-id="652ac-107">如需編解碼器列舉的詳細資訊，請參閱 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)。</span><span class="sxs-lookup"><span data-stu-id="652ac-107">For details about codec enumeration, see [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span>

<span data-ttu-id="652ac-108">這些值是由 Microsoft 所指派。</span><span class="sxs-lookup"><span data-stu-id="652ac-108">Merit values are assigned by Microsoft.</span></span> <span data-ttu-id="652ac-109">目前，只有硬體編解碼器才有資格獲得相關價值。</span><span class="sxs-lookup"><span data-stu-id="652ac-109">Currently, only hardware codecs are eligible to receive a merit value.</span></span> <span data-ttu-id="652ac-110">編解碼器廠商也會發出數位憑證，用來驗證編解碼器的業績值。</span><span class="sxs-lookup"><span data-stu-id="652ac-110">The codec vendor is also issued a digital certificate, which is used to verify the codec's merit value.</span></span> <span data-ttu-id="652ac-111">若要取得憑證，請傳送電子郵件要求至 wmla@microsoft.com 。</span><span class="sxs-lookup"><span data-stu-id="652ac-111">To obtain a certificate, send an email request to wmla@microsoft.com.</span></span> <span data-ttu-id="652ac-112">取得憑證的套裝程式括簽署授權，以及提供一組資訊檔給 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="652ac-112">The process for obtaining a certificate includes signing a license and providing a set of information files to Microsoft.</span></span>

<span data-ttu-id="652ac-113">編解碼器功能的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="652ac-113">Codec merit works as follows:</span></span>

1.  <span data-ttu-id="652ac-114">編解碼器廠商會實行下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="652ac-114">The codec vendor implements one of the following:</span></span>
    -   <span data-ttu-id="652ac-115">AVStream 迷你驅動程式。</span><span class="sxs-lookup"><span data-stu-id="652ac-115">An AVStream mini-driver.</span></span> <span data-ttu-id="652ac-116">媒體基礎為 AVStream 驅動程式提供標準的 proxy MFT。</span><span class="sxs-lookup"><span data-stu-id="652ac-116">Media Foundation provides an standard proxy MFT for AVStream drivers.</span></span> <span data-ttu-id="652ac-117">這是建議選項。</span><span class="sxs-lookup"><span data-stu-id="652ac-117">This is the recommended option.</span></span>
    -   <span data-ttu-id="652ac-118">媒體基礎轉換 (作為硬體的 proxy 的 MFT) 。</span><span class="sxs-lookup"><span data-stu-id="652ac-118">A Media Foundation transform (MFT) that acts as a proxy to the hardware.</span></span> <span data-ttu-id="652ac-119">如需詳細資訊，請參閱 [硬體 MFTs](hardware-mfts.md)。</span><span class="sxs-lookup"><span data-stu-id="652ac-119">For more information, see [Hardware MFTs](hardware-mfts.md).</span></span>
2.  <span data-ttu-id="652ac-120">編解碼器的業績值會儲存在登錄中，以供快速查閱。</span><span class="sxs-lookup"><span data-stu-id="652ac-120">The codec's merit value is stored in the registry for quick lookup.</span></span>
3.  <span data-ttu-id="652ac-121">[**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函式會依所需的順序來排序編解碼器。</span><span class="sxs-lookup"><span data-stu-id="652ac-121">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function sorts codecs in order of merit.</span></span> <span data-ttu-id="652ac-122">具有值的編解碼器會出現在本機註冊之編解碼器的清單中 (參閱 [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)) ，但在其他編解碼器之前。</span><span class="sxs-lookup"><span data-stu-id="652ac-122">Codecs with merit values appear in the list behind locally registered codecs (see [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), but ahead of other codecs.</span></span>
4.  <span data-ttu-id="652ac-123">建立 MFT 之後，會使用 [輸出保護管理員](output-protection-manager.md) (OPM) API 來驗證編解碼器的業績。</span><span class="sxs-lookup"><span data-stu-id="652ac-123">When the MFT is created, the codec's merit is verified using the [Output Protection Manager](output-protection-manager.md) (OPM) API.</span></span>
5.  <span data-ttu-id="652ac-124">若為 proxy MFT，編解碼器會實作為 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 介面。</span><span class="sxs-lookup"><span data-stu-id="652ac-124">For a proxy MFT, the codec implements the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface.</span></span> <span data-ttu-id="652ac-125">若為 AVStream 驅動程式，編解碼器會實 KSPROPSETID \_ OPMVideoOutput 屬性集。</span><span class="sxs-lookup"><span data-stu-id="652ac-125">For an AVStream driver, the codec implements the KSPROPSETID\_OPMVideoOutput property set.</span></span>

<span data-ttu-id="652ac-126">下圖顯示如何在這兩種情況下進行驗證：</span><span class="sxs-lookup"><span data-stu-id="652ac-126">The following diagram shows how merit is verified in both cases:</span></span>

![顯示兩個處理常式的圖表：一個是透過 media foundation proxy mft 和 avstream 驅動程式，另一個則是透過自訂 proxy mft](images/codecmerit.png)

## <a name="custom-proxy-mft"></a><span data-ttu-id="652ac-128">自訂 Proxy MFT</span><span class="sxs-lookup"><span data-stu-id="652ac-128">Custom Proxy MFT</span></span>

<span data-ttu-id="652ac-129">如果您提供硬體編解碼器的 proxy MFT，請依照下列方式執行編解碼器的業績值：</span><span class="sxs-lookup"><span data-stu-id="652ac-129">If you provide a proxy MFT for the hardware codec, implement the codec merit value as follows:</span></span>

1.  <span data-ttu-id="652ac-130">在 MFT 中執行 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 介面。</span><span class="sxs-lookup"><span data-stu-id="652ac-130">Implement the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface in the MFT.</span></span> <span data-ttu-id="652ac-131">本主題的下一節會顯示範常式序代碼。</span><span class="sxs-lookup"><span data-stu-id="652ac-131">Example code is shown in the next section of this topic.</span></span>
2.  <span data-ttu-id="652ac-132">將 [ [MFT \_ 編 \_ 解碼器 \_ ](mft-codec-merit-attribute.md) ] 的 [內容] 屬性新增至登錄，如下所示：</span><span class="sxs-lookup"><span data-stu-id="652ac-132">Add the [MFT\_CODEC\_MERIT\_Attribute](mft-codec-merit-attribute.md) attribute to the registry, as follows:</span></span>

    1.  <span data-ttu-id="652ac-133">呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 來建立新的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="652ac-133">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
    2.  <span data-ttu-id="652ac-134">呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) 來設定 [ [MFT \_ 編 \_ 解碼器 \_](mft-codec-merit-attribute.md) ] 的 [內容] 屬性。</span><span class="sxs-lookup"><span data-stu-id="652ac-134">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to set the [MFT\_CODEC\_MERIT\_Attribute](mft-codec-merit-attribute.md) attribute.</span></span> <span data-ttu-id="652ac-135">屬性的值是編解碼器指派的業績。</span><span class="sxs-lookup"><span data-stu-id="652ac-135">The value of the attribute is the codec's assigned merit.</span></span>
    3.  <span data-ttu-id="652ac-136">呼叫 [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) 以註冊 MFT。</span><span class="sxs-lookup"><span data-stu-id="652ac-136">Call [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) to register the MFT.</span></span> <span data-ttu-id="652ac-137">傳遞 *pAttributes* 參數中的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="652ac-137">Pass the attribute store in the *pAttributes* parameter.</span></span>

3.  <span data-ttu-id="652ac-138">應用程式會呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)。</span><span class="sxs-lookup"><span data-stu-id="652ac-138">The application calls [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="652ac-139">此函式會傳回 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標的陣列，每個符合列舉準則的編解碼器都有一個陣列。</span><span class="sxs-lookup"><span data-stu-id="652ac-139">This function returns an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, one for each codec that matches the enumeration criteria.</span></span>
4.  <span data-ttu-id="652ac-140">應用程式會呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 來建立 MFT。</span><span class="sxs-lookup"><span data-stu-id="652ac-140">The application calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the MFT.</span></span>
5.  <span data-ttu-id="652ac-141">[**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)方法會呼叫 [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit)函式，以驗證憑證和價值。</span><span class="sxs-lookup"><span data-stu-id="652ac-141">The [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method calls the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function to verify the certificate and the merit value.</span></span>
6.  <span data-ttu-id="652ac-142">[**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit)函式會呼叫 [**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) ，並傳送 [**OPM \_ 取得 \_ 編解碼器 \_ 資訊**](opm-get-codec-info.md)狀態要求。</span><span class="sxs-lookup"><span data-stu-id="652ac-142">The [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function calls [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) and sends an [**OPM\_GET\_CODEC\_INFO**](opm-get-codec-info.md) status request.</span></span> <span data-ttu-id="652ac-143">此狀態要求會傳回編解碼器的已指派業績值。</span><span class="sxs-lookup"><span data-stu-id="652ac-143">This status request returns the codec's assigned merit value.</span></span> <span data-ttu-id="652ac-144">如果這個值與登錄值不符， [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="652ac-144">If this value does not match the registry value, [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) may fail.</span></span>

<span data-ttu-id="652ac-145">下列程式碼示範如何在您註冊 MFT 時，將 [內容] 值新增至登錄：</span><span class="sxs-lookup"><span data-stu-id="652ac-145">The following code shows how to add the merit value to the registry when you register the MFT:</span></span>


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



### <a name="implementing-iopmvideooutput-for-codec-merit"></a><span data-ttu-id="652ac-146">實施適用于編解碼器的 IOPMVideoOutput</span><span class="sxs-lookup"><span data-stu-id="652ac-146">Implementing IOPMVideoOutput for Codec Merit</span></span>

<span data-ttu-id="652ac-147">下列程式碼會示範如何針對編解碼器提供執行 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 。</span><span class="sxs-lookup"><span data-stu-id="652ac-147">The following code shows how to implement [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) for codec merit.</span></span> <span data-ttu-id="652ac-148">如需 OPM API 的一般討論，請參閱 [輸出保護管理員](output-protection-manager.md)。</span><span class="sxs-lookup"><span data-stu-id="652ac-148">For a more general discussion of the OPM API, see [Output Protection Manager](output-protection-manager.md).</span></span>

> [!Note]  
> <span data-ttu-id="652ac-149">此處所示的程式碼沒有模糊化或其他安全性機制。</span><span class="sxs-lookup"><span data-stu-id="652ac-149">The code shown here has no obfuscation or other security mechanisms.</span></span> <span data-ttu-id="652ac-150">其目的是要顯示 OPM 交握和狀態要求的基本執行。</span><span class="sxs-lookup"><span data-stu-id="652ac-150">It is meant to show the basic implementation of the OPM handshake and status request.</span></span>

 

<span data-ttu-id="652ac-151">此範例假設 *g \_ >testcert.pfx* 是包含編解碼器憑證鏈的位元組陣列，而 *g \_ PrivateKey* 是包含憑證私密金鑰的位元組陣列：</span><span class="sxs-lookup"><span data-stu-id="652ac-151">This example assumes that *g\_TestCert* is a byte array that contains the codec's certificate chain, and *g\_PrivateKey* is a byte array that contains the private key from the certificate:</span></span>


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



<span data-ttu-id="652ac-152">在 [**IOPMVideoOutput：： StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) 方法中，產生交握的亂數字。</span><span class="sxs-lookup"><span data-stu-id="652ac-152">In the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method, generate a random number for the handshake.</span></span> <span data-ttu-id="652ac-153">將此數位和憑證傳回給呼叫者：</span><span class="sxs-lookup"><span data-stu-id="652ac-153">Return this number and the certificate to the caller:</span></span>


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



<span data-ttu-id="652ac-154">[**IOPMVideoOutput：： FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization)方法會完成 OPM 交握：</span><span class="sxs-lookup"><span data-stu-id="652ac-154">The [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) method completes the OPM handshake:</span></span>


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



<span data-ttu-id="652ac-155">在 [**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) 方法中，執行 [**OPM \_ 取得 \_ 編解碼器 \_ 資訊**](opm-get-codec-info.md) 狀態要求。</span><span class="sxs-lookup"><span data-stu-id="652ac-155">In the [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method, implement the [**OPM\_GET\_CODEC\_INFO**](opm-get-codec-info.md) status request.</span></span> <span data-ttu-id="652ac-156">輸入資料是 [**OPM \_ 取得 \_ 編解碼器 \_ 資訊 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) 結構，其中包含您的 MFT CLSID。</span><span class="sxs-lookup"><span data-stu-id="652ac-156">The input data is an [**OPM\_GET\_CODEC\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) structure that contains the CLSID of your MFT.</span></span> <span data-ttu-id="652ac-157">輸出資料是 [**OPM \_ 取得 \_ 編解碼器 \_ 資訊 \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) 結構，其中包含編解碼器的資訊。</span><span class="sxs-lookup"><span data-stu-id="652ac-157">The output data is an [**OPM\_GET\_CODEC\_INFO\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) structure that contains the codec merit.</span></span>


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



<span data-ttu-id="652ac-158">[**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)方法必須使用 OMAC-1 演算法來計算訊息驗證碼 (MAC) ;請參閱 [計算 OMAC-1 值](opm-example-code.md)。</span><span class="sxs-lookup"><span data-stu-id="652ac-158">The [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method must compute a Message Authentication Code (MAC) using the OMAC-1 algorithm; see [Computing the OMAC-1 Value](opm-example-code.md).</span></span>

<span data-ttu-id="652ac-159">不需要支援任何其他 OPM 狀態要求。</span><span class="sxs-lookup"><span data-stu-id="652ac-159">It is not necessary to support any other OPM status requests.</span></span>

<span data-ttu-id="652ac-160">在編解碼器方面，不需要 [**iopmvideooutput：： COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) 和 [**Iopmvideooutput：： Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) 方法，因此這些方法可以傳回 **E \_ >notimpl**。</span><span class="sxs-lookup"><span data-stu-id="652ac-160">The [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) and [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) methods are not required for codec merit, so these methods can return **E\_NOTIMPL**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="652ac-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="652ac-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="652ac-162">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="652ac-162">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="652ac-163">撰寫自訂的 MFT</span><span class="sxs-lookup"><span data-stu-id="652ac-163">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 



