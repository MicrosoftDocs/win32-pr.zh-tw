---
title: 著色器模型6
description: 著色器模型6.0 新增了圖元和計算著色器的一系列 wave 作業內建函式。
ms.assetid: 2F28F86D-F599-47EA-90D7-6833ABA976FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609f0a9d36fbf7414e724cd31bc05a8e4d6abdefa5c842f30934feba0dffb868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790697"
---
# <a name="shader-model-6"></a>著色器模型6

所有的非四個相關 Wave 內建都可在所有著色器階段中使用。 四 wave 內建函式僅適用于圖元和計算著色器。

## <a name="in-this-section"></a>本節內容



| 主題                                                                 | 描述                                                                                                                                                               |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QuadReadAcrossDiagonal**](quadreadacrossdiagonal.md)<br/> | 傳回指定的區域值，此值是從這個四個對角線中的相反通道讀取的。<br/>                                                                |
| [**QuadReadLaneAt**](quadreadlaneat.md)<br/>                   | 從目前四內的通道識別碼所識別的通道傳回指定的來源值。<br/>                                                            |
| [**QuadReadAcrossX**](quadswapx.md)<br/>                      | 傳回指定的區域值，此值會從這個四的 X 方向中的另一個通道讀取。<br/>                                                                    |
| [**QuadReadAcrossY**](quadswapy.md)<br/>                      | 傳回從這個四個 Y 方向的其他通道讀取的指定來源值。<br/>                                                                   |
| [**WaveActiveAllEqual**](waveactiveallequal.md)<br/>           | 如果目前 wave (中的每個使用中通道的運算式相同，則會傳回 true，因此) 之間保持一致。<br/>                                             |
| [**WaveActiveBitAnd**](waveallbitand.md)<br/>                  | 傳回目前 wave 中所有使用中通道的所有運算式值的位 AND，然後將它複製回所有使用中的通道。 <br/>           |
| [**WaveActiveBitOr**](waveallbitor.md)<br/>                    | 傳回目前 wave 中所有使用中通道的所有運算式值位 OR，然後將其複寫回所有使用中的通道。 <br/>            |
| [**WaveActiveBitXor**](waveallbitxor.md)<br/>                  | 傳回目前 wave 中所有使用中通道的所有運算式值的位 XOR，然後將它複製回所有使用中的通道。 <br/>           |
| [**WaveActiveCountBits**](waveactivecountbits.md)<br/>         | 計算在目前 wave 的所有作用中通道上評估為 true 的布林值變數數目，並將結果複製到 wave 中的所有通道。<br/> |
| [**WaveActiveMax**](waveallmax.md)<br/>                        | 傳回目前 wave 中所有使用中通道的運算式的最大值，並將其複寫回所有使用中的通道。 <br/>                           |
| [**WaveActiveMin**](waveallmin.md)<br/>                        | 傳回在目前 wave 的所有作用中通道上，運算式的最小值，將它複製回所有使用中的通道。 <br/>                               |
| [**WaveActiveProduct**](waveallproduct.md)<br/>                | 將運算式的值與目前 wave 中所有使用中的車道相乘，並將其複寫回所有使用中的通道。<br/>                       |
| [**WaveActiveSum**](waveallsum.md)<br/>                        | 加總目前 wave 中所有使用中通道的運算式值，並將其複製到目前 wave 中的所有通道。<br/>                            |
| [**WaveActiveAllTrue**](wavealltrue.md)<br/>                   | 如果目前 wave 的所有作用中通道中的運算式為 true，則傳回 true。<br/>                                                                                |
| [**WaveActiveAnyTrue**](waveanytrue.md)<br/>                   | 如果目前 wave 的任何使用中通道中的運算式為 true，則傳回 true。<br/>                                                                         |
| [**WaveActiveBallot**](waveballot.md)<br/>                     | 針對指定 wave 中所有使用中的通道，傳回評估布林運算式的4位不帶正負號的整數位遮罩。 <br/>                              |
| [**WaveGetLaneCount**](wavegetlanecount.md)<br/>               | 傳回 wave 在此架構上的航道數目。 <br/>                                                                                                   |
| [**WaveGetLaneIndex**](wavegetlaneindex.md)<br/>               | 傳回目前 wave 內目前通道的索引。 <br/>                                                                                                |
| [**WaveIsFirstLane**](waveisfirstlane.md)<br/>                 | 只針對目前 wave 中具有最小索引的使用中通道傳回 true。 <br/>                                                                            |
| [**WavePrefixCountBits**](waveprefixcountbytes.md)<br/>        | 傳回所有在所有作用中的通道上，所有指定的布林值變數設定為 true 的總和，其索引小於目前的航道。 <br/>                        |
| [**WavePrefixProduct**](waveprefixproduct.md)<br/>             | 使用小於此通道的索引，傳回這個波中使用中通道內所有值的乘積。<br/>                                                    |
| [**WavePrefixSum**](waveprefixsum.md)<br/>                     | 傳回使用中通道的所有值加上小於此值的總和。<br/>                                                                   |
| [**WaveReadLaneFirst**](wavereadfirstlane.md)<br/>             | 傳回目前 wave （具有最小索引）之使用中通道的運算式值。 <br/>                                                          |
| [**WaveReadLaneAt**](wavereadlaneat.md)<br/>                   | 傳回指定 wave 內給定通道索引的運算式值。<br/>                                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型與著色器設定檔](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 





