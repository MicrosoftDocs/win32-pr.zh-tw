---
title: 如何取得裝置功能等級
description: 本主題說明如何取得裝置支援的最高功能層級。
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e587ad488a84641a92f0058d201014030e3467e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840584"
---
# <a name="how-to-get-the-device-feature-level"></a>如何：取得裝置功能等級

本主題說明如何取得[裝置](overviews-direct3d-11-devices-intro.md)支援的最高[功能層級](overviews-direct3d-11-devices-downlevel-intro.md)。 Direct3D 11 裝置可支援在 [**D3D \_ 功能 \_ 層級**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) 列舉中定義的一組固定功能等級。 當您知道裝置支援的最高 [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 時，您可以執行適用于該裝置的程式碼路徑。

**取得裝置功能等級**

1.  針對 *ppDevice* 參數指定 **Null** 時，請呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice)函數或 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)函數。 您可以在裝置建立之前完成此動作。

    \- 或 -

    建立裝置之後，請呼叫 [**ID3D11Device：： GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) 。

2.  檢查從上一個步驟傳回的 [**D3D \_ 功能 \_ 層級**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) 列舉值，以判斷支援的功能層級。

下列程式碼範例示範如何藉由呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 函數來判斷最高支援的功能層級。 **D3D11CreateDevice** 會將最高支援的功能層級儲存在 FeatureLevel 變數中。 您可以使用此程式碼來檢查 **D3D11CreateDevice** 傳回的 [**D3D \_ 功能 \_ 層級**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)列舉型別值。 請注意，此程式碼會針對 Direct3D 11.1 和 Direct3D 11.2) 明確 (列出所有功能層級。

> [!Note]  
> 如果電腦上有 Direct3D 11.1 執行時間，且 *pFeatureLevels* 設定為 **Null**，則此函式不會建立 [**D3D \_ 功能 \_ 等級 \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) 的裝置。 若要建立 **d3d \_ 功能 \_ 等級 \_ 11 \_ 1** 的裝置，您必須明確提供包含 **d3d \_ 功能等級 \_ \_ 11 \_ 1** 的 **d3d \_ 功能 \_ 等級** 陣列。 如果您在未安裝 Direct3D 11.1 執行時間的電腦上提供包含 **d3d \_ 功能 \_ 等級 \_ 11 \_ 1** 的 **d3d \_ 功能 \_ 層級** 陣列，此函式會立即失敗，並出現 E \_ INVALIDARG。

 


```C++
HRESULT hr = E_FAIL;
D3D_FEATURE_LEVEL MaxSupportedFeatureLevel = D3D_FEATURE_LEVEL_9_1;
D3D_FEATURE_LEVEL FeatureLevels[] = {
    D3D_FEATURE_LEVEL_11_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1
    };

hr = D3D11CreateDevice(
    NULL,
    D3D_DRIVER_TYPE_HARDWARE,
    NULL, 
    0, 
    &FeatureLevels, 
    ARRAYSIZE(FeatureLevels), 
    D3D11_SDK_VERSION, 
    NULL, 
    &MaxSupportedFeatureLevel, 
    NULL 
    );

if(FAILED(hr))
{
    return hr;
}
```



[ [10Level9 參考](d3d11-graphics-reference-10level9.md) ] 區段會列出各種 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 和 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 方法在各種10Level9 功能層級的行為方式之間的差異。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[舊版硬體上的 Direct3D 11](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




