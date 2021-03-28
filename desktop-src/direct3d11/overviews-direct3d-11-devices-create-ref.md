---
title: 如何建立參照裝置
description: 本主題說明如何建立參考裝置，以執行執行時間的高度精確、軟體執行。
ms.assetid: 00d3f5f2-02c6-4ff4-82a9-0726ad4a8cb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dec5f3834bf1f10027da2a3f3a8e22acdee742b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372477"
---
# <a name="how-to-create-a-reference-device"></a>如何：建立參考裝置

本主題說明如何建立參考裝置，以執行執行時間的高度精確、軟體執行。 若要建立參考設備，只要指定您要建立的裝置將使用參照驅動程式。 此範例會同時建立裝置和交換鏈。

**建立參照裝置**

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

    

2.  要求可執行應用程式所需功能的功能層級。 您可以針對 Direct3D 11 執行時間成功建立參考裝置。

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_11_0;
    ```

    

    請參閱 [**D3D \_ 功能 \_ 層級**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) 列舉中的功能層級詳細資訊。

3.  藉由呼叫 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)來建立裝置。


```
    HRESULT hr = S_OK;
    D3D_FEATURE_LEVEL FeatureLevel;

    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_REFERENCE,
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



您將需要使用來自 [**D3D \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) 列舉的參考驅動程式類型來提供 API 呼叫。 方法成功之後，它會傳回交換連結口、裝置介面、驅動程式所授與的功能等級指標，以及立即內容介面。

如需有關在特定功能層級上建立參考設備的限制的詳細資訊，請參閱 [建立變形和參照裝置的限制](overviews-direct3d-11-devices-limitations.md)。[如何使用 Direct3D 11](how-to-use-direct3d-11.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置](overviews-direct3d-11-devices.md)
</dt> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




