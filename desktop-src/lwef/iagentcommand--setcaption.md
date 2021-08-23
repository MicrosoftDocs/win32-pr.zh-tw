---
title: IAgentCommand SetCaption
description: IAgentCommand SetCaption
ms.assetid: f4fdd37a-28b4-4e00-885c-58addedec659
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ffccf42a972ec9635c929fb954d58bfaff967af364d24ae505e1dbb2bd8772
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976358"
---
# <a name="iagentcommandsetcaption"></a>IAgentCommand::SetCaption

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Command
);
```

設定針對 [**命令**](/windows/desktop/lwef/the-command-object)顯示的 [**標題**](caption-property.md)文字。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

指定 [**命令**](/windows/desktop/lwef/the-command-object)之 [**Caption**](caption-property.md)屬性文字的 BSTR。

</dd> </dl>

設定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**Caption**](caption-property.md)屬性，可定義當其 [**Visible**](visible-property.md)屬性設定為 **True** 且您的應用程式不是輸入-主動用戶端時，該屬性在字元的快顯功能表上的顯示方式。 若要為您的 **標題** 指定 (unlined 助憶鍵) 的存取金鑰，請在該字元前面加上連字號 (&) 字元。 若要讓它成為可選取的，其 [**Enabled**](enabled-property.md) 屬性必須設定為 **True**。

## <a name="see-also"></a>另請參閱

[**IAgentCommand：： GetCaption**](iagentcommand--getcaption.md)、 [**IAgentCommand：： SetEnabled**](iagentcommand--setenabled.md)、 [**IAgentCommand：： SetVisible**](iagentcommand--setvisible.md)、 [**IAgentCommand：： SetVoice**](iagentcommand--setvoice.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)


 

 