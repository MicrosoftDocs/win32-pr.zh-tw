---
title: 加密和解密
description: 加密和解密
ms.assetid: 6aef4138-0391-4edd-b4fc-d6d0ec3c735b
keywords:
- Windows Media 裝置管理員，加密
- 裝置管理員，加密
- 桌面應用程式，加密
- 服務提供者，加密
- 程式設計指南，加密
- 加密
- Windows Media 裝置管理員，解密
- 裝置管理員，解密
- 桌面應用程式，解密
- 服務提供者，解密
- 程式設計指南，解密
- 解密
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78688c1b4ca9991d8b322c6991de96a51e7e8d22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382661"
---
# <a name="encryption-and-decryption"></a><span data-ttu-id="df57d-115">加密和解密</span><span class="sxs-lookup"><span data-stu-id="df57d-115">Encryption and Decryption</span></span>

<span data-ttu-id="df57d-116">Windows Media 裝置管理員需要加密服務提供者和應用程式之間傳送的檔案。</span><span class="sxs-lookup"><span data-stu-id="df57d-116">Windows Media Device Manager requires encryption of files sent between the service provider and the application.</span></span> <span data-ttu-id="df57d-117">完成此步驟的方式有兩種：</span><span class="sxs-lookup"><span data-stu-id="df57d-117">This can be done in one of two ways:</span></span>

-   <span data-ttu-id="df57d-118">如果服務提供者只支援 [**IMDSPObject：： Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) 和 [**IMDSPObject：： Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)，則必須分別使用 [CSecureChannelClient](csecurechannelclient-class.md) 和 [CSecureChannelServer](csecurechannelserver-class.md) 方法，以將資料加密和解密為應用程式和服務提供者。</span><span class="sxs-lookup"><span data-stu-id="df57d-118">If the service provider supports only [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) and [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), the data must be encrypted and decrypted by the application and service provider by using [CSecureChannelClient](csecurechannelclient-class.md) and [CSecureChannelServer](csecurechannelserver-class.md) methods respectively.</span></span>
-   <span data-ttu-id="df57d-119">如果服務提供者支援 [**IMDSPObject2：： ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) 和 [**IMDSPObject2：： WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel)，則您的應用程式可以避免昂貴的安全通道訊息驗證。</span><span class="sxs-lookup"><span data-stu-id="df57d-119">If the service provider supports [**IMDSPObject2::ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) and [**IMDSPObject2::WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel), your application can avoid costly secure channel message authentication.</span></span> <span data-ttu-id="df57d-120"> (保留安全通道，讓未執行 [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) 的舊版服務提供者仍能繼續運作。 ) </span><span class="sxs-lookup"><span data-stu-id="df57d-120">(The secure channel is retained so that legacy service providers that do not implement [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) can still continue to function.)</span></span>

<span data-ttu-id="df57d-121">加密需求可防止惡意應用程式取得在軟體元件之間傳遞的資料，同時也可保護在裝置上傳送之資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="df57d-121">The encryption requirement prevents malicious applications from obtaining data that is being passed between software components, and also protects the integrity of data being sent to or from the device.</span></span>

<span data-ttu-id="df57d-122">下列三種方法需要加密或解密。</span><span class="sxs-lookup"><span data-stu-id="df57d-122">The following three methods require encryption or decryption.</span></span>



| <span data-ttu-id="df57d-123">方法</span><span class="sxs-lookup"><span data-stu-id="df57d-123">Method</span></span>                                                                          | <span data-ttu-id="df57d-124">描述</span><span class="sxs-lookup"><span data-stu-id="df57d-124">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df57d-125">**IWMDMOperation::TransferObjectData**</span><span class="sxs-lookup"><span data-stu-id="df57d-125">**IWMDMOperation::TransferObjectData**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) | <span data-ttu-id="df57d-126"> (的應用程式) 加密或解密，視應用程式是否正在傳送或接收資料而定。</span><span class="sxs-lookup"><span data-stu-id="df57d-126">(Application) Encryption or decryption, depending on whether the application is sending or receiving data.</span></span> |
| [<span data-ttu-id="df57d-127">**IMDSPObject：： Read**</span><span class="sxs-lookup"><span data-stu-id="df57d-127">**IMDSPObject::Read**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)                                   | <span data-ttu-id="df57d-128"> (服務提供者) 加密。</span><span class="sxs-lookup"><span data-stu-id="df57d-128">(Service provider) Encryption.</span></span>                                                                             |
| [<span data-ttu-id="df57d-129">**IMDSPObject：： Write**</span><span class="sxs-lookup"><span data-stu-id="df57d-129">**IMDSPObject::Write**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)                                 | <span data-ttu-id="df57d-130"> (服務提供者) 解密。</span><span class="sxs-lookup"><span data-stu-id="df57d-130">(Service Provider) Decryption.</span></span>                                                                             |



 

