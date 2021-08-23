---
title: IAgentCommand
description: IAgentCommand
ms.assetid: 70873093-df71-4377-9c39-c7528400052f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e2288a7b913becc54e2c0baa43eb14903e65fb7eddf6620d5cefbd78968026
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665478"
---
# <a name="iagentcommand"></a>IAgentCommand

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

[**命令**](/windows/desktop/lwef/the-command-object)物件是 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中的專案。 伺服器可讓使用者存取您的命令，讓您的用戶端應用程式變成啟用輸入。 若要取得 **命令**，請呼叫 [**IAgentCommands：： GetCommand**](iagentcommands--getcommand.md)。

**IAgentCommand** 會定義介面，讓應用程式能夠設定命令物件的屬性，並查詢這些 [**命令**](/windows/desktop/lwef/the-command-object) 物件可以出現在字元的快顯功能表和 [語音命令] 視窗中。 這些函數也可從 [**IAgentCommandEx**](iagentcommandex.md)取得。 **命令** 物件是 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中的專案。 當您的用戶端應用程式變成使用中時，伺服器會為使用者提供您命令的存取權。

[**命令**](/windows/desktop/lwef/the-command-object)可能會出現在字元的快顯功能表和 [語音命令] 視窗中。 若要出現在快顯功能表中，它必須有 [**標題**](caption-property.md) ，並將 [**Visible**](visible-property.md) 屬性設為 **True**。 當您的用戶端應用程式為輸入-主動時，命令集合物件的 **Visible** 屬性也必須設為 **True** [**，命令才**](/windows/desktop/lwef/the-commands-collection-object)會出現在快顯功能表中。 若要顯示在 [語音命令] 視窗中， **命令** 必須設定其 [**VoiceCaption**](voicecaption-property.md) 和 [**Voice**](voice-property.md) 屬性。  (為了回溯相容性，如果沒有 **VoiceCaption**，則會使用 **標題** 設定。 ) 

顯示功能表時，不會變更字元的快顯功能表專案。 如果您在顯示字元的快捷方式功能表時，新增或移除命令或變更其屬性，則在重新顯示時，功能表會顯示這些變更。 不過，[語音命令] 視窗會在您進行變更時顯示變更。

下表摘要說明命令的屬性如何影響其呈現方式。



| Caption 屬性 | Voice-Caption 屬性 | Voice 屬性 | Visible 屬性 | 出現在字元的快顯功能表中             | 出現在 [語音命令] 視窗中                         |
|------------------|------------------------|----------------|------------------|------------------------------------------------|----------------------------------------------------------|
| 是              | 是                    | 是            | 是             | 是，使用 [**標題**](caption-property.md) | 是，使用 [ **VoiceCaption**](voicecaption-property.md) |
| 是              | 是                    | 否¹            | 是             | 是，使用 [**標題**](caption-property.md) | 否                                                       |
| 是              | 是                    | 是            | False            | 否                                             | 是，使用 [ **VoiceCaption**](voicecaption-property.md) |
| 是              | 是                    | 否¹            | False            | 否                                             | 否                                                       |
| 否¹              | 是                    | 是            | True             | 否                                             | 是，使用 [ **VoiceCaption**](voicecaption-property.md) |
| 否¹              | 是                    | 是            | False            | 否                                             | 是，使用 [ **VoiceCaption**](voicecaption-property.md) |
| 否¹              | Yes                    | 否¹            | True             | 否                                             | 否                                                       |
| 否¹              | Yes                    | 否¹            | False            | 否                                             | 否                                                       |
| 是              | 否¹                    | Yes            | 是             | 是，使用 [**標題**](caption-property.md) | 是，使用 [**標題**](caption-property.md)           |
| Yes              | 否¹                    | 否¹            | True             | 是                                            | 否                                                       |
| 是              | 否¹                    | Yes            | False            | 否                                             | 是，使用 [**標題**](caption-property.md)           |
| Yes              | 否¹                    | 否¹            | False            | 否                                             | 否                                                       |
| 否¹              | 否¹                    | Yes            | True             | 否                                             | 否²                                                      |
| 否¹              | 否¹                    | Yes            | False            | 否                                             | 否²                                                      |
| 否¹              | 否¹                    | 否¹            | True             | 否                                             | 否                                                       |
| 否¹              | 否¹                    | 否¹            | False            | 否                                             | 否                                                       |



 

