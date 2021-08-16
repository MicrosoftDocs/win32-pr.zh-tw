---
title: texldb-ps
description: 偏誤材質載入指示。 此指示會使用第四個元素 (. 或. w) ，在取樣之前，偏差紋理取樣的詳細程度。
ms.assetid: cafd72c9-b7bb-4e3f-8a8c-de26a4446864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ddf340840e377ee03641ae33c0731f27e90ce4760cad4ddb6c636c1831fa80ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505791"
---
# <a name="texldb---ps"></a>texldb-ps

偏誤材質載入指示。 此指示會使用第四個元素 (. 或. w) ，在取樣之前，偏差紋理取樣的詳細程度。

## <a name="syntax"></a>Syntax



| texldb dst、src0、src1 |
|------------------------|



 

其中：

-   dst 是目的地註冊。
-   src0 是一種來源暫存器，可提供紋理範例的材質座標。 請參閱 [材質座標註冊](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)。
-   src1 會識別 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# ，其中 \# 指定要取樣的材質取樣器數目。 取樣器已將材質與 [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype)定義的材質和取樣器狀態相關聯。

如需使用 texldb 的限制，請參閱 [texld-ps \_ 2 \_ 0 和 up](texld---ps-2-0.md) 指令。

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 和 ps \_ 2 \_ x

dst 必須是 [暫時性的註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) ，而且只允許) 的 xyzw mask (預設遮罩。

src0 必須是 [紋理座標](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) 暫存器 (t \#) 或 (r) 的 [臨時](dx9-graphics-reference-asm-ps-registers-temporary.md) 暫存器 \# ，但不含修飾詞或 swizzle。

src1 必須是 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# ，沒有修飾詞或 swizzle。

如果 D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT cap 位未設定 (在 D3DPSHADERCAPS2 \_ 0) 中，指定的材質指令 (texld、texldp、texldb、texldd) 可能會相依于最多第三個順序。 第一個順序相依材質指令是一個材質指令，其中：

-   src0 是 (r) 的 [暫時性註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) \# 。
-   dst 先前已寫入，現在正在撰寫中。

第二個順序相依的材質指令定義為材質指令，可讀取或寫入 [暫存註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) 其內容在執行材質 (指令之前的內容，可能會在第一個順序相依材質指令的結果上間接) 。  (n) <sup>第</sup>一個順序的相依材質指令會衍生自 (n-1) <sup>第</sup>一個順序的材質指令。

### <a name="ps_3_0"></a>ps \_ 3 \_ 0

src1 必須是 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \#) ，沒有修飾詞的取樣器。 Swizzle 可在 src1 上使用，並且在套用時，紋理查閱結果會在寫入 dst 之前預先 swizzled。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldb                |      |      |      |      | x    | x    | x     | x    | x     |



 

texldb 會偏差 mipmap 的詳細層級，並以 src0 中 (簽署的) 值做為範例進程的一部分來計算。 正偏差值會導致選取較小的 mipmap，反之亦然。 針對 ps \_ 2 \_ 0 和 ps \_ 2 \_ x，偏差值可以在 \[ -3.0、+ 3.0 範圍內 \] 。 針對 ps \_ 3 \_ 0，偏差值可以在 \[ -16.0、+ 15.0 範圍內 \] 。 這些範圍之外的偏差值會產生未定義的結果。 仍會接受取樣器狀態 D3DSAMP \_ MIPMAPLODBIAS，並將 texldb 偏差新增至此，但以每圖元為基礎。 計算出偏高的詳細資料層級之後， \_ 仍會接受 D3DSAMP MAXMIPLEVEL，並產生紋理範例。 Texldb 之後，除非 dst 是相同的註冊) ，否則 src0 的內容不會受到 (的影響。

Src0 執行材質範例所需的座標數目取決於 src1 的宣告方式，以及 w 元件。 取樣器型別是以 [dcl \_ samplerType 宣告 (sm2、sm3 ps asm) ](dcl-samplertype---ps.md)。 如果 src1 宣告為2D 取樣器，則 src0 必須包含 xyw 座標;如果 src1 宣告為 cube 取樣器或磁片區取樣器，則 src0 必須包含 xyzw 座標。 使用 xyzw 座標取樣2D 材質 (會忽略) 的 z 座標。

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

 

 