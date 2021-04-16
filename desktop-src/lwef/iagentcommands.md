---
title: IAgentCommands
description: IAgentCommands
ms.assetid: a171a2f0-7c1c-440f-9b19-28447cc68b95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fc57b7e2e5f628708f46ace98700605f1eb5d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507899"
---
# <a name="iagentcommands"></a>IAgentCommands

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

Microsoft 代理程式伺服器會維護使用者目前可用的命令清單。 這份清單包含伺服器為一般互動所定義的命令，例如隱藏和 Microsoft Agent 屬性、可用 (清單、非輸入主動) 用戶端，以及目前作用中用戶端所定義的命令。 前兩組命令是全域命令;也就是說，無論輸入-主動用戶端為何，都可以隨時使用它們。 用戶端定義的命令只有在該用戶端為輸入-主動時才可使用。

藉由查詢 **IAgentCommands** 的 [**IAgentCharacter**](https://www.bing.com/search?q=**IAgentCharacter**)介面來取出 **IAgentCommands** 介面。 每個 Microsoft 代理程式用戶端應用程式都可以定義一個稱為 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合的命令集合。 若要將 [**命令**](/windows/desktop/lwef/the-command-object) 加入至集合，請使用 [**add**](add-method.md) 或 [**Insert**](insert-method.md) 方法。 雖然您可以使用 [**IAgentCommand**](iagentcommand.md)方法來指定 **命令的** 屬性，但為了獲得最佳的程式碼效能，請在最初設定新 **命令** 的屬性時，于 [**IAgentCommands：： Add**](iagentcommands--add.md)或 [**IAgentCommands：： Insert**](iagentcommands--insert.md)方法中指定所有 **命令** 的屬性。 您可以使用 **IAgentCommand** 方法來查詢或變更屬性設定。

您可以針對 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中的每個 [**命令**](/windows/desktop/lwef/the-command-object)，判斷命令是否出現在字元的快顯功能表、[語音命令] 視窗、[兩者] 或 [兩者] 中。 例如，如果您想要在字元的快顯功能表上出現命令，請設定命令的 [**標題**](caption-property.md) 和 [**可見**](visible-property.md) 的屬性。 若要在 [ **語音命令] 視窗** 中顯示命令，請設定命令的 **標題** 和 [**語音**](voice-property.md) 屬性。

只有當您的用戶端應用程式為輸入-使用中且該字元可見時，使用者才能存取命令集合中的個別命令。 因此，您通常會想要針對 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合物件以及集合中的命令設定 [**Caption**](caption-property.md)、 [**VoiceCaption**](voicecaption-property.md)和 [**Voice**](voice-property.md)屬性，因為這會在字元的快顯功能表和 [語音命令] 視窗中放置 **命令** 集合的專案。 當使用者選擇其 **命令** 專案切換至您的用戶端時，伺服器會自動讓您的用戶端進入作用中狀態，使用 [**IAgentNotifySink：： ActivateInputState**](https://www.bing.com/search?q=**IAgentNotifySink::ActivateInputState**) 來通知用戶端應用程式，並讓其集合中的 **命令** 可供使用。 伺服器也會通知用戶端，該用戶端不再具有 **IAgentNotifySink：： ActivateInputState** 事件的輸入活動。 如此一來，伺服器就只會顯示並接受套用至目前輸入-主動用戶端內容的 **命令** 。 它也可避免用戶端之間的 [**命令**](/windows/desktop/lwef/the-command-object)名稱衝突。

用戶端也可以使用 [**IAgentCharacter：： Activate**](iagentcharacter--activate.md) 方法，明確要求使其成為輸入主動用戶端。 這個方法也支援將您的應用程式設定為非輸入-主動用戶端。 當您與其他應用程式共用字元時，可能會想要使用這個方法，將您的應用程式設定為在應用程式視窗取得焦點而非輸入-主動時，將其設為輸入-主動。

同樣地，您可以使用 [**IAgentCharacter：： Activate**](iagentcharacter--activate.md) 將您的應用程式設定為 (，或不要) 字元的使用中用戶端。 作用中用戶端是用戶端，會在其字元為最頂端的字元時收到輸入。 當此狀態變更時，伺服器會使用 [**IAgentNotifySinkEx：： ActiveClientChange**](iagentnotifysinkex--activeclientchange.md) 事件通知您的應用程式。

當出現字元的快顯功能表時，在使用者重新顯示功能表之前，不會顯示 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合屬性的變更或其集合中的命令。 不過，當開啟時，[語音命令] 視窗會在變更發生時顯示變更。

**IAgentCommands** 會定義一個介面，可讓應用程式加入、移除、設定和查詢 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合的屬性。 這些函數也可從 [**IAgentCommandsEx**](iagentcommandsex.md)取得。

[**命令**](/windows/desktop/lwef/the-commands-collection-object)集合可以在一個字元的快顯功能表和 [語音命令] 視窗中顯示為命令。 若要讓 **命令** 集合出現，您必須設定其 [**標題**](caption-property.md) 屬性。 下表摘要說明 **命令** 集合的屬性如何影響其呈現方式。



| Caption 屬性 | Voice-Caption 屬性 | Voice 屬性 | Visible 屬性 | 出現在字元的快顯功能表中             | 出現在 [語音命令] 視窗中                         |
|------------------|------------------------|----------------|------------------|------------------------------------------------|----------------------------------------------------------|
| 是              | 是                    | 是            | 對             | 是，使用 [**標題**](caption-property.md) | 是，使用 [ **VoiceCaption**](voicecaption-property.md) |
| 是              | 是                    | 否¹            | 對             | 是，使用 [**標題**](caption-property.md) | 否                                                       |
| 是              | 是                    | 是            | False            | 否                                             | 是，使用 [ **VoiceCaption**](voicecaption-property.md) |
| 是              | 是                    | 否¹            | False            | 否                                             | 否                                                       |
| 否¹              | 是                    | 是            | True             | 否                                             | 是，使用 [ **VoiceCaption**](voicecaption-property.md) |
| 否¹              | 是                    | 是            | False            | 否                                             | 是，使用 [ **VoiceCaption**](voicecaption-property.md) |
| 否¹              | Yes                    | 否¹            | True             | 否                                             | 否                                                       |
| 否¹              | Yes                    | 否¹            | False            | 否                                             | 否                                                       |
| 是              | 否¹                    | Yes            | 對             | 是，使用 [**標題**](caption-property.md) | 是，使用 [**標題**](caption-property.md)           |
| Yes              | 否¹                    | 否¹            | True             | 是                                            | 否                                                       |
| 是              | 否¹                    | Yes            | False            | 否                                             | 是，使用 [**標題**](caption-property.md)           |
| Yes              | 否¹                    | 否¹            | False            | 否                                             | 否                                                       |
| 否¹              | 否¹                    | Yes            | True             | 否                                             | 否²                                                      |
| 否¹              | 否¹                    | Yes            | False            | 否                                             | 否²                                                      |
| 否¹              | 否¹                    | 否¹            | True             | 否                                             | 否                                                       |
| 否¹              | 否¹                    | 否¹            | False            | 否                                             | 否                                                       |



 

¹，如果屬性設定為 null。 在某些程式設計語言中，空字串可能不會被解釋為 null 字串。

²命令仍可存取語音。

**依照 Vtable 順序的方法**



| IAgentCommands 方法                           | Description                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**GetCommand**](iagentcommands--getcommand.md) | 從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中抓取 [**命令**](/windows/desktop/lwef/the-command-object)物件。              |
| [**GetCount**](iagentcommands--getcount.md)     | 傳回 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中的 [**命令**](/windows/desktop/lwef/the-command-object)數目值。 |
| [**SetCaption**](iagentcommands--setcaption.md) | 設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Caption**](caption-property.md)屬性值。    |
| [**GetCaption**](iagentcommands--getcaption.md) | 傳回 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Caption**](caption-property.md)屬性值。  |
| [**SetVoice**](iagentcommands--setvoice.md)     | 設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Voice**](voice-property.md)屬性值。        |
| [**GetVoice**](iagentcommands--getvoice.md)     | 傳回 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Voice**](voice-property.md)屬性值。      |
| [**SetVisible**](iagentcommands--setvisible.md) | 設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Visible**](visible-property.md)屬性值。    |
| [**GetVisible**](iagentcommands--getvisible.md) | 傳回 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Visible**](visible-property.md)屬性值。  |
| [**加入**](iagentcommands--add.md)               | 將 [**命令**](/windows/desktop/lwef/the-command-object) 物件加入至 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合。                       |
| [**插入**](iagentcommands--insert.md)         | 在 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中插入 [**Command**](/windows/desktop/lwef/the-command-object)物件。                    |
| [**移除**](iagentcommands--remove.md)         | 移除 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中的 [**命令**](/windows/desktop/lwef/the-command-object)物件。                    |
| [**RemoveAll**](iagentcommands--removeall.md)   | 從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中移除所有的 [**命令**](/windows/desktop/lwef/the-command-object)物件。               |



 

 

 