---
title: IAgentUserInput GetItemText
description: IAgentUserInput GetItemText
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd9c1392bd56e3bb59212edeb79d862260786edb87583c0e8fdf049e8345b40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359038"
---
# <a name="iagentuserinputgetitemtext"></a>IAgentUserInput：： GetItemText

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

抓取傳遞給 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代聲音文字。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

傳遞至 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代索引。

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

接收 [**命令**](command-event.md)的語音文字值之 BSTR 的位址。

</dd> </dl>

如果語音輸入不是命令的來源，例如，如果使用者從字元的快顯功能表中選取了命令，伺服器就會針對 [**命令**](command-event.md)的語音文字傳回 **Null** 。

## <a name="see-also"></a>另請參閱

[**IAgentUserInput：： GetItemConfidence**](iagentuserinput--getitemconfidence.md)、 [**IAgentUserInput：： GetItemID**](iagentuserinput--getitemid.md)、 [**IAgentUserInput：： GetAllItemData**](iagentuserinput--getallitemdata.md)


 

 




