---
title: IAgentCharacter Play
description: IAgentCharacter Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320572322d7a28b52693c80eb918ebf78fcb50083e012e35c65df3a7bffdf0a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976398"
---
# <a name="iagentcharacterplay"></a>IAgentCharacter：:P 的版面配置

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

播放指定的動畫。

-   傳回 \_ [確定] 表示作業成功。 當函式傳回時， *pdwReqID* 會包含要求的識別碼。

<dl> <dt>

<span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*
</dt> <dd>

動畫的名稱。

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

接收 **IAgentCharacter：:P** 配置要求識別碼之變數的位址。

</dd> </dl>

使用 Microsoft Agent 字元編輯器來編譯字元時，會定義動畫的名稱。 在播放指定的動畫之前，伺服器會嘗試播放先前 **動畫的傳回動畫 (** 如果已指派) 的話）。

當字元的動畫資料儲存在使用者的本機電腦上時，您可以使用 **IAgentCharacter：:P** 配置方法，並指定動畫的名稱。 使用 HTTP 通訊協定來存取動畫資料時，請在呼叫這個方法之前，先使用 [**Prepare**](iagentcharacter--prepare.md) 方法來確保動畫的可用性。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：:P 準備**](iagentcharacter--prepare.md)


 

 




