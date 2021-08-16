---
description: LINEDEVCAPFLAGS \_ 位旗標常數是布林值的集合，其描述各種線路裝置功能。
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: 'LINEDEVCAPFLAGS_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d54acf1855bc09d9b2160e1ae681b25ff1de8ce310049fd4aabf4af6f8f2f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761715"
---
# <a name="linedevcapflags_-constants"></a>LINEDEVCAPFLAGS \_ 常數

**LINEDEVCAPFLAGS \_** 位旗標常數是布林值的集合，其描述各種線路裝置功能。

<dl> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS \_ CALLHUB**
</dt> <dd> <dl> <dt>



指出這一行是否支援呼叫中樞。 此旗標只會公開給協調 TAPI 3.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS \_ CALLHUBTRACKING**
</dt> <dd> <dl> <dt>



指出這一行是否支援呼叫中樞追蹤。 此旗標只會公開給協調 TAPI 3.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS \_ CLOSEDROP**
</dt> <dd> <dl> <dt>



指定當應用程式在行上有使用中的時，當開啟的行關閉時，會發生什麼事。 若 **為 TRUE**，則服務提供者會卸載 (清除) 當最後一個開啟該行的應用程式以 [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)關閉該行時，該行上所有使用中的呼叫。 如果 **為 FALSE**，則服務提供者不會在這種情況下捨棄使用中的呼叫。 相反地，呼叫會保持作用中狀態，並受外部裝置控制。 如果有其他裝置可讓通話保持運作，則服務提供者通常會將此位設定為 **FALSE** ，例如，如果類比線路路的電腦和電話組都是在合作物件設定中直接連接到它們，則即使在電腦關機之後，offhook 電話也會自動讓通話保持使用中狀態。

應用程式應該檢查此旗標，以判斷是否要使用 [確定]/[取消] 對話方塊來警告使用者 (，) 使用中的呼叫將會遺失。


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS \_ CROSSADDRCONF**
</dt> <dd> <dl> <dt>



指定是否可以 conferenced 此行上不同位址的呼叫。


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS \_ DIALBILLING**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS \_ DIALQUIET**
</dt> <dd> <dl> <dt>



這些旗標會指出指定的線路裝置是否支援 "$"、"@" 或 "W" 可撥出字串修飾詞。 如果支援修飾詞則為 **TRUE** ;否則 **為 FALSE**。 線路裝置永遠不支援 "？" (提示使用者繼續撥號) 。 這些旗標可讓應用程式事先判斷哪些修飾詞會導致產生 LINEERR。 應用程式可選擇預先掃描的可辨識字串是否有不支援的字元，或將「原始」字串從 [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) 直接傳遞給提供者，做為 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) 或 [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) 等函式的一部分，並讓函式產生錯誤，以告訴它不支援的修飾詞在字串中第一次發生。


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS \_ HIGHLEVCOMP**
</dt> <dd> <dl> <dt>



指定這一行是否支援高層級的相容性資訊元素。


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS \_ LOWLEVCOMP**
</dt> <dd> <dl> <dt>



指定這一行是否支援低層級的相容性資訊元素。


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS \_ MEDIACONTROL**
</dt> <dd> <dl> <dt>



指定是否可在這一行呼叫媒體控制項作業。


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS \_ MSP**
</dt> <dd> <dl> <dt>



指出媒體服務提供者 (MSP) 是否與該行相關聯。 此旗標只會公開給協調 TAPI 3.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS \_ MULTIPLEADDR**
</dt> <dd> <dl> <dt>



指定 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)、 [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)、 [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)或 [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) 是否能夠一次處理多個位址 (與反向多工) 。


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS \_ PRI加值稅EOBJECTS**
</dt> <dd> <dl> <dt>



指出是否已執行 [提供者特定的介面](./provider-specific-interfaces.md) 。 此旗標只會公開給協調 TAPI 3.0 版或更新版本的應用程式。


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

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

