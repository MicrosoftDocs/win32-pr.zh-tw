---
title: IAgentCommandWindow GetSize
description: IAgentCommandWindow GetSize
ms.assetid: 24ad3b48-6557-4790-b9c4-2cf7df92fa7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 200853d88f4f4ea70fce0f80d73f343a2a4d46935a2dfca0ebf78021b0b884ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961578"
---
# <a name="iagentcommandwindowgetsize"></a>IAgentCommandWindow：： GetSize

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for Voice Commands Window width
   long * plHeight  // address of variable for Voice Commands Window height
);
```

抓取語音命令視窗的目前大小。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

以圖元為單位的變數位址，以圖元為單位來接收語音命令視窗的寬度， (左上) 。

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

以圖元為單位的變數位址，此變數會以圖元為單位來接收語音命令視窗的高度（相對於螢幕原點 (左上) ）。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCommandWindow：： GetPosition**](iagentcommandwindow--getposition.md)


 

 




