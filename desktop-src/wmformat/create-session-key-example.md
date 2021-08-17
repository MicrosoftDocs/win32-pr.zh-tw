---
title: 建立工作階段金鑰範例
description: 建立工作階段金鑰範例
ms.assetid: 4347502b-3900-4306-b58c-16d151200e6c
keywords:
- Windows媒體格式 SDK，工作階段金鑰
- Windows媒體格式 SDK，內容金鑰
- Windows媒體格式 SDK，範例程式碼
- Windows媒體格式 SDK，程式碼範例
- 數位版權管理 (DRM) ，工作階段金鑰
- DRM (數位版權管理) ，工作階段金鑰
- 數位版權管理 (DRM) 、內容金鑰
- DRM (數位版權管理) 、內容金鑰
- 數位版權管理 (DRM) ，範例程式碼
- DRM (數位版權管理) ，範例程式碼
- 數位版權管理 (DRM) ，程式碼範例
- DRM (數位版權管理) ，程式碼範例
- DRM 用戶端擴充 Api，工作階段金鑰
- 用戶端擴充 Api、工作階段金鑰
- DRM 用戶端擴充 Api，內容金鑰
- 用戶端擴充 Api，內容金鑰
- DRM 用戶端擴充 Api，範例程式碼
- 用戶端擴充 Api，範例程式碼
- DRM 用戶端擴充 Api，程式碼範例
- 用戶端擴充 Api，程式碼範例
- 工作階段金鑰
- 內容金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef4a9c673b0aef24e010bff0f9a84beaf6321a81fe4ac8a8a9935c126983eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964137"
---
# <a name="create-session-key-example"></a>建立工作階段金鑰範例

工作階段金鑰是用來保護內容金鑰。 下列程式碼示範如何建立工作階段金鑰，但會留下隨機金鑰產生的詳細資料。


```C++
HRESULT CreateSessionKey( WMDRM_IMPORT_SESSION_KEY **ppSessionKey, DWORD *pcbSessionKey )
{
    // TODO: Set this value to the desired number of bytes for the session key data. 
    const DWORD SESSION_KEY_DATA_SIZE = 20; 

    HRESULT hr = S_OK;
    WMDRM_IMPORT_SESSION_KEY *pSessionKey = NULL;

    if( NULL == ppSessionKey )
    {
        hr = E_POINTER;
        goto EXIT;
    }
    
    // Compute the size of the session key structure plus the session key.
    DWORD cbSessionKey = sizeof( WMDRM_IMPORT_SESSION_KEY ) + SESSION_KEY_DATA_SIZE;

    // Allocate memory for the session key.
    pSessionKey = (WMDRM_IMPORT_SESSION_KEY *)new BYTE[ cbSessionKey ];
    if( NULL == pSessionKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }
    ZeroMemory( pSessionKey, cbSessionKey );

    // Set the key type and the key size.
    pSessionKey->dwKeyType = WMDRM_KEYTYPE_RC4;
    pSessionKey->cbKey = SESSION_KEY_DATA_SIZE;
    
    // Set the key to a random value. Note that the random number
    //  generator is not very good. It is only intended to be demonstrative
    //  and it is not recommended for use in shipping code.
    srand((unsigned int)time(NULL));
    BYTE* pKeyData = pSessionKey->rgbKey;
    for (size_t i = 0; i < SESSION_KEY_DATA_SIZE; ++i)
    {
        *pKeyData++ = (BYTE)(rand() & 0xFF); 
    }
    
    // If all has been successful set the parameters.
    *ppSessionKey = pSessionKey;
    pSessionKey = NULL;
    *pcbSessionKey = cbSessionKey;

EXIT:
    
    SAFE_ARRAY_DELETE( pSessionKey );
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DRM 匯入範例**](drm-import-examples.md)
</dt> </dl>

 

 




