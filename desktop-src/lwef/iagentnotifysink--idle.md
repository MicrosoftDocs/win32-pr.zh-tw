---
title: IAgentNotifySink 閒置
description: IAgentNotifySink 閒置
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43e060f361499b02bc0a83db697938975c76291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968663"
---
# <a name="iagentnotifysinkidle"></a>IAgentNotifySink：：閒置

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

當字元的 **閒置** 狀態變更時，通知用戶端應用程式。

-   沒有傳回值。

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

啟動之要求的識別碼。

</dd> <dt>

<span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*
</dt> <dd>

開始旗標。 當字元開始閒置時，這個布林值是 **True** ，而當字元停止閒置時，則為 **False** 。

</dd> </dl>

此事件可讓您追蹤 Microsoft 代理程式伺服器啟動或停止閒置處理某個字元的時間。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： GetIdleOn**](iagentcharacter--getidleon.md)、 [ **IAgentCharacter：： SetIdleOn**](iagentcharacter--setidleon.md)


 

 




