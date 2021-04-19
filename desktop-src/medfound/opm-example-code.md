---
description: 本主題包含使用輸出保護管理員的範例程式碼。
ms.assetid: ad2303a0-f3f3-43a0-83eb-023640da2ece
title: OPM 範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9883643829815d27725c392e2c4f13f34e816988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977805"
---
# <a name="opm-example-code"></a><span data-ttu-id="a0b26-103">OPM 範例程式碼</span><span class="sxs-lookup"><span data-stu-id="a0b26-103">OPM Example Code</span></span>

<span data-ttu-id="a0b26-104">本主題包含使用 [輸出保護管理員](output-protection-manager.md)的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="a0b26-104">This topic contains example code for using [Output Protection Manager](output-protection-manager.md).</span></span>

<span data-ttu-id="a0b26-105">本主題中的範例程式碼示範如何執行 OPM 交握、傳送狀態要求，以及傳送 OPM 命令。</span><span class="sxs-lookup"><span data-stu-id="a0b26-105">The example code in this topic demonstrates how to perform the OPM handshake, send a status request, and send an OPM command.</span></span> <span data-ttu-id="a0b26-106">針對密碼編譯作業，程式碼會使用密碼編譯 API：新一代 (CNG) 。</span><span class="sxs-lookup"><span data-stu-id="a0b26-106">For cryptographic operations, the code uses Cryptography API: Next Generation (CNG).</span></span> <span data-ttu-id="a0b26-107">本主題的重點是要顯示 OPM 功能，因此不會顯示與 x.509 憑證相關的工作，例如剖析和驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="a0b26-107">The focus of this topic is to show OPM functionality, so tasks related to the X.509 certificate, such as parsing and validating the certificate, are not shown.</span></span>

<span data-ttu-id="a0b26-108">本主題所顯示的程式會在 [使用「輸出保護管理員](using-output-protection-manager.md)」中有更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="a0b26-108">The procedures shown in this topic are explained in more detail in [Using Output Protection Manager](using-output-protection-manager.md).</span></span>

