---
title: 中斷方法
description: 中斷方法
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e66814963bb3de3db95d60cbc25777244626168e95ceee4bd3d8d76992dd72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749255"
---
# <a name="interrupt-method"></a>中斷方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

中斷指定字元的動畫。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。中斷_ *  *要求*



| 部分      | 描述                                                                  |
|-----------|------------------------------------------------------------------------------|
| *要求* | 特定動畫呼叫的 [**要求**](/windows/desktop/lwef/the-request-object) 物件。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

您可以使用這個來同步處理字元之間的動畫。 例如，如果另一個字元在迴圈動畫中，此方法將會停止迴圈，並移至字元佇列中的下一個動畫。 您無法中斷未使用 (未) 載入的字元動畫。

若要指定要求參數，您必須建立變數，並指派您要中斷的動畫要求：


```
   Dim GenieRequest as Object
   Dim RobbyRequest as Object
   Dim Genie as Object
   Dim Robby as Object

   Sub FormLoad()

      MyAgent1.Characters.Load "Genie", "Genie.acs"

      MyAgent1.Characters.Load "Robby", "Robby.acs"

      Set Genie = MyAgent1.Characters ("Genie")
      Set Robby = MyAgent1.Characters ("Robby")

      Genie.Show

      Genie.Speak "Just a moment"

      Set GenieRequest = Genie.Play ("Processing")

      Robby.Show
      Robby.Play "confused"
      Robby.Speak "Hey, Genie. What are you doing?"
      Robby.Interrupt GenieRequest

      Genie.Speak "I was just checking on something."

   End Sub
```



您無法中斷您在此方法中指定之相同字元的動畫，因為伺服器會將該字元的動畫佇列中的 **中斷** 方法排入佇列。 因此，您只能使用插 **斷來停止** 已載入之另一個字元的動畫。

如果您宣告物件參考，並將它設定為此方法，則會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。

> [!Note]  
> **中斷** 不會排清字元的佇列;它會中止現有的動畫，並移至字元佇列中的下一個動畫。 若要停止並清除字元的佇列，請使用 [**Stop**](stop-method.md) 方法。

 

## <a name="see-also"></a>另請參閱

[**Stop 方法**](stop-method.md)


 

 