¹，如果屬性設定為 null。 在某些程式設計語言中，空字串可能不會解讀為與 null 字串相同的字串。

²命令仍可存取語音。

一般而言，如果您定義具有 [**語音**](voice-property.md)設定的 [**命令**](/windows/desktop/lwef/the-command-object)，您也可以為其相關聯的 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合定義 [**標題**](caption-property.md)和 **語音** 設定。 如果一組命令的 **命令** 集合沒有任何 **聲音** 或沒有 **標題** 的設定，而且目前輸入為作用中，但這些 **命令** 具有 **標題** 和 **聲音** 設定，則當用戶端應用程式變成輸入-主動時， **命令** 會出現在 [ (未定義的命令) ] 下的 [語音命令] 視窗樹狀檢視中。

當伺服器收到的輸入符合您針對 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合所定義的其中一個 [**命令**](/windows/desktop/lwef/the-command-object)物件時，它會傳送 [**IAgentNotifySink：：命令**](https://www.bing.com/search?q=**IAgentNotifySink::Command**)事件，並將命令的識別碼傳回為 [**IAgentUserInput**](https://www.bing.com/search?q=**IAgentUserInput**)物件的屬性。 然後，您可以使用條件陳述式來比對和處理命令。

**依照 Vtable 順序的方法**



| IAgentCommand 方法                                                   | 描述                                                                                                                         |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**SetCaption**](https://www.bing.com/search?q=**SetCaption**)                             | 設定 [**命令**](/windows/desktop/lwef/the-command-object)物件的 [**標題**](caption-property.md)值。                         |
| [**GetCaption**](https://www.bing.com/search?q=**GetCaption**)                             | 傳回 [**Command**](/windows/desktop/lwef/the-command-object)物件的 [**Caption**](caption-property.md)屬性值。               |
| [**SetVoice**](iagentcommand--setvoice.md)                             | 設定 [**命令**](/windows/desktop/lwef/the-command-object)物件之 [**語音**](voice-property.md)文字的值。                        |
| [**GetVoice**](iagentcommand--getvoice.md)                             | 傳回 [**Command**](/windows/desktop/lwef/the-command-object)物件的 [**Voice**](voice-property.md)屬性值。                   |
| [**SetEnabled**](iagentcommand--setenabled.md)                         | 設定 [**Command**](/windows/desktop/lwef/the-command-object)物件的 [**Enabled**](enabled-property.md)屬性值。                 |
| [**GetEnabled**](iagentcommand--getenabled.md)                         | 傳回 [**命令**](/windows/desktop/lwef/the-command-object)物件的 [**Enabled**](enabled-property.md)屬性值。               |
| [**SetVisible**](iagentcommand--setvisible.md)                         | 設定 [**Command**](/windows/desktop/lwef/the-command-object)物件的 [**Visible**](visible-property.md)屬性值。                 |
| [**GetVisible**](iagentcommand--getvisible.md)                         | 傳回 [**命令**](/windows/desktop/lwef/the-command-object)物件的 [**Visible**](visible-property.md)屬性值。               |
| [**SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md) | 設定 [**Command**](/windows/desktop/lwef/the-command-object)物件的 [**信賴**](confidence-property.md)屬性值。           |
| [**GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md) | 傳回 [**Command**](/windows/desktop/lwef/the-command-object)物件的 [**信賴**](confidence-property.md)屬性值。         |
| [**SetConfidenceText**](iagentcommand--setconfidencetext.md)           | 設定 [**Command**](/windows/desktop/lwef/the-command-object)物件的 [**ConfidenceText**](confidencetext-property.md)屬性值。   |
| [**getConfidenceText**](iagentcommand--getconfidencetext.md)           | 傳回 [**命令**](/windows/desktop/lwef/the-command-object)物件的 [**ConfidenceText**](confidencetext-property.md)屬性值。 |
| [**getID**](iagentcommand--getid.md)                                   | 傳回 [**命令**](/windows/desktop/lwef/the-command-object) 物件的識別碼。                                                                      |



 

 

 