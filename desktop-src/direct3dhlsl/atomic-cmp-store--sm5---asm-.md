---
title: 'atomic_cmp_store (sm5-asm) '
description: 不可部分完成的比較和寫入至記憶體。
ms.assetid: 1B97E983-11A9-47E4-B274-E94083837C6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dbc57b14b4279b9bd4844d89492852ae915d9d900ed04421eeeccc367979a63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118795160"
---
# <a name="atomic_cmp_store-sm5---asm"></a>不可部分完成 \_ \_ 的 cmp 存放區 (sm5-asm) 

不可部分完成的比較和寫入至記憶體。



| 不可 \_ \_ 部分完成的 cmp store Dst、dstAddress \[ . swizzle \] 、src0 \[ 。 select \_ component \] ，src1 \[ . select \_ component\] |
|--------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                           | 描述                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*Dst*<br/>                                                   | \[在 \] 要與 *src0* 比較的元件中。 此值必須是未排序的存取視圖 (UAV)  (u \#) 。 在計算著色器中，它也可以是執行緒群組的共用記憶體 (g \#) 。 <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[在 \] 記憶體位址中。<br/>                                                                                                                                                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[\]與 *dst* 比較的32位值。<br/>                                                                                                                                 |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                                | \[\]如果比較的值相同，則為要寫入記憶體的值。 <br/>                                                                                                     |



 

## <a name="remarks"></a>備註

此指令會在每個元件位址 *dstAddress* 的32位上執行運算元 *src0* 與 *dst* 的單一元件32位值比較。

如果比較的值相同， *src1* 中的單一元件32位值會寫入目的地記憶體。 否則，不會變更目的地。

整個比較和寫入作業會以不可部分完成的方式執行。

如果 *dst* 是 u \# ，則可以宣告為 raw、具類型或結構化。 如果具型別，則必須使用 R32 uint/聖的系結資源格式宣告為 UINT/聖 \_ \_ 。

如果 *dst* 為 g \# ，則必須將它宣告為 raw 或結構化。

從位址取得的元件數目取決於 dst u \# 或 g 的維度 \# 。

沒有任何專案會傳回給著色器。

如果著色器調用處于非使用中狀態，例如，如果已在其執行之前捨棄圖元，或圖元/範例指令未以無訊息方式變更所有 (的 *dst* 記憶體) 。

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

 

 





