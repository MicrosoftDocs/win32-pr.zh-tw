---
title: IAgentUserInput GetAllItemData
description: IAgentUserInput GetAllItemData
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d74c59e05e021fdff05ee8991c4563a7a4be918f6ecb244c26402b5234b240b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105144"
---
# <a name="iagentuserinputgetallitemdata"></a>IAgentUserInput::GetAllItemData

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

抓取所有傳遞給 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代專案的資料。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*
</dt> <dd>

接收傳遞給 [**IAgentNotifySink：： Command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)識別碼之變數的位址。

</dd> <dt>

<span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*
</dt> <dd>

變數的位址，此變數會接收傳遞給 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代專案的信賴分數。

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

變數的位址，此變數會接收傳遞給 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代專案的語音文字。

</dd> </dl>

如果語音輸入觸發 [**IAgentNotifySink：：命令**](iagentnotifysink--command.md)，伺服器會傳回最符合的最相符、第二個最符合項，以及第三個相符項（如果這些是由語音引擎提供的話）。 它會在-100 到100的範圍中提供相對的信賴分數，並提供語音引擎的實際文字「赫德」。 如果最符合的是伺服器提供的命令，則伺服器會傳送 Null 識別碼，但仍會傳送信賴分數和 [**語音**](voice-property.md) 文字。

如果語音輸入不是事件的來源，例如，如果使用者從字元的快顯功能表中選取了命令，Microsoft 代理程式伺服器會傳回所選 [**命令**](command-event.md) 的識別碼，並將100和語音文字的信賴分數設定為 Null。 其他替代方案則會傳回 Null，且信賴分數為零 (0) ，而語音文字為 Null。

> [!Note]  
> 並非所有的語音辨識引擎都可能會傳回此事件所有參數的所有值。 請洽詢您的引擎廠商，判斷引擎是否支援 Microsoft 語音 API 介面，以傳回替代專案和信賴分數。

 

## <a name="see-also"></a>另請參閱

[**IAgentUserInput：： GetItemConfidence**](iagentuserinput--getitemconfidence.md)、 [**IAgentUserInput：： GetItemText**](iagentuserinput--getitemtext.md)、 [**IAgentUserInput：： GetItemID**](iagentuserinput--getitemid.md)


 

 




