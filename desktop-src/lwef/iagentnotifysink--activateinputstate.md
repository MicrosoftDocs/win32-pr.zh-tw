---
title: IAgentNotifySink ActivateInputState
description: IAgentNotifySink ActivateInputState
ms.assetid: 2476e475-d80c-47e9-bb60-e0fca41becc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437a2d86ae3d79a51bc2adc3b3d32ee719502087c4c723e2c1778103596b97d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749580"
---
# <a name="iagentnotifysinkactivateinputstate"></a>IAgentNotifySink::ActivateInputState

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT ActivateInputState(
   long dwCharID,   // character ID
   long bActivated  // input activation flag
);                          
```

通知用戶端應用程式，字元的輸入作用中狀態已變更。

-   沒有傳回值。

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

已變更其輸入啟用狀態之字元的識別碼。

</dd> <dt>

<span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*
</dt> <dd>

輸入主動旗標。 如果 *dwCharID* 所參考的字元變成使用中，則此布林值為 **True** 。如果字元遺失其輸入的作用中狀態，則 **為 False** 。

</dd> </dl>

 

 




