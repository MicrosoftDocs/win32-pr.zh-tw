---
title: texld-ps_1_4
description: 使用來源登錄的內容作為材質座標，以色彩資料 (RGBA) 取樣來載入目的地暫存器。 取樣材質是與目的地暫存器編號相關聯的材質。
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 23827dffc396a40be134be4db3996d2e9f498288
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990795"
---
# <a name="texld---ps_1_4"></a>texld-ps \_ 1 \_ 4

使用來源登錄的內容作為材質座標，以色彩資料 (RGBA) 取樣來載入目的地暫存器。 取樣材質是與目的地暫存器編號相關聯的材質。



| texld dst、src |
|----------------|



 

## <a name="registers"></a>暫存器



| 引數 | 描述          | 暫存器 |     |     |     | 版本      |
|----------|----------------------|-----------|-----|-----|-----|--------------|
|          |                      | vn        | 快遞 之 家  | Tn  | Rn  |              |
| Dst      | 目的地註冊 |           |     |     | x   | 1\_4         |
| src      | 來源註冊      |           |     | x   |     | 1 \_ 4 階段1 |
|          |                      |           |     | x   | x   | 1 \_ 4 階段   |



 

使用 r (n) 作為來源暫存器時， (XYZ) 的前三個元件必須已在著色器的上一個階段中初始化。

若要深入瞭解註冊，請參閱[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。

## <a name="remarks"></a>備註

此指令會在與目的地暫存器編號相關聯的材質階段中，填入材質的範例。 紋理會使用來自來源暫存器的材質座標資料進行取樣。

Texld 和 texcrd 指示的語法會公開支援使用材質暫存器修飾詞來分割。 針對圖元著色器1.4 版， \_ 一律會忽略 D3DTTFF 投射的材質轉換旗標。

使用 texld 的規則：

1.  相同的 xyw 修飾詞必須套用至每次讀取個別 t (n) 在 texcrd 或 texld 指令中進行註冊。 如果 xyw 是在 t (n) 登錄讀取，則可以使用 xyw dw 的相同 t (n) 註冊的其他讀取來混用。 \_
2.  \_Dz 來源修飾詞只適用于 r (n) 來源登錄 (因此僅限第2階段) 的 texld。
3.  \_每個著色器的使用次數不可超過兩次。



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texld                 |      |      |      | x    |      |      |       |      |       |



 

## <a name="examples"></a>範例

Texld 指令可讓您控制要使用來源材質座標資料的元件。 Texld 的一組完整的允許語法如下所示，並包含所有有效的來源登錄修飾詞、選取器和寫入遮罩組合。


```
texld  r(m), t(n).xyz
// Uses xyz from t(n) to sample 1D, 2D, or 3D texture
```




```
texld  r(m), t(n)
// Same as previous
```




```
texld  r(m), t(n).xyw
// Uses xyw (skipping z) from t(n) to sample 1D, 2D or 3D texture
```




```
texld  r(m), t(n)_dw.xyw  
// Samples 1D or 2D texture at x/w, y/w from t(n). The result
// is undefined for a cube-map lookup.
```




```
texld  r(m), r(n).xyz
// Samples 1D, 2D, or 3D texture at xyz from r(m) 
// This is possible in the second phase of the shader
```




```
texld  r(m), r(n)
// Same as previous
```




```
texld  r(m), r(n)_dz.xyz
// Samples 1D or 2D texture at x/z, y/z from r(m)
// Possible only in second phase
// The result is undefined for a cube-map lookup
```




```
texld  r(n), r(n)_dz
// Same as previous
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




