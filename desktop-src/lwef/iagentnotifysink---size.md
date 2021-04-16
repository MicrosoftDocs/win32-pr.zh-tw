---
title: IAgentNotifySink 大小
description: IAgentNotifySink 大小
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252ad15f6bb5201e8ec000292d1e89efe9368934
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507328"
---
# <a name="iagentnotifysinksize"></a>IAgentNotifySink：： Size

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT Size(
   long dwCharID,  // character ID
   long lWidth,    // new width
   long lHeight,   // new height
);                          
```

當字元已調整大小時，通知用戶端應用程式。

-   沒有傳回值。

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

已調整大小之字元的識別碼。

</dd> <dt>

<span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*
</dt> <dd>

字元動畫框架的寬度（以圖元為單位）。

</dd> <dt>

<span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*
</dt> <dd>

字元動畫框架的高度（以圖元為單位）。

</dd> </dl>

此事件會傳送到字元的所有用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： GetSize**](iagentcharacter--getsize.md)、 [ **IAgentCharacter：： SetSize**](iagentcharacter--setsize.md)


 

 




