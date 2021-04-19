---
title: 使用系統監視器
description: 系統監視器 (SYSMON) 可以包含在任何支援 ActiveX \ 174 的應用程式中;控制。 例如，您可以在 Microsoft Visual Basic 應用程式或 HTML 檔案中包含 SYSMON。
ms.assetid: 36931aae-b608-42d9-a3e3-09784e80f386
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd636c8b984f7c891c2222b4674dd8d0d7e747d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969047"
---
# <a name="using-system-monitor"></a><span data-ttu-id="db957-104">使用系統監視器</span><span class="sxs-lookup"><span data-stu-id="db957-104">Using System Monitor</span></span>

<span data-ttu-id="db957-105">系統監視器 (SYSMON) 可包含在支援 ActiveX®控制項的任何應用程式中。</span><span class="sxs-lookup"><span data-stu-id="db957-105">System Monitor (SYSMON) can be included in any application that supports ActiveX® controls.</span></span> <span data-ttu-id="db957-106">例如，您可以在 Microsoft Visual Basic 應用程式或 HTML 檔案中包含 SYSMON。</span><span class="sxs-lookup"><span data-stu-id="db957-106">For example, you can include SYSMON in a Microsoft Visual Basic application or in an HTML document.</span></span>

<span data-ttu-id="db957-107">下列範例顯示如何在 HTML 檔案中包含 SYSMON。</span><span class="sxs-lookup"><span data-stu-id="db957-107">The following example shows how to include SYSMON in an HTML document.</span></span> <span data-ttu-id="db957-108">此範例會使用 VBScript 來新增計數器，其值是從本機電腦抓取、修改一些控制監視顯示方式的 SYSMON 屬性，以及處理 OnCounterAdd 事件。</span><span class="sxs-lookup"><span data-stu-id="db957-108">The example uses VBScript to add counters whose values are retrieved from the local computer, modifies some of the SYSMON properties that control how the monitor is displayed, and processes the OnCounterAdd event.</span></span> <span data-ttu-id="db957-109">此範例會使用萬用字元 (\*) 加入進程計數器的所有實例。</span><span class="sxs-lookup"><span data-stu-id="db957-109">The example uses the wildcard character (\*) to add all instances of the process counter.</span></span>

``` syntax
<HTML>
<BODY BGCOLOR=#C0C0C0>

<SCRIPT LANGUAGE="VBScript">
  Sub Monitor_OnCounterAdded(index)
    Monitor.Counters.Item(1).Width = 8
  End Sub
</Script>
<OBJECT
  CLASSID="clsid:C4D2D8E0-D1DD-11CE-940F-008029004347"
  ID="Monitor"
  HEIGHT=80%
  WIDTH=100%>
</OBJECT>

<SCRIPT LANGUAGE="VBScript">
  Sub Window_OnLoad
    On Error Resume Next
    Monitor.ShowValueBar = False
    Monitor.ShowHorizontalGrid = True
    Monitor.Counters.Add("\Process(*)\% Processor Time")
    Monitor.DisplayType=sysmonLineGraph
    Monitor.GraphTitle="System Performance Overview"
  End Sub
</SCRIPT>

</BODY>
</HTML>
```

 

 




