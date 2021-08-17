---
title: IAgentPropertySheet GetPosition
description: IAgentPropertySheet GetPosition
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74609f2e5f3201be07c425db17456f17e5202e6497b8b137815ae6124335650
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976138"
---
# <a name="iagentpropertysheetgetposition"></a>IAgentPropertySheet：： GetPosition

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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


 

 




