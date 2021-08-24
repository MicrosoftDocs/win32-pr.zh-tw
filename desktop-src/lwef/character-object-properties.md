---
title: 字元物件屬性
description: 字元物件屬性
ms.assetid: 86748de2-f5c8-4057-bfa4-79d46cac1e62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c80e16bdb35d3fdfd8687eb15f200d2005ab75027e4dcc786f883d21232af4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610688"
---
# <a name="character-object-properties"></a>字元物件屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

[**字元**](/windows/desktop/lwef/the-characters-object)物件會公開下列屬性：

-   [**使用中**](active-property.md)
-   [**AutoPopupMenu**](autopopupmenu-property.md)
-   [**描述**](description-property.md)
-   [**ExtraData**](extradata-property.md)
-   [**GUID**](guid-property.md)
-   [**HasOtherClients**](hasotherclients-property.md)
-   [**高度**](height-property.md)
-   [**號**](helpcontextid-property-ch.md)
-   [**HelpFile**](helpfile-property.md)
-   [**HelpModeOn**](helpmodeon-property.md)
-   [**IdleOn**](idleon-property.md)
-   [**LanguageID**](languageid-property.md)
-   [**離開**](left-property.md)
-   [**MoveCause**](movecause-property.md)
-   [**名稱**](name-property.md)
-   [**OriginalHeight**](originalheight-property.md)
-   [**OriginalWidth**](originalwidth-property.md)
-   [**瀝青**](pitch-property.md)
-   [**SoundEffectsOn**](soundeffectson-property.md)
-   [**速度**](speed-property.md)
-   [**SRModeID**](srmodeid-property.md)
-   [**SRStatus**](srstatus-property.md)
-   [**返回頁首**](top-property.md)
-   [**TTSModeID**](ttsmodeid-property.md)
-   [**版本**](version-property.md)
-   [**VisibilityCause**](visibilitycause-property.md)
-   [**可見**](visible-property-cob.md)
-   [**寬度**](width-property-co.md)

請注意，字元的 [**高度**](height-property.md)、 [**左方**](left-property.md)、 [**頂端**](top-property.md)和 [**寬度**](width-property-co.md) 屬性，會與程式設計環境所支援的控制項位置不同。 [**字元**](/windows/desktop/lwef/the-characters-object)屬性會套用至可見的字元呈現，而不是 Microsoft Agent 控制項的位置。

如同 [**字元**](/windows/desktop/lwef/the-characters-object) 物件方法，您可以使用 [**字元**](/windows/desktop/lwef/the-characters-object) 集合來存取字元的屬性，或是藉由宣告物件變數並將它設定為集合中的字元，來簡化您的語法。 在下列範例中，Test1 和 Test2 會設定為相同的值：


```
   Dim Genie 
   Dim MyRequest
   
   Sub window_Onload

   Agent.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent.Characters("Genie")

   Genie.MoveTo 15,15
   Set MyRequest = Genie.Show()

   End Sub

   Sub Agent_RequestComplete(ByVal Request)

   If Request = MyRequest Then 
      Test1 = Agent.Characters("Genie").Top
      Test2 = Genie.Top
      MsgBox "Test 1 is " + cstr(Test1) + "and Test 2 is " + cstr(Test2)
   End If

   End Sub
```



因為伺服器會以非同步方式載入字元，所以在查詢其屬性之前，請確定已載入該字元，例如使用 [**RequestComplete**](requestcomplete-event.md) 事件。 否則，屬性可能會傳回不正確的值。

 

 