---
title: IAgentCommandsEx SetDefaultID
description: IAgentCommandsEx SetDefaultID
ms.assetid: 056ec518-bf0b-403f-adc6-9b53b0c044a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37754eb61df7879511a03dde705936d36f905376
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375120"
---
# <a name="iagentcommandsexsetdefaultid"></a>IAgentCommandsEx::SetDefaultID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetDefaultID(
   long dwID,  // default command's ID
);
```

設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合中預設命令的識別碼。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*
</dt> <dd>

要設定為預設值之 [**命令**](/windows/desktop/lwef/the-command-object) 的識別碼。

</dd> </dl>

這個屬性會設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中的預設 [**命令**](/windows/desktop/lwef/the-command-object)物件集。 在字元的快顯功能表中，預設的命令為粗體。 不過，設定預設的命令不會實際變更命令處理或按兩下事件。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentCommandsEx::GetDefaultID**](iagentcommandsex--getdefaultid.md)


 

 