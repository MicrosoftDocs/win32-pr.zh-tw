---
title: IAgentBalloon GetFontUnderline
description: IAgentBalloon GetFontUnderline
ms.assetid: 19886e94-8095-4650-bd88-34ea9d96ddaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5acf35453209679dc96c85b3017fbe76b19d53b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022035"
---
# <a name="iagentballoongetfontunderline"></a>IAgentBalloon::GetFontUnderline

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

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

 

 




