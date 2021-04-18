---
title: IAgentCharacter 等候
description: IAgentCharacter 等候
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54ac2de03c78c220803a774537230938a00a776
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301584"
---
# <a name="iagentcharacterwait"></a>IAgentCharacter：： Wait

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

在指定的動畫上保存字元的動畫佇列 (要求) ，直到另一個字元的另一個要求完成為止。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

要等候的要求識別碼。

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

接收 **等候** 要求識別碼之變數的位址。

</dd> </dl>

只有當您支援多 (同時) 個字元，而且想要排列其互動時，才使用這個方法。 針對單一字元 (，每個動畫要求都會依序播放--在先前的要求完成之後 ) 。如果您有兩個字元，而且想要讓一個字元的動畫要求等到另一個字元的動畫完成，請將 **wait** 方法設定為其他字元的動畫要求識別碼。

 

 




