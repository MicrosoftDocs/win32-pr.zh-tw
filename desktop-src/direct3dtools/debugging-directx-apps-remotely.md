---
title: 遠端偵錯程式的 DirectX 應用程式
description: 您可以使用 Visual Studio 和 Windows 8 SDK，從遠端進行 DirectX 應用程式的偵錯工具。
ms.assetid: CA471465-47C2-4706-B391-C9E6C2CD69D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55548cd282bf643e16f22177e46643c6e283a909
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382813"
---
# <a name="debugging-directx-apps-remotely"></a>遠端偵錯程式的 DirectX 應用程式

您可以使用 Visual Studio 和 Windows 8 SDK，從遠端進行 DirectX 應用程式的偵錯工具。 Windows 8 SDK 提供一組支援 DirectX 開發的元件，除了 Visual Studio 提供的偵錯工具之外，還提供錯誤檢查和參數驗證。 這些元件包括 D3D11 \_1SDKLayers.dll、D2D1Debug1.dll 和 Dxgidebug.dll。

如果您想要在未安裝 Windows 8 SDK 的電腦上遠端進行偵錯工具，而您想要此額外的偵錯工具，則必須安裝適用于您要進行偵錯工具之架構的遠端偵錯程式封裝。 中的 Windows Installer 套件會 `C:\Program Files (x86)\Windows Kits\8.0\Remote\<arch>` 安裝適當的支援。

若要啟用 Direct2D apps 的其他偵錯工具功能，請使用下列程式碼：

```cpp
    D2D1_FACTORY_OPTIONS options;
    ZeroMemory(&options, sizeof(D2D1_FACTORY_OPTIONS));

#if defined(_DEBUG)
     // If the project is in a debug build, enable Direct2D debugging via SDK Layers.
    options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;
#endif

    DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );         
```

若要啟用 Direct3D 應用程式的其他偵錯工具功能，請使用下列程式碼：

```cpp
    // This flag supports surfaces with a different color channel ordering than the API default.
    // It is recommended usage, and is required for compatibility with Direct2D.
    UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    ComPtr<IDXGIDevice> dxgiDevice;

#if defined(_DEBUG)
    // If the project is in a debug build, enable debugging via SDK Layers with this flag.
    creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
    DX::ThrowIfFailed(
        D3D11CreateDevice(
            nullptr,                    // specify null to use the default adapter
            D3D_DRIVER_TYPE_HARDWARE,
            0,                          // leave as 0 unless software device
            creationFlags,              // optionally set debug and Direct2D compatibility flags
            featureLevels,              // list of feature levels this app can support
            ARRAYSIZE(featureLevels),   // number of entries in above list
            D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION for modern
            &device,                    // returns the Direct3D device created
            &m_featureLevel,            // returns feature level of device created
            &context                    // returns the device immediate context
            )
        );
```

如需有關偵錯工具 Direct2D 應用程式的詳細資訊，請參閱 [Direct2D Debug Layer](/windows/desktop/Direct2D/direct2ddebuglayer-portal)。

如需有關偵錯工具 Direct3D 應用程式的詳細資訊，請參閱 [Direct3d Debug Layer](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers)。