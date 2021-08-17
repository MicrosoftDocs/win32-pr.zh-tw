---
title: texbem-ps
description: 套用假的凹凸環境對應轉換。 這是藉由使用 address 更動 data (du、dv) 和2D 凹凸環境矩陣來修改目的地暫存器的材質位址資料來完成。
ms.assetid: 8e773f4a-c7a2-4caf-973f-8f50dccc9c04
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 183036a56d905eed8d0d0a237445fb0f8e42fe402edabb6f6639243749b92240
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119367338"
---
# <a name="texbem---ps"></a>texbem-ps

套用假的凹凸環境對應轉換。 這是藉由使用 address 更動 data (du、dv) 和2D 凹凸環境矩陣來修改目的地暫存器的材質位址資料來完成。

## <a name="syntax"></a>Syntax



| texbem dst、src |
|-----------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texbem                | x    | x    | x    |      |      |      |       |      |       |



 

Src 暫存器中的紅色和綠色色彩資料會解讀為更動資料 (du、dv) 。

此指令會使用2D 凹凸環境對應矩陣，轉換來源暫存器中的 red 和綠元件。 結果會新增至對應至目的地暫存器編號的材質座標集合，並用來取樣目前的材質階段。

這種作業一律會將 du 和 dv 解釋為帶正負號的數量。 針對版本 1 \_ 0 和 1 \_ 1，輸入引數不允許 [來源登錄的已簽署調整](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) 輸入修飾詞 (\_ bx2) 。

當輸入紋理包含已簽署的格式資料時，此指令會產生已定義的結果。 只有當前兩個通道包含已簽署的資料時，混合格式資料才會運作。 如需有關介面格式的詳細資訊，請參閱 [D3DFORMAT](/windows/desktop/direct3d9/d3dformat)。

這可用於以位址更動為基礎的各種技術，包括假的每圖元環境對應和擴散光源 (的) 增加對應。

使用這個指令時，材質暫存器必須遵循下列順序。


```
// The texture assigned to stage t(n) contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbem  t(m),  t(n)      where m > n
```



在指令中完成的計算如下所示。


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
```



u ' = TextureCoordinates (階段 m) <sub>u</sub> + D3DTSS \_ BUMPENVMAT00 (階段 m) \* t (n) <sub>R</sub> + D3DTSS \_ BUMPENVMAT10 (階段 m) \* t (n) <sub>G</sub> v ' = TextureCoordinates (階段 m) <sub>v</sub> + D3DTSS \_ BUMPENVMAT01 (階段 m) \* t (n) <sub>R</sub> + D3DTSS \_ BUMPENVMAT11 (階段 \* <sub></sub> <sub></sub>) 

使用 (u '，v ' ) 作為座標

無法稍後再讀取 texbem/ps 或 [texbeml ps](texbeml---ps.md) 指令讀取的資料，但另一個 texbem-ps 或 texbeml-ps 除外。


```
// This example demonstrates the validation error caused by t0 being reread:
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
texbem t1, t0       ; Compute (u',v')
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



texbem 需要下列材質階段中的材質。

-   階段0會指派具有 (du、dv) 更動資料的一種凹凸地圖。
-   階段1使用材質地圖與色彩資料。
-   此指令會在已取樣的材質階段上設定矩陣資料。
-   這不同于固定函式管線的功能，其中更動資料和矩陣會佔用相同的材質階段。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 