---
title: 'ld (sm4-asm) '
description: 從指定的緩衝區或紋理中提取資料，而不進行任何篩選 (例如，使用提供的整數位址) 點取樣。 來源資料可能來自于 TextureCube 以外的任何資源類型。
ms.assetid: DEE9A55F-EDFE-478E-8169-5BF9C43E98AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaacc3d76d49cc2b3043d39036f0ff652d7b8794
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313683"
---
# <a name="ld-sm4---asm"></a>ld (sm4-asm) 

從指定的緩衝區或紋理中提取資料，而不進行任何篩選 (例如，使用提供的整數位址) 點取樣。 來源資料可能來自于 TextureCube 以外的任何資源類型。



| ld \[ \_ aoffimmi (u、v、w) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource \[ . swizzle\] |
|----------------------------------------------------------------------------------------|



 



| 項目                                                                                                               | 描述                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                    | \[在 \] 操作結果的位址中。<br/>                                                               |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[在 \] 執行範例所需的材質座標中。<br/>                                                     |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[在材質暫存器中 \] (t) 必須已經宣告， \# 以識別要從中提取的材質或緩衝區。<br/> |



 

## <a name="remarks"></a>備註

此指令是 [範例](sample--sm4---asm-.md) 指令的簡化替代方法。 不同于 **範例**， **ld** 也可以從緩衝區中提取資料。 **ld** 也可以從多範例資源中提取 (只) 圖元著色器。

*srcAddress* 提供以不帶正負號整數形式執行範例所需的材質座標集合。 如果 *srcAddress* 超出 \[ 維度 1) 中的範圍 0 ... (\# 材質 \] ，則會叫用超出範圍的行為，其中 **ld** 會在 *srcResource* 格式的所有非遺漏元件中傳回0，並將遺漏元件的預設值傳回預設值。 希望能更靈活地控制超出範圍的位址行為的應用程式應該改用 **範例** 指令，因為它會接受定義為取樣器狀態的位址包裝/鏡像/夾具/框線行為。

*srcAddress：* (POS swizzle) 一律提供不帶正負號的整數 mipmap 層級。 如果值超出範圍 \[ 0 ... (num miplevels 在資源 1) \]) 中，則會叫用超出範圍行為。 如果資源是緩衝區，它不能有任何 mipmap，則會忽略 *srcAddress*

如果緩衝區和 texture1D (非陣列) ，則會忽略 *srcAddress* (POS-swizzle) 。 texture1D 陣列和 texture2Ds 會忽略 *srcAddress b.* (POS-swizzle) 。

若是 texture1D 陣列， *srcAddress. g* (POS-swizzle) 提供陣列索引做為不帶正負號的整數。 如果值超出可用陣列索引的範圍 \[ 0 ... (陣列大小-1) \] ，則會叫用超出範圍行為。

針對 texture2D 陣列， *srcAddress. b* (POS-swizzle) 提供陣列索引，否則為與 texture1D 相同的語義。

從沒有任何系結的 *t \#* 進行提取，會針對所有元件傳回0。

### <a name="address-offset"></a>位址位移

選擇性的 \[ \_ aoffimmi (u，v，w) \] 尾碼 (以立即整數的位址位移) 表示 **ld** 的材質座標是以一組提供的立即材質空間整數常數值來位移。 常值是一組4位2的補數數位，具有整數範圍 \[ -8，7 \] 。 此修飾詞只會針對 texture1D/2D/3D 定義，包括陣列，而不是針對緩衝區。

位移會新增至材質座標（在材質空間中），相對於 **ld** 所存取的 miplevel。

Texture1D/2D 陣列的陣列軸並不會套用位址位移。

*\_ Aoffimmi v （w）* 會忽略 texture1Ds 的元件。

Texture2Ds 會忽略 *\_ aoffimmi w* 元件。

因為 **ld** 的材質座標是不帶正負號的整數，所以如果位移導致位址小於零，則會換行至大型位址，並產生超出範圍的存取權。

### <a name="return-type-control"></a>傳回型別控制項

**Ld** 所傳回的資料格式會以與 **範例** 指令所述的相同方式來決定;它是以系結至 *srcResource* 參數 (*t \#*) 的格式為基礎。

如同 **範例** 指令一樣， **ld** 的傳回值為4向量，以及格式不存在之元件的格式特定預設值。 *SrcResource* 上的 swizzle 會決定如何 swizzle 從材質載入傳回的4個元件結果。在 *目的地* 上的遮罩可判斷在 *dest* 中的哪些元件已更新。

當 *ld* 將32位浮點值讀入32位的暫存器時，不會改變位;也就是說，denormal 值仍維持 denormal。 這與 **範例** 指令不同。

### <a name="miscellaneous-details"></a>其他詳細資料

因為沒有與 **ld** 指令相關聯的篩選，」 lod 偏差這類概念並不適用于 **ld**。 因此，沒有任何取樣 *器 \# s* 參數。

### <a name="restrictions"></a>限制

-   *srcResource* 必須是 t \# 註冊，而不是 TextureCube。 *srcResource* 不可以是 constantbuffer，因為無法系結至 t \# 註冊。
-   不允許 *srcResource* 的相對定址。
-   *srcAddress* 必須是 temp (r \# /x \#) 、常數 (cb \#) 或輸入 (v \#) register。
-   *dest* 必須是 temp (r \# /x \#) 或 output (o \* \#) register。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 是       |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





