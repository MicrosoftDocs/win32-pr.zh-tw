---
title: '紋理座標註冊 (HLSL 與參考) '
description: 此頂點著色器輸出暫存器包含每個頂點的材質座標。
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad3937b8f0b3f7acd6313774f6de7cde133e69c5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093204"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a>紋理座標註冊 (HLSL 與參考) 

此頂點著色器輸出暫存器包含每個頂點的材質座標。

暫存器包含的屬性會決定每個註冊的行為。



| 屬性        | 描述   |
|-----------------|---------------|
| 名稱            | oT0 - oT7     |
| Count           | 八個向量 |
| I/o 許可權 | 唯寫    |



 

輸出材質座標暫存器是輸出資料暫存器的陣列。 「註冊」資料會依紋理取樣階段逐一查看並當做材質座標使用，以提供資料給圖元著色器。

寫入材質座標暫存器時，建議您只將許多浮點值傳遞為對應紋理對應的維度。 控制以修飾詞傳遞的值。 例如，使用 xy 作為2D 材質地圖。

如果您使用可程式化的頂點著色器，固定的函式頂點管線旗標（ [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1、D3DTTFF \_ COUNT2、D3DTTFF \_ COUNT3、D3DTTFF \_ COUNT4) ）應該設定為零。

物件頂點資料提供輸入材質座標。 未使用並排紋理的物件通常會在範圍 \[ 0，1的材質座標 \] 。 使用平鋪紋理的物件（例如地形）通常具有從 \[ -n、+ n 的材質座標， \] 其中 n 可以是任何浮點數。

紋理座標插補是在適用于光柵的頂點資料上執行。 在點陣化期間，材質座標是在物件頂點之間插入，由材質換行所修改，並以紋理大小進行縮放， (也會將材質定址模式) 以產生整數索引。 然後使用索引來執行材質查閱。 您可以使用 [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) 中的 MaxTextureRepeat 值，判斷材質可以並排顯示多少次。

## <a name="example"></a>範例

宣告材質座標註冊。


```
dcl_texcoord v7
```



將每個頂點的材質座標複製到輸出暫存器。


```
mov oT0, v7
```





| 頂點著色器版本      | 1\_1 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|-----------------------------|------|------|-------|------|------|-------|
| 材質座標註冊 | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 