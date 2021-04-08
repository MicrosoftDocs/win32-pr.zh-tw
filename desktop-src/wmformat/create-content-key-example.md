---
title: 建立內容金鑰範例
description: 建立內容金鑰範例
ms.assetid: 8e75bac3-d1fb-4a72-8088-fe5ff0899ac2
keywords:
- Windows Media Format SDK，內容金鑰
- Windows Media Format SDK，範例程式碼
- Windows Media Format SDK，程式碼範例
- 數位版權管理 (DRM) 、內容金鑰
- DRM (數位版權管理) 、內容金鑰
- 數位版權管理 (DRM) ，範例程式碼
- DRM (數位版權管理) ，範例程式碼
- 數位版權管理 (DRM) ，程式碼範例
- DRM (數位版權管理) ，程式碼範例
- DRM 用戶端擴充 Api，內容金鑰
- 用戶端擴充 Api，內容金鑰
- DRM 用戶端擴充 Api，範例程式碼
- 用戶端擴充 Api，範例程式碼
- DRM 用戶端擴充 Api，程式碼範例
- 用戶端擴充 Api，程式碼範例
- 內容金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881dfd0d318d7d699b44ca9c3f77f22f9acfc689
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022070"
---
# <a name="create-content-key-example"></a><span data-ttu-id="533d3-119">建立內容金鑰範例</span><span class="sxs-lookup"><span data-stu-id="533d3-119">Create Content Key Example</span></span>

<span data-ttu-id="533d3-120">內容金鑰是用來加密 Windows Media DRM 匯入的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="533d3-120">The content key is used to encrypt media samples for Windows Media DRM Import.</span></span> <span data-ttu-id="533d3-121">下列程式碼範例示範如何建立及初始化內容金鑰結構。</span><span class="sxs-lookup"><span data-stu-id="533d3-121">The following code example demonstrates how to create and initialize a content key structure.</span></span>


```C++
HRESULT CreateContentKey( WMDRM_IMPORT_CONTENT_KEY **ppContentKey, DWORD *pcbContentKey)
{
    // TODO: Set this value to the desired number of bytes for the content key data. 
    const DWORD IV_DATA_SIZE = 16;
    HRESULT hr = S_OK;
    WMDRM_IMPORT_CONTENT_KEY *pContentKey = NULL;

    // The content key.
    const BYTE rgbContentKey[] = {
        0x67, 0x39, 0x83, 0xb9,
        0x52, 0xa8, 0xe3
    };        
    const DWORD CONTENT_KEY_DATA_SIZE = sizeof(rgbContentKey);

    // Compute the total size of the content key structure
    DWORD cbContentKey = sizeof( WMDRM_IMPORT_CONTENT_KEY ) +
      IV_DATA_SIZE + CONTENT_KEY_DATA_SIZE;

    // Make sure we have a valid 
    if( NULL == ppContentKey )
    {
        hr = E_POINTER;
        goto EXIT;
    }

    // Allocate the content key, locally first
    pContentKey = (WMDRM_IMPORT_CONTENT_KEY *)new BYTE[ cbContentKey ];
    
    // Check the allocation was successful 
    if( NULL == pContentKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }

    // Ininitalize the key
    ZeroMemory( pContentKey, cbContentKey );
    pContentKey->dwVersion = 0;
    pContentKey->cbStructSize = cbContentKey;

    // Set the initialization vector key type 
    pContentKey->dwIVKeyType = WMDRM_KEYTYPE_RC4;
    pContentKey->cbIVKey = IV_DATA_SIZE;
    
    // Generate a random initialization vector. Note that this random number
    //  generator is not very good. It is only intended to be demonstrative
    //  and it is not recommended for use in commercial strength code.
    srand((unsigned int)time(NULL));
    BYTE* pKeyData = pContentKey->rgbKeyData;
    for (size_t i = 0; i < IV_DATA_SIZE; ++i)
    {
        *pKeyData++ = (BYTE)(rand() & 0xFF); 
    }   
    
    // Set the content key type.
    pContentKey->dwContentKeyType = WMDRM_KEYTYPE_COCKTAIL;
    pContentKey->cbContentKey = CONTENT_KEY_DATA_SIZE;

    // Fill out the content key. 
    for (size_t i = 0; i < CONTENT_KEY_DATA_SIZE; ++i)
    {
        *pKeyData++ = rgbContentKey[i]; 
    }   
    

    // If all has been successful, set the parameters
    *ppContentKey = pContentKey;
    pContentKey = NULL;
    *pcbContentKey = cbContentKey;

EXIT:
    SAFE_ARRAY_DELETE( pContentKey );
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="533d3-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="533d3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="533d3-123">**DRM 匯入範例**</span><span class="sxs-lookup"><span data-stu-id="533d3-123">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




