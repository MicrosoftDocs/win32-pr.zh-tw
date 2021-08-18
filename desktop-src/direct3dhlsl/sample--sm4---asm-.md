---
title: '範例 (sm4-asm) '
description: '使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。 |範例 (sm4-asm) '
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b6fabb75c819bb2a95fcf500799fd1e8153d6dabfe66d33ba04c518c949fa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671878"
---
# <a name="sample-sm4---asm"></a>範例 (sm4-asm) 

使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。



| 範例 \[ \_ aoffimmi (u，v，w) \] dest \[ . mask \] ，srcAddress \[ . swizzle \] ，srcResource， \[ swizzle \] ，srcSampler |
|--------------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                               | 描述                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                    | \[在 \] 操作結果的位址中。<br/>                                      |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[在 \] 一組材質座標中。 如需詳細資訊，請參閱「 **備註** 」一節。<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[在材質暫存器中 \] 。 如需詳細資訊，請參閱「 **備註** 」一節。<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[在 \] 取樣器註冊中。 如需詳細資訊，請參閱「 **備註** 」一節。<br/>           |



 

## <a name="remarks"></a>備註

來源資料可能來自于緩衝區以外的任何資源類型。

*srcAddress* 會提供執行範例所需的材質座標集合，做為參考材質中正規化空間的浮點值。 位址包裝模式 (wrap/鏡像/夾具/框線等。 ) 會套用 \[ 至 0 ... 1 範圍以外的材質座標 \] ，從取樣器狀態 (s \#) ，然後在任何位址位移套用至材質座標之後套用。

*srcResource* 是 (t) 的材質暫存器 \# 。 這只是材質的預留位置，包括所取樣資源的傳回資料類型。 所有這些資訊都是在著色器前序中宣告的。 實際要取樣的資源會系結至 t) 位置 (外部的著色器 \# \# 。

*srcSampler* 是 (s) 的取樣器註冊。 這只是篩選控制項集合的預留位置，例如 point 和線性、mipmap 和位址換行控制項。

執行取樣的硬體所需的一組資訊，會分割成兩個垂直片段。 首先，材質暫存器會提供源資料類型資訊，例如，材質是否包含 SRGB 資料的相關資訊。 它也會參考實際取樣的記憶體。 其次，取樣器註冊會定義要套用的篩選模式。

### <a name="array-resources"></a>陣列資源

針對 Texture1D 陣列， *srcAddress* g 元件 (POS swizzle) 選取要從中提取的陣列配量。 這一律會被視為縮放的浮點值，而不是標準材質座標的正規化空間，而是在值上套用四捨五入至最接近的值，接著是套用至可用 BufferArray 範圍的值。

針對 Texture2D 陣列， *srcAddress* b 元件 (POS-swizzle) 選取要從中提取的陣列配量，否則使用 Texture1D 陣列所述的相同語義。

### <a name="address-offset"></a>位址位移

選擇性的 \[ \_ aoffimmi (u，v，w) \] 尾碼 (以立即整數的位址位移) 表示樣本的材質座標是以一組提供的立即材質空間整數常數值來位移。 常值是一組4位2的補數數位，具有整數範圍 \[ -8，7 \] 。 此修飾詞會針對所有資源（包括 Texture1D/2D 陣列和 Texture3D）定義，但不會針對 TextureCube 定義。

硬體可以利用立即的知識，讓您透過一組範例指令來執行有關常見位置的一些材質使用量。 這可以使用 \_ aoffimmi (u、v、w) 來傳達。

位移會新增至材質座標（在材質空間中），相對於每個要存取的 miplevel。 因此，即使材質座標是以正規化浮點數的形式提供，位移也會套用材質空間的整數位移。

Texture1D/2D 陣列的陣列軸並不會套用位址位移。

\_aoffimmi v，會忽略 Texture1Ds 的 w 元件。

\_Texture2Ds 會忽略 aoffimmi w 元件。

位址換行模式 (wrap/鏡像/夾具/框線等。從取樣器狀態 )  (s \#) 會在任何位址位移套用至材質座標之後套用。

### <a name="return-type-control"></a>傳回型別控制項

範例所傳回的資料格式是由 (DXGI 格式的資源格式所決定，) 系 \_ 結 \* 至 (t) 的 *srcResource* 參數 \# 。 例如，如果指定的 t 系結于 \# 格式為 DXGI \_ 格式 \_ A8B8G8R8 \_ UNORM SRGB 的資源 \_ ，則取樣作業會將取樣的材質從 gamma 2.0 轉換為1.0，套用篩選，並將結果寫入至目的地暫存器做為範圍 0 ..1 中的浮點值 \[ \] 。

傳回的值為4向量 (以及格式) 不存在的元件的格式特定預設值。 *SrcResource* 上的 swizzle 會決定如何 swizzle 從紋理取樣/篩選傳回的4個元件結果，在此之後，在 *目標* 上的遮罩會決定 *目的地* 中的哪些元件會更新。

當 **範例** 將32位的 float 值讀取至32位的暫存器中，並使用點取樣 (沒有篩選) ，它可能會或可能不會排清 denormal 值，否則不會修改數位。 如果點取樣 denormal 值的不確定性是應用程式的問題，請使用 [ld](ld--sm4---asm-.md) 指令，以保證32位的 float 值會以未修改的方式讀取。

### <a name="lod-calculation"></a>」 LOD 計算

如需有關如何在判斷」 LOD 以進行篩選的過程中計算衍生的詳細資訊，請參閱 [deriv \_ rtx](deriv-rtx--sm4---asm-.md) 和 [deriv \_ rty](deriv-rty--sm4---asm-.md)。 **範例指令範例** 會使用 **deriv** 著色器指令所使用的相同定義，以隱含方式計算紋理座標上的衍生。 這並不適用于 [範例 \_ l](sample-l--sm4---asm-.md) 或 [範例 \_ d](sample-d--sm4---asm-.md) 指令。 這些指示會直接由應用程式提供」 LOD 或衍生。

針對 **範例** 指令，執行程式可以選擇在2x2 戳記中的所有4個圖元之間共用相同的」 lod 計算 (但沒有較大的區域) ，或執行每個圖元的」 lod 計算。

### <a name="miscellaneous-details"></a>其他詳細資料

針對 Buffer & Texture1D，會忽略 *srcAddress* (POS swizzle) 的 gba 元件。 若為 Texture1D 陣列，則會忽略 *srcAddress* (POS-swizzle) 的元件。 若為 Texture2Ds，則會忽略 *srcAddress* (POS-swizzle) 的元件。

從未系結任何專案的輸入位置提取，會針對所有元件傳回0。

### <a name="restrictions"></a>限制

-   *srcResource* 必須是 t \# 註冊。 *srcResource* 不能是無法系結至 t 註冊的 ConstantBuffer \# 。
-   *srcSampler* 必須是 s \# 註冊。
-   不允許 *srcResource* 或 *srcSampler* 的相對定址。
-   *srcAddress* 必須是 temp (r \# /X \#) 、constantBuffer (cb \#) 、輸入 (v \#) register 或立即值 (s) 。
-   *dest* 必須是 temp (r \# /x \#) 或 output (o \* \#) register。
-   \_TextureCubes 不允許 aoffimmi (u，v，w) 。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





