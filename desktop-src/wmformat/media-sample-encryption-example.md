---
title: 媒體範例加密範例
description: 媒體範例加密範例
ms.assetid: f57f9ffc-47fd-47fb-b553-07b9cd6abb70
keywords:
- Windows Media Format SDK，媒體範例加密
- Windows Media Format SDK，範例程式碼
- Windows Media Format SDK，程式碼範例
- 數位版權管理 (DRM) 、媒體範例加密
- DRM (數位版權管理) 、媒體範例加密
- 數位版權管理 (DRM) ，範例程式碼
- DRM (數位版權管理) ，範例程式碼
- 數位版權管理 (DRM) ，程式碼範例
- DRM (數位版權管理) ，程式碼範例
- DRM 用戶端擴充 Api、媒體範例加密
- 用戶端擴充 Api、媒體範例加密
- DRM 用戶端擴充 Api，範例程式碼
- 用戶端擴充 Api，範例程式碼
- DRM 用戶端擴充 Api，程式碼範例
- 用戶端擴充 Api，程式碼範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a669ab957aa7510cdd57daca798ec3e3ac3bf73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022044"
---
# <a name="media-sample-encryption-example"></a><span data-ttu-id="75d6c-118">媒體範例加密範例</span><span class="sxs-lookup"><span data-stu-id="75d6c-118">Media Sample Encryption Example</span></span>

<span data-ttu-id="75d6c-119">下列未完成的範例示範如何使用 DRM 加密來加密媒體範例。</span><span class="sxs-lookup"><span data-stu-id="75d6c-119">The following incomplete example demonstrates how to encrypt a media sample using DRM encryption.</span></span> <span data-ttu-id="75d6c-120">由於空間限制，RC4 加密演算法已保留在範例中。</span><span class="sxs-lookup"><span data-stu-id="75d6c-120">The RC4 encryption algorithm has been left out of the example due to space restrictions.</span></span>


```C++
QWORD GetNextSalt(QWORD qwSalt)
{
   return InterlockedIncrement64( (volatile LONGLONG*)&qwSalt );
}

HRESULT EncryptSample( INSSBuffer *pSample )
{
    HRESULT hr = S_OK;
    INSSBuffer3 *pNSSBuffer3 = NULL;
    QWORD qwSalt = 0;
    BYTE *pbData = NULL;
    DWORD cbData = 0;

    hr = pSample->QueryInterface( IID_INSSBuffer3, (void**)&pNSSBuffer3 );
    if( FAILED( hr ) ) goto EXIT;

    hr = pSample->GetBufferAndLength( &pbData, &cbData );
    if( FAILED( hr ) ) goto EXIT;

    qwSalt = GetNextSalt(qwSalt);

    // TODO: Encrypt the sample by concatenating the initialization vector
    //   and using RC4 encryption.

    hr = pNSSBuffer3->SetProperty( 
        WM_SampleExtensionGUID_SampleProtectionSalt, 
        &qwSalt, sizeof( qwSalt ) );
    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_RELEASE( pNSSBuffer3 );
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="75d6c-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="75d6c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75d6c-122">**DRM 匯入範例**</span><span class="sxs-lookup"><span data-stu-id="75d6c-122">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




