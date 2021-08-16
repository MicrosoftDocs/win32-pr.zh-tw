---
title: 優化 HLSL 著色器
description: 本章節描述您可以用來優化著色器的一般用途策略。 您可以在任何平臺上，將這些策略套用到以任何語言撰寫的著色器。
ms.assetid: 014b9cb3-a489-48d7-8174-b97de168bf3a
keywords:
- 高階著色器語言
- HLSL，效能
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9bc707f88fcc731146fcd3a5bbca641e6f0515a728b07af0863894d249c16a98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726138"
---
# <a name="optimizing-hlsl-shaders"></a>優化 HLSL 著色器

本章節描述您可以用來優化著色器的一般用途策略。 您可以在任何平臺上，將這些策略套用到以任何語言撰寫的著色器。

-   [知道要在哪裡執行著色器計算](#know-where-to-perform-shader-calculations)
-   [略過不必要的指示](#skip-unnecessary-instructions)
-   [套件變數和 Interpolants](#pack-variables-and-interpolants)
-   [減少著色器複雜度](#reduce-shader-complexity)
-   [相關主題](#related-topics)
-   [相關主題](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a>知道要在哪裡執行著色器計算

頂點著色器會執行作業，包括提取頂點和執行矩陣資料的矩陣轉換。 一般來說，每個頂點都會執行一次頂點著色器。

圖元著色器會執行包括提取材質資料和執行光源計算的作業。 一般而言，圖元著色器會針對指定的幾何片段，每個圖元執行一次。

一般而言，圖元會人數超過場景中的頂點，因此圖元著色器的執行頻率會比頂點著色器更頻繁。

當您設計著色器演算法時，請記住下列事項：

-   可能的話，請在頂點著色器上執行計算。 在圖元著色器上執行的計算，比在頂點著色器上執行的計算更昂貴。
-   考慮使用每個頂點計算，以改善密集網格等情況下的效能。 針對密集網格，每個頂點計算可能產生的結果，會與每個圖元計算產生的結果以視覺化方式區分。

## <a name="skip-unnecessary-instructions"></a>略過不必要的指示

在 HLSL 中，動態分支能讓您限制執行的指令數目。 因此，動態分支可協助加速著色器執行時間。 如果未顯示幾何或圖元，請使用動態分支來結束著色器或限制指令。 例如，如果圖元不亮，則不會有執行光源演算法的點。

下表列出您可以在著色器中測試條件，並使用動態分支來略過不必要指示的一些案例。 資料表並不完整。 相反地，它的目的是要提供您將程式碼優化的概念。



| 要檢查的條件                                    | 著色器中的回應       |
|-------------------------------------------------------|------------------------------|
| Alpha 檢查會判斷不會顯示圖元。 | 略過著色器的其餘部分。 |
| 圖元或幾何完全 fogged。                | 略過著色器的其餘部分。 |
| 外觀權重為零。                                | 略過骨骼。                  |
| 淺衰減是零。                            | 略過光源。               |
| 非正面的 Lambertian 字詞。                         | 略過光源。               |



 

## <a name="pack-variables-and-interpolants"></a>套件變數和 Interpolants

請注意著色器資料所需的空間。 盡可能將最多的資訊封裝到變數或 interpolant 中。 有時候，來自兩個變數的資訊可以封裝至單一變數的記憶體空間中。

## <a name="reduce-shader-complexity"></a>減少著色器複雜度

將著色器保持在小型和簡單的部分。 一般情況下，使用較少指令執行的著色器會以更多的指令著色器執行得更快。 您也可以更輕鬆地對較小、較不復雜的著色器進行調試和優化。

## <a name="related-topics"></a>[相關主題]

[HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>相關主題

<dl> <dt>

[HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




