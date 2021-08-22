---
title: IAgentCommandWindow GetVisible
description: IAgentCommandWindow GetVisible
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 949591bc22c93711af19ce18cb024ede9714335f249839eb4819a73e231e0d83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976238"
---
# <a name="iagentcommandwindowgetvisible"></a>IAgentCommandWindow：： GetVisible

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for Visible setting for 
);                   // Voice Commands Window
```

決定是否顯示或隱藏 [語音命令] 視窗。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

如果 [語音命令] 視窗是可見的，則為收到 **True** 的變數位址; 如果隱藏，則為 **False** 。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCommandWindow::SetVisible**](iagentcommandwindow--setvisible.md)


 

 




