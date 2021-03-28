---
title: HLSL 程式設計指南
description: 資料會將圖形管線輸入為基本類型的資料流程，並由著色器階段處理。
ms.assetid: 4894e085-30e7-4cc5-8ae6-a84b601e4ce3
ms.topic: article
ms.date: 02/21/2019
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cd242efaaf3cdb44f424a603f2fc522dda540ec8
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/12/2021
ms.locfileid: "104973860"
---
# <a name="programming-guide-for-hlsl"></a>HLSL 程式設計指南

資料會將圖形管線輸入為基本類型的資料流程，並由著色器階段處理。 實際的著色器階段相依于 Direct3D 版本，但一定要包含頂點、圖元和幾何階段。 其他階段包括鑲嵌和計算著色器的輪廓和網域著色器。 這些階段可使用高階的陰影語言 ([HLSL](dx-graphics-hlsl-reference.md)) 來完全進行程式設計。

HLSL 著色器可以在作者或執行時間進行編譯，並在執行時間設定為適當的管線階段。 Direct3D 9 著色器可以使用 [著色器模型 1](dx-graphics-hlsl-sm1.md)、 [著色器模型 2](dx-graphics-hlsl-sm2.md) 和 [著色器模型 3](dx-graphics-hlsl-sm3.md)來設計;Direct3D 10 著色器只能設計于 [著色器模型 4](dx-graphics-hlsl-sm4.md)。 您可以在 [著色器模型 5](d3d11-graphics-reference-sm5.md)上設計 Direct3D 11 著色器。 您可以在 [著色器模型 5.1](shader-model-5-1.md)上設計 direct3d 11.3 和 direct3d 12，而且也可以在 [著色器模型 6](shader-model-6-0.md)上設計 direct3d 12。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [使用著色器連結](using-shader-linking.md) | 我們會示範如何建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。 |
| [在 Direct3D 9 撰寫 HLSL 著色器](dx-graphics-hlsl-writing-shaders-9.md) | |
| [在 Direct3D 9 中使用著色器](dx-graphics-hlsl-using-shaders-9.md) | |
| [使用 Direct3D 10 中的著色器](dx-graphics-hlsl-using-shaders-10.md) | |
| [優化 HLSL 著色器](dx-graphics-hlsl-optimize.md) | |
| [Visual Studio 中的調試著色器](dx-graphics-hlsl-debug-visual-studio.md) | 偵錯工具的最新工具現在以 Microsoft Visual Studio 的功能形式隨附，稱為 Visual Studio 圖形偵錯工具。  |
| [編譯著色器](dx-graphics-hlsl-part1.md) | 現在讓我們看看如何編譯著色器程式碼的各種方式，以及著色器程式碼副檔名的慣例。 |
| [指定編譯器目標](specifying-compiler-targets.md) | 在這裡，我們會列出 **D3DCompile \** _ 函式和 HLSL 編譯器支援之各種設定檔的目標。 |
| [\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式](dx-graphics-hlsl-unpacking-packing-dxgi-format.md) | |
| [使用 HLSL 最小有效位數](using-hlsl-minimum-precision.md) | 從 Windows 8 開始，圖形驅動程式可以使用任何有效位數大於或等於指定的位精確度，來執行最小有效位數 HLSL 純量 [資料類型](dx-graphics-hlsl-scalar.md) 。  |
| [HLSL 著色器模型5](overviews-direct3d-11-hlsl.md) | |
| [HLSL 著色器模型5。1](hlsl-shader-model-5-1-features-for-direct3d-12.md) | 本節說明著色器模型5.1 的功能，在實務上適用于 D3D12 和 D3D 11.3。 所有 DirectX 12 硬體都支援著色器模型5.1。 |
| [HLSL 著色器模型6。0](hlsl-shader-model-6-0-features-for-direct3d-12.md) | 描述新增至 HLSL 著色器模型6.0 的 wave 作業內建。 |
| [HLSL 著色器模型6。4](hlsl-shader-model-6-4-features-for-direct3d-12.md) | 描述新增至 HLSL 著色器模型6.4 的機器學習內建函式。 |

## <a name="related-topics"></a>相關主題

_ [HLSL](dx-graphics-hlsl.md)
* [HLSL 的參考](dx-graphics-hlsl-reference.md)
