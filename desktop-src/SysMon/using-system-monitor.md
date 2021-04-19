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
# <a name="using-system-monitor"></a>使用系統監視器

系統監視器 (SYSMON) 可包含在支援 ActiveX®控制項的任何應用程式中。 例如，您可以在 Microsoft Visual Basic 應用程式或 HTML 檔案中包含 SYSMON。

下列範例顯示如何在 HTML 檔案中包含 SYSMON。 此範例會使用 VBScript 來新增計數器，其值是從本機電腦抓取、修改一些控制監視顯示方式的 SYSMON 屬性，以及處理 OnCounterAdd 事件。 此範例會使用萬用字元 (\*) 加入進程計數器的所有實例。

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

 

 




