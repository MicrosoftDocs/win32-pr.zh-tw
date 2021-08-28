---
title: IAgentBalloon GetFontName
description: IAgentBalloon GetFontName
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cb0bceae040f9261d2530b19d074df937dbdaf80d91a27f57b5cf9c1fd8f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725314"
---
# <a name="iagentballoongetfontname"></a>IAgentBalloon::GetFontName

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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

 

 