-   [<span data-ttu-id="a0b26-109">執行 OPM 交握</span><span class="sxs-lookup"><span data-stu-id="a0b26-109">Performing the OPM Handshake</span></span>](#performing-the-opm-handshake)
-   [<span data-ttu-id="a0b26-110">傳送 OPM 狀態要求</span><span class="sxs-lookup"><span data-stu-id="a0b26-110">Sending an OPM Status Request</span></span>](#sending-an-opm-status-request)
-   [<span data-ttu-id="a0b26-111">傳送 OPM 命令</span><span class="sxs-lookup"><span data-stu-id="a0b26-111">Sending an OPM Command</span></span>](#sending-an-opm-command)
-   [<span data-ttu-id="a0b26-112">計算 OMAC-1 值</span><span class="sxs-lookup"><span data-stu-id="a0b26-112">Computing the OMAC-1 Value</span></span>](#computing-the-omac-1-value)
-   [<span data-ttu-id="a0b26-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="a0b26-113">Related topics</span></span>](#related-topics)

## <a name="performing-the-opm-handshake"></a><span data-ttu-id="a0b26-114">執行 OPM 交握</span><span class="sxs-lookup"><span data-stu-id="a0b26-114">Performing the OPM Handshake</span></span>

1.  <span data-ttu-id="a0b26-115">列舉 OPM 裝置並選取影片輸出之後 (未顯示) ，第一個步驟是呼叫 [**IOPMVideoOutput：： StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) 來取得裝置的 x.509 憑證鏈：</span><span class="sxs-lookup"><span data-stu-id="a0b26-115">After enumerating the OPM devices and selecting a video output (not shown), the first step is to call [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) to get the device's X.509 certificate chain:</span></span>

    ```C++
        OPM_RANDOM_NUMBER random;   // Random number from driver.
        ZeroMemory(&random, sizeof(random));

        BYTE *pbCertificate = NULL; // Pointer to a buffer to hold the certificate.
        ULONG cbCertificate = 0;    // Size of the certificate in bytes.

        PUBLIC_KEY_VALUES *pKey = NULL; // The driver's public key.

        // Get the driver's certificate chain + random number
        hr = pVideoOutput->StartInitialization(
            &random, 
            &pbCertificate, 
            &cbCertificate
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Validate the X.509 certificate. (Not shown.)
        hr = ValidateX509Certificate(pbCertificate, cbCertificate);

        if (FAILED(hr))
        {
            goto done;
        }

        // Get the public key from the certificate. (Not shown.)
        hr = GetPublicKeyFromCertificate(
            pbCertificate,
            cbCertificate,
            &pKey
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Load and initialize a CNG provider (Cryptography API: Next Generation)

        BCRYPT_ALG_HANDLE hAlg = 0;

        hr = BCryptOpenAlgorithmProvider(
            &hAlg, 
            BCRYPT_RSA_ALGORITHM, 
            MS_PRIMITIVE_PROVIDER, 
            0
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Import the public key into the CNG provider.

        BCRYPT_KEY_HANDLE hPublicKey = 0;

        // Import the RSA public key.
        hr = ImportRsaPublicKey(hAlg, pKey, &hPublicKey);

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  <span data-ttu-id="a0b26-116">應用程式必須驗證憑證鏈，並從鏈中的分葉憑證取得公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="a0b26-116">The application must validate the certificate chain and get the public key from the leaf certificate in the chain.</span></span> <span data-ttu-id="a0b26-117">這些步驟不會顯示在這裡。</span><span class="sxs-lookup"><span data-stu-id="a0b26-117">Those steps are not shown here.</span></span>
3.  <span data-ttu-id="a0b26-118">擁有公開金鑰之後，您就可以將金鑰匯入至 CNG 演算法提供者。</span><span class="sxs-lookup"><span data-stu-id="a0b26-118">Once you have the public key, you can import the key into a CNG algorithm provider.</span></span> <span data-ttu-id="a0b26-119">呼叫 **BCryptOpenAlgorithmProvider** 函數以載入提供者。</span><span class="sxs-lookup"><span data-stu-id="a0b26-119">Call the **BCryptOpenAlgorithmProvider** function to load the provider.</span></span> <span data-ttu-id="a0b26-120">應用程式定義的函式會匯 `ImportRsaPublicKey` 入金鑰，並將控制碼傳回至匯入的金鑰：</span><span class="sxs-lookup"><span data-stu-id="a0b26-120">The application-defined `ImportRsaPublicKey` function imports the key and returns a handle to the imported key:</span></span>
    ```C++
    void ReverseMemCopy(BYTE *pbDest, BYTE const *pbSource, DWORD cb)
    {
        for (DWORD i = 0; i < cb; i++) 
        {
            pbDest[cb - 1 - i] = pbSource[i];
        }
    }
    ```

    

    ```C++
    //------------------------------------------------------------------------
    //
    // ImportRsaPublicKey
    //
    // Converts an RSA public key from an RSAPUBKEY blob into an 
    // BCRYPT_RSAKEY_BLOB and sets the public key on the CNG provider.
    //
    //------------------------------------------------------------------------

    HRESULT ImportRsaPublicKey(
        BCRYPT_ALG_HANDLE hAlg,     // CNG provider
        PUBLIC_KEY_VALUES *pKey,    // Pointer to the RSAPUBKEY blob.
        BCRYPT_KEY_HANDLE *phKey    // Receives a handle the imported public key.
        )
    {
        HRESULT hr = S_OK;

        BYTE *pbPublicKey = NULL;
        DWORD cbKey = 0;

        // Layout of the RSA public key blob:

        //  +----------------------------------------------------------------+
        //  |     BCRYPT_RSAKEY_BLOB    | BE( dwExp ) |   BE( Modulus )      |
        //  +----------------------------------------------------------------+
        //
        //  sizeof(BCRYPT_RSAKEY_BLOB)       cbExp           cbModulus 
        //  <--------------------------><------------><---------------------->
        //
        //   BE = Big Endian Format                                                     

        DWORD cbModulus = (pKey->rsapubkey.bitlen + 7) / 8;
        DWORD dwExp = pKey->rsapubkey.pubexp;
        DWORD cbExp = (dwExp & 0xFF000000) ? 4 :
                      (dwExp & 0x00FF0000) ? 3 :
                      (dwExp & 0x0000FF00) ? 2 : 1;

        BCRYPT_RSAKEY_BLOB *pRsaBlob;
        PBYTE pbCurrent;

        hr = DWordAdd(cbModulus, sizeof(BCRYPT_RSAKEY_BLOB), &cbKey);

        if (FAILED(hr))
        {
            goto done;
        }

        cbKey += cbExp;

        pbPublicKey = (BYTE*)CoTaskMemAlloc(cbKey);
        if (NULL == pbPublicKey) 
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }    
        
        ZeroMemory(pbPublicKey, cbKey);
        pRsaBlob = (BCRYPT_RSAKEY_BLOB *)(pbPublicKey);
        
        // Make the Public Key Blob Header
        pRsaBlob->Magic = BCRYPT_RSAPUBLIC_MAGIC;
        pRsaBlob->BitLength = pKey->rsapubkey.bitlen;
        pRsaBlob->cbPublicExp = cbExp;
        pRsaBlob->cbModulus = cbModulus;
        pRsaBlob->cbPrime1 = 0;
        pRsaBlob->cbPrime2 = 0;

        pbCurrent = (PBYTE)(pRsaBlob + 1);
        
        // Copy pubExp Big Endian 
        ReverseMemCopy(pbCurrent, (PBYTE)&dwExp, cbExp);
        pbCurrent += cbExp;

        // Copy Modulus Big Endian 
        ReverseMemCopy(pbCurrent, pKey->modulus, cbModulus);

        // Set the key.
        hr = BCryptImportKeyPair(
            hAlg, 
            NULL, 
            BCRYPT_RSAPUBLIC_BLOB, 
            phKey,
            (PUCHAR)pbPublicKey,
            cbKey,
            0
            );

    done:
        CoTaskMemFree(pbPublicKey);
        return hr;
    }
    ```

    

4.  <span data-ttu-id="a0b26-121">接下來，準備包含起始序號和 AES 工作階段金鑰的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a0b26-121">Next, prepare the buffer that contains the starting sequence numbers and the AES session key.</span></span>
    ```C++
    void CopyAndAdvancePtr(BYTE*& pDest, const BYTE* pSrc, DWORD cb)
    {
        memcpy(pDest, pSrc, cb);
        pDest += cb;
    }
    ```

    

    ```C++
        //--------------------------------------------------------------------
        // Prepare the signature for key exchnage.
        //--------------------------------------------------------------------

        UINT uStatusSeq = 0;     // Status sequence number.
        UINT uCommandSeq = 0;    // Command sequence number.

        OPM_RANDOM_NUMBER AesKey;   // Session key

        // Generate the starting sequence number for queries.
        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&uStatusSeq, 
            sizeof(UINT), 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }


        // Generate the starting sequence number for commands.
        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&uCommandSeq, 
            sizeof(UINT), 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Generate the AES session key.
        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&AesKey, 
            sizeof(AesKey), 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Fill in the initialization structure.
        OPM_ENCRYPTED_INITIALIZATION_PARAMETERS initParams;
        ZeroMemory(&initParams, sizeof(initParams));
        
        // Use a temporary pointer for copying into the array.
        BYTE *pBuffer = &initParams.abEncryptedInitializationParameters[0];

        CopyAndAdvancePtr(pBuffer, random.abRandomNumber, sizeof(random)); // Random number from the friver.
        CopyAndAdvancePtr(pBuffer, AesKey.abRandomNumber, sizeof(AesKey)); // Session key.
        CopyAndAdvancePtr(pBuffer, (BYTE*)&uStatusSeq, sizeof(uStatusSeq));
        CopyAndAdvancePtr(pBuffer, (BYTE*)&uCommandSeq, sizeof(uCommandSeq));
    ```

    

5.  <span data-ttu-id="a0b26-122">使用驅動程式的公開金鑰，以 RSAES-PKCS1-OAEP 加密加密此緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a0b26-122">Encrypt this buffer with RSAES-OAEP encryption, using the driver's public key.</span></span>
    ```C++
        //--------------------------------------------------------------------
        // RSAES-OAEP encrypt the signature. Use SHA2 hashing algorithm.
        //--------------------------------------------------------------------

        PBYTE pbDataIn = &initParams.abEncryptedInitializationParameters[0];
        ULONG cbDataIn = (ULONG)(pBuffer - pbDataIn);  

        DWORD cbOutput = 0;
        DWORD cbDataOut= 0;

        BYTE *pbDataOut = NULL;

        BCRYPT_OAEP_PADDING_INFO paddingInfo;
        ZeroMemory(&paddingInfo, sizeof(paddingInfo));

        paddingInfo.pszAlgId = BCRYPT_SHA512_ALGORITHM;

        //Encrypt the signature.
        hr = BCryptEncrypt(
            hPublicKey,
            (PUCHAR)pbDataIn,
            cbDataIn,
            &paddingInfo,
            NULL,
            0,
            NULL,
            0,
            &cbOutput,
            BCRYPT_PAD_OAEP
            );

        if (FAILED(hr))
        {
            goto done;
        }


        pbDataOut = new (std::nothrow) BYTE[cbOutput];
        if (NULL == pbDataOut) 
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }
        
        hr = BCryptEncrypt(
            hPublicKey,
            (PUCHAR)pbDataIn,
            cbDataIn,
            &paddingInfo,
            NULL,
            0,
            pbDataOut,
            cbOutput,
            &cbDataOut,
            BCRYPT_PAD_OAEP
            );

        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

6.  <span data-ttu-id="a0b26-123">呼叫 [**IOPMVideoOutput：： FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) 來完成交握。</span><span class="sxs-lookup"><span data-stu-id="a0b26-123">Call [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) to complete the handshake.</span></span>
    ```C++
        // Complete the handshake.
        hr = pVideoOutput->FinishInitialization(
            (OPM_ENCRYPTED_INITIALIZATION_PARAMETERS *)pbDataOut
            );

        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

## <a name="sending-an-opm-status-request"></a><span data-ttu-id="a0b26-124">傳送 OPM 狀態要求</span><span class="sxs-lookup"><span data-stu-id="a0b26-124">Sending an OPM Status Request</span></span>

<span data-ttu-id="a0b26-125">下一個範例顯示如何傳送 [**OPM \_ GET \_ CONNECTOR \_ 類型**](opm-get-connector-type.md) 狀態要求。</span><span class="sxs-lookup"><span data-stu-id="a0b26-125">The next example shows how to send the [**OPM\_GET\_CONNECTOR\_TYPE**](opm-get-connector-type.md) status request.</span></span>

1.  <span data-ttu-id="a0b26-126">使用狀態要求的資訊填入 [**OPM \_ 取得 \_ 資訊 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) 結構。</span><span class="sxs-lookup"><span data-stu-id="a0b26-126">Fill in an [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure with the information for the status request.</span></span>
    ```C++
        //--------------------------------------------------------------------
        // Prepare the status request structure.
        //--------------------------------------------------------------------

        OPM_GET_INFO_PARAMETERS     StatusInput;
        OPM_REQUESTED_INFORMATION   StatusOutput;

        ZeroMemory(&StatusInput, sizeof(StatusInput));
        ZeroMemory(&StatusOutput, sizeof(StatusOutput));

        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&(StatusInput.rnRandomNumber), 
            OPM_128_BIT_RANDOM_NUMBER_SIZE, 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }

        StatusInput.guidInformation = OPM_GET_CONNECTOR_TYPE; // Request GUID.
        StatusInput.ulSequenceNumber = uStatusSeq;            // Sequence number.

        //  Sign the request structure, not including the omac field.

        hr = ComputeOMAC(
            AesKey,                                             // Session key.
            (BYTE*)&StatusInput + OPM_OMAC_SIZE,                // Data
            sizeof(OPM_GET_INFO_PARAMETERS) - OPM_OMAC_SIZE,    // Size
            &StatusInput.omac                                   // Receives the OMAC
            );

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  <span data-ttu-id="a0b26-127">[**OPM \_ 取得 \_ 資訊 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)結構的 **OMAC** 成員是單一金鑰的 CBC MAC (針對結構的其餘部分計算的 omac) 。</span><span class="sxs-lookup"><span data-stu-id="a0b26-127">The **omac** member of the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure is a one-key CBC MAC (OMAC) computed for the rest of the structure.</span></span> <span data-ttu-id="a0b26-128">稍後所示的 ComputeOMAC 函式 () 宣告如下：</span><span class="sxs-lookup"><span data-stu-id="a0b26-128">The ComputeOMAC function (shown later) is declared as follows:</span></span>
    ```C++
    HRESULT ComputeOMAC(
        OPM_RANDOM_NUMBER&  AesKey,     // Session key
        PUCHAR pb,                      // Data
        DWORD cb,                       // Size
        OPM_OMAC *pTag                  // Receives the OMAC
        );
    ```

    

3.  <span data-ttu-id="a0b26-129">呼叫 [**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) 以傳送狀態要求。</span><span class="sxs-lookup"><span data-stu-id="a0b26-129">Call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) to send the status request.</span></span>
    ```C++
        //  Send the status request.
        hr = pVideoOutput->GetInformation(&StatusInput, &StatusOutput);

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

4.  <span data-ttu-id="a0b26-130">驅動程式會將回應寫入至 [**OPM \_ 所要求的 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) 結構。</span><span class="sxs-lookup"><span data-stu-id="a0b26-130">The driver writes the response to the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure.</span></span> <span data-ttu-id="a0b26-131">回應結構包含 OMAC 值，此值是針對結構的其餘部分所計算。</span><span class="sxs-lookup"><span data-stu-id="a0b26-131">The response structure includes an OMAC value, computed for the remainder of the structure.</span></span> <span data-ttu-id="a0b26-132">信任回應資料之前，請先確認此值：</span><span class="sxs-lookup"><span data-stu-id="a0b26-132">Verify this value before trusting the response data:</span></span>
    ```C++
        //--------------------------------------------------------------------
        // Verify the signature.
        //--------------------------------------------------------------------

        OPM_OMAC rgbSignature = { 0 };

        // Calculate our own signature.

        hr = ComputeOMAC(
            AesKey,
            (BYTE*)&StatusOutput + OPM_OMAC_SIZE, 
            sizeof(OPM_REQUESTED_INFORMATION) - OPM_OMAC_SIZE, 
            &rgbSignature
            );

        if (FAILED(hr))
        {
            goto done;
        }

        if (memcmp(StatusOutput.omac.abOMAC, rgbSignature.abOMAC, OPM_OMAC_SIZE))
        {
            // The signature does not match.
            hr = E_FAIL; 
            goto done;
        }

        // Update the sequence number.
        uStatusSeq++;
    ```

    

5.  <span data-ttu-id="a0b26-133">[**OPM 所 \_ 要求之 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)結構的 **abRequestedInformation** 成員包含回應資料。</span><span class="sxs-lookup"><span data-stu-id="a0b26-133">The **abRequestedInformation** member of the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure contains the response data.</span></span> <span data-ttu-id="a0b26-134">針對 [**OPM \_ GET \_ CONNECTOR \_ 型**](opm-get-connector-type.md) 別要求，回應資料是由 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) 結構所組成。</span><span class="sxs-lookup"><span data-stu-id="a0b26-134">For the [**OPM\_GET\_CONNECTOR\_TYPE**](opm-get-connector-type.md) request, the response data consists of a [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span>
    ```C++
        // Examine the response. 
        // The response data is an OPM_STANDARD_INFORMATION structure.

        OPM_STANDARD_INFORMATION StatusInfo;
        ZeroMemory(&StatusInfo, sizeof(StatusInfo));

        ULONG cbLen = min(sizeof(OPM_STANDARD_INFORMATION), StatusOutput.cbRequestedInformationSize);    

        if (cbLen != 0)
        {
            // Copy the repinse into the array.
            CopyMemory((BYTE*)&StatusInfo, StatusOutput.abRequestedInformation, cbLen);
        }
        
        //  Verify the random number.
        if (0!= memcmp(
            (BYTE*)&StatusInfo.rnRandomNumber, 
            (BYTE*)&StatusInput.rnRandomNumber, 
            sizeof(OPM_RANDOM_NUMBER)) 
            ) 
        {
            hr = E_FAIL;
            goto done;
        }    

        // Verify the status of the OPM session.
        if (StatusInfo.ulStatusFlags != OPM_STATUS_NORMAL)
        {
            // Abnormal status
            hr = E_FAIL;
            goto done;
        }    
        
        ULONG ConnectorType = StatusInfo.ulInformation & OPM_BUS_TYPE_MASK;
    ```

    

## <a name="sending-an-opm-command"></a><span data-ttu-id="a0b26-135">傳送 OPM 命令</span><span class="sxs-lookup"><span data-stu-id="a0b26-135">Sending an OPM Command</span></span>

<span data-ttu-id="a0b26-136">下一個範例顯示如何藉由傳送 [**OPM \_ SET \_ Protection \_ LEVEL**](opm-set-protection-level.md) 命令，來啟用 High-Bandwidth 數位內容保護 (HDCP) 。</span><span class="sxs-lookup"><span data-stu-id="a0b26-136">The next example shows how to enable High-Bandwidth Digital Content Protection (HDCP) by sending the [**OPM\_SET\_PROTECTION\_LEVEL**](opm-set-protection-level.md) command.</span></span>

1.  <span data-ttu-id="a0b26-137">所有 OPM 命令都使用 [**OPM \_ 設定 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) 結構來輸入資料。</span><span class="sxs-lookup"><span data-stu-id="a0b26-137">All OPM commands use the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure for input data.</span></span> <span data-ttu-id="a0b26-138">此結構中的 **abParameters** 陣列包含命令特有的資料。</span><span class="sxs-lookup"><span data-stu-id="a0b26-138">The **abParameters** array in this structure contains command-specific data.</span></span> <span data-ttu-id="a0b26-139">針對 [**OPM \_ set \_ protection \_ level**](opm-set-protection-level.md) 命令， **abParameters** 陣列包含 [**OPM \_ SET \_ 保護 \_ 層級的 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) 結構。</span><span class="sxs-lookup"><span data-stu-id="a0b26-139">For the [**OPM\_SET\_PROTECTION\_LEVEL**](opm-set-protection-level.md) command, the **abParameters** array contains an [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure.</span></span> <span data-ttu-id="a0b26-140">填寫此結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="a0b26-140">Fill in this structure as follows:</span></span>
    ```C++
        //--------------------------------------------------------------------
        // Prepare the command structure.
        //--------------------------------------------------------------------

        // Data specific to the OPM_SET_PROTECTION_LEVEL command.
        OPM_SET_PROTECTION_LEVEL_PARAMETERS CommandInput;

        ZeroMemory(&CommandInput, sizeof(CommandInput));

        CommandInput.ulProtectionType = OPM_PROTECTION_TYPE_HDCP;   
        CommandInput.ulProtectionLevel = OPM_HDCP_ON;        

        ULONG ulAdditionalParametersSize = 0;
        BYTE* pbAdditionalParameters = NULL;
    ```

    

2.  <span data-ttu-id="a0b26-141">接下來，填寫 [**OPM \_ 設定 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) 結構並計算 OMAC。</span><span class="sxs-lookup"><span data-stu-id="a0b26-141">Next, fill in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure and compute the OMAC.</span></span>
    ```C++
        // Common command parameters
        OPM_CONFIGURE_PARAMETERS Command;
        ZeroMemory(&Command, sizeof(Command));

        Command.guidSetting = OPM_SET_PROTECTION_LEVEL;
        Command.ulSequenceNumber = uCommandSeq;
        Command.cbParametersSize = sizeof(OPM_SET_PROTECTION_LEVEL_PARAMETERS);
        CopyMemory(&Command.abParameters[0], (BYTE*)&CommandInput, Command.cbParametersSize);

        //  Sign the command structure, not including the omac field.
        hr = ComputeOMAC(
            AesKey,
            (BYTE*)&Command + OPM_OMAC_SIZE, 
            sizeof(OPM_CONFIGURE_PARAMETERS) - OPM_OMAC_SIZE,
            &Command.omac
            );

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

