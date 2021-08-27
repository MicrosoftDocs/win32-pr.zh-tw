---
title: texldp-ps
description: 投射的材質載入指示。 此指令會將輸入材質座標除以第四個元素 (. w) 在取樣之前。
ms.assetid: 82e62ba3-a9f5-4afb-8dca-4c54a00843eb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5c362e81af22b46cd443ade7cd4b466112ba9a4d98bd5852ee3d92a285936aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117848"
---
# <a name="texldp---ps"></a>texldp-ps

投射的材質載入指示。 此指令會將輸入材質座標除以第四個元素 (. w) 在取樣之前。

## <a name="syntax"></a>Syntax



| texldp dst、src0、src1 |
|------------------------|



 

其中

-   dst 是目的地註冊。
-   src0 是一種來源暫存器，可提供紋理範例的材質座標。 請參閱 [材質座標註冊](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)。
-   src1 會識別 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# ，其中 \# 指定要取樣的材質取樣器數目。 取樣器已將材質與 [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype)定義的材質和取樣器狀態相關聯。

如需使用 texldp 時的限制集合，請參閱 [texld](texld---ps-2-0.md)。

## <a name="remarks"></a>備註

texldp 會在執行範例之前，對從 src0 讀取的座標執行投射。 每個材質座標都會以 src0 除以 w，然後取樣紋理。 當 texldp 完成時，除非 dst 是相同的註冊) ，否則 src0 的內容不會受到 (的影響。 使用 texldp 的另一種方式是在著色器中手動執行投影除法。 不過，在著色器程式碼中執行除法通常比 texldp 指令執行的速度慢，因此請盡可能避免這類額外的數學運算。

Src0 執行材質範例所需的座標數目取決於 src1 的宣告方式，以及 w 元件。 取樣器型別是以 [dcl \_ samplerType 宣告 (sm2、sm3 ps asm) ](dcl-samplertype---ps.md)。 如果 src1 宣告為2D 取樣器，則 src0 必須包含 xyw 座標;如果 src1 宣告為 cube 取樣器或磁片區取樣器，則 src0 必須包含 xyzw 座標。 使用 xyzw 座標取樣2D 材質 (會忽略) 的 z 座標。

如果來源材質包含四個以上的元件，預設值就會放置在遺漏的元件中。 預設值取決於下表所示的材質格式。



| 材質格式                                                                                          | 遺漏元件的預設值 |
|---------------------------------------------------------------------------------------------------------|---------------------------------------|
| D3DFMT \_ R5G6B5、D3DFMT \_ R8G8B8、D3DFMT \_ L8、D3DFMT \_ l16 也、D3DFMT \_ R3G3B2、D3DFMT \_ CxV8U8、D3DFMT \_ L6V5U5 | A = 1。0                               |
| D3DFMT \_ V8U8、D3DFMT \_ V16U16、D3DFMT \_ G16R16、D3DFMT \_ G16R16F、D3DFMT \_ G32R32F                          | B = A = 1。0                           |
| D3DFMT \_ A8                                                                                              | R = G = B = 0。0                       |
| D3DFMT \_ R16F、D3DFMT \_ R32F                                                                              | G = B = A = 1。0                       |
| 所有深度/樣板格式                                                                               | R = B = 0.0，A = 1。0                  |



 

下列版本支援此指令：



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldp                |      |      |      |      | x    | x    | x     | x    | x     |



 

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 和 ps \_ 2 \_ x

dst 必須是 [暫時性的註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) ，而且只允許) 的 xyzw mask (預設遮罩。

src0 必須是 [紋理座標](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) 暫存器 (t \#) 或 (r) 的 [臨時](dx9-graphics-reference-asm-ps-registers-temporary.md) 暫存器 \# ，但不含修飾詞或 swizzle。

src1 必須是 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# ，沒有修飾詞或 swizzle。

如果 D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT cap 位未設定 (在 D3DPSHADERCAPS2 \_ 0) 中，指定的材質指令 ([texld](texld---ps-1-4.md)、texldp、 [texldb-ps](texldb---ps.md)、 [texldd](texldd---ps.md) ) 可能會相依于最多第三個順序。 第一個順序相依材質指令是一個材質指令，其中：

-   src0 是 (r) 的[暫時性註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) \#
-   dst 先前已寫入，現在正在撰寫中。

第二個順序相依的材質指令定義為材質指令，可讀取或寫入 [暫存註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) 其內容在執行材質 (指令之前的內容，可能會在第一個順序相依材質指令的結果上間接) 。  (n) <sup>第</sup>一個順序的相依材質指令會衍生自 (n-1) <sup>第</sup>一個順序的材質指令。

### <a name="ps_3_0"></a>ps \_ 3 \_ 0

針對 ps \_ 3 \_ 0，src1 必須是 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# ，沒有修飾詞。 Swizzle 可在 src1 上使用，並且在套用時，紋理查閱結果會在寫入 dst 之前預先 swizzled。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 