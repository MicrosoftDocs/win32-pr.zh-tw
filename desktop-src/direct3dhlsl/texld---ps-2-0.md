---
title: texld-ps_2_0 和更新
description: 使用提供的材質座標，在特定取樣器上取樣材質。 這個指令不同于 \_ \_ 圖元著色器第1版中所使用的 texld-ps 1 4 指令 \_ 。
ms.assetid: 2b0d02b4-d9dd-4388-aa86-03b27bc4fdc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b71990e230290403bca2a5af11eeca11b093402f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507980"
---
# <a name="texld---ps_2_0-and-up"></a>texld-ps \_ 2 \_ 0 和更新的

使用提供的材質座標，在特定取樣器上取樣材質。 這個指令不同于圖元著色器第1版中所使用的 [texld-ps \_ 1 \_ 4](texld---ps-1-4.md) 指令 \_ 。

## <a name="syntax"></a>Syntax



| texld dst、src0、src1 |
|-----------------------|



 

其中：

-   dst 是目的地註冊。
-   src0 是一種來源暫存器，可提供紋理範例的材質座標。
-   src1 會識別 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# ，其中 \# 指定要取樣的材質取樣器數目。 取樣器已將材質與 [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype)定義的材質和取樣器狀態相關聯。

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 和 ps \_ 2 \_ x

dst 必須是 [暫時性的註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) ，而且只允許) 的 xyzw mask (預設遮罩。

src0 必須是 [紋理座標](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) 暫存器 (t \#) 或 (r) 的 [臨時](dx9-graphics-reference-asm-ps-registers-temporary.md) 暫存器 \# ，但不含修飾詞或 swizzle。

src1 必須是 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# ，沒有修飾詞或 swizzle。

如果 D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT cap 位未設定 (在 D3DPSHADERCAPS2 \_ 0) 中，指定的材質指令 ([texld](texld---ps-1-4.md)、 [texldp](texldp---ps.md)、 [texldb-ps](texldb---ps.md)、 [texldd](texldd---ps.md) ) 可能會相依于最多第三個順序。 第一個順序相依材質指令是一個材質指令，其中：

-   src0 是 (r) 的 [暫時性註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) \# 。
-   dst 先前已寫入，現在正在撰寫中。

第二個順序相依的材質指令定義為材質指令，可讀取或寫入 [暫存註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) 其內容在執行材質 (指令之前的內容，可能會在第一個順序相依材質指令的結果上間接) 。  (n) <sup>第</sup>一個順序的相依材質指令會衍生自 (n-1) <sup>第</sup>一個順序的材質指令。

### <a name="ps_3_0"></a>ps \_ 3 \_ 0

src1 必須是 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \#) ，沒有修飾詞的取樣器。 Swizzle 可在 src0 或 src1 上使用。 Swizzle 會在紋理查閱之前套用至材質 coordintates。

## <a name="remarks"></a>備註

下列版本支援此指令：



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texld                 |      |      |      |      | x    | x    | x     | x    | x     |



 

Src0 執行材質範例所需的座標數目取決於 src1 的宣告方式，以及 w 元件。 取樣器型別是以 [dcl \_ samplerType 宣告 (sm2、sm3 ps asm) ](dcl-samplertype---ps.md)。 如果 src1 宣告為2D 取樣器，則 src0 必須包含 xy 座標;如果 src1 宣告為 cube 取樣器或磁片區取樣器，則 src0 必須包含 xyz 座標。 因為已忽略額外的材質座標元件 () ，所以允許取樣的維度數量少於材質座標中的材質。

如果來源材質包含四個以上的元件，預設值就會放置在遺漏的元件中。 預設值取決於下表所示的材質格式：



| 材質格式                                                                                          | 預設值       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| D3DFMT \_ R5G6B5、D3DFMT \_ R8G8B8、D3DFMT \_ L8、D3DFMT \_ l16 也、D3DFMT \_ R3G3B2、D3DFMT \_ CxV8U8、D3DFMT \_ L6V5U5 | A = 1。0              |
| D3DFMT \_ V8U8、D3DFMT \_ V16U16、D3DFMT \_ G16R16、D3DFMT \_ G16R16F、D3DFMT \_ G32R32F                          | B = A = 1。0          |
| D3DFMT \_ A8                                                                                              | R = G = B = 0。0      |
| D3DFMT \_ R16F、D3DFMT \_ R32F                                                                              | G = B = A = 1。0      |
| 所有深度/樣板格式                                                                               | R = B = 0.0，A = 1。0 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 