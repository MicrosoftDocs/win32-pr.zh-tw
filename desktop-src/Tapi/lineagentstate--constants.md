---
description: LINEAGENTSTATE \_ 常數描述某個位址上代理程式的狀態。
ms.assetid: 1dbc33e7-05cc-4cb9-8904-f495b884b8db
title: 'LINEAGENTSTATE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b5afa8f93cfde5529f8f57fd8e48d37ecd415b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984864"
---
# <a name="lineagentstate_-constants"></a>LINEAGENTSTATE \_ 常數

**LINEAGENTSTATE \_ 常數** 描述某個位址上代理程式的狀態。

<dl> <dt>

<span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE \_ BUSYACD**
</dt> <dd> <dl> <dt>



代理程式正忙於處理從 ACD 佇列路由傳送的呼叫。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE \_ BUSYINCOMING**
</dt> <dd> <dl> <dt>



代理程式正忙於處理未從代理程式登入的 ACD 佇列傳送至代理程式的撥入電話。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE \_ BUSYOTHER**
</dt> <dd> <dl> <dt>



代理程式正忙於處理另一種類型的呼叫，例如，預測撥號程式未傳送給代理程式的外寄個人呼叫。 當已知代理程式在呼叫上忙碌，但呼叫的類型未知時，也可以使用此值。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE \_ BUSYOUTBOUND**
</dt> <dd> <dl> <dt>



代理程式正忙於處理外寄呼叫，例如從預測撥號佇列路由傳送的呼叫。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE \_ LOGGEDOFF**
</dt> <dd> <dl> <dt>



位址上未登入任何代理程式。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE \_ NOTREADY**
</dt> <dd> <dl> <dt>



代理程式已登入，但使用的工作不是服務呼叫 (例如在中斷) 上。 不應將其他呼叫路由傳送至代理程式。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE \_ 就緒**
</dt> <dd> <dl> <dt>



代理程式已準備好接受呼叫。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE \_ UNAVAIL**
</dt> <dd> <dl> <dt>



代理程式狀態未知，而且永遠不會變成已知。 在 [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)中，這個條件也可以由設定為0的 **dwAgentState** 成員表示。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE \_ 不明**
</dt> <dd> <dl> <dt>



代理程式狀態目前是未知的，但稍後可能會變成已知。 這可以是第一次開啟行或位址時的過渡狀態。


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE \_ WORKINGAFTERCALL**
</dt> <dd> <dl> <dt>



代理程式已完成先前的呼叫，但仍佔用與該呼叫相關的工作。 代理程式應該不會收到額外的呼叫。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

這組常數的上層16位會保留給裝置專屬的擴充。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




