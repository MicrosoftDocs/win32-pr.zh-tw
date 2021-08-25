---
title: IAgentCharacter MoveTo
description: IAgentCharacter MoveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ea5a0e288e4b7d9782f1b463fdbcccf01b0da9314894be1a60c556392e25e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848538"
---
# <a name="iagentcharactermoveto"></a>IAgentCharacter：： MoveTo

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

播放相關聯的 **移動** 狀態動畫，並將字元框架移至指定的位置。

-   傳回 \_ [確定] 表示作業成功。 當函式傳回時，這個變數會包含要求的識別碼。

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

相對於螢幕原點的新位置 x 座標（以圖元為單位）， (左上) 。 字元的位置是根據其動畫框架的左上角。

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

新位置的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。 字元的位置是根據其動畫框架的左上角。

</dd> <dt>

<span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*
</dt> <dd>

參數，以毫秒為單位，指定字元的畫面格移動速度。 建議值為1000。 指定零 (0) 移動框架，而不播放動畫。

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

接收 [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) 要求識別碼之變數的位址。

</dd> </dl>

使用 HTTP 通訊協定來存取字元和動畫資料時，請使用 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 方法，以確保在呼叫這個方法之前， **移動** 狀態動畫的可用性。 即使未載入動畫，伺服器還是會移動框架。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： SetPosition**](iagentcharacter--setposition.md)


 

 