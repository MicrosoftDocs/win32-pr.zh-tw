---
title: IAgentBalloon GetFontStrikethru
description: IAgentBalloon GetFontStrikethru
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b15bfbc120f7c8d614839f55ec985a3bdbdb3f840e5a07d615f7de0dfc75e22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751022"
---
# <a name="iagentballoongetfontstrikethru"></a>IAgentBalloon::GetFontStrikethru

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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

 

 




