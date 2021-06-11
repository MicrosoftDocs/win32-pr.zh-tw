---
title: Ps_2_0 和更新版本的修飾詞
description: 指令修飾詞會在將指令寫入目的地登錄之前，先影響指令的結果。 瞭解 ps_2_0 和更新版本的修飾詞。
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc8ed91f8e103ebbab7c43ffe53201f0e1d5dfcf
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989283"
---
# <a name="modifiers-for-ps_2_0-and-above"></a>Ps \_ 2 \_ 0 和更新版本的修飾詞

指令修飾詞會在將指令寫入目的地登錄之前，先影響指令的結果。

本章節包含圖元著色器第2版和更新版本所執行之指令修飾詞的參考資訊 \_ 。



| Name                                     | 語法     | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------------------------|------------|------|------|-------|------|-------|
| [質心](#centroid)                    | \_質心 | x    | x    | x     | x    | x     |
| [部分有效 \_ 位數](#partial-precision) | \_Pp       | x    | x    | x     | x    | x     |
| [飽和](#saturate)                    | \_坐      | x    | x    | x     | x    | x     |



 

## <a name="centroid"></a>質心

距心修飾詞是選擇性的修飾詞，可在基本範圍未涵蓋多取樣圖元中心時，個屬性內插補點。 這可以在 [距心取樣](https://msdn.microsoft.com/library/ee415231(VS.85).aspx)中看到。

您可以將距心修飾詞套用至元件指令，如下所示：


```
dcl_texcoord0_centroid v0
```



您也可以將距心修飾詞套用至語義，如下所示：


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



此外，以色彩語義宣告的任何 [輸入色彩](dx9-graphics-reference-asm-ps-registers-input-color.md) 暫存器 (v \#) 都會自動套用距心。 從距心取樣的屬性計算而來的漸層不保證正確。

## <a name="partial-precision"></a>部分有效位數

部分精確度指令修飾詞 (\_ pp) 指出部分有效位數是可接受的，但前提是基礎實作為支援的區域。 您一律可以自由地忽略修飾詞，並以完整的精確度執行受影響的作業。

\_Pp 修飾詞可以出現在兩個內容中：

-   在紋理座標宣告上，以部分精確度形式啟用將材質座標傳遞給圖元著色器。 例如，這可讓您使用材質座標將色彩資料轉送至圖元著色器，但在某些實作為中，部分精確度可能會比完整有效位數更快。 如果沒有這個修飾詞，材質座標必須以完整的精確度傳遞。
-   包含材質載入指示的任何指示。 這表示可以執行實作為部分有效位數的指令，並儲存部分精確度結果。 如果沒有明確的修飾詞，就必須以完整的精確度來執行指令， (無論輸入的精確度) 為何。

範例：


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a>飽和度

飽和的指令修飾詞 (\_ sat) 在寫入至目的地暫存器之前，會將指示結果) 到範圍 \[ 0、1，以 (或個 \] 。

\_Sat 指令修飾詞可以搭配[frc-ps](frc---ps.md)、 [sincos](sincos---ps.md)和任何 tex 指令以外的任何指令使用 \* 。

若是 ps \_ 2 \_ 0、ps \_ 2 \_ x 和 ps \_ 2 \_ sw，則 \_ 不能使用 sat 指令修飾詞搭配寫入任何輸出暫存器 ([輸出色彩](dx9-graphics-reference-asm-ps-registers-output-color.md) 暫存器或 [輸出深度](dx9-graphics-reference-asm-ps-registers-output-depth.md) 暫存器) 的指示。 這種限制不適用於 ps \_ 3 \_ 0 和更新版本。

範例：


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




