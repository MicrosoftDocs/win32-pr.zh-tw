---
title: 'atomic_umax (sm5-asm) '
description: 記憶體最大不可部分完成的不帶正負號的整數。
ms.assetid: 7255B67A-37BE-443A-BDF2-A1D4A56C5E11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6984a2ef2ea8ba186976670ec3b0f03446bf188de9c619301917610f4c3ecc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794856"
---
# <a name="atomic_umax-sm5---asm"></a>不可部分完成 \_ 的 umax (sm5-asm) 

記憶體最大不可部分完成的不帶正負號的整數。



| 不可 \_ 部分完成的 umax dst，dstAddress \[ . swizzle \] ，src0 \[ . select \_ component\] |
|----------------------------------------------------------------------|



 



| Item                                                                                                           | 描述                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*Dst*<br/>                                                   | \[在 \] [要與 *src0* 比較的元件] 中。 此值必須是未排序的存取視圖 (UAV)  (u \#) 。 在計算著色器中，它也可以是執行緒群組的共用記憶體 (g \#) 。 <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[在 \] 記憶體位址中。<br/>                                                                                                                                                   |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[與 \] *dst* 比較的元件。<br/>                                                                                                                                   |



 

## <a name="remarks"></a>備註

此指令會 *32 在每* 個元件位址 dstAddress 的每個元件位址中，針對每個元件位址的 *src0* ，執行單一元件32位不帶正負號的最大運算元。

從位址取得的元件數目取決於 dst u \# 或 g 的維度 \# 。

如果 *dst* 是 u \# ，則可以宣告為 raw、具類型或結構化。 如果具型別，則必須使用 R32 uint/聖的系結資源格式宣告為 UINT/聖 \_ \_ 。

如果 *dst* 為 g \# ，則必須將它宣告為 raw 或結構化。

沒有任何專案會傳回給著色器。

如果著色器調用處于非使用中狀態，例如，如果圖元在先前的執行中已被捨棄，或圖元/樣本調用僅存在做為衍生的真實圖元/樣本的協助程式，則此指令不會在所有 (無訊息的情況下變更 *dst* 記憶體) 。

除了 u 的範圍外， \# 不會將任何內容寫入記憶體，除非 u \# 是結構化的，且在結構 (第二個元件) 的結構中的位元組位移會造成超出界限存取權，否則 UAV 的整個內容會變成未定義。

G (超出範圍的界限 \# \# ，而不是所有的共用記憶體) 會導致所有共用記憶體的整個內容變成未定義。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此指令：



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 否        |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 否        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





