---
title: 使用 VBScript
description: 使用 VBScript
ms.assetid: a078eb60-aa12-42ea-850c-7b845fc8037c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691ed6bf520c83e4b679bb174274abb984eaa2f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183633"
---
# <a name="using-vbscript"></a><span data-ttu-id="86788-103">使用 VBScript</span><span class="sxs-lookup"><span data-stu-id="86788-103">Using VBScript</span></span>

<span data-ttu-id="86788-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="86788-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="86788-105">VBScript 是 Microsoft Internet Explorer 隨附的程式設計語言。</span><span class="sxs-lookup"><span data-stu-id="86788-105">VBScript is a programming language included with Microsoft Internet Explorer.</span></span> <span data-ttu-id="86788-106">針對其他瀏覽器，請洽詢您的廠商以取得支援。</span><span class="sxs-lookup"><span data-stu-id="86788-106">For other browsers, contact your vendor about support.</span></span> <span data-ttu-id="86788-107">建議將 VBScript 2.0 (或更新版本的) 用於代理程式。</span><span class="sxs-lookup"><span data-stu-id="86788-107">VBScript 2.0 (or later) is recommended for use with Agent.</span></span> <span data-ttu-id="86788-108">雖然舊版的 VBScript 可能可與 Agent 搭配使用，但卻缺少您可能想要使用的某些功能。</span><span class="sxs-lookup"><span data-stu-id="86788-108">Although earlier versions of VBScript may work with Agent, they lack certain functions that you may want to use.</span></span> <span data-ttu-id="86788-109">您可以從 Microsoft 下載網站和 Microsoft VBScript 網站下載 VBScript 2.0，並取得 VBScript 的進一步資訊。</span><span class="sxs-lookup"><span data-stu-id="86788-109">You can download VBScript 2.0 and obtain further information on VBScript at the Microsoft Downloads site and the Microsoft VBScript site.</span></span>

<span data-ttu-id="86788-110">若要從 VBScript 編寫 Microsoft Agent 的程式，請使用 HTML</span><span class="sxs-lookup"><span data-stu-id="86788-110">To program Microsoft Agent from VBScript, use the HTML</span></span> <SCRIPT> <span data-ttu-id="86788-111">tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:</span><span class="sxs-lookup"><span data-stu-id="86788-111">tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:</span></span>

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

<span data-ttu-id="86788-112">針對 [事件]，包含控制項的名稱，後面接著事件的名稱和任何參數：</span><span class="sxs-lookup"><span data-stu-id="86788-112">For events, include the name of the control followed by the name of the event and any parameters:</span></span>

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

<span data-ttu-id="86788-113">您也可以使用來指定事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="86788-113">You can also specify an event handler using the</span></span> <SCRIPT> <span data-ttu-id="86788-114">tag's **For...Event** syntax:</span><span class="sxs-lookup"><span data-stu-id="86788-114">tag's **For...Event** syntax:</span></span>

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

<span data-ttu-id="86788-115">雖然 Microsoft Internet Explorer 支援這種語法，但並非所有的瀏覽器都支援。</span><span class="sxs-lookup"><span data-stu-id="86788-115">Although Microsoft Internet Explorer supports this latter syntax, not all browsers do.</span></span> <span data-ttu-id="86788-116">為了提供相容性，請只針對事件使用先前的語法。</span><span class="sxs-lookup"><span data-stu-id="86788-116">For compatibility, use only the former syntax for events.</span></span>

<span data-ttu-id="86788-117">使用 VBScript (2.0 或更新版本的) ，您可以嘗試建立物件並檢查是否存在，以確認是否已安裝 Microsoft 代理程式。</span><span class="sxs-lookup"><span data-stu-id="86788-117">With VBScript (2.0 or later), you can verify whether Microsoft Agent is installed by trying to create the object and checking to see if it exists.</span></span> <span data-ttu-id="86788-118">下列範例示範如何在不觸發控制項的自動下載的情況下，檢查代理程式控制項， (當您在頁面) 上包含控制項的標記時，會發生此狀況 <OBJECT> ：</span><span class="sxs-lookup"><span data-stu-id="86788-118">The following sample demonstrates how to check for the Agent control without triggering an auto-download of the control (as would happen if you included an <OBJECT> tag for the control on the page):</span></span>

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

 

 




