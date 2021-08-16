---
title: IAgentCharacter Show
description: IAgentCharacter Show
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcefb523bd2e9f477991bf6fa8352382f75b6bc76d93aab2e7f5c9e8cc1358dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693000"
---
# <a name="iagentcharactershow"></a>IAgentCharacter：： Show

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

顯示字元。

-   傳回 \_ [確定] 表示作業成功。 當函式傳回時， *pdwReqID* 會包含要求的識別碼。

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*
</dt> <dd>

顯示狀態動畫旗標。 如果此參數為 **True**， **顯示** 狀態動畫會在讓字元變成可見之後播放;如果 **為 False**，則不播放動畫。

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

接收 [**顯示**](/windows/desktop/lwef/iagentcharacter--show) 要求識別碼之變數的位址。

</dd> </dl>

避免將 *bFast* 參數設定為 **True** ，而不事先播放動畫，否則可能會顯示字元框架，但沒有可顯示的影像。 尤其要注意的是，如果您在字元未顯示時呼叫 [**MoveTo**](iagentcharacter--moveto.md) ，則不會播放任何動畫。 因此，如果您呼叫 *bFast* 設為 **True** 的 **Show** 方法，則不會顯示任何影像。 同樣地，如果您呼叫 [[**隱藏**](/windows/desktop/lwef/iagentcharacter--hide)]，並將 [ *bFast* ] 設定為 [ **True**]，就不會 **顯示** 影像。

使用 HTTP 通訊協定來存取字元和動畫資料時，請使用 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 方法，以確保在呼叫這個方法之前， **顯示** 狀態動畫的可用性。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： Hide**](iagentcharacter--hide.md)


 

 