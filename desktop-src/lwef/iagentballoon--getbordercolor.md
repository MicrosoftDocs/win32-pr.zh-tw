---
title: IAgentBalloon GetBorderColor
description: IAgentBalloon GetBorderColor
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f78bf9425cbb12c6a87f3ad64b6c5523dc7bbd8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674231"
---
# <a name="iagentballoongetbordercolor"></a>IAgentBalloon::GetBorderColor

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetBorderColor (
  long * plBorderColor// address of variable for border color displayed
);                    // for word balloon
```

抓取針對文字氣球顯示之框線色彩的值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*
</dt> <dd>

接收氣球框線色彩設定之變數的位址。

</dd> </dl>

字元文字氣球的框線色彩是在 Microsoft Agent 字元編輯器中定義。 應用程式無法變更它。 不過，使用者可以透過 Microsoft Agent 屬性工作表變更所有字元之文字批註的框線色彩。

## <a name="see-also"></a>另請參閱

[**IAgentBalloon：： GetBackColor**](iagentballoon--getbackcolor.md)、 [ **IAgentBalloon：： GetForeColor**](iagentballoon--getforecolor.md)


 

 




