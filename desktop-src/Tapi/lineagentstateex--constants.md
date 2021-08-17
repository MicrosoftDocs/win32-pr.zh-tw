---
description: LINEAGENTSTATEEX \_ 常數描述某個位址上代理程式的狀態。
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: 'LINEAGENTSTATEEX_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f46c00b337a9106165616fe2eaf86bd2b2634b0c113369558953203313d59f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140091"
---
# <a name="lineagentstateex_-constants"></a>LINEAGENTSTATEEX \_ 常數

**LINEAGENTSTATEEX \_ 常數** 描述某個位址上代理程式的狀態。

<dl> <dt>

<span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX \_ BUSYACD**
</dt> <dd> <dl> <dt>



代理程式正忙於處理從 ACD 佇列路由傳送的呼叫。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX \_ BUSYINCOMING**
</dt> <dd> <dl> <dt>



代理程式正忙於處理未從代理程式登入的 ACD 佇列傳送至代理程式的撥入電話。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX \_ BUSYOUTGOING**
</dt> <dd> <dl> <dt>



代理程式正忙於處理外寄呼叫，例如從預測撥號佇列路由傳送的呼叫。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX \_ NOTREADY**
</dt> <dd> <dl> <dt>



代理程式已登入，但使用的工作不是服務呼叫 (例如在中斷) 上。 不應將其他呼叫路由傳送至代理程式。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX \_ 就緒**
</dt> <dd> <dl> <dt>



代理程式已準備好接受呼叫。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX 已 \_ 發行**
</dt> <dd> <dl> <dt>



代理程式已經發行，可能是因為它們已登出。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX \_ 不明**
</dt> <dd> <dl> <dt>



代理程式狀態目前是未知的，但稍後可能會變成已知。 這可以是第一次開啟行或位址時的過渡狀態。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2。2<br/>                                                      |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




