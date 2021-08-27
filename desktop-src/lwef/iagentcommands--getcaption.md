---
title: IAgentCommands GetCaption
description: IAgentCommands GetCaption
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6eb40b0be58695e79a02ab0ad67ad0d26a47bd13a1637dc1d1f5a4380a7429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749884"
---
# <a name="iagentcommandsgetcaption"></a>IAgentCommands::GetCaption

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption text for Commands collection
);
```

抓取 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**標題**](caption-property.md)。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*
</dt> <dd>

BSTR 的位址，這個位址會接收針對 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合顯示之 [**標題**](caption-property.md)文字設定的值。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCommands：： SetCaption**](iagentcommands--setcaption.md)、 [**IAgentCommands：： GetVisible**](iagentcommands--getvisible.md)、 [**IAgentCommands：： GetVoice**](iagentcommands--getvoice.md)


 

 