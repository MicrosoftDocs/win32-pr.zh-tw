---
title: 計算著色器總覽
description: 計算著色器是可程式化的著色器階段，可將 Microsoft Direct3D 11 擴充到圖形程式設計之外。 計算著色器技術也稱為 DirectCompute 技術。
ms.assetid: 02c1f98e-fdd6-49b0-b8b2-efbd472ab599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485e83ab965f14342d235a07810f210e18aadc53
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222866"
---
# <a name="compute-shader-overview"></a>計算著色器總覽

計算著色器是可程式化的著色器階段，可將 Microsoft Direct3D 11 擴充到圖形程式設計之外。 計算著色器技術也稱為 DirectCompute 技術。

如同其他可程式化著色器 (頂點和幾何著色器（例如) ），計算著色器是使用 [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) 來設計和執行，但這只是相似性結束的位置。 計算著色器提供高速一般用途運算，並且利用了圖形處理器 (GPU) 大量平行處理器的優勢。 計算著色器提供了記憶體共用以及執行緒同步功能，讓平行程式設計方法更有效率。 您可以呼叫 [**>id3d11devicecoNtext：:D ispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch) 或 [**>id3d11devicecoNtext：:D ispatchindirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect) 方法，在計算著色器中執行命令。 計算著色器可在許多執行緒上平行執行。

## <a name="using-compute-shader-on-direct3d-10x-hardware"></a>在 Direct3D 2.x 硬體上使用計算著色器

Microsoft Direct3D 10 上的計算著色器也稱為 DirectCompute 4.x。

如果您使用 Direct3D 11 API 和更新的驅動程式， [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 10 和 10.1 Direct3D 硬體可以選擇性地支援使用 cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 [設定檔](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models)的有限 DirectCompute 形式。 當您在此硬體上使用 DirectCompute 時，請記住下列限制：

-   最大執行緒數目限制為每個群組 D3D11 \_ CS \_ 4 \_ X \_ 執行緒群組的 \_ \_ 最大執行緒數目 \_ \_ \_ (768) 。
-   **Numthreads** 的 X 和 Y 維度僅限於 D3D11 \_ cs \_ 4 \_ x \_ 執行緒 \_ 群組 \_ 最大 \_ x (768) 和 D3D11 \_ CS \_ 4 \_ x \_ 執行緒 \_ 群組 \_ 最大 \_ Y (768) 。
-   **Numthreads** 的 Z 維度限制為1。
-   分派的 Z 維度限制 \_ \_ \_ \_ \_ \_ \_ \_ 在 \_ z \_ 維度 (1) 的 D3D11 CS 4 X 分派最大執行緒群組。
-   只有一個未排序的存取權可系結至著色器 (D3D11 \_ CS \_ 4 \_ X \_ UAV \_ REGISTER \_ COUNT 是 1) 。
-   只有 [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s 和 [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)可以作為未排序存取的視圖。
-   執行緒只能在 groupshared 記憶體中存取自己的區域以進行寫入，不過它可以讀取任何位置。
-   [SV \_](/previous-versions/windows/desktop/legacy/ff471569(v=vs.85))存取 **groupshared** 記憶體以進行寫入時，必須使用 GroupIndex 或 [SV \_ GroupThreadID](/windows/desktop/direct3dhlsl/sv-groupthreadid) 。
-   **Groupshared** 記憶體限制為每個群組的16KB。
-   單一線程受限於 **groupshared** 記憶體的256位元組區域以進行寫入。
-   沒有可部分完成的指示。
-   沒有雙精確度值可用。

## <a name="using-compute-shader-on-direct3d-11x-hardware"></a>在 Direct3D 11. x 硬體上使用計算著色器

Direct3D 11 上的計算著色器也稱為 DirectCompute 5.0。

當您使用 DirectCompute 搭配 cs \_ 5 \_ 0 的 [設定檔](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models)時，請記住下列專案：

-   最大執行緒數目限制為每個群組 D3D11 \_ CS \_ 執行緒 \_ 群組 \_ 最大執行緒群組 \_ \_ \_ (1024) 每個群組。
-   **Numthreads** 的 x 和 Y 維度僅限於 D3D11 \_ cs \_ 執行緒 \_ 群組 \_ 最大 \_ x (1024) 和 D3D11 \_ CS \_ 執行緒 \_ 群組 \_ max \_ Y (1024) 。
-   **Numthreads** 的 z 維度限制為 D3D11 \_ CS \_ 執行緒 \_ 群組 \_ 最大 \_ z (64) 。
-   分派的最大維度限制為 \_ \_ \_ 每個維度 D3D11 CS 分派最大 \_ 執行緒 \_ 群組 \_ \_ (65535) 。
-   可系結至著色器的未排序存取視圖的最大數目為 D3D11 \_ PS \_ CS \_ UAV \_ REGISTER \_ COUNT (8) 。
-   支援 [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s、 [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)和具類型的未排序存取視圖 ([RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d)、 [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d)、 [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)等) 。
-   提供不可部分完成的指示。
-   可能會有雙精確度支援。 如需如何判斷雙精確度是否可用的詳細資訊，請參閱 [**D3D11 \_ 功能 \_ 雙**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)精度浮點數。

## <a name="in-this-section"></a>本節內容



| 主題                                                                              | 描述                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [新的資源類型](direct3d-11-advanced-stages-cs-resources.md)<br/>      | 已在 Direct3D 11 中新增數個新的資源類型。<br/>                                                                                                                                                                                                 |
| [存取資源](direct3d-11-advanced-stages-cs-access.md)<br/>        | 有數種方式可存取 [資源](overviews-direct3d-11-resources-types.md)。<br/>                                                                                                                                                                   |
| [不可部分完成函式](direct3d-11-advanced-stages-cs-atomic-functions.md)<br/> | 若要存取新的資源類型或共用記憶體，請使用連鎖內建函式。 連鎖函式保證會以不可部分完成的方式運作。 也就是說，它們保證會以程式設計的順序發生。 本節列出不可部分完成的函式。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖形管線](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[如何：建立計算著色器](direct3d-11-advanced-stages-compute-create.md)
</dt> </dl>

 

