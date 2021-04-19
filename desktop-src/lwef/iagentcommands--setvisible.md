---
title: IAgentCommands SetVisible
description: IAgentCommands SetVisible
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a4bdb3c1a7f1e11c9548eb1e1af415d0f5d18f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106979664"
---
# <a name="iagentcommandssetvisible"></a>IAgentCommands::SetVisible

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Visible**](visible-property.md)屬性值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

布林值，決定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Visible**](visible-property.md)屬性。 **True** 會在顯示字元的快顯功能表時，將 **命令** 集合的 [**標題**](caption-property.md) 設為可見。 *False* 不會顯示它。

</dd> </dl>

[**命令**](/windows/desktop/lwef/the-commands-collection-object)集合必須設定 [**標題**](caption-property.md)屬性，並將其 [**Visible**](visible-property.md)屬性設定為 **True** ，才會出現在字元的快顯功能表上。 當您的用戶端應用程式為輸入-主動時，[ **可見** ] 屬性也必須設定為 [ **True** ]，才能讓集合中的命令出現。

## <a name="see-also"></a>另請參閱

[**IAgentCommands：： GetVisible**](iagentcommands--getvisible.md)、 [ **IAgentCommand：： SetCaption**](iagentcommand--setcaption.md)


 

 