---
title: Command 物件
description: Command 物件
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9e9ce22b3a1c0c2286232b5e2204e158501332
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967890"
---
# <a name="the-command-object"></a>Command 物件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

[**命令**](/windows/desktop/lwef/the-command-object)物件是 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中的專案。 當您的用戶端應用程式變成輸入-主動時，伺服器會為使用者提供 **命令** 物件的存取權。

-   [Command 物件屬性](command-object-properties.md)

若要存取 [**命令**](/windows/desktop/lwef/the-command-object) 物件的屬性，請使用其 [ [**名稱**](name-property.md) ] 屬性在集合中參考它。 在 VBScript 和 Visual Basic 中，您可以直接使用 **Name** 屬性：


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



針對不支援集合的程式設計語言，請使用 [**命令**](command-method.md) 方法：


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



您也可以藉由建立命令物件的參考來參考它。 在 Visual Basic 中，宣告物件變數並使用 Set 語句來建立參考：


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



在 Visual Basic 5.0 中，您也可以將物件宣告為類型 [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) ，然後建立參考。 此慣例可啟用早期繫結，進而提高效能：


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



在 VBScript 中，您可以將參考宣告為特定類型，但是您仍然可以宣告變數，並將它設定為集合中的 [**命令**](/windows/desktop/lwef/the-command-object) ：


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



命令可能會出現在字元的快顯功能表和 [命令] 視窗中，或同時出現在兩者中。 若要顯示在快顯功能表中，它必須有標題，並將 [**Visible**](visible-property.md) 屬性設為 **True**。 此外，它的命令集合物件 **Visible** 屬性也必須設定為 **True**。 若要顯示在 [命令] 視窗中， [**命令**](/windows/desktop/lwef/the-command-object) 必須設定其 [**標題**](caption-property.md) 和 [**語音**](voice-property.md) 屬性。 請注意，當功能表顯示時，不會變更字元的快顯功能表專案。 如果您在顯示字元的快顯功能表時，新增或移除命令或變更其屬性，則當使用者下一次顯示時，功能表會顯示這些變更。 但是，命令視窗會動態反映您所做的任何變更。

下表摘要說明 [**命令**](/windows/desktop/lwef/the-command-object) 的屬性如何影響其呈現方式：



Caption 屬性

Voice-Caption 屬性

Voice 屬性

Visible 屬性

Enabled 屬性

出現在字元的快顯功能表中

出現在命令視窗中

是

是

是

True

True

一般，使用 [**標題**](caption-property.md)

是，使用 [ **VoiceCaption**](voicecaption-property.md)

是

是

是

是

否

已停用，使用 [**標題**](caption-property.md)

否

是

是

是

False

True

未出現

是，使用 [ **VoiceCaption**](voicecaption-property.md)

是

是

是

False

False

未出現

否

是

是

否 

True

True

一般，使用 [**標題**](caption-property.md)

否

是

是

否 

是

否

已停用，使用 [**標題**](caption-property.md)

否

是

是

否 

False

True

未出現

否

是

是

否 

False

False

未出現

否

否 

是

是

True

True

未出現

是，使用 [ **VoiceCaption**](voicecaption-property.md)

否 

是

是

是

否

未出現

否

否 

是

是

False

True

未出現

是，使用 [ **VoiceCaption**](voicecaption-property.md)

否 

是

是

False

False

未出現

否

否 

是

否 

True

True

未出現

否

否 

是

否 

是

否

未出現

否

否 

是

否 

False

True

未出現

否

否 

是

否 

False

False

未出現

否

是

否 

是

True

True

一般，使用 [**標題**](caption-property.md)

是，使用 [**標題**](caption-property.md)

是

否 

是

是

否

已停用，使用 [**標題**](caption-property.md)

否

是

否 

是

False

True

未出現

是，使用 [**標題**](caption-property.md)

是

否 

是

False

False

未出現

否

是

否 

否 

True

True

一般，使用 [**標題**](caption-property.md)

否

是

否 

否 

是

否

已停用，使用 [**標題**](caption-property.md)

否

是

否 

否 

False

True

未出現

否

是

否 

否 

False

False

未出現

否

否 

否 

是

True

True

未出現

否 

否 

否 

是

是

否

未出現

否

否 

否 

是

False

True

未出現

否 

否 

否 

是

False

False

未出現

否

否 

否 

否 

True

True

未出現

否

否 

否 

否 

是

否

未出現

否

否 

否 

否 

False

True

未出現

否

否 

否 

否 

False

False

未出現

No

 如果屬性設定為 null。 在某些程式設計語言中，空字串可能不會被解釋為 null 字串。  此命令仍然可以語音存取。<br/>



 

當伺服器收到其中一個命令的輸入時，它會傳送 [**命令**](/windows/desktop/lwef/the-command-object) 事件，並將 **命令** 的名稱傳回做為 [**userinput>**](/windows/desktop/lwef/iagentuserinput) 物件的屬性。 然後，您可以使用條件陳述式來比對和處理 **命令**。

 

