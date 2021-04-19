---
title: IAgentCommandsEx GetVoiceCaption
description: IAgentCommandsEx GetVoiceCaption
ms.assetid: 0e505295-386a-421f-a43c-6da03c8a2b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a757e1c841afd62b9b6ae13f1ef34178f133ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966445"
---
# <a name="iagentcommandsexgetvoicecaption"></a>IAgentCommandsEx::GetVoiceCaption

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption
);
```

抓取 [**命令**](/windows/desktop/lwef/the-command-object)物件的 [**VoiceCaption**](voicecaption-property.md) 。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*
</dt> <dd>

接收針對 [**命令**](/windows/desktop/lwef/the-command-object)顯示之 [**標題**](caption-property.md)文字值的 BSTR 位址。

</dd> </dl>

傳回的文字是針對 [**命令**](/windows/desktop/lwef/the-command-object) 物件設定的文字，而且當您的用戶端應用程式為輸入-主動時，會出現在 [語音命令] 視窗中。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentCommandsEx::SetVoiceCaption**](iagentcommandsex--setvoicecaption.md)


 

 