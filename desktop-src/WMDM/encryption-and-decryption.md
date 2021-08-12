---
title: 加密和解密
description: 加密和解密
ms.assetid: 6aef4138-0391-4edd-b4fc-d6d0ec3c735b
keywords:
- Windows媒體裝置管理員，加密
- 裝置管理員，加密
- 桌面應用程式，加密
- 服務提供者，加密
- 程式設計指南，加密
- 加密
- Windows媒體裝置管理員、解密
- 裝置管理員，解密
- 桌面應用程式，解密
- 服務提供者，解密
- 程式設計指南，解密
- 解密
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c154910709007e502c1505fc6fc3274665942c9eabe8e24de5b30fe932d813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584666"
---
# <a name="encryption-and-decryption"></a>加密和解密

Windows媒體裝置管理員需要加密服務提供者和應用程式之間傳送的檔案。 完成此步驟的方式有兩種：

-   如果服務提供者只支援 [**IMDSPObject：： Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) 和 [**IMDSPObject：： Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)，則必須分別使用 [CSecureChannelClient](csecurechannelclient-class.md) 和 [CSecureChannelServer](csecurechannelserver-class.md) 方法，以將資料加密和解密為應用程式和服務提供者。
-   如果服務提供者支援 [**IMDSPObject2：： ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) 和 [**IMDSPObject2：： WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel)，則您的應用程式可以避免昂貴的安全通道訊息驗證。  (保留安全通道，讓未執行 [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) 的舊版服務提供者仍能繼續運作。 ) 

加密需求可防止惡意應用程式取得在軟體元件之間傳遞的資料，同時也可保護在裝置上傳送之資料的完整性。

下列三種方法需要加密或解密。



| 方法                                                                          | 描述                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMDMOperation::TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) |  (的應用程式) 加密或解密，視應用程式是否正在傳送或接收資料而定。 |
| [**IMDSPObject：： Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)                                   |  (服務提供者) 加密。                                                                             |
| [**IMDSPObject：： Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)                                 |  (服務提供者) 解密。                                                                             |



 

加密和解密都是透過單一方法呼叫來完成。 加密是透過 [**CSecureChannelClient：： EncryptParam**](/previous-versions/bb231587(v=vs.85)) （適用于應用程式）或 [**CSecureChannelServer：： EncryptParam**](/previous-versions/ms868509(v=msdn.10)) （代表服務提供者）來完成。 解密是由 CSecureChannelClient：適用于應用程式的 [**:D ecryptparam**](/previous-versions/bb231586(v=vs.85)) 或 CSecureChannelServer：適用于服務提供者的 [**:D ecryptparam**](/previous-versions/bb231598(v=vs.85)) 所完成。 用戶端和伺服器方法之間的參數相同。

下列步驟說明如何加密和解密資料。 只有當您的應用程式與不會執行 [IWMDMOperation3：： TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel)的舊版服務提供者通訊時，這些步驟才有其重要性。 )  (

**加密**

1.  為加密資料建立 MAC 金鑰，如 [訊息驗證](message-authentication.md)中所述。
2.  使用要加密的資料來呼叫 **EncryptParam** ，以執行就地加密。

下列程式碼範例示範服務提供者的 [**IMDSPObject：： Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)執行。 這個方法會使用要加密的資料和資料的大小來建立 MAC 金鑰，然後將兩者都傳送給應用程式。


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



**解密**

1.  使用要加密的資料來呼叫 **DecryptParam** ，以執行就地解密。
2.  確認解密資料的 MAC 金鑰，如 [訊息驗證](message-authentication.md)中所述。

下列程式碼範例示範服務提供者的 [**IMDSPObject：： Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)執行。 這個方法會使用要加密的資料和資料的大小來建立 MAC 金鑰，然後將兩者都傳送給應用程式。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用安全驗證通道**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 