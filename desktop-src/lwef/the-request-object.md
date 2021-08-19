---
title: Request 物件
description: Request 物件
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2bc9ecf65403ca6dbb471c81a65b105bcc5b69701760a73f8fbc8a5684a9b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882391"
---
# <a name="the-request-object"></a>Request 物件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

伺服器會以非同步方式處理一些方法。 這可讓您的應用程式程式碼在方法完成時繼續執行。 當用戶端應用程式呼叫其中一個方法時，控制項會建立並傳回要求的 [**要求**](/windows/desktop/lwef/the-request-object) 物件。 您可以藉由將物件變數指派給方法，使用 **Request** 物件來追蹤方法的狀態。 在 Visual Basic 中，先宣告物件變數：


```
   Dim MyRequest as Object
```



在 VBScript 中，您不會在宣告中包含變數類型：


```
   Dim MyRequest
```



然後使用 Visual Basic 的 Set 語句，將變數指派給方法呼叫：


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



這會將參考加入至 [**要求**](/windows/desktop/lwef/the-request-object) 物件。 當 **要求** 物件沒有其他參考時，就會終結要求物件。 當您宣告 **要求** 物件和使用它的方式時，會決定其存留期。 如果在副程式或函式的區域變數中宣告物件，則會在超出範圍時終結該物件;也就是說，當副程式或函式結束時。 如果物件是全域宣告，則在程式終止或新值 (或將值設定為 "empty" ) 指派給物件之前，將不會終結該物件。

[**Request**](/windows/desktop/lwef/the-request-object)物件提供數個可供您查詢的屬性。 例如， [**status**](status-property.md) 屬性會傳回要求的目前狀態。 您可以使用這個屬性來檢查要求的狀態：


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



[**Status**](status-property.md)屬性會以長整數值的形式傳回 [**要求**](/windows/desktop/lwef/the-request-object)物件的狀態。



| 狀態 | 定義                                        |
|--------|---------------------------------------------------|
| 0      | 要求已成功完成。                   |
| 1      | 要求失敗。                                   |
| 2      | 要求佇列中的暫止 (，但未完成) 。 |
| 3      | 要求已中斷。                              |
| 4      | 要求進行中。                              |



 

[**Request**](/windows/desktop/lwef/the-request-object)物件也會在 [**Number**](https://www.bing.com/search?q=**Number**)屬性中包含一個長整數值，此值會傳回錯誤或 [**狀態**](status-property.md)代碼的原因。 如果沒有，則這個值為零 (0) 。 [**Description**](description-property.md)屬性包含對應至錯誤號碼的字串值。 如果字串不存在， **描述** 會包含「應用程式定義或物件定義的錯誤」。

如需 [**Number**](https://www.bing.com/search?q=**Number**) 屬性所傳回的值和意義，請參閱 [錯誤碼](microsoft-agent-error-codes.md)。

伺服器會將動畫要求放在指定的字元佇列中。 這可讓伺服器在不同的執行緒上播放動畫，而您的應用程式程式碼可以在動畫播放時繼續。 如果您建立 [**要求**](/windows/desktop/lwef/the-request-object) 物件參考，伺服器會在動畫要求透過 [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) 和 [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) 事件啟動或完成時，自動通知您。 因為傳回 **要求** 物件的方法是非同步，而且可能不會在呼叫函式的範圍內完成，所以請將您的參考全域宣告給您的 **要求** 物件。

下列方法可以用來傳回 [**Request**](/windows/desktop/lwef/the-request-object)物件： [**GestureAt**](gestureat-method.md)、 [**Get**](get-method.md)、 [**Hide**](hide-method.md)、插斷、 [****](interrupt-method.md)[**載入**](load-method.md)、 [**MoveTo**](moveto-method.md)、[**播放**](play-method.md)、[**顯示**](show-method.md)、[**說話**](speak-method.md)和 [**等候**](https://www.bing.com/search?q=**Wait**)。

 

 