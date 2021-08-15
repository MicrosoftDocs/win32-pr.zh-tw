---
title: IAgentNotifySink RequestComplete
description: IAgentNotifySink RequestComplete
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c797232ca968261c5857bec8953c6c76375bafc849b17ebe21bc8f353698f02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976168"
---
# <a name="iagentnotifysinkrequestcomplete"></a>IAgentNotifySink::RequestComplete

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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


 

 




