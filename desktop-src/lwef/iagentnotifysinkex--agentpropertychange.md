---
title: IAgentNotifySinkEx AgentPropertyChange
description: IAgentNotifySinkEx AgentPropertyChange
ms.assetid: 8293cd77-320a-4b57-b3d8-52bc450d6aa0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d7a0737428d20b297d83ac92c3ce6957dac0390c719c17b96a00983a0a57af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961488"
---
# <a name="iagentnotifysinkexagentpropertychange"></a>IAgentNotifySinkEx::AgentPropertyChange

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT AgentPropertyChange(
);
```

當使用者變更 Microsoft Agent 屬性設定時，通知用戶端應用程式。

-   沒有傳回值。

當使用者變更 Microsoft Agent 屬性工作表中的 Microsoft Agent 內容設定時，除非伺服器目前已暫停，否則伺服器會將此事件傳送給所有用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentNotifySinkEx：:D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 




