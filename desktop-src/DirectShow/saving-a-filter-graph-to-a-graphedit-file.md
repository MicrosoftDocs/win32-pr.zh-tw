---
description: 將篩選圖形儲存至 GraphEdit 檔案
ms.assetid: f7eeae3c-506b-484c-8fe5-ddd391af5a59
title: 將篩選圖形儲存至 GraphEdit 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5fb24c40f11dbeb5dad8b542f0f152449f8951
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106999824"
---
# <a name="saving-a-filter-graph-to-a-graphedit-file"></a>將篩選圖形儲存至 GraphEdit 檔案

下列程式碼範例示範如何將篩選圖形儲存至 GraphEdit (. grf) 檔。 這在對您的應用程式進行偵錯工具時會很有用。


```C++
HRESULT SaveGraphFile(IGraphBuilder *pGraph, WCHAR *wszPath) 
{
    const WCHAR wszStreamName[] = L"ActiveMovieGraph"; 
    HRESULT hr;
    
    IStorage *pStorage = NULL;
    hr = StgCreateDocfile(
        wszPath,
        STGM_CREATE | STGM_TRANSACTED | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0, &pStorage);
    if(FAILED(hr)) 
    {
        return hr;
    }

    IStream *pStream;
    hr = pStorage->CreateStream(
        wszStreamName,
        STGM_WRITE | STGM_CREATE | STGM_SHARE_EXCLUSIVE,
        0, 0, &pStream);
    if (FAILED(hr)) 
    {
        pStorage->Release();    
        return hr;
    }

    IPersistStream *pPersist = NULL;
    pGraph->QueryInterface(IID_IPersistStream, (void**)&pPersist);
    hr = pPersist->Save(pStream, TRUE);
    pStream->Release();
    pPersist->Release();
    if (SUCCEEDED(hr)) 
    {
        hr = pStorage->Commit(STGC_DEFAULT);
    }
    pStorage->Release();
    return hr;
}
```



例如，下列程式碼會建立檔案播放圖形，並將它儲存至名為 MyGraph grf 的檔案：


```C++
void __cdecl main(void)
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    CoInitialize(NULL);
    
    // Create the Filter Graph Manager and render a file.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
        IID_IGraphBuilder, reinterpret_cast<void**>(&pGraph));
    hr = pGraph->RenderFile(L"C:\\Video.avi", NULL);

    if (SUCCEEDED(hr))
    {
        hr = SaveGraphFile(pGraph, L"C:\\MyGraph.grf");
    }
    
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 GraphEdit 模擬圖表建立](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[**StgCreateDocfile**](/windows/win32/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> </dl>

 

 
