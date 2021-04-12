---
title: IAgentBalloon GetFontStrikethru
description: IAgentBalloon GetFontStrikethru
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2001ec0125949144843d500f125b3502e94723db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372598"
---
# <a name="iagentballoongetfontstrikethru"></a>IAgentBalloon::GetFontStrikethru

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetFontStrikethru(
   long * pbFontStrikethru  // address of variable for strikethrough setting 
);                          // for font displayed in word balloon 
```

指出文字氣球中使用的字型是否已設定刪除線樣式。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*
</dt> <dd>

如果已設定字型刪除線樣式，值的位址會收到 **True** ，否則為 **False** 。

</dd> </dl>

字元字提示字元中使用的字型樣式是在 Microsoft Agent 字元編輯器中定義。 應用程式無法變更它。 不過，使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字型設定。

 

 




