---
title: IAgentBalloon GetBackColor
description: IAgentBalloon GetBackColor
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c58a913332d01f2982c28003c146420d34a86e96f3c833f667c968bd22ef19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888418"
---
# <a name="iagentballoongetbackcolor"></a>IAgentBalloon::GetBackColor

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

抓取文字氣球中顯示之背景色彩的值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*
</dt> <dd>

接收球標背景之色彩設定的變數位址。

</dd> </dl>

在「Microsoft 代理程式字元編輯器」中定義字元字提示字元中所使用的背景色彩。 應用程式無法變更它。 不過，使用者可以透過 Microsoft Agent 屬性工作表變更所有字元的文字球的背景色彩。

## <a name="see-also"></a>另請參閱

[**IAgentBalloon::GetForeColor**](iagentballoon--getforecolor.md)


 

 




