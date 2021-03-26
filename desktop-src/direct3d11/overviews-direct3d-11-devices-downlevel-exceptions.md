---
title: 例外狀況
description: 本主題說明在舊版硬體上使用 Direct3D 11 時的例外狀況。
ms.assetid: b3f85036-8572-40ee-b522-3b677443b840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97920ae42347cf618b22df82abc3b6e06bd5200d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316273"
---
# <a name="exceptions"></a>例外狀況

Direct3D 11 的部分功能並非由功能等級完全指定。 本主題說明在舊版硬體上使用 Direct3D 11 時的例外狀況。 這可能是在定義功能層級之後新增的功能 (而且需要更新的驅動程式) 或可能有不同的 Gpu 可執行廣泛的不同的執行方式。 功能層級的例外狀況可以收集至下列群組：

-   [擴充格式](#extended-formats)
-   [多級化消除鋸齒](#multisample-anti-aliasing)
-   [Texture2D 大小](#texture2d-sizes)
-   [功能等級9的介面卡特殊行為](#special-behavior-of-adapters-for-feature-level-9)
-   [相關主題](#related-topics)

[ [10Level9 參考](d3d11-graphics-reference-10level9.md) ] 區段會列出各種 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 和 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 方法在各種10Level9 功能層級的行為方式之間的差異。

## <a name="extended-formats"></a>擴充格式

延伸格式是針對功能層級 10 \_ 0 和 10 1 新增至 direct3d 10.1 和 direct3d 11 的像素格式 \_ 。 延伸格式需要 Direct3D 10 \_ 1 或以下) 的更新版驅動程式 (。 使用 [**ID3D11Device：： CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) 和 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) 來查詢這些延伸格式的支援。

延伸格式：

-   新增每個元件資源8位 BGRA 順序的支援。
-   允許轉換整數值交換鏈緩衝區。 這可讓應用程式新增或移除 \_ SRGB 尾碼，或轉譯成 XR \_ 偏差交換鏈。
-   為 DXGI \_ 格式 \_ R10G10B10 \_ XR \_ 偏差 \_ A2 \_ UNORM 新增選擇性支援。
-   保證 \_ 會顯示 DXGI 格式 \_ R16G16B16A16 \_ 浮點數交換鏈，如同所包含的資料未進行 sRGB 編碼。

完整支援或不支援一組完整的延伸格式，但 XR \_ 偏差格式除外。 XR \_ 偏差格式為：

-   在任何9層級中不支援
-   在 10 \_ 0 或 10 \_ 1 層級中為選擇性
-   保證為 11 \_ 0 層級

## <a name="multisample-anti-aliasing"></a>多級化消除鋸齒

MSAA 的執行在 GPU 的執行上並不常見。 功能層級10.1 已新增一些定義完善的最小值，但在較低的功能層級上，必須使用 [**ID3D11Device：： CheckMultisampleQualityLevels**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkmultisamplequalitylevels)明確測試 MSAA。

## <a name="texture2d-sizes"></a>Texture2D 大小

功能等級保證可以建立最小大小，不過，應用程式可以建立較大的紋理，直到 GPU 支援的完整大小。 如果超過最大值，則應用程式應該會預期從 [**ID3D11Device：： CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) 之類的方法失敗。

## <a name="special-behavior-of-adapters-for-feature-level-9"></a>功能等級9的介面卡特殊行為

三個最低的功能層 \_ 級 \_ ： d3d 功能等級 \_ 9 \_ 1、D3D \_ 功能 \_ 層級 \_ 9 \_ 2 和 D3D \_ 功能 \_ 層級 \_ 9 \_ 3，共用通用的實作為範本，並將 [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) 引數視為作為 \[ \] 裝置建立的一部分來 D3D11CreateDevice AndSwapchain。 這表示傳入建立常式的 **IDXGIAdapter** 將不會與透過 IDXGIDevice：： GetAdapter 從裝置上取出的介面卡相同。 這種情況的影響是從傳入的介面卡列舉的 **IDXGIOutputs** 無法使用任何層級9裝置來輸入全螢幕，因為這些輸出不是裝置的介面卡所擁有。 建議您捨棄傳入的範本介面卡，並使用 IDXGIDevice：： GetAdapter 抓取裝置所建立的介面卡，其中 [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) 可使用來自 Direct3D 裝置介面的 QueryInterface 抓取。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[舊版硬體上的 Direct3D 11](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 