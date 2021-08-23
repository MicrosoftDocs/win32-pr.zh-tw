---
title: IAgentCommands SetCaption
description: IAgentCommands SetCaption
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b38138d218804461afc782efc14ff3685f55d2f737db6fdb21c39021efbcb36e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665468"
---
# <a name="iagentcommandssetcaption"></a>IAgentCommands::SetCaption

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

設定針對 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合顯示的 [**標題**](caption-property.md)文字。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

指定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合之 [**Caption**](caption-property.md)屬性值的 BSTR。

</dd> </dl>

設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Caption**](caption-property.md)屬性，可定義當其 [**Visible**](visible-property.md)屬性設定為 **True** ，且您的應用程式不是輸入-主動用戶端時，它會在字元的快顯功能表上顯示的方式。 若要為您的 **標題** 指定 (unlined 助憶鍵) 的存取金鑰，請在該字元前面加上連字號 (&) 字元。

如果您針對已設定 [**標題**](caption-property.md)的 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合定義命令，您通常也會定義其 **命令** 集合的 **標題**。

## <a name="see-also"></a>另請參閱

[**IAgentCommands：： GetCaption**](iagentcommands--getcaption.md)、 [**IAgentCommands：： SetVisible**](iagentcommands--setvisible.md)、 [**IAgentCommands：： SetVoice**](iagentcommands--setvoice.md)


 

 