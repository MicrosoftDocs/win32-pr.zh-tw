---
title: IAgentCommandEx SetVoiceCaption
description: IAgentCommandEx SetVoiceCaption
ms.assetid: 672fdc13-25d3-4ced-b295-2b687767c17f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358514dd33fc97a98f9b63107eabc98e0387bab8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023310"
---
# <a name="iagentcommandexsetvoicecaption"></a>IAgentCommandEx::SetVoiceCaption

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

設定針對 [**命令**](/windows/desktop/lwef/the-command-object)顯示的 [**VoiceCaption**](voicecaption-property.md)文字。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

指定 [**命令**](/windows/desktop/lwef/the-command-object)之 [**VoiceCaption**](voicecaption-property.md)屬性文字的 BSTR。

</dd> </dl>

如果您在 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中定義 [**命令**](/windows/desktop/lwef/the-command-object)物件並設定其 [**Voice**](voice-property.md)屬性，您通常也會設定其 [**VoiceCaption**](voicecaption-property.md)屬性。 當您的用戶端應用程式為輸入使用中時，此文字會出現在 [語音命令] 視窗中。 如果未設定此屬性， [**Caption**](caption-property.md) 屬性的設定會決定所顯示的文字。 未設定 **VoiceCaption** 或屬性時，命令不會出現在 [語音命令] 視窗中。

[**標題**](caption-property.md)

## <a name="see-also"></a>另請參閱

[**IAgentCommand：： GetCaption**](iagentcommand--getcaption.md)、 [**IAgentCommand：： SetEnabled**](iagentcommand--setenabled.md)、 [**IAgentCommand：： SetVisible**](iagentcommand--setvisible.md)、 [**IAgentCommand：： SetVoice**](iagentcommand--setvoice.md)、 [**IAgentCommandsEx：： AddEx**](iagentcommandsex--addex.md)、 [**IAgentCommandsEx：： InsertEx**](iagentcommandsex--insertex.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)


 

 