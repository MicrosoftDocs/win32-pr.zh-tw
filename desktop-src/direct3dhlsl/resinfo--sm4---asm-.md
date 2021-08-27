---
title: 'resinfo (sm4-asm) '
description: 查詢指定輸入資源的維度。
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb23a6790c113702e59fc53f85a4d838907fe5ff658c29d83e37e3f620a9dc79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095318"
---
# <a name="resinfo-sm4---asm"></a>resinfo (sm4-asm) 

查詢指定輸入資源的維度。



| resinfo \[ \_ uint \|\_rcpFloat \] dest \[ . mask \] ，srcMipLevel. Select \_ component，srcResource \[ . swizzle\] |
|-----------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                               | 描述                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                    | \[在 \] 操作結果的位址中。<br/>                             |
| <span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*<br/> | \[在 \] mip 層級中。<br/>                                                          |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[在要 \] \# 查詢維度的 t 或 u \# 輸入材質中。 <br/> |



 

## <a name="remarks"></a>備註

*srcMipLevel* 會讀取為不帶正負號的整數純量，因此來源暫存器需要單一元件選取器（如果它不是純量立即值）。

*dest* 會接收 \[ \] 寫入遮罩所選取的寬度、高度、深度或陣列大小，總計-mip-count。

傳回的寬度、高度和深度值適用于 *srcMipLevel* 參數所選取的 mip 層級，而且是材質數目，與材質資料大小無關。 針對高取樣資源 (texture2D \[ 陣列 \] MS \#) ，寬度和高度也會在材質中傳回，而非範例。

在 *dest* 中傳回的 mip 計數總計未受到 *srcMipLevel* 參數的影響。

針對 UAVs (u \#) ，mip 層級的數目一律為1。

此指示的所有層面都是以 t/u 系結資源檢視的特性為基礎 \# \# ，而不是基礎基底資源。

除非使用 uint 修飾詞，否則傳回的值都是浮點數， \_ 在這種情況下，傳回的值全都是整數。 如果 \_ 使用 rcpFloat 修飾詞，所有傳回的值都是浮點數，而寬度、高度和深度會傳回為 reciprocals (1.0 f/寬度、1.0 f/高度、1.0 f/深度) ，包括如果寬度/高度/深度為0（從超出範圍 *srcMipLevel* 行為）。 \_RcpFloat 修飾詞只適用于 width、height 和 depth 傳回的值，而且不會套用至設定為0且不會傳回的值，也不會套用至陣列大小傳回。

*SrcResource* 上的 swizzle 允許在將傳回的值寫入目的地之前，任意加以 swizzled。

如果 *srcResource* 是 Texture1D，則會在 *dest* 中傳回 width，而 *dest. yz* 會設定為0。

如果 *srcResource* 是 Texture1DArray，則會在 *dest* 中傳回 width，陣列大小會在 *dest* 中傳回，而 *dest* 會設定為0。

如果 *srcResource* 是 Texture2D，則會在 *dest* 中傳回寬度和高度，並將 *dest* 設定為0。

如果 *srcResource* 是 Texture2DArray，則寬度和高度會在 *dest* 中傳回，而陣列大小則會在 *目的地. z* 中傳回。

如果 *srcResource* 是 Texture3D，則會在 *dest.xyz* 中傳回寬度、高度和深度。

如果 *srcResource* 是 TextureCube，則個別 cube 臉部維度的寬度和高度會在 *dest* 中傳回，而 *目的地. z* 會設定為0。

如果 *srcResource* 是 TextureCubeArray，則個別 cube 臉部維度的寬度和高度會在 *dest* 中傳回。 *目的地 z* 設定為未定義的值。

如果在 *srcResource* 上指定了每個資源的 mip 夾具，resinfo 一律會傳回 mip 計數的視圖中的 mipmap 總數（不論是否有此夾具）。 但是，如果指定之 miplevel 的維度是由 resinfo 所要求，且 miplevel 已壓制 off (例如，2.2 的夾具表示已將 mips 0 和1壓制關閉) ，則傳回的維度並未定義。 某些實 resinfo 會在 miplevel 超出範圍時，傳回針對指定的超出範圍行為。 其他的執行會傳回 mip 的維度，就像尚未壓制。

### <a name="restrictions"></a>限制

-   *srcResource* 必須是 \# \# 非緩衝區的 t 或 u 暫存器，但卻是材質 \* 。
-   不允許 *srcResource* 的相對定址。
-   如果 *srcMipLevel* 不是純量立即的，則必須使用單一元件選取器。
-   從 \# 沒有任何系結的 t 或 u 提取，會傳回0（ \# 寬度、高度、深度或 arraysize）和總計 mip 計數。 \_在此情況下，仍會接受 rcpFloat 修飾詞，因此會針對適用的傳回值傳回 INF。
-   如果 *srcMipLevel* 超出資源中可用 miplevels 數目的範圍，則大小的行為會傳回 (*dest.xyz*) 等同于未系結的 t \# 或 u \# 資源。 在此情況下，在 *dest* 中仍會傳回 mip 總計計數。

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
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





