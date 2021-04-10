---
title: 初始化 DRM 匯入範例
description: 初始化 DRM 匯入範例
ms.assetid: 46a64305-9aac-47df-992d-6aea8ecb54bf
keywords:
- Windows Media Format SDK，DRM 匯入
- Windows Media Format SDK，匯入
- Windows Media Format SDK，範例程式碼
- Windows Media Format SDK，程式碼範例
- 數位版權管理 (DRM) ，匯入
- DRM (數位版權管理) ，匯入
- 數位版權管理 (DRM) ，初始化匯入
- DRM (數位版權管理) ，初始化匯入
- 數位版權管理 (DRM) ，範例程式碼
- DRM (數位版權管理) ，範例程式碼
- 數位版權管理 (DRM) ，程式碼範例
- DRM (數位版權管理) ，程式碼範例
- DRM 用戶端擴充 Api，初始化匯入
- 用戶端擴充 Api，初始化匯入
- DRM 用戶端擴充 Api，匯入
- 用戶端擴充 Api，匯入
- DRM 用戶端擴充 Api，範例程式碼
- 用戶端擴充 Api，範例程式碼
- DRM 用戶端擴充 Api，程式碼範例
- 用戶端擴充 Api，程式碼範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450eeaa128c17d0d64511dd028cda3ce1c4f28c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184049"
---
# <a name="initialize-drm-import-example"></a><span data-ttu-id="05d17-123">初始化 DRM 匯入範例</span><span class="sxs-lookup"><span data-stu-id="05d17-123">Initialize DRM Import Example</span></span>

<span data-ttu-id="05d17-124">下列程式碼範例說明如何初始化 drm 寫入器物件以進行 DRM 匯入：</span><span class="sxs-lookup"><span data-stu-id="05d17-124">The following code example illustrates how to initialize a DRM writer object for DRM Import:</span></span>


```C++
HRESULT InitializeImport( IWMDRMWriter3 *pDRMWriter )
{
    // Set this value to the desired number of bytes in an encrypted 
    //  session key.
    const int MODULUS_SIZE = 32;

    HRESULT hr = S_OK;
    WMDRM_IMPORT_INIT_STRUCT ImportInit;

    BYTE *pbEncryptedSessionKey = NULL;
    DWORD cbEncryptedSessionKey = 0;

    WMDRM_IMPORT_SESSION_KEY *pSessionKey = NULL;
    DWORD cbSessionKey = 0;

    WMDRM_IMPORT_CONTENT_KEY *pContentKey = NULL;
    DWORD cbContentKey = 0;
        
    // Allocate memory for the encrypted session key.
    pbEncryptedSessionKey = new BYTE[ MODULUS_SIZE ];
    if( NULL == pbEncryptedSessionKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }
    cbEncryptedSessionKey = MODULUS_SIZE;

    hr = CreateSessionKey( &pSessionKey, &cbSessionKey );
    if( FAILED( hr ) ) goto EXIT;

    if( cbSessionKey > MODULUS_SIZE )
    if( FAILED( hr ) ) goto EXIT;

    hr = CreateContentKey( &pContentKey, &cbContentKey );
    if( FAILED( hr ) ) goto EXIT;

    // TODO: Encrypt the content key with the session Key.    
    // TODO: Encrypt the session key with the machine certificate public key.   

    ImportInit.dwVersion = 0;
    ImportInit.pbEncryptedSessionKeyMessage = pbEncryptedSessionKey;
    ImportInit.cbEncryptedSessionKeyMessage = cbEncryptedSessionKey;
    ImportInit.pbEncryptedKeyMessage = (BYTE*)pContentKey;
    ImportInit.cbEncryptedKeyMessage = cbContentKey;

    hr = pDRMWriter->SetProtectStreamSamples( &ImportInit );
    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_ARRAY_DELETE( pContentKey );
    SAFE_ARRAY_DELETE( pSessionKey );

    return( hr );
}
```



## <a name="related-topics"></a><span data-ttu-id="05d17-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="05d17-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05d17-126">**建立內容金鑰範例**</span><span class="sxs-lookup"><span data-stu-id="05d17-126">**Create Content Key Example**</span></span>](create-content-key-example.md)
</dt> <dt>

[<span data-ttu-id="05d17-127">**建立工作階段金鑰範例**</span><span class="sxs-lookup"><span data-stu-id="05d17-127">**Create Session Key Example**</span></span>](create-session-key-example.md)
</dt> <dt>

[<span data-ttu-id="05d17-128">**DRM 匯入範例**</span><span class="sxs-lookup"><span data-stu-id="05d17-128">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




