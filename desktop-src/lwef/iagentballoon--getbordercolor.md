---
title: IAgentBalloon GetBorderColor
description: IAgentBalloon GetBorderColor
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ed636d5209402959adbb2a777577a87c8cc23f8eed4faeb8ac003981e5e2d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478632"
---
# <a name="iagentballoongetbordercolor"></a>IAgentBalloon::GetBorderColor

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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


 

 




