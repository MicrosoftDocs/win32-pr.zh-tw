---
title: IAgentCharacterEx GetOriginalSize
description: IAgentCharacterEx GetOriginalSize
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e1712587e70d9756e3d37ca9e0f3cbfdb82c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021264"
---
# <a name="iagentcharacterexgetoriginalsize"></a>IAgentCharacterEx::GetOriginalSize

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetOriginalSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

抓取字元動畫框架的原始大小。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

接收字元動畫框架原始寬度的變數位址（以圖元為單位）。

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

接收字元動畫框架原始高度的變數位址（以圖元為單位）。

</dd> </dl>

此呼叫會傳回內建于 Microsoft Agent 字元編輯器中之字元框架的原始大小。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： GetSize**](iagentcharacter--getsize.md)


 

 




