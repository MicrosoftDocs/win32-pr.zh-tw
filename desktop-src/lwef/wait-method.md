---
title: Wait 方法
description: Wait 方法
ms.assetid: 968a3f19-6953-473b-ba98-0dc93696e703
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2e94b0f765a9861c30b254761fbc4dc2e72763
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968488"
---
# <a name="wait-method"></a>Wait 方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

使指定字元的動畫佇列等候，直到指定的動畫要求完成為止。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "*** CharacterID ***" ) 的字元。等候*** 要求*



| 部分      | 描述                                                                     |
|-----------|---------------------------------------------------------------------------------|
| *要求* | 指定特定動畫的 [**要求**](/windows/desktop/lwef/the-request-object) 物件。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

只有當您同時支援多個 (同時) 個字元，並嘗試排序字元的互動時，才使用這個方法。 針對單一字元 (，每個動畫要求都會依序播放--在先前的要求完成之後 ) 。如果您有兩個字元，而且想要讓字元的動畫要求等候到其他字元的動畫完成，請將 **wait** 方法設定為其他字元的動畫 [**要求**](/windows/desktop/lwef/the-request-object) 物件。 若要指定要求參數，您必須建立變數，並指派您要中斷的動畫要求：


```
   Dim GenieRequest 
   Dim RobbyRequest 
   Dim Genie 
   Dim Robby 

   Sub window_Onload

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"
   Agent1.Characters.Load "Robby", "https://agent.microsoft.com/characters/v2/robby/robby.acf"

   Set Genie = Agent1.Characters("Genie")
   Set Robby = Agent1.Characters("Robby")

   Genie.Get "State", "Showing"
   Robby.Get "State", "Showing"

   Genie.Get "Animation", "Announce, AnnounceReturn, Pleased, _ 
      PleasedReturn"
   
   Robby.Get "Animation", "Confused, ConfusedReturn, Sad, SadReturn"

   Set Genie = Agent1.Characters ("Genie")
   Set Robby = Agent1.Characters ("Robby")

   Genie.MoveTo 100,100
   Genie.Show

   Robby.MoveTo 250,100
   Robby.Show

   Genie.Play "Announce"
   Set GenieRequest = Genie.Speak ("Why did the chicken cross the road?")
   
   Robby.Wait GenieRequest
   Robby.Play "Confused"
   Set RobbyRequest = Robby.Speak ("I don't know. Why did the chicken _
      cross the road?")
   
   Genie.Wait RobbyRequest
   Genie.Play "Pleased"
   Set GenieRequest = Genie.Speak ("To get to the other side.")
   
   Robby.Wait GenieRequest
   Robby.Play "Sad"
   Robby.Speak "I never should have asked."

   End Sub
```



您也可以使用特定的動畫要求，直接呼叫 **等候** ，以簡化程式碼。


```
   Robby.Wait Genie.Play "GestureRight"
```



這可避免必須明確宣告 [**Request**](/windows/desktop/lwef/the-request-object) 物件。

 

 