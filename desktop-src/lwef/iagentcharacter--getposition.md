---
title: IAgentCharacter GetPosition
description: IAgentCharacter GetPosition
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cdff0d6876fc7257e05014f3d9ba695db5d168
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311600"
---
# <a name="iagentcharactergetposition"></a>IAgentCharacter：： GetPosition

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

抓取字元的動畫畫面格位置。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

接收字元動畫框架左邊緣（以圖元為單位）之螢幕座標的變數位址，相對於螢幕原點 (左上) 。

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

以圖元為單位的變數位址，此變數會接收字元動畫框架頂端邊緣的螢幕座標（相對於螢幕原點 (左上) ）。

</dd> </dl>

雖然字元會出現在不規則形狀的區域視窗中，但字元的位置是以其矩形動畫框架為基礎。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： SetPosition**](iagentcharacter--setposition.md)、 [ **IAgentCharacter：： GetSize**](iagentcharacter--getsize.md)


 

 




