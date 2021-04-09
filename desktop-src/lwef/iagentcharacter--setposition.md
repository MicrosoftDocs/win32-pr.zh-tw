---
title: IAgentCharacter SetPosition
description: IAgentCharacter SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee48ea26c714c570f7ae11b9b2dbc0fe92ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021228"
---
# <a name="iagentcharactersetposition"></a>IAgentCharacter：： SetPosition

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

設定字元動畫框架的位置。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*
</dt> <dd>

字元動畫框架左邊緣的螢幕座標（以圖元為單位），相對於螢幕原點 (左上) 。

</dd> <dt>

<span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*
</dt> <dd>

字元動畫框架的上邊緣（以圖元為單位）的螢幕座標，相對於螢幕原點 (左上) 。

</dd> </dl>

這個屬性的設定會套用到字元的所有用戶端。 雖然字元會出現在不規則形狀的區域視窗中，但字元的位置是以其矩形動畫框架為基礎。

> [!Note]  
> 與 [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) 方法不同的是，此函式未排入佇列。

 

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： GetPosition**](iagentcharacter--getposition.md)


 

 




