---
title: IAgentCharacter 等候
description: IAgentCharacter 等候
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fba3f292b9dc7a0651cf3a1a27adcfe0ea808127d8ce00ae62cb1e84cc126a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014217"
---
# <a name="iagentcharacterwait"></a>IAgentCharacter：： Wait

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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

 

 




