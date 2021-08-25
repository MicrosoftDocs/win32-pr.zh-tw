---
title: IAgentCharacter SetSize
description: IAgentCharacter SetSize
ms.assetid: 8324ab84-2b59-4459-b375-700d72b621bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089226f98969594a1d19afc7f3bb529c30943e06ec4083364dc5ae2f9850c9c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848518"
---
# <a name="iagentcharactersetsize"></a>IAgentCharacter：： SetSize

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetSize(
   long * lWidth,  // width of the character frame
   long * lHeight  // height of the character frame
);
```

設定字元的動畫框架大小。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*
</dt> <dd>

字元動畫框架的寬度（以圖元為單位）。

</dd> <dt>

<span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*
</dt> <dd>

字元動畫框架的高度（以圖元為單位）。

</dd> </dl>

變更字元的框架大小會將字元調整為使用這個方法所設定的大小。 這個屬性的設定會套用到字元的所有用戶端。

雖然字元會出現在不規則形狀的區域視窗中，但字元的位置是以其矩形動畫框架為基礎。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： GetSize**](iagentcharacter--getsize.md)


 

 




