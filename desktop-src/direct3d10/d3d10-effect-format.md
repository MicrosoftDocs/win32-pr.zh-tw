---
description: 效果 (通常儲存在副檔名為 fx 的檔案中) 宣告由效果設定的管線狀態。
ms.assetid: 75b76d65-be97-41c2-8c45-4369fcfd69ce
title: " (Direct3D 10) 的效果格式"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5671750d7b4146ae5da8b0ba61ceae390b60a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386005"
---
# <a name="effect-format-direct3d-10"></a> (Direct3D 10) 的效果格式

效果 (通常儲存在副檔名為 fx 的檔案中) 宣告由效果設定的管線狀態。 效果狀態大致可以分為三個類別：

-   [變數](d3d10-effect-variable-syntax.md)，通常會在效果頂端宣告。
-   函[式，可](d3d10-effect-function-syntax.md)執行著色器程式碼，或作為其他函式的 helper 函式使用。
-   [一種技術](d3d10-effect-technique-syntax.md)，它會使用一或多個效果傳遞來實行轉譯順序。 每個階段都會設定一個或多個 [狀態群組](d3d10-effect-states.md) ，並呼叫著色器函式。

![效果狀態類別的圖表](images/d3d10-effect-intro.png)

上圖顯示效果狀態的類別。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果參考](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



