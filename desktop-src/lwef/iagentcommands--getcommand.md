---
title: IAgentCommands GetCommand
description: IAgentCommands GetCommand
ms.assetid: 0f4a9152-d5dc-4045-b469-8a03f0369e34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ae5e8a92ce8d4a8e04ff049569195e5a2baa21ec3bc398f5fa6ba6ef3c1e3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609688"
---
# <a name="iagentcommandsgetcommand"></a>IAgentCommands：： GetCommand

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetCommand(
   long dwCommandID,         // Command ID
   IUnknown ** ppunkCommand  // address of IUnknown interface
);                    
```

從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中抓取 [**命令**](/windows/desktop/lwef/the-command-object)物件。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

[**命令集合中**](/windows/desktop/lwef/the-commands-collection-object)[**命令**](/windows/desktop/lwef/the-command-object)物件的識別碼。

</dd> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

[**命令**](/windows/desktop/lwef/the-command-object)物件的 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面位址。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCommand**](iagentcommand.md)


 

 