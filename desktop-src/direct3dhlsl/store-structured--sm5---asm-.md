---
title: 'store_structured (sm5-asm) '
description: 以隨機方式將 1-4 32 位元件寫入至結構化緩衝區未排序的存取視圖 (UAV) 。
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5890d30fac57923365f0bdea89fcce55f7922c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022812"
---
# <a name="store_structured-sm5---asm"></a>儲存 \_ 結構化 (sm5-asm) 

以隨機方式將 1-4 32 位元件寫入至結構化緩衝區未排序的存取視圖 (UAV) 。



| 儲存 \_ 結構化 dst0 \[ 。寫入 \_ mask \] ，dstAddress \[ 。 select component， \_ \] dstByteOffset \[ . select \_ component \] ，src0 \[ . swizzle\] |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                                       | 描述                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[在 \] 操作結果的位址中。<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/>             | \[在 \] 要寫入的位址中。<br/>               |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*<br/> | \[在 \] 要寫入之結構的索引中。<br/>         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[在 \] 要寫入的元件中。<br/>                     |



 

## <a name="remarks"></a>備註

此指令會在 \* *DstAddress* 和 *dstByteOffset* 中的位址，執行從 *src0* 寫入至 *dst0* 的1-4 元件32位元件。 沒有格式轉換。

*dst0* 必須是 UAV (u \#) 。 在計算著色器中，它也可以是執行緒群組的共用記憶體 (g \#) 。

*dstAddress* 指定要寫入的結構索引。

寫入的資料位置相當於下列虛擬程式碼，它會顯示位移、位址、緩衝區內容的指標、來源的 stride，以及以線性方式儲存的資料。

``` syntax
                    BYTE *BufferContents;             // from dst0
                    UINT BufferStride;                // from dst0
                    UINT dstAddress, dstByteOffset;   // source registers
                    BYTE *WriteLocation;              // value to calculate

                    // calculate writing location
                     WriteLocation = BufferContents 
                                + BufferStride * dstAddress 
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
                             WriteComponents * sizeof(INT32));
```

這個虛擬虛擬的會顯示作業的運作方式，但實際的資料不需要以線性方式儲存。 如果資料不是以線性方式儲存，則實際的指令運算必須符合上述作業的行為。

*dst0* 只能有下列其中一項的寫入遮罩：. x、xy、.xyz、. xyzw。 寫入遮罩可決定要在沒有間距的情況下寫入的32位元件數目。

依 DstAddress 的 u casued 超出範圍定址， \# 表示不會將任何內容寫入超出範圍的記憶體。 

如果 *dstByteOffset*（包括 *dstWriteMask*）是導致超出範圍存取權的原因，則 \# UAV 的整個內容都會變成未定義。

G (界限的範圍外， \# 該特定 g 的界限 \# ，而不是任何指定32位元件的所有共用記憶體) ，會導致所有共用記憶體的整個內容變成未定義。

*dstByteOffset* 是不同于 *dstAddress* 的引數，因為它通常是常值。 尚未對結構化記憶體上的 atomics 執行此參數分離。

cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援 UAV 和 TGSM 的這個指令。

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

 

 





