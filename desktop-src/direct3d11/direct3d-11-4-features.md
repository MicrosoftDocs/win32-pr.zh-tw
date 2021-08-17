---
title: Direct3D 11.4 功能
description: Direct3D 11.4 已新增下列功能。
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57190dbd244a565d579e807f7b7b2322ebfec0216d8a6862c4772c4cd4ebe142
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124533"
---
# <a name="direct3d-114-features"></a>Direct3D 11.4 功能

Direct3D 11.4 已新增下列功能。

另請參閱 [DIRECTX SDK 的位置](../directx-sdk--august-2009-.md)。

## <a name="direct3d-device-removal"></a>移除 Direct3D 裝置

[**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)和 [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved)方法是由新的介面 [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4)所支援，可支援在移除 Direct3D 裝置時接收非同步事件通知。

## <a name="multithreaded-protection"></a>多執行緒保護

為了確保特定的圖形命令會以特定循序執行， [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) 介面具有開啟和關閉多執行緒保護的方法，以及輸入和離開需要這項保護的關鍵程式碼的方法。

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a>使用 Direct3D 12 進行多重裝置同步處理和交互操作的圍牆

[**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence)、 [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5)和 [**ID3D11DeviceCoNtext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4)提供與 direct3d 11 的 direct3d 12 相同的隔離功能。 您可以使用「使用」來同步處理多個 Direct3D11 裝置，以及針對 Direct3D 11 和 Direct3D 12 之間的 interop。 Windows 10 Creators Update 支援的。

## <a name="extended-nv12-texture-support"></a>外延 NV12 材質支援

具有 capture 和影片編碼功能的 NV12 紋理現在支援共用。 適用于影片編碼和捕捉的較舊 D3D11 材質旗標已被取代為 NV12，因為它會在新驅動程式的所有時間進行設定。 這類紋理不僅可以與 D3D11 共用，也可與 D3D12 共用。 在 D3D12 中，沒有任何新的旗標代表這些材質功能。

請參閱 [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4)中的布林值設定。

## <a name="shader-caching"></a>著色器快取

驅動程式在 Windows 10 建立者更新中，可能支援作業系統管理的 Direct3D11 應用程式的著色器快取。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11 的新功能](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 