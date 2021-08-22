---
description: 說明如何在 Direct3D 9 中使用硬體覆蓋。
ms.assetid: fa9d5bf5-4c0f-471a-b639-d329b0cd89a4
title: 硬體覆蓋支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f537c91bc217344206c0a23cf5ca8a14254a9c983e4ae550e96457bbb055e5d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600398"
---
# <a name="hardware-overlay-support"></a>硬體覆蓋支援

硬體重迭是視訊記憶體的私人區域，可在主要介面上重迭。 當重迭顯示時，不會執行任何複製。 覆迭作業是在硬體中執行，而不需要修改主要介面中的資料。

使用硬體重迭來播放影片在舊版 Windows 中很常見，因為重迭對於具有高畫面播放速率的影片內容而言很有效率。 從 Windows 7 開始，Direct3D 9 支援硬體覆蓋。 這項支援主要是為了播放影片，而且與舊版 DirectDraw Api 的部分不同：

-   無法壓縮、鏡像或 deinterlaced 重迭。
-   不支援來源色彩索引鍵和 Alpha 混色。
-   如果重迭硬體支援重迭，則重迭可能會延長。 否則，不支援延展。 在實務上，並非所有圖形驅動程式都支援伸展。
-   每個裝置最多支援一個重迭。
-   重迭是使用目的色鍵來執行，但是 Direct3D runtime 會自動選取色彩並繪製目的矩形。 Direct3D 會自動追蹤視窗的位置，並在每次呼叫 **PresentEx** 時更新覆迭的位置。

### <a name="creating-a-hardware-overlay-surface"></a>建立硬體重迭表面

若要查詢重迭支援，請呼叫 **IDirect3D9：： GetDeviceCaps**。 如果驅動程式支援硬體重迭，則會在 D3DCAPS9 中設定 D3DCAPS 重迭旗標 **\_** **。Caps** 成員。

若要瞭解給定的顯示模式是否支援特定的重迭格式，請呼叫 [**IDirect3D9ExOverlayExtension：： CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype)。

若要建立覆迭，請呼叫 **IDirect3D9Ex：： CreateDeviceEx** ，並指定 D3DSWAPEFFECT 重迭交換效果。 **\_** 如果硬體支援，則背景緩衝區可以使用非 RGB 格式。

重迭表面有下列限制：

-   應用程式無法建立一個以上的重迭交換鏈。
-   重迭必須在視窗模式中使用。 無法在全螢幕模式中使用。
-   重迭交換效果必須搭配 **IDirect3DDevice9Ex** 介面使用。 **IDirect3DDevice9** 不支援此功能。
-   無法使用多級取樣。
-   不支援 **D3DPRESENT \_ DONOTFLIP** 和 **D3DPRESENT \_ FLIPRESTART** 旗標。
-   無法針對重迭表面使用簡報統計資料。

如果硬體不支援延展，建議您建立與顯示模式大的交換鏈，讓視窗可以調整大小為任何維度。 重新建立交換鏈並不是處理調整視窗大小的最佳方式，因為這可能會造成嚴重的轉譯成品。 此外，由於 GPU 管理覆迭記憶體的方式，重新建立交換鏈可能會導致應用程式用盡視頻記憶體。

### <a name="new-d3dpresent_parameters-flags"></a>新的 D3DPRESENT \_ 參數旗標

下列 **D3DPRESENT \_ 參數** 旗標是針對建立覆迭而定義的。



| 旗標                                      | 描述                                                                                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DPRESENTFLAG 重迭 \_ \_ LIMITEDRGB**   | RGB 範圍是16–235。 預設值為0–255。 <br/> 需要 **D3DOVERLAYCAPS \_ LIMITEDRANGERGB** 功能。<br/>                                                 |
| **D3DPRESENTFLAG 重迭 \_ \_ YCbCr \_ BT709** | YUV 色彩使用709定義。 預設值為 BT. 601。 <br/> 需要 **D3DOVERLAYCAPS \_ YCbCr \_ BT709** 功能。<br/>                                      |
| **D3DPRESENTFLAG 重迭 \_ \_ YCbCr \_ xvYCC** | 使用外延 YCbCr (xvYCC) 輸出資料。<br/> 需要 **D3DOVERLAYCAPS \_ YCbCr \_ BT601 \_ xvYCC** 或 **D3DOVERLAYCAPS \_ YCbCr \_ BT709 \_ xvYCC** 的功能。<br/> |



 

### <a name="using-hardware-overlays"></a>使用硬體覆蓋

為了顯示重迭表面，應用程式會呼叫 **IDirect3DDevice9Ex：:P resentex**。 Direct3D runtime 會自動繪製目的色鍵。

