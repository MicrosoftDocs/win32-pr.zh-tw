---
title: 字元物件方法
description: 字元物件方法
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141c0fbcfe26e198984fd4a4d8c6c67858085e41178786d2cb78d2938231fdf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480312"
---
# <a name="character-object-methods"></a>字元物件方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

伺服器也會公開 [**字元**](/windows/desktop/lwef/the-characters-object) 集合中每個字元的方法。 以下是支援的方法：

-   [**啟用**](activate-method.md)
-   [**GestureAt**](gestureat-method.md)
-   [**獲取**](get-method.md)
-   [**隱藏**](hide-method.md)
-   [**中斷**](interrupt-method.md)
-   [**接聽**](listen-method.md)
-   [**MoveTo**](moveto-method.md)
-   [**播放**](play-method.md)
-   [**顯示**](show-method.md)
-   [**ShowPopupMenu**](showpopupmenu-method.md)
-   [**Speak**](speak-method.md)
-   [**停止**](stop-method.md)
-   [**StopAll**](stopall-method.md)
-   [**認為**](think-method.md)
-   [**等候**](wait-method.md)

若要使用方法，請參考集合中的字元。 在 VBScript 和 Visual Basic 中，您可以藉由指定字元的識別碼來執行此動作：


```
   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Display the character
   Agent1.Characters("Genie").Show
   Agent1.Characters("Genie").Play "Greet"
   Agent1.Characters("Genie").Speak "Hello. "

   End Sub
```



若要簡化程式碼的語法，您可以定義物件變數，並將它設定為參考 [**字元**](/windows/desktop/lwef/the-characters-object) 集合中的字元物件;然後，您可以使用變數來參考字元的方法或屬性。 下列範例示範如何使用 Visual Basic Set 語句來執行這項作業：


```
   'Define a global object variable
   Dim Genie as Object

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", " Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   'Get the Restpose animation
   Genie.Get "animation", "RestPose"

   'Make the character say Hello
   Genie.Speak "Hello."

   End Sub
```



在 Visual Basic 5.0 中，您也可以將變數宣告為 [**字元**](/windows/desktop/lwef/the-characters-object)物件來建立參考：


```
   Dim Genie as IAgentCtlCharacterEx

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   End Sub
```



宣告 IAgentCtlCharacterEx 型別的物件，可在物件上進行早期繫結，進而產生更好的效能。

在 VBScript 中，您無法將參考宣告為特定類型。 不過，您可以直接宣告變數參考：


```
<SCRIPT LANGUAGE = "VBSCRIPT">
<!—--

   Dim Genie
   
   Sub window_OnLoad
   
   'Load the character
   AgentCtl.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   'Create an object reference to the character in the collection
   set Genie= AgentCtl.Characters ("Genie")

   'Get the Showing state animation
   Genie.Get "state", "Showing"

   'Display the character
   Genie.Show

   End Sub

-->
   </SCRIPT>
```



某些程式設計語言不支援集合。 不過，您可以使用 [**字元**](character-method.md)方法來存取 [**字元**](/windows/desktop/lwef/the-characters-object)物件的方法：


```
   agent.Characters.Character("CharacterID").method
```



此外，您也可以建立 [**字元**](/windows/desktop/lwef/the-characters-object) 物件的參考，讓腳本程式碼更容易遵循：


```
<SCRIPT LANGUAGE="JScript" FOR="window" EVENT="onLoad()">
<!--
   
   //Load the character's data
   AgentCtl.Characters.Load ("Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf");   

   //Create a reference to this object
   Genie = AgentCtl.Characters.Character("Genie");
   
   //Get the Showing state animation
   Genie.Get("state", "Showing");

   //Display the character
   Genie.Show();

-->
</SCRIPT>
```



 

 