3.  <span data-ttu-id="a0b26-142">若要傳送命令，請呼叫 [**IOPMVideoOutput：： Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)。</span><span class="sxs-lookup"><span data-stu-id="a0b26-142">To send the command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="a0b26-143">請記得在每個命令之後遞增命令序號。</span><span class="sxs-lookup"><span data-stu-id="a0b26-143">Remember to increment the command sequence number after each command.</span></span>
    ```C++
        //  Send the command.
        hr = pVideoOutput->Configure(
            &Command, 
            0,      // Size of additional command data.
            NULL    // Additional command data.
            );

        if (FAILED(hr))
        {
            goto done;
        }

        //  Update the sequence number.
        uCommandSeq++;    
    ```

    

4.  <span data-ttu-id="a0b26-144">若要確認是否已啟用 HDCP，請傳送 [**OPM \_ 取得 \_ 虛擬 \_ 保護 \_ 層級**](opm-get-virtual-protection-level.md) 狀態要求 (未顯示) 。</span><span class="sxs-lookup"><span data-stu-id="a0b26-144">To verify that HDCP is enabled, send an [**OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL**](opm-get-virtual-protection-level.md) status request (not shown).</span></span>

## <a name="computing-the-omac-1-value"></a><span data-ttu-id="a0b26-145">計算 OMAC-1 值</span><span class="sxs-lookup"><span data-stu-id="a0b26-145">Computing the OMAC-1 Value</span></span>

