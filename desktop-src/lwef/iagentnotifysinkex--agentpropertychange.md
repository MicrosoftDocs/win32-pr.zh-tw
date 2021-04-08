---
title: IAgentNotifySinkEx AgentPropertyChange
description: IAgentNotifySinkEx AgentPropertyChange
ms.assetid: 8293cd77-320a-4b57-b3d8-52bc450d6aa0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e27fe9e2318af0642c2df680af3a279ab57253d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932225"
---
# <a name="iagentnotifysinkexagentpropertychange"></a>IAgentNotifySinkEx::AgentPropertyChange

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT AgentPropertyChange(
);
```

當使用者變更 Microsoft Agent 屬性設定時，通知用戶端應用程式。

-   沒有傳回值。

當使用者變更 Microsoft Agent 屬性工作表中的 Microsoft Agent 內容設定時，除非伺服器目前已暫停，否則伺服器會將此事件傳送給所有用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentNotifySinkEx：:D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 




