---
description: Direct3D 10 可程式化管線是設計用來產生即時遊戲應用程式的圖形。 下圖顯示透過每個可程式化階段輸入至輸出的資料流程。
ms.assetid: 3ead6c7c-c7cc-48f1-81d5-b4b67326d610
title: " (Direct3D 10) 的管線階段"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78bf6e904051fcac255a5bf1b99ca0f7d43ca3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110540"
---
# <a name="pipeline-stages-direct3d-10"></a> (Direct3D 10) 的管線階段

Direct3D 10 可程式化管線是設計用來產生即時遊戲應用程式的圖形。 下圖顯示透過每個可程式化階段輸入至輸出的資料流程。

![direct3d 10 程式化管線中資料流程的圖表](images/d3d10-pipeline-stages.png)

所有階段都可以使用 API 進行設定。 使用 HLSL 的程式設計語言，可使用的程式設計語言， (圓角矩形) 區塊的常見著色器核心階段。 如您所見，這會讓管線極具彈性且更具彈性。 每個階段的用途如下所示。

-   [輸入組合語言階段](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) -輸入組合語言階段負責提供資料 (三角形、線條和點) 至管線。
-   [頂點著色器階段](https://www.bing.com/search?q=Vertex-Shader+Stage) - 頂點著色器階段處理頂點，通常執行轉換、貼圖與光照等作業。 頂點著色器一律採用單一輸入頂點，並產生單一輸出頂點。
-   [幾何-著色器階段](https://www.bing.com/search?q=Geometry-Shader+Stage) -幾何著色器階段會處理整個基本專案。 它的輸入是完整的基本 (，其為三角形的三個頂點、線條的兩個頂點，或點) 的單一頂點。 此外，每個基本專案也可以包含任何邊緣相鄰基本專案的頂點資料。 這最多可以包含三角形的三個頂點或一行的額外兩個頂點。 幾何著色器也支援有限的幾何放大以及取消放大。 即使有輸入基本類型，幾何著色器可捨棄基本類型，或發出一種或多種新的基本類型。
-   [資料流程輸出階段](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md) ：資料流程輸出階段是設計用來將管線中的基本資料串流處理至轉譯器的記憶體。 資料可串流輸出及/或傳遞進入點陣化。 串流輸出到記憶體的資料可重新循環回管線，做為輸入資料或從 CPU 讀回。
-   轉譯器[階段](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md)-轉譯器會負責裁剪基本專案、準備圖元著色器的基本專案，以及決定如何叫用圖元著色器。
-   [像素著色器階段](https://www.bing.com/search?q=Pixel-Shader+Stage) - 像素著色器階段會接收基本型別的插補資料，並產生每一像素資料，如色彩。
-   [輸出合併階段](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) -輸出合併階段負責將各種類型的輸出資料結合 (圖元著色器值、深度和樣板資訊) 與轉譯目標的內容和深度/樣板緩衝區，以產生最終的管線結果。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 10 程式設計手冊](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
