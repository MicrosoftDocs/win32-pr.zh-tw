---
title: texbeml-ps
description: 套用具有亮度校正的假凸塊環境對應轉換。 這是藉由使用位址更動資料 (du、dv) 、2D 凹凸環境矩陣和亮度來修改目的地註冊的材質位址資料來完成。
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c549e93829c3165d4921342d4e74a8dc15bc1518f7c88aa205f8afc889fae95e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788062"
---
# <a name="texbeml---ps"></a>texbeml-ps

套用具有亮度校正的假凸塊環境對應轉換。 這是藉由使用位址更動資料 (du、dv) 、2D 凹凸環境矩陣和亮度來修改目的地註冊的材質位址資料來完成。

## <a name="syntax"></a>Syntax



| texbeml dst、src |
|------------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texbeml               | x    | x    | x    |      |      |      |       |      |       |



 

Src 暫存器中的紅色和綠色色彩資料會解讀為更動資料 (du、dv) 。 Src 暫存器中的藍色資料會被視為亮度資料。

此指令會使用2D 凹凸環境對應矩陣來轉換來源暫存器中的紅色和綠色元件。 結果會新增至對應至目的地暫存器編號的材質座標集合。 使用亮度值和偏差紋理階段值來套用亮度校正。 結果會用來取樣目前的材質階段。

這可用於根據地址更動的各種技術，例如假的每圖元環境對應。

這種作業一律會將 du 和 dv 解釋為帶正負號的數量。 針對版本 1 \_ 0 和 1 \_ 1，輸入引數不允許 [來源登錄的已簽署調整](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) 輸入修飾詞 (\_ bx2) 。

當輸入紋理包含混合的格式資料時，此指令會產生已定義的結果。 如需有關介面格式的詳細資訊，請參閱 [D3DFORMAT](/windows/desktop/direct3d9/d3dformat)。


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



此範例顯示在指令中完成的計算。


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



u ' = TextureCoordinates (階段 m) <sub>u</sub> +

D3DTSS \_ BUMPENVMAT00 (階段 m) \* t (n) <sub>R</sub> +

D3DTSS \_ BUMPENVMAT10 (階段 m) \* t (n) <sub>G</sub>

v ' = TextureCoordinates (階段 m) <sub>v</sub> +

D3DTSS \_ BUMPENVMAT01 (階段 m) \* t (n) <sub>R</sub> +

D3DTSS \_ BUMPENVMAT11 (階段 m) \* t (n) <sub>G</sub>

t (m) <sub>RGBA</sub> = TextureSample (階段 m) 使用 (u '，v ' ) 作為座標

t (m) <sub>rgba</sub> = t (m) <sub>RGBA</sub>\*

\[ (t (n) <sub>B</sub> \* D3DTSS \_ BUMPENVLSCALE (階段 m) ) +

D3DTSS \_ BUMPENVLOFFSET (階段 m) \]

除了其他 texbem 或 texbeml 之外，無法稍後再讀取 [texbem](texbem---ps.md) 或 texbeml 指令讀取的資料。


```
// This example demonstrates the validation error caused by 
//   t0 being reread
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a>範例

以下是已識別材質地圖和識別材質階段的範例著色器。


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



此範例需要下列紋理階段中的材質。

-   階段0會指派具有 (du、dv) 更動資料的一種凹凸地圖。
-   第1階段會指派具有色彩資料的材質地圖。
-   texbeml 會在已取樣的材質階段上設定矩陣資料。 這不同于固定函式管線的功能，其中更動資料和矩陣會佔用相同的材質階段。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 