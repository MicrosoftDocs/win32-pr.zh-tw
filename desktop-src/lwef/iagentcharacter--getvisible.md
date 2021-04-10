---
title: IAgentCharacter GetVisible
description: IAgentCharacter GetVisible
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0593b9b3a193b9d5910888b81b4ecba90469b1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092654"
---
# <a name="iagentcharactergetvisible"></a>IAgentCharacter：： GetVisible

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for character Visible setting
);
```

判斷字元的動畫框架目前是否可見。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

如果可以看到字元的框架，則為收到 **True** 之變數的位址，如果隱藏，則為 **False** 。

</dd> </dl>

您可以使用這個方法來判斷字元的框架目前是否可見。 若要讓字元可見，請使用 [**Show**](/windows/desktop/lwef/iagentcharacter--show) 方法。 若要隱藏字元，請使用 [**hide**](/windows/desktop/lwef/iagentcharacter--hide) 方法。

 

 