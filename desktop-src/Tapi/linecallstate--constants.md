---
description: LINECALLSTATE \_ 位旗標常數描述呼叫可以位於的撥號狀態。
ms.assetid: 18d881ee-cf98-4dec-a561-333c2518935d
title: 'LINECALLSTATE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d50301dfeca49513a919fba90cc960c7ccb572d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994736"
---
# <a name="linecallstate_-constants"></a>LINECALLSTATE \_ 常數

**LINECALLSTATE \_** 位旗標常數描述呼叫可以位於的撥號狀態。

<dl> <dt>

<span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE 已 \_ 接受**
</dt> <dd> <dl> <dt>



通話處於供應狀態且已被接受。 這會向其他 (監視，指出目前的擁有者應用程式已宣稱接聽通話的責任，) 應用程式。 在 ISDN 中，當呼叫方設備傳送訊息給交換器時，即會輸入接受的狀態，指出它願意向呼叫的人員提出呼叫。 這會產生警示 (在來電的兩端) 使用者的副作用。 傳入的呼叫一律可以立即獲得解答，而不需要先個別接受。


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE \_ 忙碌**
</dt> <dd> <dl> <dt>



呼叫收到忙碌的聲音。 忙碌的色調表示呼叫無法完成， (主幹) 或遠端合作物件的站在使用中。 請參閱 [**LINEBUSYMODE \_ 常數**](linebusymode--constants.md)。


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE \_ CONFERENCED**
</dt> <dd> <dl> <dt>



呼叫是會議通話的成員，並在邏輯上處於已線上狀態。


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE \_ 已連線**
</dt> <dd> <dl> <dt>



已建立通話，並進行連接。 資訊可以在來源位址和目的地位址之間的呼叫之間流動。


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**LINECALLSTATE \_ 撥號**
</dt> <dd> <dl> <dt>



建立者是通話的撥號位數。 交換器會收集撥號位數。 請注意， [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) 和 [**TSPI \_ lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) 都不會將這一行放入撥號狀態。


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE \_ 撥號**
</dt> <dd> <dl> <dt>



呼叫會從交換器接收撥號音，這表示交換器已準備好接收撥接的號碼。 請參閱特殊撥號音的識別碼 [**LINEDIALTONEMODE \_ 常數**](linedialtonemode--constants.md) ，例如一般語音信箱的斷斷續續聲。


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE 已 \_ 中斷連線**
</dt> <dd> <dl> <dt>



遠端方已與呼叫中斷連線。


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE \_ 閒置**
</dt> <dd> <dl> <dt>



呼叫存在但尚未連接。 呼叫上沒有任何活動存在，這表示目前沒有作用中的呼叫。 呼叫永遠不會從閒置狀態轉換。


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**LINECALLSTATE \_ 供應專案**
</dt> <dd> <dl> <dt>



呼叫會提供給站，以通知新通話的抵達。 供應專案狀態與造成電話或電腦響鈴的情況不同。 在某些環境中，供應專案狀態中的呼叫不會環形使用者，直到切換器指示線路響鈴為止。 使用範例可能是撥入電話出現在數個工作站組上，但只有主要位址環形的位置。 環形的指示不會影響任何撥號狀態。


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE \_ 舉 SERVICEREQUESTSTATUSENUM.ONHOLD**
</dt> <dd> <dl> <dt>



開關正在保留呼叫。 這會釋出實體行，讓另一個呼叫使用該行。


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE \_ ONHOLDPENDCONF**
</dt> <dd> <dl> <dt>



呼叫目前正在進行中，正在新增至會議中。


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE \_ ONHOLDPENDTRANSFER**
</dt> <dd> <dl> <dt>



呼叫目前正在等待轉移至另一個數位。


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE \_ 繼續**
</dt> <dd> <dl> <dt>



撥號已完成，並透過交換器或電話網絡進行呼叫。 這會發生在撥號完成之後，以及呼叫抵達撥打的合作物件之前，如回電、忙碌或解答。


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**LINECALLSTATE \_ 回電**
</dt> <dd> <dl> <dt>



已到達要呼叫的工作站，而目的地的交換器正在將環形聲提示傳回給建立者。 *回電* 表示目的地位址會收到呼叫的警示。


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE \_ SPECIALINFO**
</dt> <dd> <dl> <dt>



呼叫收到特殊的資訊信號，此信號位於預先錄製的宣告之前，指出無法完成呼叫的原因。 請參閱 [**LINESPECIALINFO \_ 常數**](linespecialinfo--constants.md)。


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE \_ 不明**
</dt> <dd> <dl> <dt>



呼叫存在，但其狀態目前未知。 這可能是因為服務提供者的呼叫進度偵測不佳所造成。 可能也會產生撥號狀態設為 unknown 的撥號狀態消息，以在呼叫的實際撥號狀態不是已知時，一次通知 TAPI DLL 有新的呼叫。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

高序位8位可以定義任何預先定義狀態的裝置特定子狀態，前提 \_ 是您也會設定上述定義的其中一個 LINECALLSTATE 位。 低序位24位是保留給預先定義的狀態。

傳送至應用程式的 [**行 \_ CALLSTATE**](line-callstate.md)訊息會使用 **LINECALLSTATE \_ 常數** 作為參數。 訊息會攜帶呼叫轉換的新撥號狀態。 這些常數也會當做 [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)函數所傳回之 [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)結構中的成員使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ CALLSTATE**](line-callstate.md)
</dt> <dt>

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> </dl>

 

