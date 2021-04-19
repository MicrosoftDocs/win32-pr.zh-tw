---
title: IAgentCommandsEx SetVoiceCaption
description: IAgentCommandsEx SetVoiceCaption
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fcc0f3ce98ff0187b7ed2f01b7131cc8e101bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968281"
---
# <a name="iagentcommandsexsetvoicecaption"></a>IAgentCommandsEx::SetVoiceCaption

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

設定針對 [**命令**](/windows/desktop/lwef/the-command-object)物件顯示的 [**VoiceCaption**](voicecaption-property.md)文字。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

指定 [**命令**](/windows/desktop/lwef/the-command-object)之 [**VoiceCaption**](voicecaption-property.md)屬性文字的 BSTR。

</dd> </dl>

如果您在 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中定義 [**命令**](/windows/desktop/lwef/the-command-object)物件並設定其 [**Voice**](voice-property.md)屬性，您通常也會設定其 [**VoiceCaption**](voicecaption-property.md)屬性。 當您的用戶端應用程式為輸入-使用中且字元可見時，此文字會出現在 [語音命令] 視窗中。 如果未設定此屬性， [**Caption**](caption-property.md) 屬性的設定會決定所顯示的文字。 當 **VoiceCaption** 或 **Caption** 屬性都未設定時，命令不會出現在 [語音命令] 視窗中。

## <a name="see-also"></a>另請參閱

[**IAgentCommandsEx::GetVoiceCaption**](iagentcommandsex--getvoicecaption.md)


 

 