---
title: ps_1_1、ps_1_2、ps_1_3、ps_1_4
description: 圖元著色器組合器是由一組對暫存器中包含的圖元資料操作的指令所組成。
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e10e4eee48490e7ae998e39d71265aef74339c1979112e2fcf0e47e5b07cda7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512939"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a>ps \_ 1 \_ 1、ps \_ 1 \_ 2、ps \_ 1 \_ 3、ps \_ 1 \_ 4

圖元著色器組合器是由一組對暫存器中包含的圖元資料操作的指令所組成。 作業會以運算子和一或多個運算元組成的指示來表示。 指示使用暫存器，將資料傳入和傳出圖元著色器 ALU。 某些指示也可以使用暫存器來保留暫存結果。

> [!Note]  
> 圖元著色器1.x 的 HLSL 支援已被取代。

 

## <a name="instructions"></a>指示

有兩個主要的圖元著色器指令類別：算術指令和材質定址指示。 算術指令會修改色彩資料。 材質定址作業會處理材質座標資料，在大部分情況下，則會取樣材質。 圖元著色器指令會以每圖元為基礎執行;也就是說，它們不知道管線中的其他圖元。

材質定址指示每個都使用一個位置，但可以將算術指令配對，以啟用兩個色彩元件 (RGB) 和一個插槽中的 Alpha 元件指令。

[ps \_ 1 \_ 1、ps \_ 1 \_ 2、ps \_ 1 \_ 3、ps \_ 1 \_ 4 指示](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) 包含可用指令的清單。

啟用取樣時，圖元著色器每圖元只會執行一次，而不是每個子圖元執行一次。 取樣只會增加多邊形邊緣的解析度，以及深度和樣板測試。 例如，如果已啟用3x3 取樣，而且發現有一條圖元的三角形涵蓋了特定圖元之九個 subpixels 的五個，則圖元著色器會執行一次，而且相同的色彩結果會套用至所有五個 subpixels。

## <a name="registers"></a>暫存器

[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)表列出著色器 ALU 所使用的不同暫存器。

## <a name="modifiers"></a>修飾詞

您可以使用[ps \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md)的修飾詞來變更指令的功能，或從登錄讀取或寫入的資料。

Direct3D 9 需要中繼計算以針對所有表面格式維持至少8位的有效位數。 針對進行中的數學，較高的精確度 (12 位) ，建議使用紋理階段之間的飽和度到8位。 不支援可修改的舍入模式或例外狀況。 應以四捨五入到最接近的精確度來支援乘法，以保持最小精確度的精確度。

## <a name="sampler-count"></a>取樣器計數

可用的紋理取樣器數目如下：

-   若是 ps \_ 1 \_ 0-ps \_ 1 \_ 3，最大值為4。
-   針對 ps \_ 1 \_ 4，最大值為6。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




