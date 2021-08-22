---
title: IAgentUserInput GetItemID
description: IAgentUserInput GetItemID
ms.assetid: 3afd4d9d-51bb-4086-bf7b-7c9a2ddcd807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde65fc10a4cb467bd69f200e3244f1a2a73c0424d64f6a4babbd2cefd18e0be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609258"
---
# <a name="iagentuserinputgetitemid"></a>IAgentUserInput::GetItemID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetItemID(
   long dwItemIndex,    // index of Command alternative
   long * pdwCommandID  // address of a variable for number of alternatives 
);
```

抓取傳遞給 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代識別碼。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

傳遞至 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代索引。

</dd> <dt>

<span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwCommandID*
</dt> <dd>

接收 [**命令**](command-event.md)識別碼之變數的位址。

</dd> </dl>

如果語音輸入觸發 [**IAgentNotifySink：： Command**](iagentnotifysink--command.md) 回呼，伺服器會傳回您應用程式所定義之任何相符 [**命令**](command-event.md) 的識別碼。

## <a name="see-also"></a>另請參閱

[**IAgentUserInput：： GetItemConfidence**](iagentuserinput--getitemconfidence.md)、 [**IAgentUserInput：： GetItemText**](iagentuserinput--getitemtext.md)、 [**IAgentUserInput：： GetAllItemData**](iagentuserinput--getallitemdata.md)


 

 




