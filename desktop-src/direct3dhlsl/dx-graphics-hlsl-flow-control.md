---
title: 流量控制
description: 大部分的硬體都設計為逐行執行著色器程式碼，並執行每個 HLSL 語句一次。
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70bb7706e520818c86286947acfba6cae0759b4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300507"
---
# <a name="flow-control"></a>流量控制

大部分的硬體都設計為逐行執行著色器程式碼，並執行每個 HLSL 語句一次。 流程式控制制語句會在執行時間決定要執行下一個 HLSL 語句的區塊。 著色器可以使用流程式控制制語句，在一組語句中執行迴圈，或將 (分支) 到下一行的指令以外的指令。 某些流程式控制制語句支援在編譯時期指定的靜態控制項;其他則提供前提控制項，這是在執行時間進行的每個元件決策，而其他人則支援動態控制項，也就是在執行時間根據變數的內容進行決策。

HLSL 支援下列流程式控制制語句。

-   [break](dx-graphics-hlsl-break.md)
-   [繼續](dx-graphics-hlsl-continue.md)
-   [丟棄](dx-graphics-hlsl-discard.md)
-   [do](dx-graphics-hlsl-do.md)
-   [for](dx-graphics-hlsl-for.md)
-   [if](dx-graphics-hlsl-if.md)
-   [switch](dx-graphics-hlsl-switch.md)
-   [而](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (DirectX HLSL 的語言語法) ](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




