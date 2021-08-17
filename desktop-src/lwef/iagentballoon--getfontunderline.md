---
title: IAgentBalloon GetFontUnderline
description: IAgentBalloon GetFontUnderline
ms.assetid: 19886e94-8095-4650-bd88-34ea9d96ddaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325f383aa76c55068ca7244b4ce0f822602651fa196ee336060fcc21fe3ab068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962358"
---
# <a name="iagentballoongetfontunderline"></a>IAgentBalloon::GetFontUnderline

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetFontUnderline(
   long * pbFontUnderline  // address of variable for underline setting
);                         // for font displayed in word balloon 
```

指出文字氣球中使用的字型是否已設定底線樣式。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbFontUnderline*
</dt> <dd>

如果設定字型底線樣式，則為值的位址，如果不是 **，則為** **False** 。

</dd> </dl>

字元字提示字元中使用的字型樣式是在 Microsoft Agent 字元編輯器中定義。 應用程式無法變更它。 不過，使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字型設定。

 

 




