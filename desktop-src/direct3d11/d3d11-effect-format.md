---
title: " (Direct3D 11) 的效果格式"
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: '深入瞭解：效果格式 (Direct3D 11) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c08589fcb041591591d033b88e4fafe597e98520
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187703"
---
# <a name="effect-format-direct3d-11"></a> (Direct3D 11) 的效果格式

效果 (通常儲存在副檔名為 fx 的檔案中) 宣告由效果設定的管線狀態。 效果狀態大致可以分為三個類別：

-   [變數](d3d11-effect-variable-syntax.md)，通常會在效果頂端宣告。
-   函[式，可](d3d11-effect-function-syntax.md)執行著色器程式碼，或作為其他函式的 helper 函式使用。
-   可以在效果群組中排列，並使用一或多個效果階段來實行轉譯順序的[技巧](d3d11-effect-technique-syntax.md)。 每個階段都會設定一個或多個 [狀態群組](d3d11-effect-states.md) ，並呼叫著色器函式。

![效果宣告分類的圖表，包括頂端的變數、中間的函式，以及底部的技巧](images/d3d10-effect-intro.png)

上圖顯示效果狀態的類別。

效果二進位格式的定義可以在效果原始程式碼的二進位 EffectBinaryFormat 中找到 \\ 。


## <a name="in-this-section"></a>本節內容



| 主題                                                                   | 描述                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [效果變數語法](d3d11-effect-variable-syntax.md)<br/>   | 效果變數是利用本節所述的語法來宣告。<br/>                                 |
| [注釋語法](d3d11-effect-annotation-syntax.md)<br/>      | 批註是使用者定義的資訊片段，以本節所述的語法來宣告。<br/> |
| [效果函數語法](d3d11-effect-function-syntax.md)<br/>   | 效果函式是以 HLSL 撰寫，並使用本節所述的語法來宣告。<br/>          |
| [效果技巧語法](d3d11-effect-technique-syntax.md)<br/> | 效果技術會以本節所述的語法來宣告。<br/>                                |
| [效果狀態群組](d3d11-effect-states.md)<br/>               | 效果狀態是運算式形式的名稱值配對。<br/>                                          |
| [效果群組語法](d3d11-effect-group-syntax.md)<br/>         | 使用本節所述的語法來宣告效果群組。<br/>                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果11參考](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





