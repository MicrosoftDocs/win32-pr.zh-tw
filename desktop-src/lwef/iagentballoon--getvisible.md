---
title: IAgentBalloon GetVisible
description: IAgentBalloon GetVisible
ms.assetid: 328af211-4ea4-482c-8487-42c8e4cd66b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 939026026e18e550ca18838977f00a8878db9039595d9eadd0b30b88235a0248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962318"
---
# <a name="iagentballoongetvisible"></a>IAgentBalloon：： GetVisible

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for word balloon
);                   // Visible setting
```

決定是否顯示或隱藏文字提示。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

如果可以看到文字批註，則為收到 **True** 的變數位址，如果隱藏，則為 **False** 。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentBalloon::SetVisible**](iagentballoon--setvisible.md)


 

 




