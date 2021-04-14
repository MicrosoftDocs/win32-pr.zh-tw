---
title: texcrd-ps
description: 將材質座標資料從來源材質座標反覆運算器註冊複製為目的地暫存器中的色彩資料。
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1b7bda7ab06c4af43eaa40393d2c5d64b09d9f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990923"
---
# <a name="texcrd---ps"></a>texcrd-ps

將材質座標資料從來源材質座標反覆運算器註冊複製為目的地暫存器中的色彩資料。

## <a name="syntax"></a>Syntax



| texcrd dst、src |
|-----------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcrd                |      |      |      | x    |      |      |       |      |       |



 

此指令會將座標資料解讀為色彩資料 (RGBA) 。

此指令未取樣任何紋理。 只有在此材質階段設定的材質座標是相關的。

使用 texcrd 時，請記住下列有關如何將資料從來源暫存器複製到目的地登錄的詳細資料。 來源材質座標暫存器 (t \#) 將資料存放在 D3DCAPS9 範圍內 \[ 。MaxTextureRepeat, D3DCAPS9.MaxTextureRepeat \] ，而目的地登錄 (r \#) 只能將資料存放在 (可能較小) 範圍 \[ D3DCAPS9。PixelShader1xMaxValue, D3DCAPS9.PixelShader1xMaxValue \] 。 請注意，對於圖元著色器第1版 \_ ，D3DCAPS9。PixelShader1xMaxValue 必須至少為8。 Texcrd 指令在固定來源資料超出目的地登錄範圍的過程中，可能會在不同的硬體上有不同的行為。 市場上第1個圖元著色器第 1 \_ 4 個硬體，將會針對超出範圍的值執行特殊的夾具。 此夾具的設計目的是要產生可符合目的地暫存器的數位，但也可以保留超出範圍資料的材質定址行為 (查看 [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) 如果資料後續用於紋理取樣。 不過，不同製造商的新硬體可能不會顯示這種行為，而且可能只會切割資料以符合目的地暫存器範圍。 因此，使用圖元著色器第1版 texcrd 時，最安全的動作 \_ 就是將材質座標資料僅提供給已在8到8範圍內的圖元著色器， \[ \] 如此您就不會依賴硬體個的方式。

不同于 texcoord \_ ，texcrd 不會在0和1之間進行值的夾具。

使用 texcrd 的規則：

1.  在 texcrd 或 texld 指令中，每次讀取個別 t (n) 註冊時，都必須套用相同的 xyz 或 xyw 修飾詞。
2.  在所有情況下，texcrd 的第四個通道結果都是未設定/未定義。
3.  Xyw dw 案例的第三個通道未設定/未定義 \_ 。

## <a name="examples"></a>範例

以下顯示一組完整的 texcrd 語法，其中會將所有有效的來源修飾詞/選取器和目的地寫入遮罩組合納入考慮。 請注意，您可以交換使用 rgba 和. xyzw 標記法。

將材質座標反覆運算器註冊的前三個通道（t (n) ）複製到 r (m) 。 R (m) 的第四個通道未初始化。


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



將 t (n) 的第一個、第二個和第四個元件放置於 r (m) 的前三個通道中。 R (m) 的第四個通道未初始化。


```
texcrd  r(m).rgb, t(n).xyw
```



以下是使用 dw 修飾詞的 projective 除法範例 \_ 。

此範例會將 x/w 和 y/w 從 t (n) 複製到 r (m) 的前兩個通道中。 R (m) 的第三個和第四個通道未初始化。 先前寫入 r (m) 的第三個通道的任何資料將會遺失。 R (m) 的第四個通道中的資料會因為階段標記而遺失。 若為第1版 \_ ，則 \_ 會忽略 D3DTTFF 投射旗標。


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 