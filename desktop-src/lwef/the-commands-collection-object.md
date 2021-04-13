---
title: 命令集合物件
description: 命令集合物件
ms.assetid: 8726ce04-77d3-4ae3-bd46-e75f42b36d6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2367035d86f92d57dc459564943b9e7797ecb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104374989"
---
# <a name="the-commands-collection-object"></a>命令集合物件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

Microsoft 代理程式伺服器會維護使用者目前可用的命令清單。 這份清單包含伺服器為一般互動所定義的命令 (例如隱藏和開啟 [語音命令] 視窗) 、可用 (清單，但是非輸入主動) 用戶端，以及目前作用中用戶端所定義的命令。 前兩組命令是全域命令;也就是說，無論輸入-主動用戶端為何，都可以隨時使用它們。 用戶端定義的命令只有在該用戶端為輸入-主動且可看見該字元時才可使用。

每個用戶端應用程式都可以定義稱為 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合的命令集合。 若要將命令加入至集合，請使用 [**add**](add-method.md) 或 [**Insert**](insert-method.md) 方法。 雖然您可以使用不同的語句來指定命令的屬性，但是為了獲得最佳的程式碼效能，請在 **Add** 或 **Insert** 方法語句中指定所有命令的屬性。 您可以針對集合中的每個命令，判斷使用者對命令的存取是否出現在字元的快顯功能表、[語音命令] 視窗、[兩者] 或 [兩者] 中。 例如，如果您想要在字元的快顯功能表上出現命令，請設定命令的 [**標題**](caption-property.md) 和 [**可見**](visible-property.md) 的屬性。 若要在 [語音命令] 視窗中顯示命令，請設定命令的 [**VoiceCaption**](voicecaption-property.md) 和 [**Voice**](voice-property.md) 屬性。

只有當您的用戶端應用程式為輸入-主動時，使用者才能存取集合中的個別通訊 [**命令**](/windows/desktop/lwef/the-commands-collection-object)and。 因此，當您共用其他用戶端應用程式的字元時，通常會想要設定 **命令** 集合物件的 [**Caption**](caption-property.md)、 [**VoiceCaption**](voicecaption-property.md)和 [**Voice**](voice-property.md)屬性，以及集合中的命令。 這會在字元的快顯功能表和 [語音命令] 視窗中放置 **命令** 集合的專案。

當使用者選擇其 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 專案切換至您的用戶端時，伺服器會自動讓您的用戶端進入作用中狀態，使用 [**ActivateInput**](activateinput-event.md) 事件通知用戶端應用程式，並讓其集合中的命令可供使用。 伺服器也會通知用戶端，它不再是使用 [**DeActivateInput**](deactivateinput-event.md) 事件的輸入。 如此一來，伺服器就只會顯示並接受套用至目前輸入-主動用戶端內容的命令。 它也可避免用戶端之間的命令名稱衝突。

用戶端也可以使用 [**啟動**](activate-method.md) 方法，明確要求使其成為輸入-主動用戶端。 這個方法也支援將您的應用程式設定為非輸入-主動用戶端。 當您與另一個應用程式共用一個字元時，可能會想要使用這個方法，當應用程式視窗取得焦點時，將應用程式設定為輸入-主動，而當應用程式視窗失去焦點時，則設定為非作用中。

同樣地，您可以使用 [**啟動**](activate-method.md) 方法，將您的應用程式設定為 (，或不) 字元的使用中用戶端。 作用中用戶端是用戶端，會在其字元為最頂端的字元時收到輸入。 當此狀態變更時，伺服器會使用 [**ActiveClientChange**](activeclientchange-event.md) 事件來通知您的應用程式。

當字元的快顯功能表顯示時，在使用者重新顯示功能表之前， [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合的屬性或其集合中的命令變更都不會出現。 不過，[命令] 視窗會在發生變更時顯示變更。

-   [命令物件方法](commands-object-methods.md)
-   [命令物件屬性](commands-object-properties.md)

 

 