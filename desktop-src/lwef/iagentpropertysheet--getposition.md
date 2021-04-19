---
title: IAgentPropertySheet GetPosition
description: IAgentPropertySheet GetPosition
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff4dcac994901824d7dc37868d7fcfc3f39cefd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968846"
---
# <a name="iagentpropertysheetgetposition"></a>IAgentPropertySheet：： GetPosition

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

抓取 Microsoft 代理程式的屬性工作表視窗位置。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

以圖元為單位的變數位址，此變數會接收屬性工作表左邊緣的螢幕座標（以圖元為單位），相對於螢幕原點 (左上角) 。

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

以圖元為單位的變數位址，此變數會接收屬性工作表上邊緣的螢幕座標（以圖元為單位），相對於螢幕原點 (左上角) 。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentPropertySheet：： GetSize**](iagentpropertysheet--getsize.md)


 

 




