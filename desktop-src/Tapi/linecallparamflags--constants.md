---
description: LINECALLPARAMFLAGS \_ 常數描述有關呼叫的各種狀態旗標。
ms.assetid: f323ec9f-5bab-4b5d-93ef-8a552ee0d591
title: 'LINECALLPARAMFLAGS_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e70fe2721e6fce0ac509b50290b1ec3788f3c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983963"
---
# <a name="linecallparamflags_-constants"></a>LINECALLPARAMFLAGS \_ 常數

**LINECALLPARAMFLAGS \_** 常數描述有關呼叫的各種狀態旗標。

<dl> <dt>

<span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS \_ 區塊識別碼**
</dt> <dd> <dl> <dt>



建立者身分識別應該隱藏 (區塊呼叫端識別碼) 。


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS \_ DESTOFFHOOK**
</dt> <dd> <dl> <dt>



呼叫方的電話應該會自動 offhook。


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS \_ 閒置**
</dt> <dd> <dl> <dt>



呼叫應源自閒置通話的外觀，而不是聯結進行中的呼叫。 使用 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) 函式時，如果 \_ 未設定 LINECALLPARAMFLAGS 閒置值，而且該行有現有的呼叫，則函式會在需要進行新的呼叫時，中斷至現有的呼叫。 如果沒有任何現有的呼叫，此函式會依指定進行新的呼叫。


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS \_ NOHOLDCONFERENCE**
</dt> <dd> <dl> <dt>



這個位只會搭配 [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) 和 [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)使用。 要使用目前的呼叫 conferenced 的位址，是在 [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)的 **TargetAddress** 成員中指定。 諮詢電話不會實際從交換器中繪製撥號音，但會透過各種不同的通話建立狀態進行 (例如，撥接、繼續) 。 當諮詢通話達到線上狀態時，就會自動建立會議;原先保持線上狀態的原始呼叫會進入 conferenced 狀態;諮詢通話進入 conferenced 狀態;hConfCall 會進入 [已連線] 狀態。 如果諮詢通話失敗 (進入已中斷連線的狀態，並在閒置) 之後進入閒置狀態，則 hConfCall 也會進入閒置狀態，而原始呼叫 (可能是現有的會議，在 **linePrepareAddToConference**) 會保持線上狀態。 原始的合作物件 (或合作物件) 不會察覺到通話是否已舉 servicerequeststatusenum.onhold。 這項功能通常用來在需要監視與 irate 呼叫者的互動時，將監督員新增至 ACD 代理程式通話。


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS \_ ONESTEPTRANSFER**
</dt> <dd> <dl> <dt>



這個位只會與 [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)搭配使用。 它結合了 **lineSetupTransfer** 的作業，後面接著 [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) 的諮詢通話，成為單一步驟。 要撥號的位址是在 [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)的 **TargetAddress** 成員中指定。 原始呼叫會處於 *onholdpendingtransfer* 狀態，就像是正常呼叫 **lineSetupTransfer** 一樣，並且會正常建立諮詢通話。 應用程式仍然必須呼叫 [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) 來影響傳送。 這項功能通常是在透過協力廠商呼叫控制連結叫用來自伺服器的傳輸時使用，因為這類連結通常不支援一般的雙步驟程式。


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS \_ ORIGOFFHOOK**
</dt> <dd> <dl> <dt>



建立者的電話應該會自動取得 offhook。


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS \_ PREDICTIVEDIAL**
</dt> <dd> <dl> <dt>



只有在呼叫具有預測撥號功能的位址時，才會使用此位 (LINEADDRCAPFLAGS \_ PREDICTIVEDIALER 在 [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)) 的 **dwAddrCapFlags** 成員中。 您必須開啟此位，才能啟用裝置的增強通話進度和/或媒體裝置監視功能。 如果沒有開啟此位，則會在沒有增強通話進度或媒體類型監視的情況下進行呼叫，而且不會根據撥號狀態起始自動傳輸。


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS \_ 安全**
</dt> <dd> <dl> <dt>



呼叫應該設定為安全的。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




