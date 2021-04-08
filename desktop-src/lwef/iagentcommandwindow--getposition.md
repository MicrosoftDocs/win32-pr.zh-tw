---
title: IAgentCommandWindow GetPosition
description: IAgentCommandWindow GetPosition
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8c036d02c210ecb26da5dfde207bfe56afe8a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932300"
---
# <a name="iagentcommandwindowgetposition"></a>IAgentCommandWindow：： GetPosition

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

抓取語音命令視窗的位置。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

變數的位址，此變數會接收 [語音命令] 視窗左邊緣的螢幕座標（單位為圖元），相對於螢幕原點 (左上) 。

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

以圖元為單位的變數位址，此變數會接收 [語音命令] 視窗上邊緣的螢幕座標（以圖元為單位），相對於螢幕原點 (左上角) 。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCommandWindow：： GetSize**](iagentcommandwindow--getsize.md)


 

 




