---
title: IAgentNotifySink RequestComplete
description: IAgentNotifySink RequestComplete
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265a7111369dec687fd74b9c66c27275a40e164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301879"
---
# <a name="iagentnotifysinkrequestcomplete"></a>IAgentNotifySink::RequestComplete

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT RequestComplete(
   long dwRequestID,  // request ID
   long hrStatus      // status code
);                          
```

當要求完成時，通知用戶端應用程式。

-   沒有傳回值。

<dl> <dt>

<span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*
</dt> <dd>

啟動之要求的識別碼。

</dd> <dt>

<span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*
</dt> <dd>

狀態碼。 此參數會傳回要求的狀態碼。

</dd> </dl>

此事件可讓您使用其要求識別碼來追蹤佇列方法完成的時間。

## <a name="see-also"></a>另請參閱

[**IAgentNotifySink：： RequestStart**](iagentnotifysink--requeststart.md)、 [**IAgent：： Load**](iagent--load.md)、 [**IAgentCharacter：： GestureAt**](iagentcharacter--gestureat.md)、 [**IAgentCharacter：： Hide**](iagentcharacter--hide.md)、 [**IAgentCharacter：：中斷**](iagentcharacter--interrupt.md)、 [**IAgentCharacter：： MoveTo**](iagentcharacter--moveto.md)、 [**IAgentCharacter：:P 準備**](iagentcharacter--prepare.md)、 [**IAgentCharacter：:P**](iagentcharacter--play.md)配置、 [**IAgentCharacter：： Show**](iagentcharacter--show.md)、 [**IAgentCharacter：：說話**](iagentcharacter--speak.md)、 [**IAgentCharacter：： Wait**](iagentcharacter--wait.md)


 

 




