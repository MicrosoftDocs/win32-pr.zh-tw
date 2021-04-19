---
title: IAgentCommandWindow GetVisible
description: IAgentCommandWindow GetVisible
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66c6d7bf2ee59512f478fd8daa7cee882515690
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106996147"
---
# <a name="iagentcommandwindowgetvisible"></a>IAgentCommandWindow：： GetVisible

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

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


 

 




