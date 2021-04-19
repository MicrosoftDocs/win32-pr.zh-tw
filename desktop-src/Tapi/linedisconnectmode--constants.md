---
description: LINEDISCONNECTMODE \_ 位旗標常數描述遠端中斷連接要求的不同原因。 在撥號狀態轉換為已中斷連線之後，中斷連線模式可作為應用程式的撥號狀態。
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: 'LINEDISCONNECTMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70ba70175685e2c264343f9345227ee64c206f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990973"
---
# <a name="linedisconnectmode_-constants"></a>LINEDISCONNECTMODE \_ 常數

**LINEDISCONNECTMODE \_** 位旗標常數描述遠端中斷連接要求的不同原因。 在撥號狀態轉換為已中斷連線之後，中斷連線模式可作為應用程式的撥號狀態。

<dl> <dt>

<span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE \_ BADADDRESS**
</dt> <dd> <dl> <dt>



目的地位址無效。


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE 已 \_ 封鎖**
</dt> <dd> <dl> <dt>



無法連接呼叫，因為目的地位址未接受來自來源位址的呼叫。 這與 LINEDISCONNECTMODE 拒絕的不同之處在于 \_ ，封鎖是在網路中實 (被動拒絕) ，而拒絕是在目的地設備 (主動拒絕) 中執行。 封鎖可能是因為來源位址的特定排除，或是目的地只接受一組選取的來源位址 (關閉的使用者群組) 的呼叫。  (TAPI 2.0 版和更新版本) 

LINEDISCONNECTMODE \_ 封鎖適用于封鎖回應。 例如，數據機已收到答案、未偵測到回電超過6秒、無法連接定義的次數、判斷電話號碼不是有效的電話號碼，而且會發出 ' 封鎖 ' 回應。


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE \_ 忙碌**
</dt> <dd> <dl> <dt>



遠端使用者的工作站忙碌中。


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE 已 \_ 取消**
</dt> <dd> <dl> <dt>



呼叫已取消。  (TAPI 2.0 版和更新版本) 


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**LINEDISCONNECTMODE \_ 擁塞**
</dt> <dd> <dl> <dt>



網路擁塞。


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE \_ DONOTDISTURB**
</dt> <dd> <dl> <dt>



因為目的地已叫用「請勿打擾」功能，所以無法連線。  (TAPI 2.0 版和更新版本) 


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE \_ 轉送**
</dt> <dd> <dl> <dt>



呼叫是由參數轉寄。


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE \_ 不相容**
</dt> <dd> <dl> <dt>



遠端使用者的工作站設備與要求的撥號類型不相容。


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE \_ NOANSWER**
</dt> <dd> <dl> <dt>



遠端使用者的工作站沒有回應。


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE \_ NODIALTONE**
</dt> <dd> <dl> <dt>



在服務提供者定義的超時時間內偵測到撥號音，在撥號期間的某個時間點會出現一次， (例如在無限制的字串) 中的 "W"。 如果沒有服務提供者定義的超時時間，或在 [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)結構的 **dwWaitForDialTone** 成員中未指定值，也可能會發生這種情況。  (TAPI 1.4 版和更新版本) 


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE \_ 正常**
</dt> <dd> <dl> <dt>



這是遠端方的一般中斷連接要求。 呼叫已正常終止。


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE \_ NUMBERCHANGED**
</dt> <dd> <dl> <dt>



因為目的地號碼已變更，但未提供自動重新導向至新的數位，所以無法連接此呼叫。  (TAPI 2.0 版和更新版本) 


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE \_ OUTOFORDER**
</dt> <dd> <dl> <dt>



無法連線或中斷連線，因為目的地裝置未按順序 (硬體故障) 。  (TAPI 2.0 版和更新版本) 


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**LINEDISCONNECTMODE \_ 取貨**
</dt> <dd> <dl> <dt>



已從其他位置挑選呼叫。


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE \_ QOSUNAVAIL**
</dt> <dd> <dl> <dt>



無法連接或中斷連線，因為無法取得或維持最小服務品質。 這與 LINEDISCONNECTMODE \_ 不相容，因為缺少資源可能是目的地的暫時性狀況。  (TAPI 2.0 版和更新版本) 


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE \_ 拒絕**
</dt> <dd> <dl> <dt>



遠端使用者已拒絕呼叫。


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE \_ TEMPFAILURE**
</dt> <dd> <dl> <dt>



因為網路發生暫時性失敗，所以無法連線或中斷連線的呼叫;呼叫可以稍後 rerun，且預期最終會完成。  (TAPI 2.0 版和更新版本) 

LINEDISCONNECTMODE \_ TEMPFAILURE 適合作為延遲的回應。 例如，在特定的時間週期內，數據機取得忙碌的信號或對等太多次，最後不應該再次呼叫該數位，直到定義的時間已過，併發出「延遲」的回應。


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE \_ UNAVAIL**
</dt> <dd> <dl> <dt>



中斷連線的原因無法使用，稍後將不會變成已知。


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE \_ 不明**
</dt> <dd> <dl> <dt>



中斷連線要求的原因不明，但稍後可能會變成已知。


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE \_ 無法連線**
</dt> <dd> <dl> <dt>



無法連線到遠端使用者。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

您可以為裝置專屬的延伸模組指派高序位16位。 低序位16位是保留的。

針對指定呼叫的遠端中斷連接要求會導致撥號狀態轉換為已中斷連線的狀態，並將 [**一行 \_ CALLSTATE**](line-callstate.md) 訊息傳送至應用程式。 LINEDISCONNECTMODE \_ 資訊會提供遠端中斷連線要求的詳細資料。 當呼叫處於中斷線上狀態時，就可以在呼叫的 [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) 結構中使用它。 當通話處於這種狀態時，仍然可以使用應用程式來查詢呼叫的資訊和狀態。 例如，在遠端中斷的情況下收到的使用者使用者資訊可供使用。 應用程式可以藉由卸載呼叫來清除中斷連線的呼叫。

為了回溯相容性，服務提供者必須負責檢查該行上的已協商 API 版本，如果未在協商版本上支援，則不使用此 LINEDISCONNECTMODE \_ 值 (LINEDISCONNECTMODE \_ NORMAL 或 \_ UNKNOWN 可改為使用) 。

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

[**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




