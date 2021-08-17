---
title: 輸出色彩暫存器
description: 圖元著色器色彩輸出會註冊 (的 oC \ ) 是僅限寫入的暫存器，可將結果輸出至多個呈現目標。
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 038446bb7d588222e04028727a447b6a47c941ab6a18a3ba4216f46e93440961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119702"
---
# <a name="output-color-register"></a>輸出色彩暫存器

圖元著色器色彩輸出會註冊 (的 oC # ) 是僅限寫入的暫存器，可將結果輸出至多個呈現目標。

Syntax



| Oc# |
|------|



 

其中：



| 名稱 | 描述       |
|------|-------------------|
| oC0  | 轉譯目標 \# 0 |
| oC1  | 轉譯目標 \# 1 |
| oC2  | 轉譯目標 \# 2 |
| oC3  | 轉譯目標 \# 3 |



 

## <a name="remarks"></a>備註

-   如果寫入 oCn 但沒有對應的轉譯目標，則會忽略此寫入 oCn。
-   轉譯狀態 D3DRS \_ COLORWRITEENABLE、D3DRS \_ COLORWRITEENABLE1、D3DRS \_ COLORWRITEENABLE2 和 D3DRS \_ COLORWRITEENABLE3 決定在 blend 之後 (oCn 的哪些元件會寫入轉譯目標（如果適用) ）。 如果著色器針對指定的 oCn 暫存器，寫入 D3DRS COLORWRITEENABLE 轉譯狀態所定義的部分（而非全部 \_ \* ）元件，則不成文通道會在對應的呈現目標中產生未定義的值。 如果未寫入 oCn 的元件，則不一定要在上述) 的所有 (更新對應的轉譯目標，因此 D3DRS \_ COLORWRITEENABLE 轉譯 \* 狀態不適用。

### <a name="shader-model-2-restrictions"></a>著色器模型2限制

-   oCn 只能使用 [mov-ps](mov---ps.md) 指令來撰寫。
-   oC0 必須一律寫入著色器中。
-   在寫入任何 oCn 時，不允許來源 swizzle (除了 xyzw = default swizzle) 或 source 修飾詞。
-   除了 xyzw = 預設遮罩) 或指令修飾詞寫入任何 oCn 時，不允許目的地寫入遮罩 (。
-   如果寫入 oCn，則也必須寫入 oC0-oCn-1。 例如，若要寫入 oC2，您也必須寫入 oC0 和 oC1。
-   每個著色器最多隻能寫入一個 oC #。
-   針對 ps \_ 2 \_ x 和 ps \_ 3 \_ 0，您無法寫入至動態流程式控制制或 predication 中的 oc # 和 oD 暫存器 \# (寫入靜態流程式控制制內的 oc #) 。

### <a name="shader-model-3-restrictions"></a>著色器模型3限制

-   針對 ps \_ 3 \_ 0，輸出會將 oC # 和 oD \# 寫入任意次數。 圖元著色器的輸出來自于著色器執行結束時的輸出暫存器內容。 如果未進行寫入至輸出暫存器（可能是因為流量控制），或著色器剛剛未寫入，則對應的 rendertarget 也不會更新。 如果寫入輸出暫存器中的通道子集，則會將未定義的值寫入其餘的通道。
-   若是 ps \_ 3 \_ 0，可以使用任何 Writemasks 寫入 oC # 暫存器。
-   針對 ps \_ 2 \_ x 和 ps \_ 3 \_ 0，您無法寫入至動態流程式控制制或 predication 中的 oc # 和 oD 暫存器 \# (寫入靜態流程式控制制內的 oc #) 。
-   您可能不會執行任何漸層計算 (或隱含叫用漸層計算的作業（例如 [texld-ps \_ 2 \_ 0 和 up](texld---ps-2-0.md)、 [texldb-ps](texldb---ps.md)、 [texldp-ps](texldp---ps.md)) 在流程式控制制語句內，其分支條件會因每個基準而異 (例如：動態流程式控制制指示) 。 指令 predication 不會被視為動態流量控制。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[寄存 器](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[ (Direct3D 9) 的多個呈現目標 ](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 