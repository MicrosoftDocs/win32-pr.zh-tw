---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63c24abd41f0509293ba2fafeb055f195a4d13ad354662e8d32d0fb1715e1fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477026"
---
# <a name="iagentnotifysinkdragcomplete"></a>IAgentNotifySink：:D ragComplete

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

當使用者停止拖曳字元時，通知用戶端應用程式。

-   沒有傳回值。

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

拖曳字元的識別碼。

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

指出滑鼠按鍵和輔助按鍵狀態的參數。 參數可以傳回下列任何組合：



| 值  | 描述      |
|--------|------------------|
| 0x0001 | 左方按鈕      |
| 0x0010 | 中間按鈕    |
| 0x0002 | 右鍵按鈕     |
| 0x0004 | 向下 Shift 鍵   |
| 0x0008 | 控制索引鍵關閉 |
| 0x0020 | ALT 鍵向下鍵     |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

滑鼠指標的 x 座標（以圖元為單位），相對於螢幕原點 (左上) 。

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

滑鼠指標的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。

</dd> </dl>

 

 




