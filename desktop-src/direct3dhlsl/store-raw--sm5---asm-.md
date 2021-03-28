---
title: 'store_raw (sm5-asm) '
description: 隨機存取將 1-4 32 位元件寫入至無型別的記憶體。
ms.assetid: D166116A-CF4E-4020-9F6A-F9CEEFCDAB21
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44b4d22a576853fb8b7d2c43fcb6a2d7fc9a448
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373883"
---
# <a name="store_raw-sm5---asm"></a>儲存 \_ 原始 (sm5-asm) 

隨機存取將 1-4 32 位元件寫入至無型別的記憶體。



| store \_ raw dst0 \[ . write \_ mask \] ，dstByteOffset \[ . select \_ component \] ，src0 \[ . swizzle\] |
|----------------------------------------------------------------------------------------|



 



| 項目                                                                                                                       | 描述                                |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[在 \] 記憶體位址中。<br/>      |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*<br/> | \[在 \] 位移中。<br/>              |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[在 \] 要寫入的元件中。<br/> |



 

## <a name="remarks"></a>備註

此指令會 \* 在 *dstByteOffset* 中的位移執行從 *src0* 寫入至 *dst0* 的1-4 元件32位元件。 沒有格式轉換。

*dst0* 必須是 UAV (u \#) ，或在計算著色器中，它也可以是執行緒群組的共用記憶體 (g \#) 。

*dstByteOffset* 會根據其他參數上的 swizzle 和 mask，將記憶體中的基底32位值指定為4個連續32位值的視窗，其中可能會寫入資料。

寫入的資料位置相當於下列虛擬程式碼，它會顯示位址、緩衝區內容的指標，以及以線性方式儲存的資料。

``` syntax
                    BYTE *BufferContents;          // from src0
                    UINT dstByteOffset;            // source register
                    BYTE *WriteLocation;           // value to calculate

                    // calculate writing location
                    WriteLocation = BufferContents 
                                + dstByteOffset;

                    // calculate the number of components to write
                    switch (dstWriteMask)
                    {
                        x:    WriteComponents = 1; break;
                        xy:   WriteComponents = 2; break;
                        xyz:  WriteComponents = 3; break;
                        xyzw: WriteComponents = 4; break;
                        default:  // only these masks are valid                              
                    }

                    // copy the data from the source register with
                    //    the swizzle applied
                    memcpy(WriteLocation, swizzle(src0, src0.swizzle), 
                             WriteComponents * sizeof(UINT32));
```

這個虛擬虛擬的會顯示作業的運作方式，但實際的資料不需要以線性方式儲存。 *dst0* 只能有下列其中一項的寫入遮罩：. x、xy、.xyz、. xyzw。 寫入遮罩可決定要在沒有間距的情況下寫入的32位元件數目。

U 的超出範圍定址 \# 表示不會將任何內容寫入超出範圍記憶體; 任何範圍內的部分都會正確寫入。

G (界限的範圍外， \# 該特定 g 的界限 \# ，而不是任何指定32位元件的所有共用記憶體) ，會導致所有共用記憶體的整個內容變成未定義。

cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援這個 UAV 指令。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此指令：



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 不可以        |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 不可以        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





