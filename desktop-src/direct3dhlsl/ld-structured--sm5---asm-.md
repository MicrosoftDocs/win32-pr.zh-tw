---
title: 'ld_structured (sm5-asm) '
description: 從結構化緩衝區中讀取 1-4 32 位元件的隨機存取。
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfb3c19b56271a02c20ff85dd71352b545843f62b3d01292e87c2edbd6384d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562308"
---
# <a name="ld_structured-sm5---asm"></a>ld \_ 結構化 (sm5-asm) 

從結構化緩衝區中讀取 1-4 32 位元件的隨機存取。



| ： ld \_ 結構化 dst0 \[ . mask \] ，srcAddress \[ . select \_ component \] ，srcByteOffset \[ . select \_ component \] ，src0 \[ . swizzle\] |
|-------------------------------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                                       | 描述                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[在 \] 操作結果的位址中。<br/>                                                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>             | \[在中， \] 指定要讀取之結構的索引。<br/>                                                                                            |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[在中， \] 指定要開始讀取的結構中的位元組位移。 <br/>                                                                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | 要從中讀取的緩衝區。 此參數必須是 SRV (t \#) ，UAV (u \#) 。 在計算著色器中，它也可以是執行緒群組的共用記憶體 (g \#) 。 <br/> |



 

## <a name="remarks"></a>備註

從結構讀取的資料相當於下列虛擬程式碼：其中有位移、位址、緩衝區內容的指標、來源的 stride，以及以線性方式儲存的資料。

``` syntax
                    BYTE *BufferContents;         // from SRV or UAV
                    UINT BufferStride;            // from base resource
                    UINT srcAddress, srcByteOffset;   // from source registers
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + BufferStride * srcByteOffset
                                + srcOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

這個虛擬虛擬的會顯示作業的運作方式，但實際的資料不需要以線性方式儲存。 如果資料不是以線性方式儲存，則實際的指令運算必須符合上述作業的行為。

除了 SrcByteOffset 之外，任何給定32位元件之 u/t 上的界限定址都會傳回 \# \# 0，但除了，加上 swizzle 也會導致超出範圍存取您/t 的限制之外 \# \# ，所有元件)  (的傳回值都是未定義的。

G (界限的範圍外， \# 該特定 g 的界限 \# ，而非任何指定32位元件的所有共用記憶體) 會傳回未定義的結果。

*srcByteOffset* 是不同于 *srcAddress* 的引數，因為它通常是常值。 尚未對結構化記憶體上的 atomics 執行此參數分離。

cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援這個 UAV、SRV 和 TGSM 的指令。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此，此指示適用于適用于 Direct3D 11.1 執行時間的所有 UAVs 著色器階段（從 Windows 8 開始提供）。



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



 

cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援這個 UAV、SRV 和 TGSM 的指令。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





