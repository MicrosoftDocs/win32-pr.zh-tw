---
title: IAgentCharacter GetSize
description: IAgentCharacter GetSize
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af078eb9980399793e00f8bd3deaefef7f048a900423c1ee50ac8d4f4a310b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962228"
---
# <a name="iagentcharactergetsize"></a>IAgentCharacter：： GetSize

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

抓取字元動畫框架的大小。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

接收字元動畫框架寬度的變數位址（以圖元為單位），相對於螢幕原點 (左上) 。

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

接收字元動畫框架高度的變數位址（以圖元為單位），相對於螢幕原點 (左上) 。

</dd> </dl>

雖然字元會出現在不規則形狀的區域視窗中，但字元的位置是以其矩形動畫框架為基礎。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： SetSize**](iagentcharacter--setsize.md)


 

 




