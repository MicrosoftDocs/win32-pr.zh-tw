---
description: LINECALLREASON \_ 位旗標常數描述呼叫的原因。
ms.assetid: 16278146-886f-433a-afe5-64f4894b1428
title: 'LINECALLREASON_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6d2411c652c13add1620ca6029cabbf2b878e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998704"
---
# <a name="linecallreason_-constants"></a>LINECALLREASON \_ 常數

**LINECALLREASON \_** 位旗標常數描述呼叫的原因。

<dl> <dt>

<span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON \_ CALLCOMPLETION**
</dt> <dd> <dl> <dt>



呼叫完成要求的結果。


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**LINECALLREASON \_ CAMPEDON**
</dt> <dd> <dl> <dt>



已 camped 位址上的呼叫。 通常，它一開始會處於舉 servicerequeststatusenum.onhold 狀態，而且可以切換為使用 [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)。 如果使用中的呼叫變成閒置，camped 呼叫可能會變更為供應狀態，且裝置會開始響鈴。


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON \_ DIRECT**
</dt> <dd> <dl> <dt>



這是直接傳入或傳出的呼叫。


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON \_ FWDBUSY**
</dt> <dd> <dl> <dt>



此呼叫已從另一個在呼叫時忙碌的延伸模組轉送。


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON \_ FWDNOANSWER**
</dt> <dd> <dl> <dt>



已從另一個延伸模組轉送呼叫，而該擴充未在數個環形之後接聽通話。


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON \_ FWDUNCOND**
</dt> <dd> <dl> <dt>



呼叫已從另一個數位無條件轉送。


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON \_ INTRUDE**
</dt> <dd> <dl> <dt>



呼叫會 intruded 到行上，由另一個工作站或運算子動作叫用的呼叫完成動作。 視切換執行而定，呼叫可能會顯示在線上狀態中，或使用現有的使用中呼叫 conferenced。


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON \_ 暫停**
</dt> <dd> <dl> <dt>



通話已在位址上暫停。 通常，它一開始會處於舉 servicerequeststatusenum.onhold 狀態。


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**LINECALLREASON \_ 取貨**
</dt> <dd> <dl> <dt>



已從另一個擴充功能挑選呼叫。


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**LINECALLREASON 重新 \_ 導向**
</dt> <dd> <dl> <dt>



已將呼叫重新導向至此工作站。


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**LINECALLREASON \_ 提醒**
</dt> <dd> <dl> <dt>



此呼叫是提醒 (或「回想」 ) 使用者已暫停或保持 (可能) 很長一段時間。


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON \_ ROUTEREQUEST**
</dt> <dd> <dl> <dt>



呼叫會顯示在位址上，因為交換器需要來自應用程式的路由指示。 應用程式應該檢查 [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)中的 **CalledID** 成員，然後使用 [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect)函式來提供新的可撥打位址給呼叫。 如果要改為封鎖呼叫，應用程式可能會呼叫 [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)。 如果應用程式無法在參數定義的超時期間內採取動作，則會執行預設動作。 只有當該行的協商版本是2.0 或更高版本時，服務提供者才能使用此常數。 否則服務提供者應替代 LINECALLREASON \_ UNAVAIL。


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**LINECALLREASON \_ 傳輸**
</dt> <dd> <dl> <dt>



呼叫已從另一個數位轉移。


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON \_ UNAVAIL**
</dt> <dd> <dl> <dt>



呼叫的原因無法使用，稍後將不會變成已知。


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON \_ 不明**
</dt> <dd> <dl> <dt>



呼叫的原因目前未知，但稍後可能會變成已知。


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**LINECALLREASON \_ UNPARK**
</dt> <dd> <dl> <dt>



已將呼叫取出為暫停呼叫。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

LINECALLREASON \_ 常數用於 [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)資料結構的 **dwReason** 成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect)
</dt> <dt>

[**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)
</dt> </dl>

 

 




