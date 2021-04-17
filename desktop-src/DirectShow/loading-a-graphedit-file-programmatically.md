---
description: 以程式設計方式載入 GraphEdit 檔案
ms.assetid: 0e1cff4e-43f8-4d0a-b7a7-b6d0278e9e4a
title: 以程式設計方式載入 GraphEdit 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a4780ead7b65d883bdd48917c6372425612435
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467698"
---
# <a name="loading-a-graphedit-file-programmatically"></a><span data-ttu-id="5c40d-103">以程式設計方式載入 GraphEdit 檔案</span><span class="sxs-lookup"><span data-stu-id="5c40d-103">Loading a GraphEdit File Programmatically</span></span>

<span data-ttu-id="5c40d-104">應用程式可以使用 **IPersistStream** 介面載入 GraphEdit (. grf) 檔。</span><span class="sxs-lookup"><span data-stu-id="5c40d-104">An application can use the **IPersistStream** interface to load a GraphEdit (.grf) file.</span></span> <span data-ttu-id="5c40d-105">使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="5c40d-105">Use the following code:</span></span>


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
> <span data-ttu-id="5c40d-106">在先前的程式碼範例中，對 **IPersistStream：： Load** 的呼叫可能會傳回 DirectShow 錯誤或成功碼。</span><span class="sxs-lookup"><span data-stu-id="5c40d-106">The call to **IPersistStream::Load** in the previous code example can return a DirectShow error or success code.</span></span> <span data-ttu-id="5c40d-107">如需可能傳回值的清單，請參閱 [錯誤和成功碼](error-and-success-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="5c40d-107">For a list of possible return values, see [Error and Success Codes](error-and-success-codes.md).</span></span>

 

<span data-ttu-id="5c40d-108">GraphEdit 檔案僅供測試和偵測之用。</span><span class="sxs-lookup"><span data-stu-id="5c40d-108">GraphEdit files are intended only for testing and debugging.</span></span> <span data-ttu-id="5c40d-109">它們並非供使用者應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="5c40d-109">They are not meant for use by end-user applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c40d-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c40d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c40d-111">使用 GraphEdit 模擬圖表建立</span><span class="sxs-lookup"><span data-stu-id="5c40d-111">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[<span data-ttu-id="5c40d-112">**StgIsStorageFile**</span><span class="sxs-lookup"><span data-stu-id="5c40d-112">**StgIsStorageFile**</span></span>](/windows/win32/api/coml2api/nf-coml2api-stgisstoragefile)
</dt> <dt>

[<span data-ttu-id="5c40d-113">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="5c40d-113">**StgOpenStorage**</span></span>](/windows/win32/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 
