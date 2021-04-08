---
title: IAgentCommands RemoveAll
description: IAgentCommands RemoveAll
ms.assetid: fab43363-6325-4566-b7bb-599591f67321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bd374b7c5767c416d2c3bb2281e651ba71acd8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682292"
---
# <a name="iagentcommandsremoveall"></a>IAgentCommands：： RemoveAll

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT Remove();
```

從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中移除所有 [**命令**](/windows/desktop/lwef/the-command-object)。

-   傳回 \_ [確定] 表示作業成功。

從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合移除所有 [**命令**](/windows/desktop/lwef/the-command-object)，也會在您的應用程式為輸入-主動時，從快顯功能表和 [**語音命令] 視窗** 中移除它們。 **RemoveAll** 不會移除伺服器或其他用戶端的專案。

## <a name="see-also"></a>另請參閱

[**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)、 [**IAgentCommands：： Remove**](iagentcommands--remove.md)


 

 