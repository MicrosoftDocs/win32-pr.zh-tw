---
title: 內建函式
description: 下表列出 HLSL 中可用的內建函式。 每個函式都有簡短描述，以及參考頁面的連結，其中包含有關輸入引數和傳回型別的詳細資料。
ms.assetid: 7f1a3284-6053-4b6d-bd2e-5b33264fe883
keywords:
- 內建函式 HLSL
topic_type:
- apiref
api_name:
- Intrinsic Functions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60421d4278c4817f9b02811369fb7937a5f67aa734c6fae0c0c280d2edcf3d4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068178"
---
# <a name="intrinsic-functions"></a>內建函式

下表列出 HLSL 中可用的內建函式。 每個函式都有簡短描述，以及參考頁面的連結，其中包含有關輸入引數和傳回型別的詳細資料。



| 名稱                                                                                    | 描述                                                                                                                                                     | 最小著色器模型 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| [**中止**](abort.md)                                                                  | 終止目前正在執行的繪圖或分派呼叫。                                                                                                    | 4                    |
| [**Abs**](dx-graphics-hlsl-abs.md)                                                     | 每個元件) 的絕對值 (。                                                                                                                                 | 1¹                   |
| [**acos**](dx-graphics-hlsl-acos.md)                                                   | 傳回 x 各元件的反余弦。                                                                                                                   | 1¹                   |
| [**所有**](dx-graphics-hlsl-all.md)                                                     | 測試 x 的所有元件是否為非零。                                                                                                                        | 1¹                   |
| [**AllMemoryBarrier**](allmemorybarrier.md)                                            | 封鎖群組中所有線程的執行，直到所有記憶體存取都完成為止。                                                                       | 5                    |
| [**AllMemoryBarrierWithGroupSync**](allmemorybarrierwithgroupsync.md)                  | 封鎖群組中所有線程的執行，直到所有記憶體存取都已完成，且群組中的所有線程都已達到此呼叫。                   | 5                    |
| [**任何**](dx-graphics-hlsl-any.md)                                                     | 測試 x 的任何元件是否為非零。                                                                                                                          | 1¹                   |
| [**asdouble**](asdouble.md)                                                            | 將轉換值向量成雙精度浮點數。                                                                                                                        | 5                    |
| [**asfloat**](dx-graphics-hlsl-asfloat.md)                                             | 將輸入類型轉換成浮點數。                                                                                                                              | 4                    |
| [**asin**](dx-graphics-hlsl-asin.md)                                                   | 傳回 x 各元件的反正弦。                                                                                                                     | 1¹                   |
| [**asint**](dx-graphics-hlsl-asint.md)                                                 | 將輸入類型轉換成整數。                                                                                                                           | 4                    |
| [**asuint**](asuint.md)                                                                | 將64位類型的位模式向量為 uint。                                                                                                        | 5                    |
| [**asuint**](dx-graphics-hlsl-asuint.md)                                               | 將輸入類型轉換成不帶正負號的整數。                                                                                                                  | 4                    |
| [**atan**](dx-graphics-hlsl-atan.md)                                                   | 傳回 x 的反正切值。                                                                                                                                    | 1¹                   |
| [**atan2**](dx-graphics-hlsl-atan2.md)                                                 | 傳回兩個值 (x，y) 的反正切值。                                                                                                                  | 1¹                   |
| [**ceil**](dx-graphics-hlsl-ceil.md)                                                   | 傳回大於或等於 x 的最小整數。                                                                                               | 1¹                   |
| [**CheckAccessFullyMapped**](checkaccessfullymapped.md)                                | 判斷 **範例** 或 **載入** 作業中的所有值是否已在並排顯示的 [資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚。 | 5                    |
| [**鉗**](dx-graphics-hlsl-clamp.md)                                                 | 個 x 至範圍 \[ 最小值（最大值） \] 。                                                                                                                             | 1¹                   |
| [**clip**](dx-graphics-hlsl-clip.md)                                                   | 如果 x 的任何元件小於零，則會捨棄目前的圖元。                                                                                            | 1¹                   |
| [**因為**](dx-graphics-hlsl-cos.md)                                                     | 傳回 x 的余弦值。                                                                                                                                        | 1¹                   |
| [**cosh**](dx-graphics-hlsl-cosh.md)                                                   | 傳回 x 的雙曲余弦值。                                                                                                                             | 1¹                   |
| [**countbits**](countbits.md)                                                          | 計算輸入整數中每個元件)  (的位數。                                                                                                 | 5                    |
| [**跨越**](dx-graphics-hlsl-cross.md)                                                 | 傳回兩個3D 向量的交叉乘積。                                                                                                                    | 1¹                   |
| [**D3DCOLORtoUBYTE4**](dx-graphics-hlsl-d3dcolortoubyte4.md)                           | Swizzles 和調整4D 向量 xto 的元件，以彌補某些硬體中缺乏 UBYTE4 支援。                                                 | 1¹                   |
| [**ddx**](dx-graphics-hlsl-ddx.md)                                                     | 傳回 x 的部分衍生（相對於螢幕空間 x 座標）。                                                                              | 2¹                   |
| [**ddx \_ 粗略**](ddx-coarse.md)                                                       | 計算相對於螢幕空間 x 座標的低精確度部分衍生。                                                                      | 5                    |
| [**ddx \_ 正常**](ddx-fine.md)                                                           | 計算相對於螢幕空間 x 座標的高精確度部分衍生。                                                                     | 5                    |
| [**ddy**](dx-graphics-hlsl-ddy.md)                                                     | 傳回 x 的部分衍生（相對於螢幕空間的 y 座標）。                                                                              | 2¹                   |
| [**ddy \_ 粗略**](ddy-coarse.md)                                                       | 計算相對於螢幕空間 y 座標的低精確度部分衍生。                                                                      | 5                    |
| [**ddy \_ 沒問題**](ddy-fine.md)                                                           | 計算相對於螢幕空間 y 座標的高精確度部分衍生。                                                                     | 5                    |
| [**度**](dx-graphics-hlsl-degrees.md)                                             | 將 x 從弧度轉換成度數。                                                                                                                             | 1¹                   |
| [**行列 式**](dx-graphics-hlsl-determinant.md)                                     | 傳回正方形矩陣 m 的行列式。                                                                                                                 | 1¹                   |
| [**DeviceMemoryBarrier**](devicememorybarrier.md)                                      | 封鎖群組中所有線程的執行，直到所有裝置記憶體存取都完成為止。                                                                | 5                    |
| [**DeviceMemoryBarrierWithGroupSync**](devicememorybarrierwithgroupsync.md)            | 封鎖群組中所有線程的執行，直到所有裝置記憶體存取都已完成，且群組中的所有線程都已達到此呼叫。            | 5                    |
| [**距離**](dx-graphics-hlsl-distance.md)                                           | 傳回兩個點之間的距離。                                                                                                                        | 1¹                   |
| [**點**](dx-graphics-hlsl-dot.md)                                                     | 傳回兩個向量的內積。                                                                                                                         | 1                    |
| [**Dst**](dst.md)                                                                      | 計算距離向量。                                                                                                                                   | 5                    |
| [**errorf**](errorf.md)                                                                | 將錯誤訊息提交至資訊佇列。                                                                                                              | 4                    |
| [**EvaluateAttributeAtCentroid**](evaluateattributeatcentroid.md)                      | 在圖元距心進行評估。                                                                                                                                | 5                    |
| [**EvaluateAttributeAtSample**](evaluateattributeatsample.md)                          | 在索引範例位置評估。                                                                                                                       | 5                    |
| [**EvaluateAttributeSnapped**](evaluateattributesnapped.md)                            | 以位移的圖元距心進行評估。                                                                                                                 | 5                    |
| [**exp**](dx-graphics-hlsl-exp.md)                                                     | 傳回以 e 為底數的指數。                                                                                                                                    | 1¹                   |
| [**exp2**](dx-graphics-hlsl-exp2.md)                                                   | 每個元件) 的基底2指數 (。                                                                                                                                | 1¹                   |
| [**f16tof32**](f16tof32.md)                                                            | 將儲存在 uint 低半部的 float16 轉換為浮點數。                                                                                             | 5                    |
| [**f32tof16**](f32tof16.md)                                                            | 將輸入轉換成 float16 型別。                                                                                                                          | 5                    |
| [**faceforward**](dx-graphics-hlsl-faceforward.md)                                     | 傳回-n \* 號 (點 (i，ng) ) 。                                                                                                                                 | 1¹                   |
| [**firstbithigh**](firstbithigh.md)                                                    | 取得第一個集合位從最高順序位開始，每個元件往下工作的位置。                                                 | 5                    |
| [**firstbitlow**](firstbitlow.md)                                                      | 傳回第一個設定位的位置，從最小的順序位開始，然後每個元件向上處理。                                                 | 5                    |
| [**地板**](dx-graphics-hlsl-floor.md)                                                 | 傳回小於或等於 x 的最大整數。                                                                                                  | 1¹                   |
| [**fma**](dx-graphics-hlsl-fma.md)                                                     | 傳回 b + c 的雙精確度融合乘積 \* 。                                                                                             | 5                    |
| [**fmod**](dx-graphics-hlsl-fmod.md)                                                   | 傳回 x/y 的浮點數餘數。                                                                                                                    | 1¹                   |
| [**壓裂**](dx-graphics-hlsl-frac.md)                                                   | 傳回 x 的小數部分。                                                                                                                               | 1¹                   |
| [**frexp**](dx-graphics-hlsl-frexp.md)                                                 | 傳回 x 的尾數和指數。                                                                                                                         | 2¹                   |
| [**fwidth**](dx-graphics-hlsl-fwidth.md)                                               | 傳回 abs (ddx (x) ) + abs (ddy (x) )                                                                                                                                | 2¹                   |
| [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md)       | 傳回呈現目標範例的數目。                                                                                                                    | 4                    |
| [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) | 傳回指定範例索引 (x，y) 的樣本位置。                                                                                                       | 4                    |
| [**GroupMemoryBarrier**](groupmemorybarrier.md)                                        | 封鎖群組中所有線程的執行，直到所有群組共用存取都完成為止。                                                                 | 5                    |
| [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md)              | 封鎖群組中所有線程的執行，直到完成所有群組共用存取，而且群組中的所有線程都已達到此呼叫。             | 5                    |
| [**InterlockedAdd**](interlockedadd.md)                                                | 針對 dest 資源變數執行保證的不可部分完成加入值。                                                                                        | 5                    |
| [**InterlockedAnd**](interlockedand.md)                                                | 執行保證的不可部分完成和。                                                                                                                               | 5                    |
| [**InterlockedCompareExchange**](interlockedcompareexchange.md)                        | 以不可部分完成的方式比較輸入與比較值，並交換結果。                                                                                 | 5                    |
| [**InterlockedCompareStore**](interlockedcomparestore.md)                              | 以原子方式將輸入與比較值進行比較。                                                                                                          | 5                    |
| [**InterlockedExchange**](interlockedexchange.md)                                      | 將值指派給 dest，並傳回原始值。                                                                                                           | 5                    |
| [**InterlockedMax**](interlockedmax.md)                                                | 執行保證的不可部分完成上限。                                                                                                                               | 5                    |
| [**InterlockedMin**](interlockedmin.md)                                                | 執行保證不可部分完成的最小值。                                                                                                                               | 5                    |
| [**InterlockedOr**](interlockedor.md)                                                  | 執行保證的不可部分完成或。                                                                                                                                | 5                    |
| [**InterlockedXor**](interlockedxor.md)                                                | 執行保證的不可部分完成 xor。                                                                                                                               | 5                    |
| [**isfinite**](dx-graphics-hlsl-isfinite.md)                                           | 如果 x 是有限的，則傳回 true，否則傳回 false。                                                                                                                   | 1¹                   |
| [**isinf**](dx-graphics-hlsl-isinf.md)                                                 | 如果 x 是 + INF 或-INF，則傳回 true，否則傳回 false。                                                                                                             | 1¹                   |
| [**isnan**](dx-graphics-hlsl-isnan.md)                                                 | 如果 x 是 NAN 或 QNAN，則傳回 true，否則傳回 false。                                                                                                              | 1¹                   |
| [**ldexp**](dx-graphics-hlsl-ldexp.md)                                                 | 傳回 x \* 2exp                                                                                                                                               | 1¹                   |
| [**長度**](dx-graphics-hlsl-length.md)                                               | 傳回向量 v 的長度。                                                                                                                             | 1¹                   |
| [**lerp**](dx-graphics-hlsl-lerp.md)                                                   | 傳回 x + s (y x) 。                                                                                                                                           | 1¹                   |
| [**點燃**](dx-graphics-hlsl-lit.md)                                                     | 傳回光源向量 (環境、擴散、反光、1)                                                                                                        | 1¹                   |
| [**日誌**](dx-graphics-hlsl-log.md)                                                     | 傳回 x 的底數（以 e 為底數）。                                                                                                                              | 1¹                   |
| [**log10**](dx-graphics-hlsl-log10.md)                                                 | 傳回 x 以10為底數的對數。                                                                                                                             | 1¹                   |
| [**log2**](dx-graphics-hlsl-log2.md)                                                   | 傳回 x 的以2為底數的對數。                                                                                                                              | 1¹                   |
| [**瘋狂**](mad.md)                                                                      | 針對三個值執行算術乘法/add 運算。                                                                                                  | 5                    |
| [**max**](dx-graphics-hlsl-max.md)                                                     | 選取 x 和 y 的較大。                                                                                                                                 | 1¹                   |
| [**分鐘**](dx-graphics-hlsl-min.md)                                                     | 選取 x 和 y 的較小者。                                                                                                                                  | 1¹                   |
| [**modf**](dx-graphics-hlsl-modf.md)                                                   | 將值 x 分割成小數和整數部分。                                                                                                           | 1¹                   |
| [**msad4**](dx-graphics-hlsl-msad4.md)                                                 | 比較4位元組的參考值和8位元組的來源值，並累積4加總的向量。                                                                | 5                    |
| [**mul**](dx-graphics-hlsl-mul.md)                                                     | 使用 x 和 y 執行矩陣乘法。                                                                                                                   | 1                    |
| [**雜訊**](dx-graphics-hlsl-noise.md)                                                 | 使用 Perlin 雜訊演算法產生隨機值。                                                                                                      | 1¹                   |
| [**規範**](dx-graphics-hlsl-normalize.md)                                         | 傳回正規化的向量。                                                                                                                                    | 1¹                   |
| [**戰俘**](dx-graphics-hlsl-pow.md)                                                     | 傳回 x<sup>y</sup>。                                                                                                                                          | 1¹                   |
| [**Printf**](printf.md)                                                                | 將自訂著色器訊息提交至資訊佇列。                                                                                                       | 4                    |
| [**Process2DQuadTessFactorsAvg**](process2dquadtessfactorsavg.md)                      | 產生四個修補程式的已更正鑲嵌因數。                                                                                                  | 5                    |
| [**Process2DQuadTessFactorsMax**](process2dquadtessfactorsmax.md)                      | 產生四個修補程式的已更正鑲嵌因數。                                                                                                  | 5                    |
| [**Process2DQuadTessFactorsMin**](process2dquadtessfactorsmin.md)                      | 產生四個修補程式的已更正鑲嵌因數。                                                                                                  | 5                    |
| [**ProcessIsolineTessFactors**](processisolinetessfactors.md)                          | 產生等值線的圓角鑲嵌因數。                                                                                                      | 5                    |
| [**ProcessQuadTessFactorsAvg**](processquadtessfactorsavg.md)                          | 產生四個修補程式的已更正鑲嵌因數。                                                                                                  | 5                    |
| [**ProcessQuadTessFactorsMax**](processquadtessfactorsmax.md)                          | 產生四個修補程式的已更正鑲嵌因數。                                                                                                  | 5                    |
| [**ProcessQuadTessFactorsMin**](processquadtessfactorsmin.md)                          | 產生四個修補程式的已更正鑲嵌因數。                                                                                                  | 5                    |
| [**ProcessTriTessFactorsAvg**](processtritessfactorsavg.md)                            | 產生三個修補程式的已更正鑲嵌因數。                                                                                                   | 5                    |
| [**ProcessTriTessFactorsMax**](processtritessfactorsmax.md)                            | 產生三個修補程式的已更正鑲嵌因數。                                                                                                   | 5                    |
| [**ProcessTriTessFactorsMin**](processtritessfactorsmin.md)                            | 產生三個修補程式的已更正鑲嵌因數。                                                                                                   | 5                    |
| [**弧度**](dx-graphics-hlsl-radians.md)                                             | 將 x 從度數轉換成弧度。                                                                                                                             | 1                    |
| [**rcp**](rcp.md)                                                                      | 計算每個元件的快速、近似、每個元件。                                                                                                       | 5                    |
| [**反映**](dx-graphics-hlsl-reflect.md)                                             | 傳回反映向量。                                                                                                                                    | 1                    |
| [**折射**](dx-graphics-hlsl-refract.md)                                             | 傳回折射向量。                                                                                                                                  | 1¹                   |
| [**reversebits**](reversebits.md)                                                      | 反轉每個元件的位順序。                                                                                                                  | 5                    |
| [**輪**](dx-graphics-hlsl-round.md)                                                 | 將 x 四捨五入到最接近的整數                                                                                                                                 | 1¹                   |
| [**rsqrt**](dx-graphics-hlsl-rsqrt.md)                                                 | 傳回 1/sqrt (x)                                                                                                                                              | 1¹                   |
| [**飽和**](dx-graphics-hlsl-saturate.md)                                           | 個 x 至範圍 \[ 0，1\]                                                                                                                                  | 1                    |
| [**標誌**](dx-graphics-hlsl-sign.md)                                                   | 計算 x 的正負號。                                                                                                                                         | 1¹                   |
| [**罪**](dx-graphics-hlsl-sin.md)                                                     | 傳回 x 的正弦函數                                                                                                                                           | 1¹                   |
| [**sincos**](dx-graphics-hlsl-sincos.md)                                               | 傳回 x 的正弦和余弦。                                                                                                                               | 1¹                   |
| [**sinh**](dx-graphics-hlsl-sinh.md)                                                   | 傳回 x 的雙曲正弦值                                                                                                                                | 1¹                   |
| [**smoothstep**](dx-graphics-hlsl-smoothstep.md)                                       | 傳回介於0和1之間的平滑 Hermite 插補。                                                                                                         | 1¹                   |
| [**sqrt**](dx-graphics-hlsl-sqrt.md)                                                   | 每個元件) 的平方根 (                                                                                                                                     | 1¹                   |
| [**步**](dx-graphics-hlsl-step.md)                                                   | 傳回 (x >= a) ？ 1 : 0                                                                                                                                     | 1¹                   |
| [**潭**](dx-graphics-hlsl-tan.md)                                                     | 傳回 x 的正切函數                                                                                                                                        | 1¹                   |
| [**tanh**](dx-graphics-hlsl-tanh.md)                                                   | 傳回 x 的雙曲正切值                                                                                                                             | 1¹                   |
| [**tex1D (s，t)**](dx-graphics-hlsl-tex1d.md)                                           | 1D 紋理查閱。                                                                                                                                              | 1                    |
| [**tex1D (s、t、ddx、ddy)**](dx-graphics-hlsl-tex1d-s-t-ddx-ddy.md)                     | 1D 紋理查閱。                                                                                                                                              | 2¹                   |
| [**tex1Dbias**](dx-graphics-hlsl-tex1dbias.md)                                         | 具有偏差的1D 紋理查閱。                                                                                                                                    | 2¹                   |
| [**tex1Dgrad**](dx-graphics-hlsl-tex1dgrad.md)                                         | 使用漸層的1D 紋理查閱。                                                                                                                              | 2¹                   |
| [**tex1Dlod**](dx-graphics-hlsl-tex1dlod.md)                                           | 使用」 LOD 的1D 紋理查閱。                                                                                                                                     | 3¹                   |
| [**tex1Dproj**](dx-graphics-hlsl-tex1dproj.md)                                         | 使用 projective 除的1D 紋理查閱。                                                                                                                       | 2¹                   |
| [**tex2D (s，t)**](dx-graphics-hlsl-tex2d.md)                                           | 2D 材質查閱。                                                                                                                                              | 1¹                   |
| [**tex2D (s、t、ddx、ddy)**](dx-graphics-hlsl-tex2d-s-t-ddx-ddy.md)                     | 2D 材質查閱。                                                                                                                                              | 2¹                   |
| [**tex2Dbias**](dx-graphics-hlsl-tex2dbias.md)                                         | 具有偏差的2D 材質查閱。                                                                                                                                    | 2¹                   |
| [**tex2Dgrad**](dx-graphics-hlsl-tex2dgrad.md)                                         | 2D 紋理查閱與漸層。                                                                                                                              | 2¹                   |
| [**tex2Dlod**](dx-graphics-hlsl-tex2dlod.md)                                           | 使用」 LOD 進行2D 紋理查閱。                                                                                                                                     | 3                    |
| [**tex2Dproj**](dx-graphics-hlsl-tex2dproj.md)                                         | 使用 projective 除的2D 材質查閱。                                                                                                                       | 2¹                   |
| [**tex3D (s，t)**](dx-graphics-hlsl-tex3d.md)                                           | 3D 紋理查閱。                                                                                                                                              | 1¹                   |
| [**tex3D (s、t、ddx、ddy)**](dx-graphics-hlsl-tex3d-s-t-ddx-ddy.md)                     | 3D 紋理查閱。                                                                                                                                              | 2¹                   |
| [**tex3Dbias**](dx-graphics-hlsl-tex3dbias.md)                                         | 具有偏差的3D 紋理查閱。                                                                                                                                    | 2¹                   |
| [**tex3Dgrad**](dx-graphics-hlsl-tex3dgrad.md)                                         | 使用漸層的3D 紋理查閱。                                                                                                                              | 2¹                   |
| [**tex3Dlod**](dx-graphics-hlsl-tex3dlod.md)                                           | 使用」 LOD 的3D 紋理查閱。                                                                                                                                     | 3¹                   |
| [**tex3Dproj**](dx-graphics-hlsl-tex3dproj.md)                                         | 使用 projective 除的3D 紋理查閱。                                                                                                                       | 2¹                   |
| [**texCUBE (s，t)**](dx-graphics-hlsl-texcube.md)                                       | Cube 紋理查閱。                                                                                                                                            | 1¹                   |
| [**texCUBE (s、t、ddx、ddy)**](dx-graphics-hlsl-texcube-s-t-ddx-ddy.md)                 | Cube 紋理查閱。                                                                                                                                            | 2¹                   |
| [**texCUBEbias**](dx-graphics-hlsl-texcubebias.md)                                     | 具有偏差的 Cube 紋理查閱。                                                                                                                                  | 2¹                   |
| [**texCUBEgrad**](dx-graphics-hlsl-texcubegrad.md)                                     | 具有漸層的立方體紋理查閱。                                                                                                                            | 2¹                   |
| [**texCUBElod**](dx-graphics-hlsl-texcubelod.md)                                       | 使用」 LOD 的 Cube 紋理查閱。                                                                                                                                   | 3¹                   |
| [**texCUBEproj**](dx-graphics-hlsl-texcubeproj.md)                                     | 使用 projective 除的 Cube 紋理查閱。                                                                                                                     | 2¹                   |
| [**變為**](dx-graphics-hlsl-transpose.md)                                         | 傳回矩陣 m 的調換。                                                                                                                          | 1                    |
| [**trunc**](dx-graphics-hlsl-trunc.md)                                                 | 將浮點值 (s) 截斷為整數值 (s)                                                                                                            | 1                    |



 

¹請參閱參考頁面中的限制。

## <a name="component-and-template-types"></a>元件和範本類型

HLSL 內建函式聲明會針對輸入參數引數和傳回值使用元件類型和範本類型。 下表列出可用的類型。



| 這些範本類型 | 描述                                           | 支援這些資料類型                                        |
|----------------------|-------------------------------------------------------|-----------------------------------------------------------------|
| 矩陣               | 最多16個元件，取決於宣告      | [基本 HLSL 類型](dx-graphics-hlsl-data-types.md)             |
| object               | 取樣器物件                                        | *取樣* 器、 *sampler1D*、 *sampler2D*、 *sampler3D*、 *samplerCUBE* |
| 純量 (scalar)               | 1個元件                                           | [基本 HLSL 類型](dx-graphics-hlsl-data-types.md)             |
| 向量               | 1個元件最小值，4個元件最大 (內含)  | [基本 HLSL 類型](dx-graphics-hlsl-data-types.md)             |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[HLSL 的參考](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 