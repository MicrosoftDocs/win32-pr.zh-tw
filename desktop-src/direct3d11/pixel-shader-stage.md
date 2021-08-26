---
title: 圖元著色器階段
description: 圖元著色器階段 (PS) 啟用豐富的陰影技術，例如每圖元光源和後置處理。
ms.assetid: 09831B10-4FD1-41E7-8D81-5AA63DC90020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd58bbc55bbc2fb7d590036bceb061f2a304c0be16ff058d04f226021dfe3cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988158"
---
# <a name="pixel-shader-stage"></a>圖元著色器階段

圖元著色器階段 (PS) 啟用豐富的陰影技術，例如每圖元光源和後置處理。 像素著色器是結合常數變數、紋理資料、插補每個頂點值和其他資料的程式，以產生每個像素的輸出。 轉譯器階段會針對基本型別所涵蓋的每個圖元叫用一次圖元著色器，不過，您可以指定 **Null** 著色器來避免執行著色器。

## <a name="the-pixel-shader"></a>圖元著色器

多重取樣紋理時，像素著色器會在每個涵蓋的多重取樣發生深度/樣板測試期間，叫用一次每個涵蓋像素。 通過深度/樣板測試的樣本會以像素著色器輸出色彩進行更新。

像素著色器的內建功能會產生或使用數量的導數，與螢幕空間 x 和 y 相關。 導數的常見用途是計算紋理取樣的詳細層級，而在非等向性篩選的案例中，選取樣本連同非等向性軸。 通常的硬體實作會同時對多個像素執行像素著色器 (例如 2x2 格線)，如此在像素著色器中運算的數量導數可以合理地在相鄰的相同執行點大略估算為差異值。

### <a name="inputs"></a>輸入

若管線設定後沒有幾何著色器，像素著色器限於 16、32 位元、4 個元件的輸入。 否則，像素著色器最多可以採用 32、32 位元、4 個元件的輸入。

像素著色器輸入資料包括頂點屬性 (可插補，無論是否有透視修正)，也可以視為每個基本類型常數。 像素著色器輸入會從點陣化的基本類型的頂點屬性插補，根據宣告的插補模式。 如果在點陣化之前基本類型被裁剪，則插補模式也會在裁剪過程中採用。

頂點屬性是在像素著色器中心位置插補 (或評估)。 像素著色器屬性插補模式會在輸入登錄宣告中宣告，以每個元素為基礎，如[引數](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)或[輸入結構](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-struct)。 可以用線性方式或使用 [距心取樣](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)來插入屬性。 距心評估只在多重取樣到基本類型所涵蓋的像素時相關，但像素中心可能不是；距心評估盡可能發生在靠近 (非涵蓋) 像素中心。

輸入也可以使用[系統值語意](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)宣告，這會由其他管線階段使用的參數標記。 例如，圖元位置應該以 SV \_ 位置語義標記。 IA 階段可以針對使用 SV PrimitiveID)  (的圖元著色器產生一個純量 \_ ; 轉譯器階段也可以為圖元著色器產生一個純量， (使用 sv \_ IsFrontFace) 。

### <a name="outputs"></a>輸出

像素著色器可以輸出最多 8、32 位元、4 個元件的色彩，或無色彩 (如果捨棄像素)。 像素著色器輸出暫存器元件必須先宣告，才能使用；每個暫存器可以有不同的輸出寫入遮罩。

您可以使用 [輸出合併] 階段中的深度寫入啟用狀態 () 來控制是否要將深度資料寫入深度緩衝區 (或使用捨棄指令來捨棄該圖元) 的資料。 圖元著色器也可以輸出選擇性的32位、1元件、浮點數、深度測試值，以使用 SV \_ 深度語義)  (深度測試。 深度值是在 oDepth 登錄中輸出，並會取代深度測試的插補深度值 (假設已啟用深度測試的話)。 無法在使用固定函式深度或著色器 oDepth 之間動態變更。

像素著色器無法輸出樣板值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖形管線](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[ (Direct3D 10) 的管線階段 ](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 