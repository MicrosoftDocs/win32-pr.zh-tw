---
title: IAgentNotifySink RequestStart
description: IAgentNotifySink RequestStart
ms.assetid: acac2bf8-7472-4952-a984-a29654fb8b0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ced12596114214cf712cef8dbbe81edb5af278
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675280"
---
# <a name="iagentnotifysinkrequeststart"></a>IAgentNotifySink::RequestStart

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT RequestStart(
   long dwRequestID  // request ID
);                          
```

在要求開始時通知用戶端應用程式。

-   沒有傳回值。

<dl> <dt>

<span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*
</dt> <dd>

啟動之要求的識別碼。

</dd> </dl>

此事件可讓您追蹤佇列要求開始使用其要求識別碼的時間。

## <a name="see-also"></a>另請參閱

[**IAgentNotifySink：： RequestComplete**](iagentnotifysink--requestcomplete.md)、 [**IAgent：： Load**](iagent--load.md)、 [**IAgentCharacter：： GestureAt**](iagentcharacter--gestureat.md)、 [**IAgentCharacter：： Hide**](iagentcharacter--hide.md)、 [**IAgentCharacter：：中斷**](iagentcharacter--interrupt.md)、 [**IAgentCharacter：： MoveTo**](iagentcharacter--moveto.md)、 [**IAgentCharacter：:P 準備**](iagentcharacter--prepare.md)、 [**IAgentCharacter：:P**](iagentcharacter--play.md)配置、 [**IAgentCharacter：： Show**](iagentcharacter--show.md)、 [**IAgentCharacter：：說話**](iagentcharacter--speak.md)、 [**IAgentCharacter：： Wait**](iagentcharacter--wait.md)


 

 




