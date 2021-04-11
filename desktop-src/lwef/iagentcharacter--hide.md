---
title: IAgentCharacter 隱藏
description: IAgentCharacter 隱藏
ms.assetid: a8128fe8-9a3b-41a3-bfe3-82ace1baff6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd0ef91eb4d2738f19fb594ac1ab186efaec6e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023399"
---
# <a name="iagentcharacterhide"></a>IAgentCharacter：： Hide

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT Hide(
   long bFast,      // play Hiding state animation flag
   long * pdwReqID  // address of request ID
);
```

隱藏字元。

-   傳回 \_ [確定] 表示作業成功。 當函式傳回時， *pdwReqID* 會包含要求的識別碼。

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*
</dt> <dd>

**隱藏** 狀態動畫旗標。 如果此參數為 **True** **，隱藏的動畫不** 會在隱藏字元框架之前播放;如果 **為 False**，則會播放動畫。

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

接收 **隱藏** 要求識別碼之變數的位址。

</dd> </dl>

伺服器會將與字元佇列中的 **Hide** 方法相關聯的動畫排入佇列。 這可讓您使用它來隱藏其他動畫序列之後的字元。 您可以在呼叫 **Hide** 方法之前，使用 [**Stop**](iagentcharacter--stop.md)方法立即播放動作。

使用 HTTP 通訊協定來存取字元和動畫資料時，請在呼叫這個方法之前，先使用 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 方法來確保 **隱藏** 狀態動畫的可用性。

隱藏字元也可能導致觸發另一個可見字元的 [**IAgentNotifySink：： ActivateInputState**](iagentnotifysink--activateinputstate.md) 事件。

隱藏的字元無法存取音訊通道。 如果您產生動畫要求且隱藏字元，伺服器將會在 [**RequestComplete**](iagentnotifysink--requestcomplete.md) 事件中傳回失敗狀態。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： Show**](iagentcharacter--show.md)


 

 