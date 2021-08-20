---
title: IAgentNotifySink 大小
description: IAgentNotifySink 大小
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 430dc26dc4f7bb8f5c5e68fe5e9898d62f16b3480b8d8969726e8c2bec02da74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692614"
---
# <a name="iagentnotifysinksize"></a>IAgentNotifySink：： Size

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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


 

 




