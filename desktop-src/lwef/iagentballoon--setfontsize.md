---
title: IAgentBalloon SetFontSize
description: IAgentBalloon SetFontSize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6e19d79429ddf98f67a281cd11aefb1dc6bc2e54b1289e36c7cfb5a62bd538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976468"
---
# <a name="iagentballoonsetfontsize"></a>IAgentBalloon::SetFontSize

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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


 

 




