---
title: IAgentBalloon GetFontSize
description: IAgentBalloon GetFontSize
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc392bd12fccfb01b8aee41a5a06ed50b388ac8223e622d75218c840f706c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962488"
---
# <a name="iagentballoongetfontsize"></a>IAgentBalloon::GetFontSize

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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

 

 




