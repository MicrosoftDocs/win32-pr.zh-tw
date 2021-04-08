---
title: RequestStart 事件
description: RequestStart 事件
ms.assetid: ecfb9691-cbc4-48f5-8e26-a99389e85eed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2be5954636084d3cbc299c718f2b4e6d9330ef90
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682289"
---
# <a name="requeststart-event"></a>RequestStart 事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

當伺服器開始排入佇列的要求時發生。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**子***代理程式 * * \_ RequestStart* *  **(ByVal** *要求 * * * )**



| 部分      | 描述                                            |
|-----------|--------------------------------------------------------|
| *要求* | 傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。 |



 

</dd> </dl>

### <a name="remarks"></a>備註

此事件會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。 由於要求是以非同步方式進行處理，因此您可以使用此事件來判斷伺服器開始處理要求 (例如 [**Get**](get-method.md)、 [**Play**](play-method.md)或 [**對話**](speak-method.md) 方法) ，進而與您應用程式所產生的其他動作同步處理。 只有在您針對要求參考定義了全域變數時，才會將事件傳送給建立 **要求** 物件參考的用戶端：


```
   Dim MyRequest 
   Dim Genie 

   Sub window_Onload
   
   Agent1.Characters.Load "Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf"   

   Set Genie = Agent1.Characters("Genie")

   ' This syntax will generate RequestStart and RequestComplete events.
   Set MyRequest = Genie.Get("state", "Showing")

   ' This syntax will not generate RequestStart and RequestComplete events.
   Genie.Get ("state", "Hiding")

   End Sub

   Sub Agent1_RequestStart(ByVal Request)

   If Request = MyRequest Then
      Status = "Loading the Showing animation"

   End Sub
```



[**狀態**](status-property.md)會針對傳回的 [**要求**](/windows/desktop/lwef/the-request-object)物件，傳回 4 (要求進行中) 。

因為在伺服器處理要求之前，不會指派動畫 [**要求**](/windows/desktop/lwef/the-request-object) 物件，請先確定 **要求** 物件存在，然後再嘗試進行評估。 例如，在 Visual Basic 中，如果您使用條件來測試特定要求是否已完成，您可以使用 **Nothing** 關鍵字：


```
   Sub Agent1_RequestStart (ByVal Request)

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

[**RequestComplete 事件**](requestcomplete-event.md)


 

 