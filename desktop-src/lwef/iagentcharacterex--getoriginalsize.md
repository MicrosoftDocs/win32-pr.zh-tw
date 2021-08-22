---
title: IAgentCharacterEx GetOriginalSize
description: IAgentCharacterEx GetOriginalSize
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55abb64a8466b13ee41119e2a8a359ceeb182c92f7b4d2b1071547df07110052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750516"
---
# <a name="iagentcharacterexgetoriginalsize"></a>IAgentCharacterEx::GetOriginalSize

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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


 

 




