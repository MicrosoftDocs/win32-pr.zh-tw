---
title: IAgentNotifySink 命令
description: IAgentNotifySink 命令
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d9c20de96c1bb14cf003ad7beff98e716e272ad3de39532d9b455e279d97af3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105199"
---
# <a name="iagentnotifysinkcommand"></a>IAgentNotifySink：： Command

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

通知用戶端應用程式已選取使用者的 [**命令**](/windows/desktop/lwef/the-command-object) 。

-   沒有傳回值。

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

最符合命令替代選項的識別碼。

</dd> <dt>

<span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*
</dt> <dd>

[**IAgentUserInput**](iagentuserinput.md)物件的 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面位址。

</dd> </dl>

使用 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 取出 [**IAgentUserInput**](iagentuserinput.md) 介面。

當使用者以語音選擇命令或從字元的快顯功能表中選取命令時，伺服器會通知輸入-主動用戶端。 即使使用者選取其中一個伺服器的命令，也會發生此事件。 在此情況下，伺服器會傳回 null 命令識別碼、信賴分數，以及該專案的語音引擎所傳回的語音文字。

## <a name="see-also"></a>另請參閱

[**IAgentUserInput**](iagentuserinput.md)


 

 