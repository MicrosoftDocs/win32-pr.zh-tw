---
title: 'ld_raw (sm5-asm) '
description: 從原始緩衝區隨機存取 1-4 32 位元件。
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85fd8ec84b574d506a02812b20f4728e3f7a996ec76ad8569645d4c1643b0ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511088"
---
# <a name="ld_raw-sm5---asm"></a>ld \_ raw (sm5-asm) 

從原始緩衝區隨機存取 1-4 32 位元件。



| ld \_ raw dst0 \[ mask \] ，srcByteOffset \[ . select \_ component \] ，src0 \[ . swizzle\] |
|------------------------------------------------------------------------------|



 



| 項目                                                                                                                       | 描述                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[在 \] 操作結果的位址中。<br/> |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[在中， \] 指定要讀取的位移。<br/>          |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[在 \] 要讀取的元件中。 <br/>                     |



 

## <a name="remarks"></a>備註

*src0* 必須是：

-   任何著色器階段： SRV (t \#) ld st
-   計算著色器或圖元著色器： UAV (u \#) 
-   計算著色器：執行緒群組共用記憶體 (g \#) 

*srcByteOffset* 會將基底32位值指定在記憶體中，以供可讀取資料的4個連續32位值的視窗使用，視其他參數上的 swizzle 和遮罩而定。

從原始緩衝區讀取的資料相當於下列虛擬程式碼：其中有位移、位址、緩衝區內容的指標、來源的 stride，以及以線性方式儲存的資料。

``` syntax
                    BYTE *BufferContents;         // from src0
                    UINT srcByteOffset;           // from srcRegister
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + srcByteOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

\#任何指定32位元件之 u/t 上的界限定址 \# 都為該元件傳回0。

G (界限的範圍外， \# 該特定 g 的界限 \# ，而非任何指定32位元件的所有共用記憶體) 會傳回未定義的結果。

cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援此 UAV 和 SRV 指令。

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



 

cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援此 UAV 和 SRV 指令。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





