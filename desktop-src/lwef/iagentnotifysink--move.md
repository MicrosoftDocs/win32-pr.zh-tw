---
title: IAgentNotifySink 移動
description: IAgentNotifySink 移動
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52563ff3838348b7bf8e6a2bcdfdf20a51c79723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932518"
---
# <a name="iagentnotifysinkmove"></a>IAgentNotifySink：： Move

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT Move(
   long dwCharID,  // character ID
   long x,         // x-coordinate of new location
   long y,         // y-coordinate of new location
   long dwCause    // cause of move state
);                          
```

移動字元時通知用戶端應用程式。

-   沒有傳回值。

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

已移動之字元的識別碼。

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

相對於螢幕原點的新位置 x 座標（以圖元為單位）， (左上) 。 字元的位置是根據其動畫框架的左上角。

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

新位置的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。 字元的位置是根據其動畫框架的左上角。

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

字元移動的原因。 參數可以是下列其中一項：



| 值                                                          | 描述                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const 不帶正負號短** **NeverMoved = 0;**<br/>        | 尚未移動字元。                                                        |
| **const 不帶正負號短** **UserMoved = 1;**<br/>         | 使用者拖曳字元。                                                          |
| **const 不帶正負號短** **ProgramMoved = 2;**<br/>      | 您的應用程式移動了該字元。                                                |
| **const 不帶正負號短** **OtherProgramMoved = 3;**<br/> | 另一個應用程式移動字元。                                             |
| **const 不帶正負號短** **SystemMoved = 4**<br/>        | 伺服器移動字元，以在螢幕解析度變更之後讓它保持在畫面上。 |



 

</dd> </dl>

此事件會傳送到字元的所有用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： GetMoveCause**](iagentcharacter--getmovecause.md)， [ **IAgentCharacter：： MoveTo**](iagentcharacter--moveto.md)


 

 





