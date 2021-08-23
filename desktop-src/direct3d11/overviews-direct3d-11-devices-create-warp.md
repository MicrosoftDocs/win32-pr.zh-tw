---
title: 如何建立變形裝置
description: 本主題說明如何建立可執行高速度軟體轉譯器的變形裝置。
ms.assetid: 6daf661e-bc24-4b90-83a7-031acb57cf87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78d3e8b5224018fb9f45df2c6eec5ee6f9d88cdd664715a31050eaab4ddd948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407798"
---
# <a name="how-to-create-a-warp-device"></a>如何：建立變形裝置

本主題說明如何建立可執行高速度軟體轉譯器的變形裝置。 若要建立變形裝置，只要指定您要建立的裝置將使用變形驅動程式。 此範例會同時建立裝置和交換鏈。

**建立變形裝置**

1.  定義交換鏈的初始參數。
    ```
        DXGI_SWAP_CHAIN_DESC sd;
        ZeroMemory( &sd, sizeof( sd ) );
        sd.BufferCount = 1;
        sd.BufferDesc.Width = 640;
        sd.BufferDesc.Height = 480;
        sd.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
        sd.BufferDesc.RefreshRate.Numerator = 60;
        sd.BufferDesc.RefreshRate.Denominator = 1;
        sd.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        sd.OutputWindow = g_hWnd;
        sd.SampleDesc.Count = 1;
        sd.SampleDesc.Quality = 0;
        sd.Windowed = TRUE;
    ```

    

2.  要求可執行應用程式所需功能的功能層級。 您可以成功地為功能層級 **d3d 功能層 \_ 級 \_ \_ \_ 2 1** 到 **d3d \_ 功能 \_ 層級 \_ 10 \_ 1** 建立變形裝置，並從所有功能等級的 Windows 8 開始。

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    請參閱 [**D3D \_ 功能 \_ 層級**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) 列舉中的功能層級詳細資訊。

3.  藉由呼叫 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)來建立裝置。


```
    HRESULT hr = S_OK;
    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_WARP,
                    NULL, 
                    0,
                    &FeatureLevels, 
                    1, 
                    D3D11_SDK_VERSION, 
                    &sd, 
                    &g_pSwapChain, 
                    &g_pd3dDevice, 
                    &FeatureLevel,
                    &g_pImmediateContext )))
    {
        return hr;
    }
```



您將需要使用來自 [**D3D \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) 列舉的變形驅動程式類型來提供 API 呼叫。 方法成功之後，它會傳回交換連結口、裝置介面、驅動程式所授與的功能等級指標，以及立即內容介面。

如需有關在特定功能層級上建立變形裝置之限制的詳細資訊，請參閱 [建立變形和參照裝置的限制](overviews-direct3d-11-devices-limitations.md)。

## <a name="new-for-windows-8"></a>Windows 8 的新

當電腦的主要顯示器介面卡是「Microsoft 基本顯示器介面卡」 (變形介面卡) 時，該電腦也會有第二張介面卡。 第二張介面卡是僅限轉譯的裝置，沒有顯示輸出。 如需僅限轉譯裝置的詳細資訊，請參閱[關於列舉介面卡的 Windows 8 中的新資訊](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置](overviews-direct3d-11-devices.md)
</dt> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 