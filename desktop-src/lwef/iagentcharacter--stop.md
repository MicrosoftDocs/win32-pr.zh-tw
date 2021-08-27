---
title: IAgentCharacter 停止
description: IAgentCharacter 停止
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297f187b7045b1da5773643f2765160c71fbca0d4eb7c6ec12c4032e2f1d5806
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114778"
---
# <a name="iagentcharacterstop"></a>IAgentCharacter：： Stop

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

停止指定的動畫 (要求) ，並將其從字元的動畫佇列中移除。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

要停止的要求識別碼。

</dd> </dl>

**停止** 也可以用來終止任何已排入佇列的 [**準備**](iagentcharacter--prepare.md) 呼叫。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：:P 準備**](iagentcharacter--prepare.md)、 [ **IAgentCharacter：： StopAll**](iagentcharacter--stopall.md)


 

 




