---
title: IAgentBalloon SetFontSize
description: IAgentBalloon SetFontSize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4984382408739e2d093226d04b1c99582a1a25d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311216"
---
# <a name="iagentballoonsetfontsize"></a>IAgentBalloon::SetFontSize

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

設定出現在文字提示字元中的字型大小。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*
</dt> <dd>

字型的大小。

</dd> </dl>

在 [Microsoft 代理程式字元編輯器] 中，會定義字元字提示字元中使用的預設字型大小。 您可以使用 **IAgentBalloon：： SetFontSize** 來變更它。 不過，使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字型大小設定。

## <a name="see-also"></a>另請參閱

[**IAgentBalloon::GetFontSize**](iagentballoon--getfontsize.md)


 

 




