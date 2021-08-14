---
title: IAgentCommands 移除
description: IAgentCommands 移除
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5875d1377aecc7e28554bac6aae1ccb2b4f515f730a6ab1b0b3a83cec7573418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477191"
---
# <a name="iagentcommandsremove"></a>IAgentCommands：： Remove

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中移除指定的 [**命令**](/windows/desktop/lwef/the-command-object)。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*
</dt> <dd>

要從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中移除之 [**命令**](/windows/desktop/lwef/the-command-object)的識別碼。

</dd> </dl>

從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合移除 [**命令**](/windows/desktop/lwef/the-command-object)，也會在您的應用程式為輸入-主動時，從快顯功能表和 [**語音命令] 視窗** 中移除它。

## <a name="see-also"></a>另請參閱

[**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)、 [**IAgentCommands：： RemoveAll**](iagentcommands--removeall.md)


 

 