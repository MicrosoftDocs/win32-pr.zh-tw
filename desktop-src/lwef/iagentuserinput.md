---
title: IAgentUserInput
description: IAgentUserInput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37d195d6b5d1294c071a1b73d1da95548cb7a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375156"
---
# <a name="iagentuserinput"></a>IAgentUserInput

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

當伺服器使用 [**IAgentNotifySink：：命令**](iagentnotifysink--command.md)通知輸入-主動用戶端時，它會透過 [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) 物件傳回信息。 **IAgentUserInput** 會定義可讓應用程式查詢這些值的介面。

**依照 Vtable 順序的方法**



| IAgentUserInput 方法                                         | Description                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iagentuserinput--getcount.md)                   | 傳回 [**命令**](command-event.md) 事件中傳回的命令替代專案數目。                                         |
| [**GetItemID**](iagentuserinput--getitemid.md)                 | 傳回特定 [**命令**](command-event.md) 替代的識別碼。                                                              |
| [**GetItemConfidence**](iagentuserinput--getitemconfidence.md) | 傳回特定 [**命令**](command-event.md)替代的 [**信賴**](confidence-property.md)屬性值。 |
| [**GetItemText**](iagentuserinput--getitemtext.md)             | 傳回特定 [**命令**](command-event.md)替代的 [**語音**](voice-property.md)文字值。                   |
| [**GetAllItemData**](iagentuserinput--getallitemdata.md)       | 傳回所有 [**命令**](command-event.md) 替代專案的資料。                                                                  |



 

 

 