<span data-ttu-id="df57d-131">加密和解密都是透過單一方法呼叫來完成。</span><span class="sxs-lookup"><span data-stu-id="df57d-131">Encryption and decryption are both done by single method calls.</span></span> <span data-ttu-id="df57d-132">加密是透過 [**CSecureChannelClient：： EncryptParam**](/previous-versions/bb231587(v=vs.85)) （適用于應用程式）或 [**CSecureChannelServer：： EncryptParam**](/previous-versions/ms868509(v=msdn.10)) （代表服務提供者）來完成。</span><span class="sxs-lookup"><span data-stu-id="df57d-132">Encryption is done by [**CSecureChannelClient::EncryptParam**](/previous-versions/bb231587(v=vs.85)) for applications or by [**CSecureChannelServer::EncryptParam**](/previous-versions/ms868509(v=msdn.10)) for service providers.</span></span> <span data-ttu-id="df57d-133">解密是由 CSecureChannelClient：適用于應用程式的 [**:D ecryptparam**](/previous-versions/bb231586(v=vs.85)) 或 CSecureChannelServer：適用于服務提供者的 [**:D ecryptparam**](/previous-versions/bb231598(v=vs.85)) 所完成。</span><span class="sxs-lookup"><span data-stu-id="df57d-133">Decryption is done by [**CSecureChannelClient::DecryptParam**](/previous-versions/bb231586(v=vs.85)) for applications or [**CSecureChannelServer::DecryptParam**](/previous-versions/bb231598(v=vs.85)) for service providers.</span></span> <span data-ttu-id="df57d-134">用戶端和伺服器方法之間的參數相同。</span><span class="sxs-lookup"><span data-stu-id="df57d-134">The parameters are identical between the client and server methods.</span></span>

