---
description: 執行 DXVA-HD Array.blit
ms.assetid: fc68704e-68d5-4767-b464-e45ab4c86058
title: 執行 DXVA-HD Array.blit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37474cdb61136e3e201674695674ccb67abf03a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092706"
---
# <a name="performing-the-dxva-hd-blit"></a><span data-ttu-id="435ec-103">執行 DXVA-HD Array.blit</span><span class="sxs-lookup"><span data-stu-id="435ec-103">Performing the DXVA-HD Blit</span></span>


```C++
BOOL ProcessVideoFrame(HWND hwnd, UINT frameNumber)
{
    if (!g_pD3D || !g_pDXVAVP)
    {
        return FALSE;
    }

    RECT client;
    GetClientRect(hwnd, &client);

    if (IsRectEmpty(&client))
    {
        return TRUE;
    }

    // Check the current status of D3D9 device.  
    HRESULT hr = TestCooperativeLevel();

    switch (hr)
    {
    case D3D_OK :
        break;

    case D3DERR_DEVICELOST :
        return TRUE;

    case D3DERR_DEVICENOTRESET :
        return FALSE;
        break;

    default :
        return FALSE;
    }

    IDirect3DSurface9 *pRT = NULL;  // Render target

    DXVAHD_STREAM_DATA stream_data = { 0 };

    // Get the render-target surface.
    hr = g_pD3DDevice->GetBackBuffer(0, 0, D3DBACKBUFFER_TYPE_MONO, &pRT);
    if (FAILED(hr)) 
    { 
        goto done; 
    }

    // Initialize the stream data structures for the primary video stream 
    // and the substream.

    stream_data.Enable = TRUE;
    stream_data.OutputIndex = 0;
    stream_data.InputFrameOrField = 0;
    stream_data.pInputSurface = g_pSurface;
 
    // Perform the blit.
    hr = g_pDXVAVP->VideoProcessBltHD(
        pRT,
        frameNumber,
        1,
        &stream_data
        );

    if (FAILED(hr)) { 
        goto done; 
    }

    // Present the frame.
    hr = g_pD3DDevice->Present(NULL, NULL, NULL, NULL);

done:
    SafeRelease(&pRT);
    return SUCCEEDED(hr);
}
```



## <a name="related-topics"></a><span data-ttu-id="435ec-104">相關主題</span><span class="sxs-lookup"><span data-stu-id="435ec-104">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="435ec-105">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="435ec-105">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



