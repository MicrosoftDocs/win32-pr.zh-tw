---
title: IAgentCharacterEx GetActive
description: IAgentCharacterEx GetActive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dab89ee9ba89c5982e34844917334d97169b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840540"
---
# <a name="iagentcharacterexgetactive"></a>IAgentCharacterEx::GetActive

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

抓取用戶端應用程式是否為字元的作用中用戶端，以及字元是否最上層。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*
</dt> <dd>

變數的位址，此變數會接收狀態設定的下列其中一個值：



| 值                                                              | 描述                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const 不帶正負號的 short** **ACTI加值稅E \_ NOTACTIVE = 0;**<br/>   | 您的用戶端不是字元的作用中用戶端。                |
| **const 不帶正負號短****啟用使用中 \_ = 1;**<br/>      | 您的用戶端是字元的作用中用戶端。                    |
| **const 不帶正負號的 short** **ACTI加值稅E \_ INPUTACTIVE = 2;**<br/> | 您的用戶端是輸入-主動 (最上層字元) 的作用中用戶端。 |



 

</dd> </dl>

這項設定可讓您知道您是字元的作用中用戶端，還是您的字元是否為輸入使用中的字元。 當多個用戶端應用程式共用相同的字元時，字元的作用中用戶端會收到滑鼠輸入 (例如，Microsoft Agent control click 或拖曳 events) 。 同樣地，當顯示多個字元時，最上層字元的作用中用戶端 (也稱為輸入-主動用戶端) 接收 [**IAgentNotifySink：：命令**](iagentnotifysink--command.md) 事件。

您可以使用 [**啟動**](iagentcharacter--activate.md) 方法來設定您的應用程式是字元的作用中用戶端，還是讓您的應用程式成為輸入使用中的用戶端 (也會讓字元) 最上層。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： Activate**](iagentcharacter--activate.md)、 [ **IAgentNotifySinkEx：： ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)


 

 