<span data-ttu-id="df57d-135">下列步驟說明如何加密和解密資料。</span><span class="sxs-lookup"><span data-stu-id="df57d-135">The following steps show how to encrypt and decrypt data.</span></span> <span data-ttu-id="df57d-136">只有當您的應用程式與不會執行 [IWMDMOperation3：： TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel)的舊版服務提供者通訊時，這些步驟才有其重要性。 )  (</span><span class="sxs-lookup"><span data-stu-id="df57d-136">(These steps are important only if your application communicates with a legacy service provider that does not implement [IWMDMOperation3::TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel).)</span></span>

<span data-ttu-id="df57d-137">**加密**</span><span class="sxs-lookup"><span data-stu-id="df57d-137">**Encryption**</span></span>

1.  <span data-ttu-id="df57d-138">為加密資料建立 MAC 金鑰，如 [訊息驗證](message-authentication.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="df57d-138">Create the MAC key for the encrypted data, as described in [Message Authentication](message-authentication.md).</span></span>
2.  <span data-ttu-id="df57d-139">使用要加密的資料來呼叫 **EncryptParam** ，以執行就地加密。</span><span class="sxs-lookup"><span data-stu-id="df57d-139">Call **EncryptParam** with the data to encrypt, to perform in-place encryption.</span></span>

<span data-ttu-id="df57d-140">下列程式碼範例示範服務提供者的 [**IMDSPObject：： Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)執行。</span><span class="sxs-lookup"><span data-stu-id="df57d-140">The following code example demonstrates a service provider's implementation of [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read).</span></span> <span data-ttu-id="df57d-141">這個方法會使用要加密的資料和資料的大小來建立 MAC 金鑰，然後將兩者都傳送給應用程式。</span><span class="sxs-lookup"><span data-stu-id="df57d-141">This method creates the MAC key using the data to encrypt and the size of the data, and sends them both to the application.</span></span>


```C++
HRESULT CMyStorage::Read(
    BYTE  *pData,
    DWORD *pdwSize,
    BYTE   abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwToRead;         // Bytes to read.
    DWORD    dwRead   = NULL;  // Bytes read.
    BYTE    *pTmpData = NULL;  // Temporary buffer to hold data before 
                               // it is copied to pData.

    // Use a global CSecureChannelServer member to verify that 
    // the client is authenticated.
    if (!(g_pAppSCServer->fIsAuthenticated()))
    {
        return WMDM_E_NOTCERTIFIED;
    }
    

    // Verify that the handle to the file to read is valid.
    if(m_hFile == INVALID_HANDLE_VALUE)
    {
        return E_FAIL;
    }

    // Create a buffer to hold the data read.    
    dwToRead = *pdwSize;
    pTmpData = new BYTE [dwToRead] ;
    if(!pTmpData)
        return E_OUTOFMEMORY;

    // Read data into the temporary buffer.
    if(ReadFile(m_hFile,(LPVOID)pTmpData,dwToRead,&dwRead,NULL)) 
    { 
        *pdwSize = dwRead; 

        if( dwRead )
        {
            // Create a MAC from all the parameters.
            // CORg is a macro that goes to Error label on failure.
            // MAC consists of data and size of data.
            HMAC hMAC;
            
            CORg(g_pAppSCServer->MACInit(&hMAC));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), dwRead));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(DWORD)));
            CORg(g_pAppSCServer->MACFinal(hMAC, abMac));
            
            // Encrypt the data.
            CORg(g_pAppSCServer->EncryptParam(pTmpData, dwRead));
            
            // Copy data from the temporary buffer into the out parameter.
            memcpy(pData, pTmpData, dwRead);
        }
    
        hr = S_OK; 
    }
    else
    { 
        *pdwSize = 0; 

        hr = E_FAIL; 
    }

Error:

    if(pTmpData) 
    {
        delete [] pTmpData;
    }

    return hr;
} 
```



<span data-ttu-id="df57d-142">**解密**</span><span class="sxs-lookup"><span data-stu-id="df57d-142">**Decryption**</span></span>

1.  <span data-ttu-id="df57d-143">使用要加密的資料來呼叫 **DecryptParam** ，以執行就地解密。</span><span class="sxs-lookup"><span data-stu-id="df57d-143">Call **DecryptParam** with the data to encrypt, to perform in-place decryption.</span></span>
2.  <span data-ttu-id="df57d-144">確認解密資料的 MAC 金鑰，如 [訊息驗證](message-authentication.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="df57d-144">Verify the MAC key for the decrypted data, as described in [Message Authentication](message-authentication.md).</span></span>

<span data-ttu-id="df57d-145">下列程式碼範例示範服務提供者的 [**IMDSPObject：： Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)執行。</span><span class="sxs-lookup"><span data-stu-id="df57d-145">The following code example demonstrates a service provider's implementation of [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write).</span></span> <span data-ttu-id="df57d-146">這個方法會使用要加密的資料和資料的大小來建立 MAC 金鑰，然後將兩者都傳送給應用程式。</span><span class="sxs-lookup"><span data-stu-id="df57d-146">This method creates the MAC key using the data to encrypt and the size of the data, and sends them both to the application.</span></span>


```C++
HRESULT CMyStorage::Write(BYTE *pData, DWORD *pdwSize,
                                 BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwWritten = 0;
    BYTE    *pTmpData  = NULL;          // Temporary buffer to hold the 
                                        // data during decryption.
    BYTE     pTempMac[WMDM_MAC_LENGTH]; // Temporary MAC that will be 
                                        // copied into the abMac
                                        // out parameter.

    if( m_hFile == INVALID_HANDLE_VALUE )
    {
        return E_FAIL;
    }

    // Allocate the temporary buffer and copy the encrypted data into it.
    pTmpData = new BYTE [*pdwSize];
    if(!pTmpData)
        return E_OUTOFMEMORY;
    memcpy(pTmpData, pData, *pdwSize);

    // Decrypt the data.
    CHRg(g_pAppSCServer->DecryptParam(pTmpData, *pdwSize));

    // Check the MAC passed to the method. The MAC is built from
    // the data and data size parameters.
    // CORg is a macro that goes to the Error label on failure.
    HMAC hMAC;
    CORg(g_pAppSCServer->MACInit(&hMAC));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), *pdwSize));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(*pdwSize)));
    CORg(g_pAppSCServer->MACFinal(hMAC, pTempMac));

    // If the MAC values don't match, return an error.
    if (memcmp(abMac, pTempMac, WMDM_MAC_LENGTH) != 0)
    {
        hr = WMDM_E_MAC_CHECK_FAILED;
        goto Error;
    }

    // The MAC values matched, so write the decrypted data to a local file.
    if( WriteFile(m_hFile,pTmpData,*pdwSize,&dwWritten,NULL) ) 
    {
        hr = S_OK;
    }
    else 
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    *pdwSize = dwWritten;

Error:

    if( pTmpData )
    {
        delete [] pTmpData;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="df57d-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="df57d-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df57d-148">**使用安全驗證通道**</span><span class="sxs-lookup"><span data-stu-id="df57d-148">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 