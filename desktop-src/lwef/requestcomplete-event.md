---
title: RequestComplete 事件
description: RequestComplete 事件
ms.assetid: 543b79d1-f09d-4061-a1a8-8c8ab496bceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5202cc6aee6e8727651279fd216d5f0e5676025584c9cb66c4c6ad958da54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746555"
---
# <a name="requestcomplete-event"></a>RequestComplete 事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

當伺服器完成已排入佇列的要求時發生。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**子***代理程式 * * \_ RequestComplete* *  **(ByVal** *要求 * * * )**



| 部分      | 描述                                            |
|-----------|--------------------------------------------------------|
| *要求* | 傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。 |



 

</dd> </dl>

### <a name="remarks"></a>備註

此事件會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。 因為要求是以非同步方式處理，所以您可以使用此事件來判斷伺服器完成處理要求的時間 (例如 [**Get**](get-method.md)、 [**Play**](play-method.md)或 [**說話**](speak-method.md) 方法) 將此事件與應用程式所產生的其他動作同步處理。 只有在您為要求參考定義了全域變數時，伺服器才會將事件傳送給建立 **要求** 物件參考的用戶端：


```
   Dim MyRequest 
   Dim Genie 

   Sub window_Onload
   
   Agent1.Characters.Load "Genie","https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent.Characters("Genie")

   ' This syntax will generate RequestStart and RequestComplete events.
   Set MyRequest = Genie.Get("state", "Showing")
   ' This syntax will not generate RequestStart and RequestComplete events.
   Genie.Get "state", "Hiding"
   
   End Sub

   Sub Agent1_RequestComplete(ByVal Request)

   If Request = MyRequest Then
      Status = "Showing animation is now loaded"

   End Sub
```



因為在伺服器處理要求之前，不會指派動畫 [**要求**](/windows/desktop/lwef/the-request-object) 物件，請先確定 **要求** 物件存在，然後再嘗試進行評估。 例如，在 Visual Basic 中，如果您使用條件來測試特定要求是否已完成，您可以使用 **Nothing** 關鍵字：


```
   Sub Agent1_RequestComplete (ByVal Request)

   If Not (MyRequest Is Nothing) Then
      If Request = MyRequest Then
      '-- Do whatever
      End If
   End If

   End Sub
```



> [!Note]  
> 在 VBScript 1.0 中，即使您未定義 [**要求**](/windows/desktop/lwef/the-request-object) 物件的參考，也會引發此事件。 這項功能已在可從下載的 VBScript 2.0 中修正 <https://microsoft.com/msdownload/vbscript/scripting.asp> 。

 

### <a name="see-also"></a>另請參閱

[**RequestStart 事件**](requeststart-event.md)


 

 