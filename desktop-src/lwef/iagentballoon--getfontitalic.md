---
title: IAgentBalloon GetFontItalic
description: IAgentBalloon GetFontItalic
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c1a0e1e649e325e84d4a78eee087e102e8d1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969043"
---
# <a name="iagentballoongetfontitalic"></a>IAgentBalloon::GetFontItalic

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

指出文字氣球中使用的字型是否為斜體。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*
</dt> <dd>

值的位址，如果字型為斜體，則為 **True** ，如果不是斜體，則為 **False** 。

</dd> </dl>

字元字提示字元中使用的字型樣式是在 Microsoft Agent 字元編輯器中定義。 應用程式無法變更它。 不過，使用者可以透過 Microsoft Agent 屬性工作表覆寫所有字元的字型設定。

 

 




