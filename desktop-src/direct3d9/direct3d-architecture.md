---
description: 本主題提供 Direct3D 架構的兩個高階觀點：
ms.assetid: ed08b4c8-fdd9-46fb-a2be-c2fb15af2dc6
title: Direct3D 架構 (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e557b7a36aadcaa8b96899047a721741ecef2156
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109168"
---
# <a name="direct3d-architecture-direct3d-9"></a>Direct3D 架構 (Direct3D 9)

本主題提供 Direct3D 架構的兩個高階觀點：

-   [Direct3d 圖形管線](#direct3d-graphics-pipeline) -direct3d 轉譯系統內部處理架構的觀點。
-   [Direct3d 系統整合](#direct3d-system-integration) ： direct3d 如何在應用程式和圖形硬體之間進行協調的觀點。

## <a name="direct3d-graphics-pipeline"></a>Direct3D 圖形管線

圖形管線提供強大的功能，可有效率地處理和轉譯 Direct3D 場景至顯示器，利用可用的硬體。 下圖顯示管線的建立區塊：

![direct3d 圖形管線的圖表](images/blockdiag-graphics.png)



| 管線元件  | Description                                                                                                                                                                                      | [相關主題]                                                                                                                                                                                             |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 頂點資料         | 未轉換模型頂點會儲存在頂點記憶體緩衝區中。                                                                                                                                | [ (Direct3D 9) ](vertex-buffers.md)、IDirect3DVertexBuffer9 的頂點緩衝區[ ](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)                                                                                                |
| 基本資料      | 幾何基本類型（包括點、線條、三角形和多邊形）會在具有索引緩衝區的頂點資料中參考。                                                                    |  (direct3d 9 的 [索引緩衝區)](index-buffers.md)、 [**IDirect3DIndexBuffer9**](/windows/desktop/api)、[基本](primitives.md)專案、[高序位的基本專案 (direct3d 9)](higher-order-primitives.md) |
| 鑲嵌        | Tesselator 單位會將高序位基本、置換地圖和網狀修補程式轉換成頂點位置，並將這些位置儲存在頂點緩衝區中。                                      | [ (Direct3D 9) 的鑲嵌 ](tessellation.md)                                                                                                                                                              |
| 頂點處理   | Direct3D 轉換適用于儲存在頂點緩衝區中的頂點。                                                                                                                    | [ (Direct3D 9) 的頂點管線 ](vertex-pipeline.md)                                                                                                                                                        |
| 幾何處理 | 裁剪、背面的臉部剔除、屬性評估和柵格化都會套用至轉換的頂點。                                                                                    | [ (Direct3D 9) 的圖元管線 ](pixel-pipeline.md)                                                                                                                                                          |
| 紋理表面    | Direct3D 表面的材質座標會透過 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 介面提供給 direct3d。                                                         | [Direct3d 材質 (direct3d 9)](direct3d-textures.md)、 [ **IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)                                                                                                    |
| 紋理取樣器     | 材質層級詳細資料篩選會套用至輸入材質值。                                                                                                                            | [Direct3d 材質 (Direct3D 9) ](direct3d-textures.md)                                                                                                                                                    |
| 圖元處理    | 圖元著色器作業會使用幾何資料來修改輸入頂點和材質資料，產生輸出圖元色彩值。                                                                           | [ (Direct3D 9) 的圖元管線 ](pixel-pipeline.md)                                                                                                                                                          |
| 圖元轉譯     | 最終轉譯程式會使用 Alpha、深度或樣板測試修改圖元色彩值，或是套用 Alpha 混色或霧化來修改圖元色彩值。 所有產生的圖元值都會顯示在輸出顯示中。 | [ (Direct3D 9) 的圖元管線 ](pixel-pipeline.md)                                                                                                                                                          |



 

## <a name="direct3d-system-integration"></a>Direct3D 系統整合

下圖顯示視窗應用程式、Direct3D、GDI 和硬體之間的關聯性：

![direct3d 與其他系統元件之間關聯性的圖表](images/d3dsysint.png)

Direct3D 會向應用程式公開與裝置無關的介面。 Direct3D 應用程式可以與 GDI 應用程式並存，而且兩者都可以透過圖形配接器的設備磁碟機存取電腦的圖形硬體。 與 GDI 不同的是，Direct3D 可以藉由建立 hal 裝置來利用硬體功能。

Hal 裝置會根據圖形配接器所支援的功能集，提供硬體加速給圖形管線功能。 系統會提供 Direct3D 方法，以在執行時間取得裝置顯示功能。  (參閱 [**IDirect3DDevice9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps)) 。如果硬體未提供某項功能，則 hal 不會將它報告為硬體功能。

如需 Direct3D 所支援之 hal 和參考裝置的詳細資訊，請參閱 [ (direct3d 9) 的裝置類型 ](device-types.md)。

## <a name="related-topics"></a>相關主題

[快速入門](getting-started.md)
