---
title: 使用 VBScript
description: 使用 VBScript
ms.assetid: a078eb60-aa12-42ea-850c-7b845fc8037c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0bc64419af4d8dc47de5a2393fcf5cb259374ed
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881021"
---
# <a name="using-vbscript"></a>使用 VBScript

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

VBScript 是 Microsoft Internet Explorer 隨附的程式設計語言。 針對其他瀏覽器，請洽詢您的廠商以取得支援。 建議將 VBScript 2.0 (或更新版本的) 用於代理程式。 雖然舊版的 VBScript 可能可與 Agent 搭配使用，但卻缺少您可能想要使用的某些功能。 您可以從 Microsoft 下載網站和 Microsoft VBScript 網站下載 VBScript 2.0，並取得 VBScript 的進一步資訊。

若要從 VBScript 編寫 Microsoft Agent 的程式，請使用 HTML &lt; 腳本 &gt; 標記。 若要存取程式設計介面，請使用您在物件標記中指派的控制項名稱 &lt; &gt; ，後面接著子物件 (如果有任何) 、方法或屬性的名稱，以及方法或屬性所支援的任何參數或值：

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

您也可以使用的 &lt; 腳本 &gt; 標記 **來指定事件處理常式。事件** 語法：

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

雖然 Microsoft Internet Explorer 支援這種語法，但並非所有的瀏覽器都支援。 為了提供相容性，請只針對事件使用先前的語法。

使用 VBScript (2.0 或更新版本的) ，您可以嘗試建立物件並檢查是否存在，以確認是否已安裝 Microsoft 代理程式。 下列範例示範如何在不觸發控制項的自動下載的情況下檢查代理程式控制項， (當您在 &lt; 頁面) 上包含控制項的物件標記時，就會發生這個情況 &gt; ：

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

 

 




