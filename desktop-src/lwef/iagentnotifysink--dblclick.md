---
title: IAgentNotifySink DblClick
description: IAgentNotifySink DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ec7372d524027588dae5a0a3aafaf07146556e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372194"
---
# <a name="iagentnotifysinkdblclick"></a>IAgentNotifySink：:D blClick

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

當使用者按兩下字元時，通知用戶端應用程式。

-   沒有傳回值。

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

按兩下字元的識別碼。

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

指出滑鼠按鍵和輔助按鍵狀態的參數。 參數可以傳回下列任何組合：



|        |                                                |
|--------|------------------------------------------------|
| 0x0001 | 左方按鈕                                    |
| 0x0010 | 中間按鈕                                  |
| 0x0002 | 右鍵按鈕                                   |
| 0x0004 | 向下 Shift 鍵                                 |
| 0x0008 | 控制索引鍵關閉                               |
| 0x0020 | ALT 鍵向下鍵                                   |
| 0x1000 | 在字元的工作列圖示上發生事件 |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

滑鼠指標的 x 座標（以圖元為單位），相對於螢幕原點 (左上) 。

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

滑鼠指標的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。

</dd> </dl>

此事件會傳送到字元的輸入-主動用戶端。 如果沒有任何字元的用戶端為輸入-主動，伺服器會通知該字元的作用中用戶端。 如果顯示此字元，伺服器也會讓該用戶端輸入為主動，並傳送 [**IAgentNotifySink：： ActivateInputState**](iagentnotifysink--activateinputstate.md)。 如果隱藏字元，則也會自動顯示該字元。

 

 