<span data-ttu-id="a0b26-146">下列程式碼說明如何計算用來簽署 OPM 命令和要求結構的 OMAC-1 值。</span><span class="sxs-lookup"><span data-stu-id="a0b26-146">The following code shows how to compute the OMAC-1 value that is used to sign the OPM command and request structures.</span></span>


```C++
// Helper functions for some bitwise operations.

#define AES_BLOCKLEN    (16)
#define AES_KEYSIZE_128 (16)

inline void XOR( 
    BYTE *lpbLHS, 
    const BYTE *lpbRHS, 
    DWORD cbSize = AES_BLOCKLEN 
    )
{
    for( DWORD i = 0; i < cbSize; i++ )
    {
        lpbLHS[i] ^= lpbRHS[i];
    }
}

inline void LShift(const BYTE *lpbOpd, BYTE *lpbRes)
{
    for( DWORD i = 0; i < AES_BLOCKLEN; i++ )
    {
        lpbRes[i] = lpbOpd[i] << 1;
        if( i < AES_BLOCKLEN - 1 )
        {
            lpbRes[i] |= ( (unsigned char)lpbOpd[i+1] ) >> 7;
        }
    }
}

//  Generate OMAC1 signature using AES128

HRESULT ComputeOMAC(
    OPM_RANDOM_NUMBER&  AesKey,     // Session key
    PUCHAR pb,                      // Data
    DWORD cb,                       // Size of the data
    OPM_OMAC *pTag                  // Receives the OMAC
    )
{
    HRESULT hr = S_OK;
    BCRYPT_ALG_HANDLE hAlg = NULL;
    BCRYPT_KEY_HANDLE hKey = NULL;
    DWORD cbKeyObject = 0;
    DWORD cbData = 0;
    PBYTE pbKeyObject = NULL;

    PUCHAR Key = (PUCHAR)AesKey.abRandomNumber;

    struct 
    {
        BCRYPT_KEY_DATA_BLOB_HEADER Header;
        UCHAR Key[AES_KEYSIZE_128];
    } KeyBlob;

    KeyBlob.Header.dwMagic = BCRYPT_KEY_DATA_BLOB_MAGIC;
    KeyBlob.Header.dwVersion = BCRYPT_KEY_DATA_BLOB_VERSION1;
    KeyBlob.Header.cbKeyData = AES_KEYSIZE_128;
    CopyMemory(KeyBlob.Key, Key, sizeof(KeyBlob.Key));

    BYTE rgbLU[OPM_OMAC_SIZE];
    BYTE rgbLU_1[OPM_OMAC_SIZE];
    BYTE rBuffer[OPM_OMAC_SIZE];

    hr = BCryptOpenAlgorithmProvider(
        &hAlg, 
        BCRYPT_AES_ALGORITHM, 
        MS_PRIMITIVE_PROVIDER, 
        0
        );

    //  Get the size needed for the key data
    if (S_OK == hr) 
    {
        hr = BCryptGetProperty(
            hAlg, 
            BCRYPT_OBJECT_LENGTH, 
            (PBYTE)&cbKeyObject, 
            sizeof(DWORD), 
            &cbData, 
            0
            );
    }

    //  Allocate the key data object
    if (S_OK == hr) 
    {
        pbKeyObject = new (std::nothrow) BYTE[cbKeyObject];
        if (NULL == pbKeyObject) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    //  Set to CBC chain mode
    if (S_OK == hr) 
    {
        hr = BCryptSetProperty(
            hAlg, 
            BCRYPT_CHAINING_MODE, 
            (PBYTE)BCRYPT_CHAIN_MODE_CBC, 
            sizeof(BCRYPT_CHAIN_MODE_CBC), 
            0
            );
    }

    //  Set the key
    if (S_OK == hr) 
    {
        hr = BCryptImportKey(hAlg, NULL, BCRYPT_KEY_DATA_BLOB, &hKey, 
            pbKeyObject, cbKeyObject, (PUCHAR)&KeyBlob, sizeof(KeyBlob), 0);
    }

    //  Encrypt 0s
    if (S_OK == hr) 
    {
        DWORD cbBuffer = sizeof(rBuffer);
        ZeroMemory(rBuffer, sizeof(rBuffer));

        hr = BCryptEncrypt(hKey, rBuffer, cbBuffer, NULL, NULL, 0, 
            rBuffer, sizeof(rBuffer), &cbBuffer, 0);
    }

    //  Compute OMAC1 parameters
    if (S_OK == hr)
    {
        const BYTE bLU_ComputationConstant = 0x87;
        LPBYTE pbL = rBuffer;

        LShift( pbL, rgbLU );
        if( pbL[0] & 0x80 )
        {
            rgbLU[OPM_OMAC_SIZE - 1] ^= bLU_ComputationConstant;
        }
        LShift( rgbLU, rgbLU_1 );
        if( rgbLU[0] & 0x80 )
        {
            rgbLU_1[OPM_OMAC_SIZE - 1] ^= bLU_ComputationConstant;
        }
    }

    //  Generate the hash. 
    if (S_OK == hr) 
    {
        // Redo the key to restart the CBC.

        BCryptDestroyKey(hKey);
        hKey = NULL;

        hr = BCryptImportKey(hAlg, NULL, BCRYPT_KEY_DATA_BLOB, &hKey,
            pbKeyObject, cbKeyObject, (PUCHAR)&KeyBlob, sizeof(KeyBlob), 0);
    }

    if (S_OK == hr) 
    {
        PUCHAR pbDataInCur = pb;
        cbData = cb;
        do
        {
            DWORD cbBuffer = 0;

            if (cbData > OPM_OMAC_SIZE) 
            {
                CopyMemory( rBuffer, pbDataInCur, OPM_OMAC_SIZE );

                hr = BCryptEncrypt(hKey, rBuffer, sizeof(rBuffer), NULL, 
                    NULL, 0, rBuffer, sizeof(rBuffer), &cbBuffer, 0);

                pbDataInCur += OPM_OMAC_SIZE;
                cbData -= OPM_OMAC_SIZE;
            }
            else 
            {   
                if (cbData == OPM_OMAC_SIZE)
                {
                    CopyMemory(rBuffer, pbDataInCur, OPM_OMAC_SIZE);
                    XOR(rBuffer, rgbLU);
                }
                else 
                {
                    ZeroMemory( rBuffer, OPM_OMAC_SIZE );
                    CopyMemory( rBuffer, pbDataInCur, cbData );
                    rBuffer[ cbData ] = 0x80;

                    XOR(rBuffer, rgbLU_1);
                }

                hr = BCryptEncrypt(hKey, rBuffer, sizeof(rBuffer), NULL, NULL, 
                    0, (PUCHAR)pTag->abOMAC, OPM_OMAC_SIZE, &cbBuffer, 0);

                cbData = 0;
            }
                
        } while( S_OK == hr && cbData > 0 );
    }

    //  Clean up
    if (hKey)
    {
        BCryptDestroyKey(hKey);
    }
    if (hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg, 0);
    }
    delete [] pbKeyObject;
    return hr;
}
```



<span data-ttu-id="a0b26-147">OMAC-1 演算法的詳細說明 <https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html> 。</span><span class="sxs-lookup"><span data-stu-id="a0b26-147">The OMAC-1 algorithm is described in detail at <https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html>.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0b26-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="a0b26-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0b26-149">輸出保護管理員</span><span class="sxs-lookup"><span data-stu-id="a0b26-149">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



