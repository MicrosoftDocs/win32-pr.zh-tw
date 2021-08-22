---
title: 圖形管線
description: 本節說明 Direct3D 11 可程式化管線。
ms.assetid: 8e7a6f64-0a2b-4ea5-a6a6-7bfb87e27dcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b3872fbfaf63a53a07c8c06246088a5eec1791f98be867adbe56ae1d9c7724
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565568"
---
# <a name="graphics-pipeline"></a>圖形管線

Direct3D 11 可程式化管線的設計目的是為了產生即時遊戲應用程式的圖形。 本節說明 Direct3D 11 可程式化管線。 下圖顯示透過每個可程式化階段輸入至輸出的資料流程。

![Direct3D 11 可程式化管線中的資料流程圖](images/d3d11-pipeline-stages.jpg)

Microsoft Direct3D 11 的圖形管線支援與 [Direct3D 10 圖形管線](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)相同的階段，並提供支援 advanced 功能的其他階段。

您可以使用 Direct3D 11API 來設定所有階段。 搭配常見著色器核心的階段 (圓角矩形區塊) 可使用 [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) 程式語言進行程式設計。 如您所見，這會讓管線極具彈性且更具彈性。


## <a name="in-this-section"></a>本節內容



| 主題                                                                                          | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [輸入組合階段](d3d10-graphics-programming-guide-input-assembler-stage.md)<br/> | Direct3D 10 和更新版本的 API 會將管線的功能區域與階段分開。管線中的第一個階段是輸入組合語言 (IA) 階段。<br/>                                                                                                                                                                                                                                                                                                                             |
| [頂點著色器階段](vertex-shader-stage.md)<br/>                                      | 頂點著色器 (與) 階段會處理來自輸入組合語言的頂點，以執行每個頂點的作業，例如轉換、外觀、變形，以及每個頂點的光源。 頂點著色器一律在單一輸入頂點上操作，並產生單一輸出頂點。 頂點著色器階段必須永遠作用中，才能讓管線執行。 不需要頂點修改或轉換時，必須建立穿通頂點著色器並將其設定至管線。<br/> |
| [鑲嵌階段](direct3d-11-advanced-stages-tessellation.md)<br/>                 | Direct3D 11 執行時間支援三個新階段來執行鑲嵌式，這會將低細節的細分圖介面轉換成 GPU 上較高的基本專案。 鑲嵌並排顯示高位表面 (或將其分裂) 成為適合轉譯的結構。<br/>                                                                                                                                                                                                                 |
| [幾何著色器階段](geometry-shader-stage.md)<br/>                                  | 幾何著色器 (GS) 階段會執行應用程式指定的著色器程式碼，並以頂點作為輸入，以及在輸出上產生頂點的能力。<br/>                                                                                                                                                                                                                                                                                                                                          |
| [資料流程-輸出階段](d3d10-graphics-programming-guide-output-stream-stage.md)<br/>     | 資料流程輸出階段的目的是要持續輸出 (或串流) 頂點資料從幾何著色器階段 (或頂點著色器階段（如果幾何著色器階段非使用中) 至記憶體中的一或多個緩衝區） (請參閱開始使用 [階段](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md) Stream-Output。 <br/>                                                                                                                       |
| [轉譯器階段](d3d10-graphics-programming-guide-rasterizer-stage.md)<br/>           | 點陣化階段會轉換向量資訊 (由圖形或基本類型組成) 為點陣影像 (由像素組成)，以顯示即時 3D 圖形。 <br/>                                                                                                                                                                                                                                                                                                 |
| [圖元著色器階段](pixel-shader-stage.md)<br/>                                        | 圖元著色器階段 (PS) 啟用豐富的陰影技術，例如每圖元光源和後置處理。 像素著色器是結合常數變數、紋理資料、插補每個頂點值和其他資料的程式，以產生每個像素的輸出。 轉譯器階段會針對基本型別所涵蓋的每個圖元叫用一次圖元著色器，不過，您可以指定 **Null** 著色器來避免執行著色器。<br/>                                          |
| [輸出合併階段](d3d10-graphics-programming-guide-output-merger-stage.md)<br/>     |  (OM) 階段的輸出合併會使用管線狀態的組合、圖元著色器所產生的圖元資料、轉譯目標的內容，以及深度/樣板緩衝區的內容，來產生最終呈現的圖元色彩。 OM 階段是決定哪些圖元可見 (具有深度樣板測試) 和混合最後圖元色彩的最後一個步驟。<br/>                                                                                              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[計算著色器](direct3d-11-advanced-stages-compute-shader.md)
</dt> <dt>

[Direct3D 11 的程式設計指南](dx-graphics-overviews.md)
</dt> </dl>

 

