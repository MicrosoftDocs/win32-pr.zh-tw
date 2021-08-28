---
title: IAgentCommands RemoveAll
description: IAgentCommands RemoveAll
ms.assetid: fab43363-6325-4566-b7bb-599591f67321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb855a0eb4cd8a968ec5f03a37aa99fb170158cf75eec9f69a13c392ef94cdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976278"
---
# <a name="iagentcommandsremoveall"></a>IAgentCommands：： RemoveAll

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT Remove();
```

從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中移除所有 [**命令**](/windows/desktop/lwef/the-command-object)。

-   傳回 \_ [確定] 表示作業成功。

從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合移除所有 [**命令**](/windows/desktop/lwef/the-command-object)，也會在您的應用程式為輸入-主動時，從快顯功能表和 [**語音命令] 視窗** 中移除它們。 **RemoveAll** 不會移除伺服器或其他用戶端的專案。

## <a name="see-also"></a>另請參閱

[**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)、 [**IAgentCommands：： Remove**](iagentcommands--remove.md)


 

 