---
title: IAgentNotifySink 閒置
description: IAgentNotifySink 閒置
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8263bd9bc62d4fccfad74b18b189c6e4bae426245dd3d4d6a46c826ebacf498d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105168"
---
# <a name="iagentnotifysinkidle"></a>IAgentNotifySink：：閒置

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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


 

 




