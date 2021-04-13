---
title: IAgent
description: IAgent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12900a4288b9917d695dd25d4b81362b67c93587
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300888"
---
# <a name="iagent"></a>IAgent

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

**IAgent** 定義了一個介面，可讓應用程式載入字元、接收事件，以及檢查 Microsoft 代理程式伺服器的目前狀態。 這些函數也可從 [**IAgentEx**](iagentex.md)取得。

舊版中包含的 GetSuspended 方法已淘汰，而且會傳回 **False** 以提供回溯相容性。

**依照 Vtable 順序的方法**



| IAgent 方法                               | Description                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [**載入**](load-method.md)                  | 載入字元的資料檔案。                                |
| [**卸載**](unload-method.md)              | 卸載字元的資料檔案。                              |
| [**註冊**](iagent--register.md)         | 註冊用戶端的通知接收。                 |
| [**Unegister**](iagent--unregister.md)      | 取消註冊用戶端的通知接收。                     |
| [**GetCharacter**](iagent--getcharacter.md) | 傳回已載入字元的 IAgentCharacter 介面。 |



 

 

 




