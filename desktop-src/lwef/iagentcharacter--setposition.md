---
title: IAgentCharacter SetPosition
description: IAgentCharacter SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e973ec08cdab89c2d8c2501bd9ea1778866f5f7fa1757fe746e44495e41c275a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665638"
---
# <a name="iagentcharactersetposition"></a>IAgentCharacter：： SetPosition

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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


 

 




