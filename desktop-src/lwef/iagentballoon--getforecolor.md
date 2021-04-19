---
title: IAgentBalloon GetForeColor
description: IAgentBalloon GetForeColor
ms.assetid: b06ad924-66b6-42a6-8c97-5bc4c46f6e2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7a251471b0281661b087dbfb9b141c54ff9dc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968255"
---
# <a name="iagentballoongetforecolor"></a>IAgentBalloon::GetForeColor

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetForeColor(
   long * plFGColor // address of variable for foreground color displayed
);                  // in word balloon
```

抓取文字氣球中顯示之前景色彩的值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*
</dt> <dd>

接收氣球前景色彩設定之變數的位址。

</dd> </dl>

在「Microsoft 代理程式字元編輯器」中定義字元字提示字元中使用的前景色彩。 應用程式無法變更它。 不過，使用者可以透過 Microsoft Agent 屬性工作表覆寫所有字元之文字批註的前景色彩。

## <a name="see-also"></a>另請參閱

[**IAgentBalloon::GetBackColor**](iagentballoon--getbackcolor.md)


 

 




