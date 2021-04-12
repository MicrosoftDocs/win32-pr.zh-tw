---
title: IAgentCommands 移除
description: IAgentCommands 移除
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0c3321de3d06b5e2ebea873a4bace91482d8c5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104185693"
---
# <a name="iagentcommandsremove"></a>IAgentCommands：： Remove

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

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


 

 