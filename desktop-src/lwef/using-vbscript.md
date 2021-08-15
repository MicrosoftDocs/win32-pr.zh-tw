---
title: 使用 VBScript
description: 使用 VBScript
ms.assetid: a078eb60-aa12-42ea-850c-7b845fc8037c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afa94bd5b3576e80cf8a0c17857bbb0902bd254e95113d87ae9d1d1fca1e38b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975498"
---
# <a name="using-vbscript"></a>使用 VBScript

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

VBScript 是 Microsoft Internet Explorer 隨附的程式設計語言。 針對其他瀏覽器，請洽詢您的廠商以取得支援。 建議將 VBScript 2.0 (或更新版本的) 用於代理程式。 雖然舊版的 VBScript 可能可與 Agent 搭配使用，但卻缺少您可能想要使用的某些功能。 您可以從 Microsoft 下載網站和 Microsoft VBScript 網站下載 VBScript 2.0，並取得 VBScript 的進一步資訊。

若要從 VBScript 編寫 Microsoft Agent 的程式，請使用 HTML <SCRIPT> tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

針對 [事件]，包含控制項的名稱，後面接著事件的名稱和任何參數：

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

您也可以使用來指定事件處理常式。 <SCRIPT> tag's **For...Event** syntax:

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

雖然 Microsoft Internet Explorer 支援這種語法，但並非所有的瀏覽器都支援。 為了提供相容性，請只針對事件使用先前的語法。

使用 VBScript (2.0 或更新版本的) ，您可以嘗試建立物件並檢查是否存在，以確認是否已安裝 Microsoft 代理程式。 下列範例示範如何在不觸發控制項的自動下載的情況下，檢查代理程式控制項， (當您在頁面) 上包含控制項的標記時，會發生此狀況 <OBJECT> ：

``` syntax
<!-- WARNING - This code requires VBScript 2.0.
It will always fail to detect the Agent control
in VbScript 1.x, because CreateObject doesn't work.
-->

<SCRIPT LANGUAGE=VBSCRIPT>
If HaveAgent() Then
      'Microsoft Agent control was found.
document.write "<H2 align=center>Found</H2>"
Else
      'Microsoft Agent control was not found.
document.write "<H2 align=center>Not Found</H2>"
End If

Function HaveAgent()
' This procedure attempts to create an Agent Control object.
' If it succeeds, it returns True.
'    This means the control is available on the client.
' If it fails, it returns False.
'    This means the control hasn't been installed on the client.

   Dim agent
   HaveAgent = False
   On Error Resume Next
   Set agent = CreateObject("Agent.Control.1")
   HaveAgent = IsObject(agent)

End Function

</SCRIPT>
```

 

 




