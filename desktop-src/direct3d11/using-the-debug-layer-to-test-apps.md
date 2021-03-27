---
title: 使用 debug 層來對應用程式進行偵錯工具
description: 在此，我們將討論如何啟用 debug 層，以及您可以使用 debug 圖層防止的一些問題。
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa3f4748da6893470e3bb6631c4228ec1ae3d48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671651"
---
# <a name="using-the-debug-layer-to-debug-apps"></a>使用 debug 層來對應用程式進行偵錯工具

建議您使用 [debug 層](overviews-direct3d-11-devices-layers.md) 來將您的應用程式進行偵錯工具，以確保這些應用程式的錯誤和警告都已清除。 Debug 層可協助您撰寫 Direct3D 程式碼。 此外，當您使用 debug 圖層時，您的產能會增加，因為您可以立即查看其來源的隱匿轉譯錯誤或甚至是黑色畫面的原因。 Debug 層提供許多問題的警告。 例如，debug 層會針對這些問題提供警告：

-   忘記設定材質，但在您的圖元著色器中讀取紋理
-   輸出深度，但沒有系結的深度樣板狀態
-   材質建立失敗，INVALIDARG

在此，我們將討論如何啟用 [debug 層](overviews-direct3d-11-devices-layers.md) ，以及您可以使用 debug 圖層防止的一些問題。

-   [啟用 debug 圖層](#enabling-the-debug-layer)
-   [使用 debug 層防止應用程式發生錯誤](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [不要將 Null 指標傳遞給 Map](#dont-pass-null-pointers-to-map)
    -   [來源和目的地資源內的限制來源方塊](#confine-source-box-within-source-and-destination-resources)
    -   [請勿捨棄 DiscardResource 或 DiscardView](#dont-drop-discardresource-or-discardview)
-   [相關主題](#related-topics)

## <a name="enabling-the-debug-layer"></a>啟用 debug 圖層

若要啟用 [debug 圖層](overviews-direct3d-11-devices-layers.md)，請在呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice)函式來建立轉譯裝置時，于 Flags 參數中指定 [**D3D11 \_ 建立 \_ 裝置 \_ 調試**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)旗 *標*。 此範例程式碼示範如何在您的 Microsoft Visual Studio 專案位於 debug 組建中時啟用 debug 層：


```C++
        UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
#if defined(_DEBUG)
        // If the project is in a debug build, enable the debug layer.
        creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
        // Define the ordering of feature levels that Direct3D attempts to create.
        D3D_FEATURE_LEVEL featureLevels[] =
        {
            D3D_FEATURE_LEVEL_11_1,
            D3D_FEATURE_LEVEL_11_0,
            D3D_FEATURE_LEVEL_10_1,
            D3D_FEATURE_LEVEL_10_0,
            D3D_FEATURE_LEVEL_9_3,
            D3D_FEATURE_LEVEL_9_1
        };

        ComPtr<ID3D11Device> d3dDevice;
        ComPtr<ID3D11DeviceContext> d3dDeviceContext;
        DX::ThrowIfFailed(
            D3D11CreateDevice(
                nullptr,                    // specify nullptr to use the default adapter
                D3D_DRIVER_TYPE_HARDWARE,
                nullptr,                    // specify nullptr because D3D_DRIVER_TYPE_HARDWARE 
                                            // indicates that this function uses hardware
                creationFlags,              // optionally set debug and Direct2D compatibility flags
                featureLevels,
                ARRAYSIZE(featureLevels),
                D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION
                &d3dDevice,
                nullptr,
                &d3dDeviceContext
                )
            );
```



## <a name="preventing-errors-in-your-app-with-the-debug-layer"></a>使用 debug 層防止應用程式發生錯誤

如果您誤用 Direct3D 11 API 或傳遞不正確的參數， [debug 層](overviews-direct3d-11-devices-layers.md) 的偵錯工具輸出會報告錯誤或警告。 然後您就可以更正錯誤。 接下來，我們會探討一些可能導致未定義的行為，或甚至作業系統損毀的程式碼撰寫問題。 您可以使用 debug 層來攔截及防止這些問題。

### <a name="dont-pass-null-pointers-to-map"></a>不要將 Null 指標傳遞給 Map

如果您將 **Null** 傳遞給 [**>id3d11devicecoNtext：： Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)方法的 *pResource* 或 *pMappedResource* 參數，則 **對應** 的行為未定義。 如果您建立只支援 [核心層](overviews-direct3d-11-devices-layers.md)的裝置，則 **對應** 的無效參數可能會損毀作業系統。 如果您建立了支援 [debug 層](overviews-direct3d-11-devices-layers.md)的裝置，則偵錯工具輸出會在此不正確 **對應** 呼叫上報告錯誤。

### <a name="confine-source-box-within-source-and-destination-resources"></a>來源和目的地資源內的限制來源方塊

在 [**>id3d11devicecoNtext：： CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) 方法的呼叫中，來源方塊必須在來源資源內。 目的地位移、 (x、y 和 z) 可讓來源方塊在寫入目的地資源時成為位移，但是來源方塊的維度和位移必須在資源的大小內。 如果您嘗試在目的地資源外部進行複製，或指定的來源方塊大於來源資源，則 **CopySubresourceRegion** 的行為未定義。 如果您建立了支援 [debug 層](overviews-direct3d-11-devices-layers.md)的裝置，則偵錯工具輸出會在此不正確 **CopySubresourceRegion** 呼叫上報告錯誤。 不正確 **CopySubresourceRegion** 參數會造成未定義的行為，而且可能會導致不正確的轉譯、裁剪、不復制或甚至是移除轉譯裝置。

### <a name="dont-drop-discardresource-or-discardview"></a>請勿捨棄 DiscardResource 或 DiscardView

除非您正確建立資源，否則執行時間會卸載對 [**ID3D11DeviceCoNtext1：:D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) 或 [**ID3D11DeviceCoNtext1：:D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) 的呼叫。

您傳遞給 [**ID3D11DeviceCoNtext1：:D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) 的資源，必須使用 [**D3D11 \_ 使用方式 \_ 預設值**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) 或 [**D3D11 使用方式 \_ \_ 動態**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)建立，否則執行時間會卸載對 **DiscardResource** 的呼叫。

您傳遞給 [**:D ID3D11DeviceCoNtext1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) 的視圖基礎的資源必須使用 [**D3D11 \_ 使用方式 \_ 預設值**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) 或 [**D3D11 \_ 使用方式 \_ 動態**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)建立，否則執行時間會卸載對 **DiscardView** 的呼叫。

如果您建立了支援 [debug 層](overviews-direct3d-11-devices-layers.md)的裝置，則偵錯工具輸出會報告有關已卸載呼叫的錯誤。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[軟體層](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




