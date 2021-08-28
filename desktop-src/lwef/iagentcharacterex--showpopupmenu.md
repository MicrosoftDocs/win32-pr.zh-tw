---
title: IAgentCharacterEx ShowPopupMenu
description: IAgentCharacterEx ShowPopupMenu
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67d01edae103bad10eb085c4bfd1f5ce559bf26ab030816d241367ec3c13763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105456"
---
# <a name="iagentcharacterexshowpopupmenu"></a>IAgentCharacterEx::ShowPopupMenu

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

顯示字元的快顯功能表。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

字元之快顯功能表的 x 座標（以圖元為單位），相對於螢幕原點 (左上) 。

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

字元快顯功能表的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。

</dd> </dl>

當您將 [**IAgentCharacterEx：： SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) 設定為 **False** 時，當您以滑鼠右鍵按一下該字元或其工作列圖示時，伺服器就不會再自動顯示功能表。 您可以使用這個方法來顯示功能表。

功能表會顯示，直到使用者選取命令或顯示其他功能表為止。 一次只能顯示一個快顯功能表;因此，對此方法的呼叫將會取消 (移除) 前一個功能表中。

只有當您的用戶端應用程式是字元的作用中用戶端時，才會呼叫這個方法。否則會失敗。

[**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md)

 

 




