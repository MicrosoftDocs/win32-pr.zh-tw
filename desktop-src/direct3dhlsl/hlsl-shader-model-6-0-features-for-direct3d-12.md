---
title: HLSL 著色器模型6。0
description: 描述新增至 HLSL 著色器模型6.0 的 wave 作業內建。
ms.assetid: BF968CD3-AC67-48DB-B93F-EF54B680106F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2d082fc131c7cd08db9eb1861c4af39d600f40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971725"
---
# <a name="hlsl-shader-model-60"></a>HLSL 著色器模型6。0

描述新增至 HLSL 著色器模型6.0 的 wave 作業內建。

- [著色器模型6。0](#shader-model-60)
- [術語](#terminology)
- [網底語言內建函式](#shading-language-intrinsics)
    - [Wave 查詢](#wave-query)
    - [Wave 投票](#wave-vote)
    - [Wave 廣播](#wave-broadcast)
    - [減少 Wave](#wave-reduction)
    - [Wave 掃描和前置詞](#wave-scan-and-prefix)
    - [四個全半隨機作業](#quad-wide-shuffle-operations)
- [硬體功能](#hardware-capability)
- [相關主題](#related-topics)

## <a name="shader-model-60"></a>著色器模型6。0

針對較早的著色器模型，HLSL 程式設計只會公開單一執行執行緒。 從模型6.0 開始提供新的 wave 層級作業，以明確利用目前 Gpu 的平行處理原則-許多執行緒可以同時在相同核心上的密集建置中執行。 例如，當同步處理的範圍在 SIMD 處理器的寬度內，或某些其他已知為不可部分完成的執行緒時，模型6.0 內建函式可讓您排除關卡結構。

可能的使用案例包括：資料流程壓縮、縮減、區塊變換、bitonic 排序或快速傅立葉轉換 (FFT) 、分類收納、串流消除重複和類似案例。

大部分的內建函式都會出現在圖元著色器和計算著色器中，但 (針對每個函式) 注明一些例外狀況。 這些函式已新增至在 API 層級12下的 DirectX 功能等級12.0 需求。

這些函式的 *<type>* 參數和傳回值意指運算式的類型，支援的型別是下列清單中 *也* 存在於您應用程式的目標著色器模型中的類型：

- 半、half2、half3、half4
- float、float2、float3、float4
- double、double2、double3、double4
- int、int2、int3、int4
- uint、uint2、uint3、uint4
- short、short2、short3、short4
- ushort、ushort2、ushort3、ushort4
- uint64 \_ t、uint64 \_ t2、uint64 \_ t3、uint64 \_ t4

某些作業 (例如位運算子) 只支援整數類型。

## <a name="terminology"></a>詞彙

| | |
|-|-|
| **字詞** | **[定義]** |
| 車道 | 單一線程執行。 6.0 版之前的著色器模型只會在語言層級公開上述其中一種模型，讓您完全擴充至平行 SIMD 處理以執行。 |
| Wave | 在處理器中) 同時執行的一組通道 (執行緒。 不需要明確的阻礙，以確保它們會以平行方式執行。 類似的概念包括「變形」和「wavefront」。 |
| 非使用中航道 | 未執行的通道，例如因為控制流程，或沒有足夠的工作來填滿 wave 的大小下限。 |
| 使用中車道 | 正在執行執行的通道。 在圖元著色器中，它可能包含任何協助程式圖元車道。 |
| 四 | 一組4個連續的通道，對應至以2x2 正方形排列的圖元。 它們是用來依 x 或 y 差異來預估漸層。 Wave 可能由多個四邊形組成。 作用中的四個圖元中的所有圖元都 (執行，而且可能是「使用中通道」 ) ，但不會產生可見結果的圖元稱為「協助程式通道」。 |
| Helper 航道 | 僅針對圖元著色器四邊形中的漸層用途而執行的通道。 這類通道的輸出將會被捨棄，因此不會轉譯為目的介面。 |

## <a name="shading-language-intrinsics"></a>網底語言內建函式

此著色器模型的所有作業都已新增至範圍內的內建函式。

### <a name="wave-query"></a>Wave 查詢

查詢單一 wave 的內建函式。

| | | | |
|-|-|-|-|
| **內建** | **說明** | **像素著色器** | **計算著色器** |
| [**WaveGetLaneCount**](wavegetlanecount.md) | 傳回目前 wave 中的航道數目。 | \* | \* |
| [**WaveGetLaneIndex**](wavegetlaneindex.md) | 傳回目前 wave 內目前通道的索引。 | \* | \* |
| [**WaveIsFirstLane**](waveisfirstlane.md) | 只針對目前 wave 中具有最小索引的現用通道傳回 true | \* | \* |

### <a name="wave-vote"></a>Wave 投票

這一組內建函式會比較目前在目前使用中的執行緒之間的值。

| | | | |
|-|-|-|-|
| **內建** | **說明** | **像素著色器** | **計算著色器** |
| [**WaveActiveAnyTrue**](waveanytrue.md) | 如果目前 wave 的任何使用中通道中的運算式為 true，則傳回 true。 | \* | \* |
| [**WaveActiveAllTrue**](wavealltrue.md) | 如果目前 wave 的所有作用中通道中的運算式為 true，則傳回 true。 | \* | \* |
| [**WaveActiveBallot**](waveballot.md) | 針對指定 wave 中所有使用中的通道，傳回布林運算式評估的64位不帶正負號的整數位遮罩。 | \* | \* |

### <a name="wave-broadcast"></a>Wave 廣播

這些內建函式可讓目前 wave 中的所有使用中通道，從指定的通道接收值，有效地將其廣播。 來自無效通道的傳回值未定義。

| | | | |
|-|-|-|-|
| **內建** | **說明** | **像素著色器** | **計算著色器** |
| [**WaveReadLaneAt**](wavereadlaneat.md) | 傳回指定 wave 內給定通道索引的運算式值。 | \* | \* |
| [**WaveReadLaneFirst**](wavereadfirstlane.md) | 傳回目前 wave （具有最小索引）之使用中通道的運算式值。 | \* | \* |

### <a name="wave-reduction"></a>減少 Wave

這些內建函式會在 wave 中的所有使用中通道上計算指定的作業，並將最終結果廣播到所有使用中的通道。 因此，最終的輸出保證會在 wave 之間保持一致。

| | | | |
|-|-|-|-|
| **內建** | **說明** | **像素著色器** | **計算著色器** |
| [**WaveActiveAllEqual**](waveactiveallequal.md) | 如果目前 wave (中的每個使用中通道的運算式相同，則會傳回 true，因此) 之間保持一致。 | \* | \* |
| [**WaveActiveBitAnd**](waveallbitand.md) | 傳回目前 wave 中所有使用中通道的所有運算式值的位 AND，然後將結果複製到 wave 中的所有通道。 | \* | \* |
| [**WaveActiveBitOr**](waveallbitor.md) | 傳回目前 wave 中所有使用中通道之所有運算式值的位 OR，並且將結果複寫至 wave 中的所有通道。 | \* | \* |
| [**WaveActiveBitXor**](waveallbitxor.md) | 傳回目前 wave 中所有使用中通道的所有運算式值的位互斥 OR，並將結果複寫至 wave 中的所有通道。 | \* | \* |
| [**WaveActiveCountBits**](waveactivecountbits.md) | 計算在目前 wave 的所有作用中通道上評估為 true 的布林值變數數目，並將結果複製到 wave 中的所有通道。 | \* | \* |
| [**WaveActiveMax**](waveallmax.md) | 計算目前 wave 中所有使用中通道的運算式最大值，並將結果複製到 wave 中的所有通道。 | \* | \* |
| [**WaveActiveMin**](waveallmin.md) | 計算目前 wave 中所有使用中通道的運算式最小值，並將結果複寫至 wave 中的所有通道。 | \* | \* |
| [**WaveActiveProduct**](waveallproduct.md) | 將運算式的值與目前 wave 中的所有使用中車道相乘，並將結果複寫至 wave 中的所有通道。 | \* | \* |
| [**WaveActiveSum**](waveallsum.md) | 加總目前 wave 中所有使用中通道的運算式值，並將其複製到目前 wave 中的所有通道，並將結果複寫至 wave 中的所有通道。 | \* | \* |

### <a name="wave-scan-and-prefix"></a>Wave 掃描和前置詞

這些內建函式會將作業套用到每個通道，並將計算的每個部分結果保留在對應的通道中。

| | | | |
|-|-|-|-|
| **內建** | **說明** | **像素著色器** | **計算著色器** |
| [**WavePrefixCountBits**](waveprefixcountbytes.md) | 傳回所有在所有作用中的通道上，所有指定的布林值變數設定為 true 的總和，其索引小於目前的航道。 | \* | \* |
| [**WavePrefixSum**](waveprefixsum.md) | 傳回使用中通道的所有值加上小於此值的總和。 | \* | \* |
| [**WavePrefixProduct**](waveprefixproduct.md) | 傳回信道中這個指定 wave 之前的所有值的乘積。 | \* | \* |

### <a name="quad-wide-shuffle-operations"></a>四個全半隨機作業

這些內建函式會對已知包含圖元著色器四邊形的所有值執行交換作業，如這裡所定義。 四個四個圖元的索引定義于掃描行或讀取順序中，四個中的座標如下：

+---------> X 

|[0] [1] 

|[2] [3] 

v 

Y 


這些常式可以在計算著色器或圖元著色器中運作。 在計算著色器中，它們在四邊形中的運作方式是在 SIMD wave 內定義為平均分配4群組。 在圖元著色器中，它們應該用於 WaveQuadLanes 所捕獲的波浪，否則結果會是未定義的。

| | | | |
|-|-|-|-|
| **內建** | **說明** | **像素著色器** | **計算著色器** |
| [**QuadReadLaneAt**](quadreadlaneat.md) | 從 quadLaneID 0 所識別的目前四顆線的通道中，傳回指定的來源值， \[ \] 其必須在四個之間保持一致。 | \* | |
| [**QuadReadAcrossDiagonal**](quadreadacrossdiagonal.md) | 傳回指定的區域值，此值是從這個四個對角線中的相反通道讀取的。 | \* | |
| [**QuadReadAcrossX**](quadswapx.md) | 傳回指定的來源值，此值是從這個四的 X 方向中的另一個通道讀取的。 | \* | |
| [**QuadReadAcrossY**](quadswapy.md) | 傳回從這個四個 Y 方向的其他通道讀取的指定來源值。 | \* | |

## <a name="hardware-capability"></a>硬體功能

若要檢查是否有任何特定硬體可使用 wave 作業功能，請呼叫 [**ID3D12Device：： CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)，並記下 [**D3D12 \_ 功能 \_ 資料 \_ D3D12 \_ OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1) 結構的描述與使用。

## <a name="related-topics"></a>相關主題

* [HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)
* [著色器模型6內建函式](shader-model-6-0.md)