---
title: 輸出深度註冊
description: 圖元著色器輸出深度暫存器 (oDepth) 是僅限寫入的純量暫存器，其範圍為 \ 0. 1 \，可針對深度樣板緩衝區傳回深度測試的新深度值。
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9be825d6117cf1cc14464973146dbe176d696d25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311481"
---
# <a name="output-depth-register"></a>輸出深度註冊

圖元著色器輸出深度暫存器 (oDepth) 是僅限寫入的純量暫存器，其範圍為 \[ 0 ..1 \] ，可針對深度樣板緩衝區傳回深度測試的新深度值。

Syntax



| oDepth |
|--------|



 

其中：



| Name   | 描述                                                       |
|--------|-------------------------------------------------------------------|
| oDepth | 深度測試的新深度值-樣板緩衝區 |



 

要注意的是，寫入 oDepth 會導致遺失任何硬體特定深度緩衝區優化演算法 (亦即階層式 Z) ，可加快深度測試效能。

\| \| 寫入至 oDepth 時，需要複寫來源 swizzle (. x. y. z. \| w) 。 不允許明確的寫入遮罩。

寫入至 oDepth 註冊會取代插補深度值 (，並忽略任何深度偏差/slopescale renderstates) 。 如果未建立任何深度緩衝區或將其附加至裝置，則會忽略寫入 oDepth。

如果您要進行取樣並寫入至 oDepth，因為圖元著色器每圖元只會執行一次，所以會針對所有涵蓋的子樣本位置複寫您的深度值。 深度測試仍會在每個範例中進行，但您不會有每個取樣的深度值與圖元著色器的比較，就像您未撰寫 oDepth 一樣。

如果應用程式將 w 緩衝區設定為其深度緩衝區，則在寫入至 oDepth 時，必須將該應用程式納入考慮。 它可能需要將 w 範圍資訊傳送給圖元著色器，並計算 w 範圍，以將寫出的 w 值調整為 oDepth。

### <a name="ps_2_0-and-ps_2_x-restrictions"></a>ps \_ 2 \_ 0 和 ps \_ 2 \_ x 限制

-   oDepth 只能以 [mov-ps](mov---ps.md) 指令撰寫，而且只能執行一次。
-   寫入 oDepth 時，不允許來源修飾詞。
-   寫入至 oDepth 時，不允許使用指令修飾詞。
-   從流程式控制制結構內或使用 predication 時，不會寫入至 oDepth。

### <a name="ps_3_0-restrictions"></a>ps \_ 3 \_ 0 限制

-   針對 ps \_ 3 \_ 0，輸出會將 oC # 和 oD \# 寫入任意次數。 圖元著色器的輸出來自于著色器執行結束時的輸出暫存器內容。 如果未進行寫入至輸出暫存器（可能是因為流量控制），或是著色器剛剛未寫入，則也不會更新對應的呈現目標。 如果寫入輸出暫存器中的通道子集，則會將未定義的值寫入其餘的通道。
-   您可以在流量控制或 predication 中寫入 oDepth，只要所有可能的路徑最後寫入註冊即可。
-   您可能不會執行任何漸層計算 (或隱含叫用漸層計算的作業（例如 [texld-ps \_ 2 \_ 0 和 up](texld---ps-2-0.md)、 [texldb-ps](texldb---ps.md)、 [texldp-ps](texldp---ps.md)) 在流程式控制制語句內，其分支條件會因每個基準而異 (例如：動態流程式控制制指示) 。 指令 predication 不會被視為動態流量控制。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[寄存 器](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




