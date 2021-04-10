---
title: IAgentBalloon GetFontSize
description: IAgentBalloon GetFontSize
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14b1a921f1f5c9927f58ab9e561569ba3bc98fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184146"
---
# <a name="iagentballoongetfontsize"></a>IAgentBalloon::GetFontSize

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in word balloon 
```

抓取文字氣球中所顯示字型大小的值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*
</dt> <dd>

接收字型大小之值的位址。

</dd> </dl>

在「Microsoft 代理程式字元編輯器」中定義字元字組氣球中使用的預設字型大小。 您可以使用 [**IAgentBalloon：： SetFontSize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**)來變更它。 不過，使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字型大小設定。

 

 




