---
description: 影片串流範例程式碼
ms.assetid: 735af042-9800-4f75-a5c9-e1cf17b4a472
title: 影片串流範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e9a738503174e7bcc6c0d0e7c1250e39348b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981454"
---
# <a name="video-streaming-sample-code"></a>影片串流範例程式碼

> [!Note]  
> 這些 Api 已被取代。 應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md) 篩選器或執行自訂篩選，以從 DirectShow 篩選圖形取得資料。

 

此範例程式碼會讀取檔案，並將它轉譯為主要 DirectDraw 介面。 為了簡潔起見，此範例會執行基本的錯誤檢查。


```C++
#include <stdio.h>
#include "ddraw.h"       // DirectDraw interfaces
#include "mmstream.h"    // multimedia stream interfaces
#include "amstream.h"    // DirectShow multimedia stream interfaces
#include "ddstream.h"    // DirectDraw multimedia stream interfaces

HRESULT RenderStreamToSurface(IDirectDrawSurface *pSurface, 
    IMultiMediaStream *pMMStream)
{    
    IMediaStream *pPrimaryVidStream;    
    IDirectDrawMediaStream *pDDStream;
    IDirectDrawStreamSample *pSample;
    RECT rect;
    DDSURFACEDESC ddsd;

    HRESULT hr;
    hr = pMMStream->GetMediaStream(MSPID_PrimaryVideo, &pPrimaryVidStream);
    if (FAILED(hr))
    {
        return hr;
    }
    pPrimaryVidStream->QueryInterface(IID_IDirectDrawMediaStream, (void **)&pDDStream);

    ddsd.dwSize = sizeof(ddsd);
    hr = pDDStream->GetFormat(&ddsd, NULL, NULL, NULL);
    if (SUCCEEDED(hr))
    {
        rect.top = rect.left = 0;
        rect.bottom = ddsd.dwHeight;
        rect.right = ddsd.dwWidth;
        hr = pDDStream->CreateSample(pSurface, &rect, 0, &pSample);
        if (SUCCEEDED(hr))
        {
            pMMStream->SetState(STREAMSTATE_RUN);
            while (pSample->Update(0, NULL, NULL, NULL) == S_OK)
            {
                // Empty loop.
            }
            pMMStream->SetState(STREAMSTATE_STOP);
            pSample->Release();    
        }
    }
    pDDStream->Release();
    pPrimaryVidStream->Release();
    return hr;
}

HRESULT RenderFileToMMStream(
    const char * szFileName, 
    IMultiMediaStream **ppMMStream,
    IDirectDraw *pDD)
{
    if (strlen(szFileName) > MAX_PATH)
    {
        return E_INVALIDARG;
    }

    IAMMultiMediaStream *pAMStream;
    HRESULT hr = CoCreateInstance(CLSID_AMMultiMediaStream, NULL, 
        CLSCTX_INPROC_SERVER, IID_IAMMultiMediaStream, 
        (void **)&pAMStream);
    if (FAILED(hr))
    {
        return hr;
    }

    WCHAR wPath[MAX_PATH + 1];
    MultiByteToWideChar(CP_ACP, 0, szFileName, -1, wPath, MAX_PATH + 1);

    pAMStream->Initialize(STREAMTYPE_READ, AMMSF_NOGRAPHTHREAD, NULL);
    pAMStream->AddMediaStream(pDD, &MSPID_PrimaryVideo, 0, NULL);
    pAMStream->AddMediaStream(NULL, &MSPID_PrimaryAudio, AMMSF_ADDDEFAULTRENDERER, NULL);
    hr = pAMStream->OpenFile(wPath, 0);
    if (SUCCEEDED(hr))
    {
        hr = pAMStream->QueryInterface(IID_IMultiMediaStream, 
            (void**)ppMMStream);
    }
    pAMStream->Release();
    return hr;
}

int __cdecl main(int argc, char *argv[])    
{    
    if (argc < 2) 
    {
        printf("Usage : showstrm movie.ext\n");
        exit(0);
    }    

    DDSURFACEDESC ddsd;
    IDirectDraw *pDD;    
    IDirectDrawSurface *pPrimarySurface;
    IMultiMediaStream *pMMStream;

    CoInitialize(NULL);

    DirectDrawCreate(NULL, &pDD, NULL);
    pDD->SetCooperativeLevel(GetDesktopWindow(), DDSCL_NORMAL);

    ddsd.dwSize = sizeof(ddsd);
    ddsd.dwFlags = DDSD_CAPS;
    ddsd.ddsCaps.dwCaps = DDSCAPS_PRIMARYSURFACE;
    pDD->CreateSurface(&ddsd, &pPrimarySurface, NULL);

    HRESULT hr = RenderFileToMMStream(argv[1], &pMMStream, pDD);
    if (SUCCEEDED(hr))
    {
        RenderStreamToSurface(pPrimarySurface, pMMStream);    
        pMMStream->Release();
    }
    pPrimarySurface->Release();    
    pDD->Release(); 
    
    CoUninitialize();
    return 0;
}
```



 

 