以下是針對重迭定義的 **PresentEx** 旗標。



| 旗標                              | 描述                                                                                                                                                                                                                                                                           |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DPRESENT \_ UPDATECOLORKEY**    | 如果桌面視窗管理員 (DWM) 組合已停用，請設定這個旗標。 此旗標會導致 Direct3D 重繪色彩索引鍵。<br/> 如果已啟用 DWM，則不需要此旗標，因為 Direct3D 會在 DWM 用來重新導向的介面上繪製一次色彩鍵。<br/> |
| **D3DPRESENT \_ HIDEOVERLAY**       | 隱藏覆迭。                                                                                                                                                                                                                                                                    |
| **D3DPRESENT \_ UPDATEOVERLAYONLY** | 更新覆迭而不變更內容。<br/> 如果視窗在影片暫停時移動，這個旗標就很有用。<br/>                                                                                                                                           |



 

應用程式應該準備好處理下列案例：

-   如果另一個應用程式正在使用覆迭， **PresentEx** 會傳回 **D3DERR \_ NOTAVAILABLE**。
-   如果將視窗移到另一個監視器，應用程式必須重新建立交換鏈。 否則，若應用程式呼叫 **PresentEx** 以在不同的監視器上顯示覆迭，則 **PresentEx** 會傳回 **D3DERR \_ INVALIDDEVICE**。
-   如果顯示模式變更，Direct3D 會嘗試還原覆迭。 如果新的模式不支援重迭， **PresentEx** 會傳回 **D3DERR \_ UNSUPPORTEDOVERLAY**。

### <a name="example-code"></a>範例程式碼

下列範例顯示如何建立重迭表面。


```C++
const UINT VIDEO_WIDTH = 256;
const UINT VIDEO_HEIGHT = 256;

HRESULT CreateHWOverlay(
    HWND hwnd, 
    IDirect3D9Ex *pD3D, 
    IDirect3DDevice9Ex **ppDevice
    )
{
    *ppDevice = NULL;

    D3DCAPS9                caps;
    ZeroMemory(&caps, sizeof(caps));

    HRESULT hr = pD3D->GetDeviceCaps(
        D3DADAPTER_DEFAULT,
        D3DDEVTYPE_HAL,
        &caps
        );

    if (FAILED(hr))
    {
        return hr;
    }

    // Check if overlay is supported.
    if (!(caps.Caps & D3DCAPS_OVERLAY))
    {
        return D3DERR_UNSUPPORTEDOVERLAY;
    }

    D3DOVERLAYCAPS          overlayCaps = { 0 };

    IDirect3DDevice9Ex           *pDevice = NULL;
    IDirect3D9ExOverlayExtension *pOverlay = NULL;

    // Check specific overlay capabilities.
    hr = pD3D->QueryInterface(IID_PPV_ARGS(&pOverlay));

    if (SUCCEEDED(hr))
    {
        hr = pOverlay->CheckDeviceOverlayType(
            D3DADAPTER_DEFAULT,
            D3DDEVTYPE_HAL,
            VIDEO_WIDTH,
            VIDEO_HEIGHT,
            D3DFMT_X8R8G8B8,
            NULL,
            D3DDISPLAYROTATION_IDENTITY,
            &overlayCaps
            );
    }

    // Create the overlay.
    if (SUCCEEDED(hr))
    {

        DWORD flags =   D3DCREATE_FPU_PRESERVE | 
                        D3DCREATE_MULTITHREADED | 
                        D3DCREATE_SOFTWARE_VERTEXPROCESSING;

        
        D3DPRESENT_PARAMETERS   pp = { 0 };

        pp.BackBufferWidth = overlayCaps.MaxOverlayDisplayWidth;
        pp.BackBufferHeight = overlayCaps.MaxOverlayDisplayHeight;
        pp.BackBufferFormat = D3DFMT_X8R8G8B8;
        pp.SwapEffect = D3DSWAPEFFECT_OVERLAY;
        pp.hDeviceWindow = hwnd;
        pp.Windowed = TRUE;
        pp.Flags = D3DPRESENTFLAG_VIDEO;
        pp.FullScreen_RefreshRateInHz = D3DPRESENT_RATE_DEFAULT;
        pp.PresentationInterval       = D3DPRESENT_INTERVAL_ONE;

        hr = pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL,
            NULL, flags, &pp, NULL, &pDevice);
    }

    if (SUCCEEDED(hr))
    {
        (*ppDevice) = pDevice;
        (*ppDevice)->AddRef();
    }

    SafeRelease(&pD3D);
    SafeRelease(&pDevice);
    SafeRelease(&pOverlay);
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 影片 Api](direct3d-video-apis.md)
</dt> </dl>

 

 




