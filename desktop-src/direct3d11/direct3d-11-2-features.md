---
title: Direct3D 11.2 功能
description: 下列是在 Direct3D 11.2 中新增的功能，包括在 Windows 8.1、Windows RT 8.1 和 Windows Server 2012 R2 中。
ms.assetid: 2A2D9BBB-F53A-4187-A25B-F4E58C896EE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299b720bfb91297043c8e7d76beb50067eb64e17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971737"
---
# <a name="direct3d-112-features"></a>Direct3D 11.2 功能

下列是在 Direct3D 11.2 中新增的功能，包括在 Windows 8.1、Windows RT 8.1 和 Windows Server 2012 R2 中。

-   [磚資源](#tiled-resources)
    -   [檢查磚資源支援](#check-tiled-resources-support)
-   [對變形裝置的擴充支援](#extended-support-for-warp-devices)
-   [標注圖形命令](#annotate-graphics-commands)
-   [HLSL 著色器連結](#hlsl-shader-linking)
    -   [函數連結圖形 (FLG) ](#function-linking-graph-flg)
-   [收件匣 HLSL 編譯器](#inbox-hlsl-compiler)
-   [相關主題](#related-topics)

## <a name="tiled-resources"></a>磚資源

Direct3D 11.2 可讓您建立可視為大型邏輯資源（使用少量實體記憶體）的磚資源。 並排顯示的資源很有用 (例如) 與遊戲中的地形和應用程式 UI。

藉由指定 D3D11 資源的「 [**\_ \_ 其他 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 並排顯示」旗標來建立並排的資源。 若要使用已磚的資源，請使用下列 API：

-   [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling)
-   [**ID3D11DeviceCoNtext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)
-   [**ID3D11DeviceCoNtext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings)
-   [**ID3D11DeviceCoNtext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   [**ID3D11DeviceCoNtext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings)
-   [**ID3D11DeviceCoNtext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [**ID3D11DeviceCoNtext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)
-   **D3D11 \_使用 ID3D11Debug：： SetFeatureMask 的 DEBUG 功能停用並排顯示 \_ \_ \_ \_ 資源 \_ 對應 \_ 追蹤 \_ 和 \_ 驗證** 旗標 [](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)

如需磚資源的詳細資訊，請參閱並排顯示的 [資源](tiled-resources.md)。

### <a name="check-tiled-resources-support"></a>檢查磚資源支援

使用已磚的資源之前，您必須先找出裝置是否支援磚的資源。 以下是檢查磚資源支援的方式：


```C++
HRESULT hr = D3D11CreateDevice(
    nullptr,                    // Specify nullptr to use the default adapter.
    D3D_DRIVER_TYPE_HARDWARE,   // Create a device using the hardware graphics driver.
    0,                          // Should be 0 unless the driver is D3D_DRIVER_TYPE_SOFTWARE.
    creationFlags,              // Set debug and Direct2D compatibility flags.
    featureLevels,              // List of feature levels this app can support.
    ARRAYSIZE(featureLevels),   // Size of the list above.
    D3D11_SDK_VERSION,          // Always set this to D3D11_SDK_VERSION for Windows Store apps.
    &device,                    // Returns the Direct3D device created.
    &m_d3dFeatureLevel,         // Returns feature level of device created.
    &context                    // Returns the device immediate context.
    );

if (SUCCEEDED(hr))
{
    D3D11_FEATURE_DATA_D3D11_OPTIONS1 featureData;
    DX::ThrowIfFailed(
        device->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS1, &featureData, sizeof(featureData))
        );

    m_tiledResourcesTier = featureData.TiledResourcesTier;
}
```



## <a name="extended-support-for-warp-devices"></a>對變形裝置的擴充支援

Direct3D 11.2 延伸了對 [變形](overviews-direct3d-11-devices-create-warp.md)裝置的支援，您可以在 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice)的 *DriverType* 參數中傳遞 [**D3D \_ 驅動程式 \_ 類型 \_ 變形**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)來建立這些裝置。 Direct3D 11.2 中的變形軟體轉譯器加入了對 Direct3D [功能等級](overviews-direct3d-11-devices-downlevel-intro.md) 11 1 的完整支援，包括並排顯示的 \_ [資源](#tiled-resources)、 [**IDXGIDevice3：： Trim**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidevice3-trim)、共用 BCn 表面、minblend 和地圖預設。 HLSL 著色器中的[雙重](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)支援也已啟用，並支援 16x MSAA。

## <a name="annotate-graphics-commands"></a>標注圖形命令

Direct3D 11.2 可讓您使用下列 API 將圖形命令加上批註：

-   [**ID3D11DeviceCoNtext2::IsAnnotationEnabled**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-isannotationenabled)
-   [**ID3D11DeviceCoNtext2::BeginEventInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-begineventint)
-   [**ID3D11DeviceCoNtext2::SetMarkerInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-setmarkerint)
-   [**ID3D11DeviceCoNtext2::EndEvent**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-endevent)

## <a name="hlsl-shader-linking"></a>HLSL 著色器連結

Windows 8.1 新增個別的 HLSL 著色器編譯和連結，可讓圖形程式設計人員建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。 這基本上相當於 C/c + + 個別編譯、程式庫和連結，並且可讓程式設計人員在有更多資訊可供完成計算時，撰寫先行編譯的 HLSL 程式碼。 如需如何使用著色器連結的詳細資訊，請參閱 [使用著色器連結](/windows/desktop/direct3dhlsl/using-shader-linking)。

完成這些步驟，以在執行時間使用動態連結來建立最後的著色器。

**建立和使用著色器連結**

1.  建立代表連結內容的 [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker) 連結器物件。 單一內容無法用來產生多個著色器;連結內容用來產生單一著色器，然後將連結內容擲回。
2.  使用 [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) 從其程式庫 blob 載入和設定程式庫。
3.  使用 [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) 載入和設定專案著色器 blob，或建立 [FLG 著色器](#function-linking-graph-flg)。
4.  使用 [**ID3D11Module**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module)：：[**CreateInstance**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11module-createinstance) 來建立 [**ID3D11ModuleInstance**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance) 物件，然後在這些物件上呼叫函式，以將資源重新系結至其最終位置。
5.  將程式庫新增至連結器，然後呼叫 [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker)：：[**Link**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11linker-link) 來產生最終的著色器位元組程式碼，然後在執行時間中載入及使用，就像完整先行編譯和連結的著色器一樣。

### <a name="function-linking-graph-flg"></a>函數連結圖形 (FLG) 

Windows 8.1 也會新增函數連結圖形 (FLG) 。 您可以使用 FLG 來建立著色器，其中包含一連串預先編譯的函式調用，可將值傳遞給彼此。 使用 FLG 時，不需要撰寫 HLSL 並叫用 HLSL 編譯器。 相反地，會使用 c + + API 呼叫以程式設計方式指定著色器結構。 FLG 節點代表輸入和輸出的簽章，以及先行編譯程式庫函數的調用。 註冊函式呼叫節點的順序會定義調用的順序。 必須先指定輸入簽章節點，而且必須最後指定輸出簽章節點。 FLG 邊緣定義值如何從一個節點傳遞至另一個節點。 傳遞值的資料類型必須相同;沒有隱含類型轉換。 Shape 和 swizzling 規則會遵循 HLSL 行為，而且值只能在這個順序中向前傳遞。 如需 FLG API 的詳細資訊，請參閱 [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph)。

## <a name="inbox-hlsl-compiler"></a>收件匣 HLSL 編譯器

HLSL 編譯器現在是 Windows 8.1 和更新版本上的收件匣。 現在，適用于著色器程式設計的大部分 Api 都可以在針對 Windows 8.1 和更新版本建立的 Windows Store 應用程式中使用。 適用于著色器程式設計的許多 Api 無法在針對 Windows 8 所建立的 Windows Store 應用程式中使用;這些 Api 的參考頁面會以附注標示。 但某些著色器 Api (例如， [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)) 仍然只能用來開發 windows store 應用程式，而不能用於您提交至 windows 市集中的應用程式;這些 Api 的參考頁面仍會以附注標示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11 的新功能](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 