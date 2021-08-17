---
description: 以程式設計方式載入 GraphEdit 檔案
ms.assetid: 0e1cff4e-43f8-4d0a-b7a7-b6d0278e9e4a
title: 以程式設計方式載入 GraphEdit 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf2bdff86a47e740e6cb177a70a7b1e12ffc7c865d8ad231f6ada9122f286d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153176"
---
# <a name="loading-a-graphedit-file-programmatically"></a>以程式設計方式載入 GraphEdit 檔案

應用程式可以使用 **IPersistStream** 介面載入 GraphEdit (. grf) 檔。 使用下列程式碼：


```C++
HRESULT LoadGraphFile(IGraphBuilder *pGraph, const WCHAR* wszName)
{
    IStorage *pStorage = 0;
    if (S_OK != StgIsStorageFile(wszName))
    {
        return E_FAIL;
    }
    HRESULT hr = StgOpenStorage(wszName, 0, 
        STGM_TRANSACTED | STGM_READ | STGM_SHARE_DENY_WRITE, 
        0, 0, &pStorage);
    if (FAILED(hr))
    {
        return hr;
    }
    IPersistStream *pPersistStream = 0;
    hr = pGraph->QueryInterface(IID_IPersistStream,
             reinterpret_cast<void**>(&pPersistStream));
    if (SUCCEEDED(hr))
    {
        IStream *pStream = 0;
        hr = pStorage->OpenStream(L"ActiveMovieGraph", 0, 
            STGM_READ | STGM_SHARE_EXCLUSIVE, 0, &pStream);
        if(SUCCEEDED(hr))
        {
            hr = pPersistStream->Load(pStream);
            pStream->Release();
        }
        pPersistStream->Release();
    }
    pStorage->Release();
    return hr;
}

```



> [!Note]  
> 在先前的程式碼範例中，對 **IPersistStream：： Load** 的呼叫可能會傳回 DirectShow 錯誤或成功碼。 如需可能傳回值的清單，請參閱 [錯誤和成功碼](error-and-success-codes.md)。

 

GraphEdit 檔案僅供測試和偵測之用。 它們並非供使用者應用程式使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 GraphEdit 模擬 Graph 建立](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[**StgIsStorageFile**](/windows/win32/api/coml2api/nf-coml2api-stgisstoragefile)
</dt> <dt>

[**StgOpenStorage**](/windows/win32/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 
