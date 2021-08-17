---
title: IAgentCharacter 中斷
description: IAgentCharacter 中斷
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ea2529d4da78607d3ad22bf688857c8917e3317df17ae9a5eb99d0b184878e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750903"
---
# <a name="iagentcharacterinterrupt"></a>IAgentCharacter：：中斷

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

中斷指定的動畫 (要求另一個字元) 。

-   傳回 \_ [確定] 表示作業成功。 當函式傳回時， *pdwReqID* 會包含要求的識別碼。

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

要中斷之要求的識別碼。

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

接收 **中斷** 要求識別碼之變數的位址。

</dd> </dl>

如果您載入多個字元，您可以使用這個方法來同步處理字元之間的動畫。 例如，如果有另一個字元在迴圈動畫中，此方法將會停止迴圈動畫，並啟動字元佇列中的下一個動畫。

**中斷** 會中止現有的動畫，但不會排清字元的動畫佇列。 它會啟動字元佇列中的下一個動畫。 若要停止並清除字元的佇列，請使用 [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) 方法。

您無法使用這個方法來讓字元中斷本身，因為 Microsoft 代理程式伺服器會將 **中斷** 方法排入字元的動畫佇列中。 因此，您只能使用插 **斷來停止** 已載入之另一個字元的動畫。

 

 