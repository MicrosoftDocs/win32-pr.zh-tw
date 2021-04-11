---
title: IAgentBalloon SetFontName
description: IAgentBalloon SetFontName
ms.assetid: 6babf5f6-2abd-46c2-ade0-899a8e4488bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f983064c5df8cde8322658bbd0c713bbf238ecf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022033"
---
# <a name="iagentballoonsetfontname"></a>IAgentBalloon::SetFontName

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font displayed in word balloon
);
                   
```

設定出現在文字提示字元中的字型。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*
</dt> <dd>

設定文字氣球中所顯示字型的 BSTR。

</dd> </dl>

字元的文字氣球中使用的預設字型是在 Microsoft Agent 字元編輯器中定義。 您可以使用 **IAgentBalloon：： SetFontName** 來變更它。 不過，使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字型設定。

## <a name="see-also"></a>另請參閱

[**IAgentBalloon：： GetVisible**](iagentballoon--getvisible.md)


 

 




