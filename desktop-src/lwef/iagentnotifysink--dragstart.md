---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33ae89f9e24c6c7b0ec69fba1a98b3a64a18620
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120822"
---
# <a name="iagentnotifysinkdragstart"></a>IAgentNotifySink：:D ragStart

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

當使用者開始拖曳字元時，通知用戶端應用程式。

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

 

 




