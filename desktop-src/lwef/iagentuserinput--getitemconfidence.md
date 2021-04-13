---
title: IAgentUserInput GetItemConfidence
description: IAgentUserInput GetItemConfidence
ms.assetid: 7d1ca2f0-416c-43c3-99a8-9f287cb88de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846e1fca9ea1245a62fc68330d68263b63fb7cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104299979"
---
# <a name="iagentuserinputgetitemconfidence"></a>IAgentUserInput::GetItemConfidence

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetItemConfidence(
   long dwItemIndex,    // index of Command alternative
   long * plConfidence  // address of confidence value for Command 
);
```

抓取傳遞給 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼之 [**命令**](command-event.md)的信賴值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

傳遞至 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代索引。

</dd> <dt>

<span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*
</dt> <dd>

接收傳給 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代項信賴分數的變數位址。

</dd> </dl>

如果語音輸入不是命令的來源，例如，如果使用者從字元的快顯功能表中選取了命令，Microsoft 代理程式伺服器會將最佳相符專案的信賴值傳回為100，並將所有其他替代專案的信賴值傳回為零 (0) 。

## <a name="see-also"></a>另請參閱

[**IAgentUserInput：： GetItemID**](iagentuserinput--getitemid.md)、 [**IAgentUserInput：： GetAllItemData**](iagentuserinput--getallitemdata.md)、 [**IAgentUserInput：： GetItemText**](iagentuserinput--getitemtext.md)


 

 




