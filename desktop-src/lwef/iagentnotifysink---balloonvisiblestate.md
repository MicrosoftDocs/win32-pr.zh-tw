---
title: IAgentNotifySink BalloonVisibleState
description: IAgentNotifySink BalloonVisibleState
ms.assetid: 240e049c-7167-41b7-b092-95ed2a83aad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2dd63d8eef3a7f1a70af81e13506a7e92ad84f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106978566"
---
# <a name="iagentnotifysinkballoonvisiblestate"></a>IAgentNotifySink::BalloonVisibleState

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT BalloonVisibleState(
   long dwCharID,  // character ID
   long bVisible   // visibility flag
);                          
```

當字元的單字氣球的可見度狀態變更時，通知用戶端應用程式。

-   沒有傳回值。

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

文字提示的可見度狀態已變更之字元的識別碼。

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

可見度旗標。 當字元的文字氣球變成可見時，此布林值為 **True** 。如果變成隱藏，則 **為 False** 。

</dd> </dl>

此事件會傳送到字元的所有用戶端。

 

 




