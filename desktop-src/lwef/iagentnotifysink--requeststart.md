---
title: IAgentNotifySink RequestStart
description: IAgentNotifySink RequestStart
ms.assetid: acac2bf8-7472-4952-a984-a29654fb8b0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d208e732a2e53d574c74f1a6f0b49aa7550b10343f1ed3b8b7348ed798363c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450478"
---
# <a name="iagentnotifysinkrequeststart"></a>IAgentNotifySink::RequestStart

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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


 

 




