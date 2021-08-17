---
title: IAgentCommands GetVoice
description: IAgentCommands GetVoice
ms.assetid: ef8983bc-c70c-48c7-9c5f-1dae61028d90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b348904020a53eb11d2bb7884a05f8d98e223a359f796e7d891dafb3dcc402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105333"
---
# <a name="iagentcommandsgetvoice"></a>IAgentCommands::GetVoice

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Commands collection
);
```

抓取 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Voice**](voice-property.md)屬性值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*
</dt> <dd>

接收 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**語音**](voice-property.md)文字設定值之 BSTR 的位址。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCommands：： SetVoice**](iagentcommands--setvoice.md)、 [**IAgentCommands：： GetCaption**](iagentcommands--getcaption.md)、 [**IAgentCommands：： GetVisible**](iagentcommands--getvisible.md)


 

 