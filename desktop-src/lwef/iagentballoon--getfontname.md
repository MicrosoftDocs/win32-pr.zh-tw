---
title: IAgentBalloon GetFontName
description: IAgentBalloon GetFontName
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f29ad981fb4b10249b17e55c92fb286552eedc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372600"
---
# <a name="iagentballoongetfontname"></a>IAgentBalloon::GetFontName

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

抓取文字氣球中所顯示字型的值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*
</dt> <dd>

接收文字氣球中所顯示字型名稱的 BSTR 位址。

</dd> </dl>

在「Microsoft 代理程式字元編輯器」中定義字元字提示字元中使用的預設字型。 您可以使用 [**IAgentBalloon：： SetFontName**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**)來變更它。 使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字型設定。

 

 




